# AI support agents as attack surface (IDOR / BAC / XSS)

**Rating:** 🔥 قوية  
**Category:** IDOR, Auth Bypass, XSS, API Hacking  
**Status:** Not started  

## How It Works

Companies replace human support with LLM agents that can look up accounts, change details, and issue refunds. Same bug classes with new names: agent shows another user's data = IDOR; agent does admin actions for a normal user = broken access control; unescaped agent output on a page = XSS. Start from OWASP Top 10 for LLM Apps. Prefer two test accounts and clear evidence. Do not auto-confirm from chat text alone.

## Payload / Code

```
Map support/chat/agent endpoints
Prompt injection to request other-user data (authorized tests only)
Compare agent actions with and without session
Check reflected agent HTML sinks
```

## Source

Twitter/X @dd_pwnd — support chat is part of the attack surface (Nov 2026); ~$50k reports mentioned with low competition

---

_Synced from Notion: Bug Bounty Tips and Tricks. Authorized testing only._
