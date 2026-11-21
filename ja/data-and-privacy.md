---
title: "あなたのデータ"
description: "Vythea がコンピュータに保存するもの、何をどこへ送るか、MCP サーバーからツールを追加する方法。"
---

Vythea のデータは、お使いのコンピュータのひとつのフォルダーにまとめて保存されます：

- Windows：`%LOCALAPPDATA%\Vythea\`
- macOS：`~/Library/Application Support/Vythea/`
- Linux：`~/.local/share/Vythea/`

| ファイル | 内容 |
|---|---|
| `chats.json` とセッション | 会話と、選んだゲートウェイとモデル |
| `keys.json` | ゲートウェイごとの API キー（お使いのディスク上にのみ、プレーンテキストで保存） |
| `account.json` | このコンピュータでの Vythea のログイン情報 |
| `SOUL.md` | Vythea がどんな存在かを、あなたの言葉で（任意） |
| `USER.md`、`MEMORY.md` | あなたについて知っていることと、エージェント自身のメモ（いつでも編集可） |
| `mcp.json` | ツールを使ってよい MCP サーバー（任意） |
| `media/` | プロジェクトを開かずに作った画像、音声、動画 |

プロジェクトフォルダーを開いている場合、その中の `AGENTS.md` がプロジェクトの指示として読み込まれます。チャットの内容が送られるのは、選んだゲートウェイだけです。Vythea ゲートウェイの場合、送り先は api.vythea.com で、使用量ページのために各リクエストのモデルと費用が記録されます。[Vythea Cloud](cloud.md) に送ったタスクは、Vythea のサーバー上で、タスク自身が持っているものだけを使って実行されます。

## MCP サーバーのツール

ローカルコマンドとして動く MCP サーバーを、Claude Desktop や Cursor と同じ形式で `mcp.json` に記述します：

```sh
{
  "mcpServers": {
    "everything": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-everything"],
      "autoApprove": ["echo"]
    }
  }
}
```

サーバーが応答すると、そのツールが使えるようになります。ツールが `autoApprove` にない限り、呼び出しのたびに確認します。`"disabled": true` を付けると、そのサーバーは無効のままになります。
