# Broken Access: function-level (access admin endpoint as normal user)

**Rating:** 🔥 قوية  
**Category:** Auth Bypass, IDOR  
**Status:** Not started  

## How It Works

مش IDOR object، ده endpoint كامل. جرب /admin/, /api/internal/, /manage/* بسيشن يوزر عادي.

## Payload / Code

```
As low-priv user: GET /api/admin/users or /internal/config
```

## Source

Broken Access Control 2026 blueprint

---

_Synced from Notion: Bug Bounty Tips and Tricks. Authorized testing only._
