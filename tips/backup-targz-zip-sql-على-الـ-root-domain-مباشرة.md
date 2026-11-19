# Backup tar.gz / .zip / .sql على الـ root domain مباشرة

**Rating:** 🔥 قوية  
**Category:** Recon  
**Status:** Not started  

## How It Works

مش بس على subdomains. جرب الامتدادات الشائعة على الدومين الرئيسي نفسه: /backup.tar.gz, /db.sql, /site.zip, /backup.zip, /.env.bak. كتير من الـ misconfigs بتحصل على الـ root.

## Payload / Code

```
ffuf -w backups.txt -u https://target.com/FUZZ -e .tar.gz,.zip,.sql,.bak,.old
```

## Source

Multiple real bounties + Kanhaiya Sharma style writeups

---

_Synced from Notion: Bug Bounty Tips and Tricks. Authorized testing only._
