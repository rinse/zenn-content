---
title: "JSON-LDの基礎"
emoji: "📝"
type: "tech"
topics: ["web", "json", "jsonld", "LinkedData"]
published: true
---

## はじめに JSON-LDとは

JSON-LDは、Linked dataをJSON形式で記述する規格、またはJSON形式で書かれたLinked dataを指します。
Linked dataとは、あるデータをコンピュータにとって読みやすく、かつ他のWeb上のデータと容易に結び付けられるようにしようという考え方です。

仰々しい書き方がされていますが、JSONに対して型を導入して、プロパティ名や値のデータ型・フォーマットを限定しようというのが根底にあるアイデアだと理解しています。

この記事は、JSON-LDで用いられるLinked dataの基本的な文法を紹介することを目的として書かれています。SEOの話題には一切触れませんので、ご容赦ください。

## リンク集

先んじてリンク集を貼っておきます。特にプレイグラウンドは開いた状態で記事を読み進めていただき、適宜サンプルコードを貼り付けながら記事を読むと理解の助けになるかと思います。

- プレイグラウンド

https://json-ld.org/playground

- 標準規格
    - この記事は、W3C勧告の [JSON-LD 1.1](https://www.w3.org/TR/json-ld11/) の [3. Basic Concepts](https://www.w3.org/TR/json-ld/#basic-concepts) までの記述をもとに書かれています。

https://www.w3.org/TR/json-ld11/

## 基本文法

JSON-LDはJSONとして書かれるので、基本的な文法はJSONと同一です。

例えば人物を表すデータを書くことを考えます。
一例として以下のようなJSONが考えられますが、複数のウェブサイトがそれぞれ人物のデータを掲載するときには、それぞれ独特のプロパティ名が使われたり、国の慣習や個人の好みでデータのフォーマットが違ったりする場合がしばしばあります。

```json:json
{
  "name": "John Smith",
  "birthday": "2004/01/26"
}
```

そこで次のようにJSON-LDで書き直します。

```json:json-ld
{
  "https://schema.org/name": "John Smith",
  "https://schema.org/birthDate": "2004-01-26"
}
```

ここでプロパティ名に指定されているURLは[IRI](https://datatracker.ietf.org/doc/html/rfc3987#section-2) (Internationalized Resource Identifier)と呼ばれる統一的な識別子で、これによってJSON-LDの各プロパティの性質を一意に特定しています。実際にこの[URL](https://schema.org/name)にアクセスすると、値の型やフォーマットの明確に定義を確認できます。

例えば、JSON-LDで書き直すにあたり、誕生日のフォーマットを`2004/01/26`から`2004-01-26`へと変更しました。これは、今回プロパティのIRIに https://schema.org を使おうと決めたからです。（ここは決めの問題であり、JSON-LDを使うなら https://schema.org を使わなければならないということはありません）
具体的には、まず`birthday`プロパティに https://schema.org/birthDate を使うことに決めました。そこでbirthDateプロパティの[ドキュメント](https://schema.org/birthDate)を読むと「値はDate型でなければならない」とあるため、日付は https://schema.org/Date で定められたフォーマットで指定する必要があることが分かりました。再び、今度はDate型の[ドキュメント](https://schema.org/Date)を読むと「日付は ISO 8601 date format で書かれた値である」とあるため、誕生日は[ISO 8601](https://ja.wikipedia.org/wiki/ISO_8601)の形式で書き直さなければならなかったのです。

このようにして、プロパティ名とその値の文法的なフォーマット（シンタクス）・意味論（セマンティクス）とをウェブ横断的に統一します。

なお https://schema.org は一般的な用途に使えるポピュラーなIRIを提供してくれるサイトです。専門的な分野でJSON-LDを使う場合は、そちらの規格で定められたプロパティと型を使うことが多いです。

## キーワード

JSON-LDでは、先頭に`@`がついたプロパティは特別な意味を持ち、キーワードと総称されます。

この記事では、最も重要ないくつかのキーワードに絞って紹介します。

### @id キーワード

`@id`キーワードは、そのオブジェクトを一意に特定する識別子を指定します。識別子は[IRI](https://datatracker.ietf.org/doc/html/rfc3987#section-2)である必要があります。^[> A string is interpreted as an IRI when it is the value of a map entry with the key @id https://www.w3.org/TR/json-ld/#iris]

```json
{
  "@id": "https://example.com/users/john-smith",
  "https://schema.org/name": "John Smith",
  "https://schema.org/birthDate": "2004-01-26"
}
```

### @type キーワード

`@type`キーワードは、そのオブジェクトの型を指定します。識別子と同様に、型は[IRI](https://datatracker.ietf.org/doc/html/rfc3987#section-2)である必要があります。^[> In Linked Data, types are uniquely identified with an IRI. https://www.w3.org/TR/json-ld/#node-identifiers]
以下の例では型として https://schema.org/Person を使っています。[ドキュメント](https://schema.org/Person)を読むと、このオブジェクトが持ちうるフィールドの一覧を確認できます。

```json
{
  "@type": "https://schema.org/Person",
  "https://schema.org/name": "John Smith",
  "https://schema.org/birthDate": "2004-01-26"
}
```

なお https://schema.org で使うことのできるすべての型のリストは以下にあります。

https://schema.org/docs/full.html

### @context キーワード

`@context`は、これまでとは少し毛色の違うキーワードです。

JSON-LDでは、基本的にプロパティ名を[IRI](https://datatracker.ietf.org/doc/html/rfc3987#section-2)で書くことになるため、工夫しなければ素のJSONと比べて著しく可読性が落ちてしまいます。
そこで、`@context`キーワードを使うと、IRIに対して人間が読みやすい名前を割り当てることができます。

下の例では`@context`を使って各IRIに別名を付けています。

```json
{
  "@context": {
    "name": "https://schema.org/name",
    "birthDate": "https://schema.org/birthDate",
  },
  "name": "John Smith",
  "birthDate": "2004-01-26"
}
```

また型として設定されているIRIであっても別名を付けることができます。

```json
{
  "@context": {
    "name": "https://schema.org/name",
    "birthDate": "https://schema.org/birthDate",
    "Person": "https://schema.org/Person"
  },
  "@id": "https://example.com/users/john-smith",
  "@type": "Person",
  "name": "John Smith",
  "birthDate": "2004-01-26"
}
```

キーワードに対して別名をつけることも可能です。ここでは`@id`に対して`id`という別名を付けています。

```json
{
  "@context": {
    "id": "@id",
    "name": "https://schema.org/name",
    "birthDate": "https://schema.org/birthDate",
    "Person": "https://schema.org/Person"
  },
  "id": "https://example.com/users/john-smith",
  "@type": "Person",
  "name": "John Smith",
  "birthDate": "2004-01-26"
}
```

また`@context`は、以下のようにプロパティの値の型を指定することもできます。
このようにすることで`image`プロパティの値である`https://example.com/users/john-smith/icon.png`が単なるリテラルではなく[IRI](https://datatracker.ietf.org/doc/html/rfc3987#section-2)であることを示せます。

```json
{
  "@context": {
    "id": "@id",
    "name": "https://schema.org/name",
    "birthDate": "https://schema.org/birthDate",
    "image": {
        "@id": "https://schema.org/image",
        "@type": "@id"
    }
  },
  "id": "https://example.com/users/john-smith",
  "name": "John Smith",
  "birthDate": "2004-01-26",
  "image": "https://example.com/users/john-smith/icon.png"
}
```

ここまではJSON-LDの中にインラインで文脈を書いてきました(Embedded context)が、`@context`は外部の文脈(External context document)を参照することもできます。
以下の例では schema.org で用意されているコンテキストを利用してJSON-LDを記述しています。`name`や`birthDate`のみならず、`id`や`image`についても schmea.org が定義してくれているため、`@context`を非常に簡単に済ますことができました。

```json
{
  "@context": "https://schema.org",
  "id": "https://example.com/users/john-smith",
  "name": "John Smith",
  "birthDate": "2004-01-26",
  "image": "https://example.com/users/john-smith/icon.png"
}
```

インラインの文脈と外部の文脈を同時に使いたい場合には、JSONの配列を利用できます。

```json
{
  "@context": [
    "https://schema.org",
    {
      "url": "@id"
    }
  ],
  "url": "https://example.com/users/john-smith",
  "name": "John Smith",
  "birthDate": "2004-01-26",
  "image": "https://example.com/users/john-smith/icon.png"
}
```

### その他のキーワード

すべてのキーワードの一覧は以下に網羅されています。

https://www.w3.org/TR/json-ld/#syntax-tokens-and-keywords

## RDFとの関連

JSON-LDは、RDF(Resource Description Framework)を記述するものでもあります。詳しくは [10. Relationship to RDF](https://www.w3.org/TR/json-ld/#relationship-to-rdf) を参照してください。

また [RDFを記述する構文](https://service.infocom.co.jp/das/loddiary/2015/01/20150127001259.html) も参考になります。

## 参考

- JSON-LD 1.1 A JSON-based Serialization for Linked Data
    - https://www.w3.org/TR/json-ld11/
- RDF 1.1 Concepts and Abstract Syntax
    - https://www.w3.org/TR/rdf11-concepts/
- RDFを記述する構文
    - https://service.infocom.co.jp/das/loddiary/2015/01/20150127001259.html
