---
title: "بياناتك"
description: "ما يحتفظ به Vythea على حاسوبك، وما يُرسل إلى أين، وإضافة الأدوات من خوادم MCP."
---

يحتفظ Vythea ببياناته في مجلد واحد على حاسوبك:

- Windows: `%LOCALAPPDATA%\Vythea\`
- macOS: `~/Library/Application Support/Vythea/`
- Linux: `~/.local/share/Vythea/`

| الملف | يحتوي على |
|---|---|
| `chats.json` والجلسات | محادثاتك، والبوابة والنموذج اللذان اخترتهما |
| `keys.json` | مفاتيح API لكل بوابة، بنص عادي على قرصك وحده |
| `account.json` | تسجيل دخول Vythea على هذا الحاسوب |
| `SOUL.md` | هوية Vythea، بكلماتك (اختياري) |
| `USER.md`, `MEMORY.md` | ما يعرفه عنك، وملاحظاته الخاصة؛ عدّلها في أي وقت |
| `mcp.json` | خوادم MCP التي يجوز له استخدام أدواتها (اختياري) |
| `media/` | الصور والكلام والفيديو التي أُنشئت دون مشروع مرتبط بها |

إذا أرفقت مجلد مشروع، يُقرأ ملفه `AGENTS.md` بوصفه تعليمات المشروع. يذهب نص المحادثة إلى البوابة التي اخترتها ولا يذهب إلى أي مكان آخر؛ وعند استخدام بوابة Vythea، يكون ذلك api.vythea.com، الذي يسجّل النموذج وتكلفة كل طلب لصفحة الاستخدام الخاصة بك. والمهمة التي ترسلها إلى [Vythea Cloud](cloud.md) تعمل على خوادم Vythea، بما تحمله المهمة نفسها فقط.

## الأدوات من خوادم MCP

اذكر خوادم MCP التي تعمل كأمر محلي في `mcp.json`، بالصيغة نفسها التي يستخدمها Claude Desktop وكذلك Cursor:

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

تظهر أدواتها حين تردّ الخوادم. يسأل Vythea قبل كل استدعاء ما لم تكن الأداة في `autoApprove`؛ أما `"disabled": true` فيُبقي الخادم معطّلاً.
