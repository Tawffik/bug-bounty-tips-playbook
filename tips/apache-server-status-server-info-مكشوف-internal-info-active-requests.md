# Apache server-status / server-info مكشوف → internal info + active requests

**Rating:** ⭐ جيدة  
**Category:** Recon  
**Status:** Not started  

## How It Works

/server-status بيرجع active connections، request URLs، client IPs. /server-info بيكشف modules و configuration. مفيد للـ recon العميق.

## Payload / Code

```
https://target.com/server-status
https://target.com/server-info
https://target.com/server-status?auto
```

## Source

Common misconfig still found in 2025-2026

---

_Synced from Notion: Bug Bounty Tips and Tricks. Authorized testing only._
