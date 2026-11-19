# Array-form IDOR — id[]=attacker&id[]=victim bypass

**Rating:** 🔥 قوية  
**Category:** IDOR, API Hacking  
**Status:** Not started  

## How It Works

ACL sometimes checks a single scalar id. Sending the same parameter as an array (id[]= or id as JSON array) can make the backend iterate and return or act on a second ID without ownership checks. Compare single-id 403 vs array 200 on authorized test objects only.

## Payload / Code

```
id=attacker_id  → 403
id[]=attacker_id&id[]=victim_id  → 200?
id=[attacker_id, victim_id]  (JSON)
Also: ids=1,2 or objects[0][id]=victim
```

## Source

Twitter/X IDOR edge-case tips (array/list parameters) + 2026 hunting notes

---

_Synced from Notion: Bug Bounty Tips and Tricks. Authorized testing only._
