---
title: "MCPサーバーをスクリプトのように書き捨てよう"
emoji: "⚡"
type: "tech"
topics: ["MCP", "MCP Server", "TypeScript", "script"]
published: true
---

## はじめに

みなさん、MCPを活用していますか？

良質なMCPサーバーを探したり開発したりするのも良いですが、MCPサーバーは実際のところ非常に簡単に作成できるため、ちょっとした自動化やタスクの解決にスクリプト感覚で使い捨てることができます。

この記事では、スタンドアローンで動作する非常にシンプルなMCPサーバーを作成し、適当なAIエージェントで動作させる方法を紹介します。

## 簡単なMCPサーバーの例

以下は基本的なMCPサーバーの例です。
このMCPサーバーは、エージェントからの入力をそのまま返すだけの`Echo`ツールを提供します。

このように、MCPサーバーは30行程度のボイラープレートで作成可能です。

```TypeScript
import { McpServer } from '@modelcontextprotocol/sdk/server/mcp.js';
import { StdioServerTransport } from '@modelcontextprotocol/sdk/server/stdio.js';
import { CallToolResult } from '@modelcontextprotocol/sdk/types';
import { z } from 'zod';

const mcpServer = new McpServer({
  name: 'Echo',     // MCPサーバー名
  version: '0.1.0',
});

mcpServer.tool(
  "Echo",                   // ツール名
  "returns the input text", // ツールのDescription
  { text: z.string().describe("Input for the tool"), }, // ツールが受け取るパラメータ
  async ({ text }) => {
    // 主な処理を書く
    return {
      // エージェントに返る内容になる
      content: [{ type: 'text', text: text }],
    } satisfies CallToolResult;
  },
);

async function main() {
  const transport = new StdioServerTransport();
  await mcpServer.connect(transport);
  console.log('MCP Server is running...');
}

main().catch((error) => {
  console.error('Error starting MCP Server:', error);
  process.exit(1);
});
```

## スタンドアローンスクリプトにする

1ファイルにMCPサーバーを押し込んで、それを単独で実行できれば、MCPサーバーをスクリプト的に使い捨てるのも簡単になりそうです。

そこで次のshebangを先ほどのファイルの先頭につけて、外部の依存関係を解決できるようにします。

```TypeScript
#!/bin/sh
":" //# ; npx --yes --package @modelcontextprotocol/sdk --package zod --package tsx tsx $0 "$@"

import { McpServer } from '@modelcontextprotocol/sdk/server/mcp.js';
...
```

このようにすると、次のようにしてお使いのAIエージェントが手軽にMCPサーバーを利用できるようになります。

```json
{
  "mcpServers": {
    "echo-mcp": {
      "command": "bash",
      "args": ["/path/to/echo.mcp.ts"],
    }
  }
}
```

## おわりに

MCPサーバーの作成は一見すると複雑そうですが、実際には非常に簡単に作ることができます。
日常的なタスクを自動化したり、特定の作業を効率化したりするために、気軽にスクリプトを書く感覚でMCPサーバーを作ってみてください。

ぜひ、お手軽にMCPサーバー作りを試してみてください。
