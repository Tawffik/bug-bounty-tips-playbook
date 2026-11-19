# Bypass File Upload Validation بـ Magic Bytes

**Rating:** 🔥 قوية  
**Category:** General  
**Status:** Not started  

## How It Works

بعض الأنظمة بتتحقق من أول بايتات فقط في الملف المرفوع (Magic Bytes/File Signature) بدون ما تفحص كل الملف. لو حطيت Magic Bytes بتاعة PNG/JPG في أول الملف وبعدين حطيت كود ضار (webshell)، الفاليديشن بتعدية بتقبله — ويتنفّذ لو السيرفر بيمشيه بامتداد الملف الأصلي.

## Payload / Code

```
مثال: ابدأ الملف بـ magic bytes PNG (x89PNGrnx1an) ثم ضيف كود الـ PHP shell بعدين
دمجها مع double extension: shell.png.php أو content-type manipulation لنتيجة أقوى
```

## Source

Intigriti Official — 31 Bug Bounty Tips 2026 (Tip 19)

---

_Synced from Notion: Bug Bounty Tips and Tricks. Authorized testing only._
