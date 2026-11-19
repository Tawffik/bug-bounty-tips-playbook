# AWS tip: probe /ramp_core.js for embedded AccessKey material

**Rating:** ⭐ جيدة  
**Category:** Recon, API Hacking  
**Status:** Not started  

## How It Works

بعض تطبيقات/SDK قديمة أو حزم front-end تضع مسارات ثابتة فيها مفاتيح أو config. إضافة /ramp_core.js (ومسارات مشابهة من wordlists السحابية) لمرحلة content discovery قد تكشف AccessKeyId/Secret في JS. المفتاح وحده يحتاج إثبات صلاحية وتأثير داخل النطاق قبل البلاغ.

## Payload / Code

```
Add to content wordlist:
/ramp_core.js
/.aws/credentials
/config.json
/aws-config.js
After hit: extract AKIA… patterns; verify only with program-allowed checks; never use keys outside authorized testing.
```

## Source

Mr_mars_hacker AWS tip (X)

---

_Synced from Notion: Bug Bounty Tips and Tricks. Authorized testing only._
