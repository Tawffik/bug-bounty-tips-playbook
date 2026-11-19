# .DS_Store + Thumbs.db exposure → directory structure leak

**Rating:** ⭐ جيدة  
**Category:** Recon  
**Status:** Not started  

## How It Works

ملفات macOS/Windows hidden بتتساب على السيرفر. .DS_Store بيكشف أسماء الملفات والمجلدات، Thumbs.db نفس الفكرة. مفيد جداً لما تلاقي directory listing مقفول.

## Payload / Code

```
https://target.com/.DS_Store
https://target.com/Thumbs.db
# استخدم dsstore parser بعد التحميل
```

## Source

Classic overlooked recon (still pays when combined with sensitive paths)

---

_Synced from Notion: Bug Bounty Tips and Tricks. Authorized testing only._
