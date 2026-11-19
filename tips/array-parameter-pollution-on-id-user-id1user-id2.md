# Array / parameter pollution on ID (user_id[]=1&user_id[]=2)

**Rating:** ⭐ جيدة  
**Category:** IDOR  
**Status:** Not started  

## How It Works

بعض الـ backends بياخدوا أول أو آخر قيمة، أو بيعملوا array. جرب [] أو تكرار الباراميتر.

## Payload / Code

```
user_id[]=victim&user_id[]=attacker
id=1&id=2
```

## Source

Classic still works

---

_Synced from Notion: Bug Bounty Tips and Tricks. Authorized testing only._
