# Backup files (wp-config.php.bak, .env.bak, .sql, ~ files) → credentials leak

**Rating:** 📌 للمراجعة  
**Category:** Recon  
**Status:** Not started  

## How It Works

اكتشاف أسماء ملفات backup مفيد، لكن ليس كل ملف يحتوي credentials ولا كل كشف قابل للدفع. استخدم wordlist على الأصول المصرح بها بمعدل منخفض، وتحقق من نوع الملف ومحتواه بأقل دليل ممكن دون تحميل قواعد بيانات أو استخدام أسرار.

## Payload / Code

```
ffuf -u https://target.com/FUZZ -w backup_wordlist.txt
# أمثلة: wp-config.php.bak, .env.bak, backup.sql, database.sql
```

## Source

Intigriti WordPress guide + Burp labs + common practice

---

_Synced from Notion: Bug Bounty Tips and Tricks. Authorized testing only._
