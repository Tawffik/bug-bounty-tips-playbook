# CSRF token bypass via HTTP method override

**Rating:** ⭐ جيدة  
**Category:** CSRF, Auth Bypass  
**Status:** Not started  

## How It Works

Some apps only enforce CSRF tokens on POST. Switching method to GET with X-HTTP-Method-Override: POST, or using PUT/DELETE, can skip the token check while the backend still performs the state change. Confirm SameSite and cookie behavior; only test authorized actions on your accounts.

## Payload / Code

```
Original: POST /change-email with CSRF token
Test: GET /change-email?email=attacker@x.com
Header: X-HTTP-Method-Override: POST
Also try: X-HTTP-Method: PUT , _method=POST form field
```

## Source

Twitter/X @yogsec — CSRF Token Bypass via Method Override (Nov 2026)

---

_Synced from Notion: Bug Bounty Tips and Tricks. Authorized testing only._
