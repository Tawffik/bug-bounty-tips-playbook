# Cloudflare R2.dev public access left on → data exposure

**Rating:** 🔥 قوية  
**Category:** Recon  
**Status:** Not started  

## How It Works

Cloudflare R2 buckets ممكن تتفتح عبر R2.dev للتجربة. لو المطور نسي يقفلها، تقدر توصل للـ objects بدون auth. دور على *.r2.dev أو CNAME لـ R2.

## Payload / Code

```
https://bucket-name.account-id.r2.dev/
# أو ابحث عن r2.dev في JS / DNS
```

## Source

Intigriti complete guide (updated 2026)

---

_Synced from Notion: Bug Bounty Tips and Tricks. Authorized testing only._
