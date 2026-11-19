# AI Builder Project Visibility Regression → Source / Chat History Authorization Boundary

**Rating:** 📌 للمراجعة  
**Category:** Recon, General  
**Status:** Not started  

## How It Works

Official historical evidence: Lovable reported and fixed a regression that exposed public-project chat history/source to other authenticated users with a project link. This supports the general authorization-boundary test idea, but does not establish a currently exploitable bug on Lovable or another product. Since this test needs two controlled accounts/projects and a current in-scope product, keep it as a review lead until a current candidate is independently verified.

## Payload / Code

```
For an explicitly in-scope AI builder or collaboration SaaS, compare permissions between the published app URL, project/editor URL, remix/share links, version history, generated source, and prompt/chat history using two accounts you control. Check whether an ordinary user can access project metadata or conversation history belonging to the second test account. Do not guess private links or access real customers' projects. Avoid retesting the disclosed Lovable regression unless the program explicitly requests verification.
```

## Source

Lovable official incident response (reported fixed) ; Escape research methodology on vibe-coded apps

---

_Synced from Notion: Bug Bounty Tips and Tricks. Authorized testing only._
