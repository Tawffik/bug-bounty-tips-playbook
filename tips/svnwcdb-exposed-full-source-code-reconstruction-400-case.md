# .svn/wc.db exposed → full source code reconstruction ($400 case)

**Rating:** 🔥 قوية  
**Category:** Recon  
**Status:** Not started  

## How It Works

جرب /.svn/wc.db. لو موجود، حمله واستخدم sqlite3 عشان تستخرج الـ pristine paths وتبني الـ source كامل (زي .git).

## Payload / Code

```
wget https://target.com/.svn/wc.db
sqlite3 wc.db 'select local_relpath from NODES;'
```

## Source

Vipul Sahu Medium writeup ($400)

---

_Synced from Notion: Bug Bounty Tips and Tricks. Authorized testing only._
