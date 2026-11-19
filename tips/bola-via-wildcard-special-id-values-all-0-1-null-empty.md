# BOLA via Wildcard / Special ID Values (*, all, 0, -1, null, empty)

**Rating:** 🔥 قوية  
**Category:** IDOR, API Hacking  
**Status:** Not started  

## How It Works

Some backends treat special values as "all objects" or skip ownership checks when the ID is not a normal UUID/integer. Replace the object ID with *, all, any, 0, -1, null, empty string, or undefined. Also try path tricks (../users/victim, trailing / or ?). High impact when it returns mass data or allows mass modification.

## Payload / Code

```
GET /api/users/*
GET /api/users/all
GET /api/users/0
GET /api/users/-1
GET /api/users/null
GET /api/users/

Also: id=*, id[], id[0]=victim
```

## Source

Twitter/X @yogsec — BOLA via Wildcard & Special ID Values (Nov 2026)

---

_Synced from Notion: Bug Bounty Tips and Tricks. Authorized testing only._
