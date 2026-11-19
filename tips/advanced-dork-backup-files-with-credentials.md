# Advanced Dork: Backup files with credentials

**Rating:** ⭐ جيدة  
**Category:** Recon  
**Status:** Not started  

## How It Works

الـ dork قد يجد ملفات backup مفهرسة، لكن نتائج البحث قد تكون قديمة أو أمثلة أو خارج النطاق. تحقق من وجود الملف واستجابة الخادم دون تنزيل dumps أو أسرار. أضف رابط مصدر محدد يثبت الطريقة بدل الاكتفاء بعبارة multiple guides.

## Payload / Code

```
site:target.com (ext:bak OR ext:old OR ext:backup OR ext:~ OR ext:swp) (password OR secret OR key OR db_)
```

## Source

Undercode + multiple guides

---

_Synced from Notion: Bug Bounty Tips and Tricks. Authorized testing only._
