---
title: "הנתונים שלכם"
description: "מה Vythea שומר על המחשב שלכם, מה הוא שולח לאן, והוספת כלים מתוך שרתי MCP."
---

Vythea שומר את הנתונים שלו בתיקייה אחת על המחשב שלכם:

- Windows: `%LOCALAPPDATA%\Vythea\`
- macOS: `~/Library/Application Support/Vythea/`
- Linux: `~/.local/share/Vythea/`

| קובץ | מכיל |
|---|---|
| `chats.json` והסשנים | השיחות שלכם, והשער והמודל שנבחרו |
| `keys.json` | מפתחות API לכל שער, בטקסט פשוט, רק על הדיסק שלכם |
| `account.json` | ההתחברות ל-Vythea במחשב הזה |
| `SOUL.md` | מי Vythea הוא, במילים שלכם (אופציונלי) |
| `USER.md`, `MEMORY.md` | מה הוא יודע עליכם, וההערות שלו; אפשר לערוך אותם בכל עת |
| `mcp.json` | שרתי MCP שמותר להשתמש בכלים שלהם (אופציונלי) |
| `media/` | תמונות, דיבור וסרטונים שנוצרו בלי פרויקט מקושר |

כשמצורפת תיקיית פרויקט, הקובץ `AGENTS.md` שבה נקרא כהוראות הפרויקט. טקסט הצ'אט נשלח לשער שבחרתם ולשום מקום אחר; בשער Vythea, זה api.vythea.com, שרושם לכל בקשה את המודל ואת העלות לעמוד השימוש שלכם. משימה ששולחים ל-[Vythea Cloud](cloud.md) רצה על השרתים של Vythea, ורק עם מה שהמשימה עצמה נושאת איתה.

## כלים מתוך שרתי MCP

רשמו את שרתי MCP שרצים כפקודה מקומית ב-`mcp.json`, באותה צורה שבה Claude Desktop ו-Cursor משתמשים:

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

הכלים שלהם מופיעים כשהשרתים עונים. כל קריאה שואלת קודם, אלא אם הכלי נמצא ב-`autoApprove`; `"disabled": true` משאיר שרת כבוי.
