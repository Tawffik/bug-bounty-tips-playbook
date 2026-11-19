# Default-ish admin password pattern: admin / [company]12345

**Rating:** ⭐ جيدة  
**Category:** Auth Bypass  
**Status:** Not started  

## How It Works

Some internal or legacy admin panels still use predictable defaults built from the company name. Only test on in-scope login surfaces with program-allowed credentials testing; never spray broadly.

## Payload / Code

```
Username: admin
Password candidates (examples only):
[company]12345
[company]1234
[Company]@123
admin@[company]

Prefer single-target manual checks over mass spraying. Log only whether login succeeded for your test account scope.
```

## Source

Mohamed Ahmed — default password tip

---

_Synced from Notion: Bug Bounty Tips and Tricks. Authorized testing only._
