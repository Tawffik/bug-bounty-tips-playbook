# AI Chat / Support Agent — conversationID / session UUID BOLA (unauthenticated or cross-user)

**Rating:** 🔥 قوية  
**Category:** IDOR, API Hacking, Auth Bypass  
**Status:** Not started  

## How It Works

AI assistants and support agents assign conversation or session UUIDs. GraphQL/REST resolvers frequently skip ownership and even authentication checks on history/read endpoints. Swap the conversationID (from URL, body, or WebSocket) with another user's; also test completely unauthenticated. Leaks private prompts, PII, booking details, or internal tool actions. Low competition surface in 2026.

## Payload / Code

```
POST /graphql
{"query":"query { papayaConversationHistory(conversationID: "victim-uuid") { messages } }"}

Or REST:
GET /api/chat/history?conversationId=victim-uuid
(without auth header)
```

## Source

Twitter/X @Bug_Breakdown + @dd_pwnd — unauthenticated GraphQL IDOR on AI chat history + support agents as attack surface (Nov 2026)

---

_Synced from Notion: Bug Bounty Tips and Tricks. Authorized testing only._
