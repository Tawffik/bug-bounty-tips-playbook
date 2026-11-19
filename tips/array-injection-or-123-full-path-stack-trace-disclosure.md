# Array injection ([] or [1,2,3]) → Full Path / Stack Trace Disclosure

**Rating:** ⭐ جيدة  
**Category:** Recon, General  
**Status:** Not started  

## How It Works

حط array في أي parameter (حتى لو مش متوقع). كتير من الـ frameworks بترمي error فيها full path أو stack trace أو internal class names. مفيد جدًا لـ path disclosure وخطأ oracle.

## Payload / Code

```
param[]=1
param[1,2,3]=test
param[][]=1
```

## Source

Book of Bug Bounty Tips + multiple hunters

---

_Synced from Notion: Bug Bounty Tips and Tricks. Authorized testing only._
