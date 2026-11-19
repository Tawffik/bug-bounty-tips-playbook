# BOLA / IDOR via Batch & Bulk ID Mixing

**Rating:** 🔥 قوية  
**Category:** IDOR, API Hacking  
**Status:** Not started  

## How It Works

Many APIs expose batch/bulk endpoints that accept arrays of object IDs (ids[], JSON array of objects, /api/batch). Authorization is often checked only on the first ID or skipped per-item. Mix your own IDs with a victim ID in the same request; also try duplicate keys, partial-failure responses that leak existence, and array stuffing. If the server processes the victim object, you have scalable BOLA.

## Payload / Code

```
POST /api/batch
{"ids": ["your-id", "victim-id"]}

or
ids[]=your-id&ids[]=victim-id

or mixed objects:
[{"id":"your-id"}, {"id":"victim-id"}]
```

## Source

Twitter/X @yogsec — BOLA via Batch/Bulk Request ID Mixing (Nov 2026)

---

_Synced from Notion: Bug Bounty Tips and Tricks. Authorized testing only._
