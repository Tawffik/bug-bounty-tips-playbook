# Empty API response subdomain → still try full Swagger paths

**Rating:** ⭐ جيدة  
**Category:** Recon, API Hacking  
**Status:** Not started  

## How It Works

حتى لو الـ API subdomain بيرجع empty body، جرب المسارات الكاملة لـ Swagger: /swagger-ui.html /swagger/index.html /api/swagger-ui.html /v1/swagger-ui.html /swagger/swagger-ui.html

## Payload / Code

```
ffuf -u https://api.target.com/FUZZ -w swagger_paths.txt -mc 200
```

## Source

Book of BugBounty Tips

---

_Synced from Notion: Bug Bounty Tips and Tricks. Authorized testing only._
