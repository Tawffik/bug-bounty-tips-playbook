# .htpasswd / .htaccess exposed → Basic Auth credentials

**Rating:** ⭐ جيدة  
**Category:** Recon  
**Status:** Not started  

## How It Works

لو .htpasswd مكشوف، تقدر تعمل crack للـ hashes وتدخل على الـ protected areas.

## Payload / Code

```
https://target.com/.htpasswd
https://target.com/.htaccess
```

## Source

Classic misconfig

---

_Synced from Notion: Bug Bounty Tips and Tricks. Authorized testing only._
