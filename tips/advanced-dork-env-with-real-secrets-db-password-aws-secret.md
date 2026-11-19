# Advanced Dork: .env with real secrets (DB_PASSWORD / AWS_SECRET)

**Rating:** 🔥 قوية  
**Category:** Recon  
**Status:** Not started  

## How It Works

ابحث عن .env اللي فيه علامات secrets حقيقية مش مجرد أسماء. دي بتجيب نتائج عالية الجودة.

## Payload / Code

```
site:target.com (ext:env OR inurl:.env) ("DB_PASSWORD" OR "AWS_SECRET_ACCESS_KEY" OR "SECRET_KEY" OR "APP_KEY")
```

## Source

dorksearch.com + multiple 2025-2026 guides

---

_Synced from Notion: Bug Bounty Tips and Tricks. Authorized testing only._
