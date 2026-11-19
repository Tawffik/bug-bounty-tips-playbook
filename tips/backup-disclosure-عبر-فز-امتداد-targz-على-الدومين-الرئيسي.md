# Backup Disclosure عبر فزّ امتداد tar.gz على الدومين الرئيسي

**Rating:** 🔥 قوية  
**Category:** Recon, General  
**Status:** Done  

## How It Works

فزّ الدومين الرئيسي (مش subdomain فرعي) بامتداد أرشيف شائع زي tar.gz بدل الوقوف عند .env أو .git بس. نسخة احتياطية كاملة لإعدادات التطبيق ممكن تتسرب فيها بيانات اعتماد قاعدة البيانات ومفاتيح المصادقة والأسرار كاملة. الدرس: نفس فكرة ملفات الباك اب المنسية (.env, .git, .svn/wc.db) بس بامتداد مختلف وعلى نطاق أساسي بدل فرعي.

## Payload / Code

```
fuzz: main-domain.com/FUZZ with extension .tar.gz
(جرّب كمان .zip .rar .bak .old على نفس الدومين الرئيسي)
```

## Source

Kanhaiya Sharma (@krishnsec) — Standoff Bug Bounty, 12 Oct 2025, بونتي موثّق (8,081 views)

---

_Synced from Notion: Bug Bounty Tips and Tricks. Authorized testing only._
