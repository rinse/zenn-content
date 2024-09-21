---
title: "型クラスパターン"
emoji: "📝"
type: "tech"
topics: ["Kotlin", "Java"]
published: false
---

## 型クラスパターンとは

型クラスパターンは、KotlinやJavaのようなインターフェースを使う言語において、Scala, Rust, Haskellなどで使われる型クラスの利点を得る手法です。

これから紹介する型クラスパターンは、単にインターフェースを使う場合に比べて、次のような利点があります。

- 特定のstatic関数を持つことを抽象化できる
    - ファクトリーメソッドや型変換など
- 既存の型に対しても抽象化を適用できる
    - プリミティブな型やライブラリによって提供される型など

::: message
型クラスを言語機能として持つ言語は通常インターフェースを持ちませんが、型クラスパターンはインターフェースを置き換えるものではありません。
:::

型クラスパターンは、1. 型クラスの定義 2. 型クラスのインスタンスの定義 という二段階に分けられます。ここでは[Monoid](https://ja.wikipedia.org/wiki/%E3%83%A2%E3%83%8E%E3%82%A4%E3%83%89)を例に、型クラスの実装例を紹介します。

Monoidとは、単位元と結合的な二項演算を備えた代数的な構造です。プログラミングではしばしば畳み込みの文脈で使われるため、普段の開発でも有用な型クラスのうちの一つです。（参考: [fold](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/fold.html), [Stream.reduce](https://docs.oracle.com/en/java/javase/21/docs/api/java.base/java/util/stream/Stream.html#reduce(T,java.util.function.BinaryOperator))）

- 結合的な二項演算とは、`(a * b) * c = a * (b * c)` が成り立つような二項演算 `*` をいいます
- 単位元とは、ある二項演算 `*` を考えたときに `a * e = e * a = a` が成り立つような元 `e` をいいます

### 型クラスの定義

まずは型クラスを定義します。型クラスはインターフェースで書きますが、通常のインターフェースと区別するために、型クラスの先頭にはType classを表す`TC`の接頭辞をつけています。

Monoidは単位元と結合的な二項演算を備えているため、それぞれをインターフェースのメソッドとして実装します。

```Kotlin:TCMonoid.kt
interface TCMonoid<M> {
    val empty: M
    fun compose(a: M, b: M): M
}
```

::: details Java

```Java:TCMonoid.java
interface TCMonoid<M> {
    M empty();
    M compose(M a, M b);
} 
```

:::

### 型クラスのインスタンス宣言

次に、型クラスのインスタンスを定義します。型クラスのインスタンスはクラスで書きます。型クラスのインスタンスは、ある型がその型クラスが課す条件を満たすことを表現します。

Monoidの課す条件は、1. 結合的な二項演算を持つこと 2. 単位元を持つこと の2点でした。

例として文字列を考えてみましょう。文字列は、1. 文字列の結合が結合的である (`(s + t) + u = s + (t + u)`) 2. 空文字は文字列の結合操作の単位元である (`s + "" = "" + s = s`) 点から、Monoidのインスタンスになることが分かります。

```Kotlin:MonoidString.kt
object MonoidString : Monoid<String> {
    override val empty: String = ""
    override fun compose(a: String, b: String) = a + b
}
```

::: details Java

```Java:MonoidString.java
class MonoidString implements TCMonoid<String> {
    @Override
    public String empty() {
        return "";
    }

    @Override
    public String compose(String a, String b) {
        return a + b;
    }
} 
```

:::

### 型クラスの利用

型クラスとそのインスタンスが揃ったので、型クラスを利用した多相的な関数を書いてみましょう。以下はMonoidを使った`fold`の実装です。

```Kotlin:TCMonoid.kt
fun <M> fold(instance: TCMonoid<M>, iter: Iterable<M>): M {
    return iter.fold(instance.empty, instance::compose)
}
```

::: details Java

Javaでは関数を何らかメソッドにしなければならないため、ここでは型クラス`TCMonoid`のデフォルトメソッドとして実装することを想定しています。

```Java:TCMonoid.java
    default M fold(Iterable<M> iter) {
        M result = empty();
        for (var e : iter) {
            result = compose(result, e);
        }
        return result;
    }
```

:::

この多相的な関数は、次のように型クラスのインスタンスを用いて呼び出します。

```Kotlin:Main.kt
fold(MonoidString, listOf("Hello ", "Beautiful ", "World")
```

::: details Java

```Java:Main.java
new MonoidString()
    .fold(List.of("Hello ", "Beautiful ", "World"));
```

:::


::: message
コードの全文は次で見ることができます。

- [Kotlin](https://pl.kotl.in/OUZoM5s6i)
- [Java](https://codapi.org/embed/?sandbox=java&code=data%3A%3Bbase64%2ChVFNT8MwDL3nV1g9ZTD1BzCGEFxAIuIwJA6IQ9q6U1CaVPkomtD%2BO26bbkEg4UsS%2B71n%2B0V1vXUBPuQgyxiULi82jPWx0qqGWkvvQUhl4IsBRcr7IAMdg1UNdFTlu%2BCU2b%2B9g3R7v0rgMQbpQJk%2BBtjCk%2FKhtC0vHlBrC8UaijuU1LONenq9WqebYrX5wbYxzHSDnyCsoZ5zN74qW6sbPslnpN3BB%2BxK4pU94YI2fNZImCM7MkZ5dK2sEV7uZ9FrcZPmFoBdHw484QXUljzyyAXINT0rKkyVBlsZdaDUNMgjScpK46ik6J77IMChH7Hbn%2BJjtNYBH1dFuPpFHONEXQaZE2vATOXIzvAQnUmsbOf0m5mFoLpeY4cm%2BLMPc2kx4%2FZ5QOdUg%2Fn%2FJ3baJJs2tS6Kpe2%2FGstK6UkGp1v1h66ES6hOG30D)
:::

### Monoidの他の例

Monoidの例には文字列の結合以外にも様々なものがあります。

もし時間があれば、自分で何かしらのMonoidのインスタンスを実装してみてください。そのうえで`fold`を呼び出してみて、結果がどのようなものになるか確認してみましょう。

参考までに、以下はMonoidの例です：

- 足し算, 0
- 掛け算, 1
- 論理AND, true
- 論理OR, false
- ビットAND, ~0
- ビットOR, 0
- `Math.max`, 最小値
- `Math.min`, 最大値
- `Function<T, T>.andThen`, `Function.identity`
- `Predicate<T>.and`, `() -> true`

## 発展：型クラスの継承

型クラスを継承することで、ある型クラスが別のある型クラスを前提条件として持つことを表現できます。

例えば結合的な二項演算を持つ構造である[半群](https://ja.wikipedia.org/wiki/%E5%8D%8A%E7%BE%A4)を考えると、Monoidは明らかに半群でもあることが分かります。

```Kotlin:TCSemigroup.kt
interface TCSemigroup<G> {
    fun compose(a: G, b: G): G
}

interface TCMonoid<M> : TCSemigroup<M> {
    val empty: M
}
```

このように型クラスをより細かい単位に分割すると、ジェネリックな関数に対してより正確な条件を課すことができるようになります。

::: message
コードの全文は次で見ることができます。

- [Kotlin](https://pl.kotl.in/YGNnMcKHC)
- [Java](https://codapi.org/embed/?sandbox=java&code=data%3A%3Bbase64%2ChVLJTsMwEL3nK0Y5uVDlA%2BgiBIeCRMShSBwQB6eZVEaOHdnjQIX670wSpw2LxFzsWd6bmWerurGO4E22MgukdHaxSJImFFrtYKel95BLZeAzAbYY9ySJj9aqEmrOii05ZfYvryDd3s9icWetdKBMEwhW8KA8ZbYS6R1qbSGdQ3qDkntWQffes3W6TGeLb2gbaIAbfIfcGu45dBOzrLK6FD39BLQ9eMI6Y1zWcB1pIwaOWHNMjknCcXSV3CE83W6xVntnQ7PcrOPoG9hZ1sWj2ICcs1sw%2BAdsmGWZrwE%2FCE3pv1HlI1UOWDd0EEzQ%2ByVWMmjieD%2F9PRPKQmMHUHyfipeDQ9%2FVrs4cY66yDkSnD8LVL2BnJ%2Bi4yRCYA05Yjsm5nIIzETURKn6Bie6g6kZjjYb8WYUhNe58%2Fdiic6rE6aeJ6LjJZNrYOk3Htv9yjCtFl18o3oo%2FeCVcQnHa6As%3D)
:::

## 発展：条件付きの型クラス

Javaの`Optional`型のように、ジェネリックなクラスであって、型パラメータ`T`がMonoidを満たす場合にのみ`Optional<T>`もMonoidを満たすような構造を考えることができます。

このような構造のインスタンス宣言は、前提条件（この場合は型パラメータ`T`がMonoidであること）をコンストラクタで受け取ることによって実現できます。

```Kotlin:MonoidOptional.kt
class MonoidOptional<T>(
    private val instance: TCMonoid<T>
) : TCMonoid<T?> {
    override val empty: T? = null
    override fun compose(a: T?, b: T?): T? {
        if (a == null) {
            return b
        }
        if (b == null) {
            return a
        }
        return instance.compose(a, b)
    }
}
```

::: details Java

```Java:MonoidOptional.java
class MonoidOptional<T> implements TCMonoid<Optional<T>> {
    private final TCMonoid<T> instance;

    public MonoidOptional(TCMonoid<T> instance) {
        this.instance = instance;
    }

    @Override
    public Optional<T> empty() {
        return Optional.empty();
    }

    @Override
    public Optional<T> compose(
        Optional<T> a,
        Optional<T> b
    ) {
        return a.map(a2 ->
            b.map(b2 ->
                instance.compose(a2, b2)
            ).orElse(a2)
        ).or(() -> b);
    }
}
```

:::

::: message
コードの全文は次で見ることができます。

- [Kotlin](https://pl.kotl.in/FAW6_bcNX)
- [Java](https://codapi.org/embed/?sandbox=java&code=data%3A%3Bbase64%2ClZPBboMwDIbvPIXFKWyMQ69s1aRp0i6oh1baYdoh0LTNFBIUAlU19d3n0EBTxNaOC4n9%2B4vtOLyslDbwRVuaNIaL5C4NgqrJBS%2BgELSuIaNcwncA%2BDl7bajBX6v4Gkr0kqXRXG4%2FPoHqbR05sf1aqqFUEoUnCTyBZHvIPBOJ0gn5ojJcSSouAnrj4ylyTnz0CLNjQiiMvsQlhcJ6a0YGg9qQ8M1qwyiGwcrKyhxINGLulRbrG5gu2uPZU95tdDhmdnneCp5Odhq%2BPNSGlYlqTFJhf4yQpDvrb0mXyQ0UX3cMjkGAPqY3tGCwejnd1mM2d5OQgetI6rZ9YRnQGLc5OhDhxs0fF15WgpVMmvqMdZfv2M%2BLlmnN18wfUBftTvXmUTPTaAlh2Gd%2BldGn6raYr1vlE1wK95B7TfErGoZ3NZ8sy%2FP3tWHHW2oYbLh9CYPSAiS%2BQVmwNPBTvjyITAX4SZsdr5PegdN3hl7rjV%2FLr00eP4f%2FYcezb200vpBM3kBS0orQGTygv1vn3bqvbXhTdBZDPouiROlX0e27NcFKbOh5tH8A)

:::

## 応用：Universal mapping property

型クラスを応用して、実装に対して一意性を与える性質(Universal mapping property, UMP)を、型クラスによって与えることができます。この型クラスのインスタンスは、純粋な関数を書く限りにおいて、どのような実装を書いてもプログラムの意味が同じことが保障される性質を持ちます。

### Pair型クラス

ここでは例として、**2つ組**を表す型クラスを作成してみたいと思います。

Javaでは`Pair`というクラスは用意されていません。しかしながら`Pair`に相当するクラスは様々に実装されています。

そこでこれらを統一的に扱える`Pair`インターフェースを作成することを考えます。このインターフェースを実装していれば、それは`Pair`に相当するクラスであるということです。

```Kotlin:Pair.kt
interface Pair<T, U> {
    val first: T
    val second: U
}
```

::: details Java

```Java:Pair.java
interface Pair<T, U> {
    T first();
    U second();
}
```

:::

実際これはうまく動作するように見えます。2つ組であればどのようなクラスであっても`Pair`を実装できます。

```Kotlin:Tuple2.kt
data class Tuple2<T, U>(
    override val first: T,
    override val second: U,
) : Pair<T, U>
```

```Kotlin:Size.kt
data class Size<T>(
    val width: T,
    val height: T,
) : Pair<T, T> {
    override val first: T
        get() = width
    override val second: T
        get() = height
}
```

::: details Java

```Java:Tuple2.java
record Tuple2<T, U>(
    T first,
    U second
) implements Pair<T, U> {
}
```

```Java:Size.java
record Size<T>(
    T width,
    T height
) implements Pair<T, T> {
    @Override
    public T first() {
        return this.width;
    }

    @Override
    public T second() {
        return this.height;
    }
}
```

:::

しかしながら、ここで問題が発生します。

`Pair`インターフェースは、実際のところ、2つ組ではなくても実装することができてしまいます。例えば3つ組でも実装できることは想像に難くありません。`Pair`インターフェースは条件が緩すぎるのです。

```Kotlin:Tuple3.kt
data class Tuple3<A, B, C>(
    override val first: A,
    override val second: B,
    val third: C,
) : Pair<A, B>
```

::: details Java

```Java:Tuple3.java
record Tuple3<A, B, C>(
    A first,
    B second,
    C third
) implements Pair<A, B> {
}
```

:::

そこで、新たに型クラスを使ってUniversal mapping propertyを導入します。次の定義では、`Pair`を実装する任意の型`P`に対する追加の制約を導入します。

すなわち**2つ組**とは、任意の`Pair`インターフェースを満たす型から一意に得られるような型である、という制約です。

```Kotlin:TCPair.kt
interface TCPair<
        T, U, P : Pair<T, U>> {
    fun <Q : Pair<T, U>> terminal(
        other: Q,
    ): P
}
```

::: details Java

```Java:TCPair.java
interface TCPair<
        T, U, P extends Pair<T, U>> {
    <Q extends Pair<T, U>> P terminal(
        Q other
    );
}
```

:::

この型クラスには、2つ組であれば自明なインスタンスを与えることができます。

```Kotlin:TCPairInstances.kt
class Tuple2TCPair<T, U> :
        TCPair<T, U, Tuple2<T, U>> {
    override fun <Q : Pair<T, U>> terminal(
        other: Q,
    ) = Tuple2(other.first, other.second)
}

class SizeTCPair<T> :
        TCPair<T, T, Size<T>> {
    override fun <Q : Pair<T, T>> terminal(
        other: Q,
    ) = Size(other.first, other.second)
}
```

::: details Java

```Java:TCPairInstances.java
class Tuple2TCPair<T, U> implements
        TCPair<T, U, Tuple2<T, U>> {
    public <Q extends Pair<T, U>> Tuple2<T, U> terminal(
        Q q
    ) {
        return new Tuple2<>(
            q.first(),
            q.second()
        );
    }
}

class SizeTCPair<T> implements
        TCPair<T, T, Size<T>> {
    public <Q extends Pair<T, T>> Size<T> terminal(
        Q q
    ) {
        return new Size<>(
            q.first(),
            q.second()
        );
    }
}
```

:::

しかしながら`Tuple3`は`Pair`インターフェースを実装するものの`TCPair`のインスタンスを作れないため、2つ組ではありません。

```Kotlin:Tuple3.kt
class Tuple3TCPair<A, B, C> :
        TCPair<A, B, Tuple3<A, B, C>> {
    override fun <Q : Pair<A, B>> terminal(
        other: Q,
    ) = Tuple3(
        other.first,
        other.second,
        /* thirdがないので実装できない */
    )
}
```

::: details Java

```Java:Tuple3.java
class Tuple3TCPair<A, B, C> implements
        TCPair<A, B, Tuple3<A, B, C>> {
    public <Q extends Pair<A, B>> Tuple3<A, B, C> terminal(
        Q other
    ) {
    	return new Tuple3(
            other.first,
            other.second,
            /* thirdがないので実装できない */
        )
    }
}
```

:::

### TCPairの一般化

`TCPair`型クラスのような、UMPを提供する型クラスは次のように一般化できます。UMPには二種類があり、それぞれ`Initial`と`Terminal`と名前をつけています。

実際のところ`TCPair`型クラスは`TCTerminal`型クラスの特殊化です。

#### Initial型クラス

```Kotlin:TCInitial.kt
interface TCInitial<I : Condition, Condition> {
    fun <J : Condition> initial(other: I): J
}
```

::: details Java

```Java:TCInitial.java
interface TCInitial<I extends Condition, Condition> {
    <J extends Condition> J initial(I other);
}
```

:::

#### Terminal型クラス

```Kotlin:TCTerminal.kt
interface TCTerminal<T : Condition, Condition> {
    fun <U : Condition> terminal(other: U): T;
}
```

::: details Java

```Java:TCTerminal.java
interface TCTerminal<T extends Condition, Condition> {
    <U extends Condition> T terminal(U other);
}
```

:::

#### TCPair

`TCPair`の`TerminalTC`を使った定義です。

```Kotlin:TCPair.kt
interface TCPair<T, U, P : Pair<T, U>> :
        TCTerminal<P, Pair<T, U>> {
    override fun <Q : Pair<T, U>> terminal(other: Q): P
}
```

::: details Java

```Java:TCPair.java
interface TCPair<T, U, P extends Pair<T, U>> extends
    TerminalTC<P, Pair<T, U>> {
}
```

:::

::: message
コードの全文は次で見ることができます。

- [Kotlin](https://pl.kotl.in/xgpXPL3UR)
- [Java](https://codapi.org/embed/?sandbox=java&code=data%3A%3Bbase64%2CjVJNb4MwDL3zK3wEKeph1yI0qedprRpO0w4ZuMUSpG0S2mlT%2F%2FsCCRA09oGQwMnz8%2FOzz%2B1bTQUUtdAangRJ%2BIzAPmd3ro0w9nM9UQmNvY33RpE8vryCUEedePA9ukcRSYPqIAqErSCVcgZ55u85HEhpEyfrPsxBY3GSZRfbRGUDVQJvzzU%2BuLw4TGOzpCgBaiyyQWn0vNTEtacPTPlIc6PSVMwHFdKxMss0fFD8%2BHxFpajE0IyxDQ%2FqHoWmVRJMRXrVl1l7R36jGdr%2FgccpXC9Zy1E1JEXNNykHfDcoSw0bS0aGTpJNv0Mjaf4dllkJxhPFObRuDEGRzWgrg%2B2YP3mdjWeBni2bIfpxuLVykw1Ys8D70YFZ1XAZsvlKprtFRWHG1N0OLgsuS7wN%2BCy%2BrPxUGVxWw2SSwH3XRLdSg8RQf6Dbvn7x%2FpbcYTz4P2p76J9avwA%3D)
:::
