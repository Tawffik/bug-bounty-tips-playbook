# Different 404 Fingerprint → Look for a Separate Backend API Context

**Rating:** ⭐ جيدة  
**Category:** Recon, API Hacking  
**Status:** Not started  

## How It Works

A useful clue from Berserker's write-up: malformed or unusual paths produced a 404 response with a different structure from the normal frontend 404. That suggested the request had reached a different routing/backend layer. The researchers then inspected public JavaScript for a production API hostname and found that it exposed the same API behind a different edge configuration. Treat response differences as a lead, not proof of a bypass: frameworks, gateways, and error handlers can also produce different 404s.

## Payload / Code

```
Passive-first workflow for an in-scope target:
1. Save one normal 404 response and one response from a harmless, invalid route; compare body template, headers, server/framework fingerprints, and request IDs.
2. Inspect publicly served JavaScript and source maps for API base URLs, service hostnames, version prefixes, and environment-specific endpoints.
3. Compare documented/public API surfaces on discovered in-scope hostnames; look for OpenAPI/WADL metadata only where access is permitted.
4. If a separate backend is found, verify its ownership and scope, then test authorization using your own account and harmless resources.
5. Report only a demonstrated security difference; a distinct 404 or a hostname difference alone is not a vulnerability.
```

## Source

https://medium.com/@Berserker1337/secondary-context-leads-to-company-takeover-0dc88ca751ea

---

_Synced from Notion: Bug Bounty Tips and Tricks. Authorized testing only._
