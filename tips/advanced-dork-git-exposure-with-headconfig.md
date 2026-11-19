# Advanced Dork: .git exposure with HEAD/config

**Rating:** ⭐ جيدة  
**Category:** Recon  
**Status:** Not started  

## How It Works

ده dork لاكتشاف صفحات قد تشير إلى كشف .git، لكنه يعتمد على فهرسة محركات البحث وقد يرجع نتائج قديمة أو نتائج غير مؤكدة. افتح النتيجة يدويًا داخل نطاق البرنامج، وتحقق من إمكانية قراءة ملف غير حساس مثل HEAD. لا تعتبر مجرد ظهور المسار إثباتًا لكشف المستودع.

## Payload / Code

```
site:target.com inurl:.git ("HEAD" OR "config" OR "index of")
```

## Source

dorksearch.com + Proviesec + real cases

---

_Synced from Notion: Bug Bounty Tips and Tricks. Authorized testing only._
