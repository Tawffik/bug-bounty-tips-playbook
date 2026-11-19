# Disable JavaScript → legacy / forgotten form still live

**Rating:** ⭐ جيدة  
**Category:** Recon, Auth Bypass  
**Status:** Not started  

## How It Works

SPA frontends often hide or replace old flows with JS. Turning JS off (or fetching without executing scripts) can expose forgotten HTML forms and endpoints still wired on the server. Bots rarely do this. Use only on authorized targets; document the exact path and impact.

## Payload / Code

```
Browser: disable JS → reload sensitive flows (password reset, recovery, signup)
curl without following SPA redirects; compare HTML to JS-enabled view
Look for old form actions still posting to live APIs
```

## Source

Twitter/X @dd_pwnd — Google account recovery with JS off loaded an old form that leaked phone numbers ($5k, 2025 story retold 2026)

---

_Synced from Notion: Bug Bounty Tips and Tricks. Authorized testing only._
