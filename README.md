# Bug Bounty Tips & Tricks Playbook

Professional knowledge base of **bug bounty tips, techniques, and payloads**, exported from the Notion database **🐞 Bug Bounty Tips and Tricks**.

> **Authorized testing only.** These notes are research methodology and LEAD guidance. Never use them outside explicit program scope. Empty or weak evidence is not a finding.

## Status

| Item | Value |
|------|-------|
| Tips in this export | **100** |
| Tips in Notion source | **333** (as of export date) |
| Source | Notion DB `Bug Bounty Tips and Tricks` |
| License | For personal/team research use; respect original writeup licenses |

The remaining tips will be synced in a follow-up commit after Notion query quota resets.

## Structure

```text
tips/              # one Markdown file per tip
by-category/       # indexes per category (Recon, IDOR, SSRF, …)
data/tips.json     # machine-readable export
INDEX.md           # flat index of all tips in this export
CATEGORIES.md      # category map
```

## Categories in this export

- **Recon**: 57
- **API Hacking**: 28
- **General**: 17
- **Auth Bypass**: 15
- **IDOR**: 11
- **WAF Bypass**: 7
- **XSS**: 5
- **CSRF**: 4
- **Fuzzing**: 3
- **Subdomain Enum**: 1
- **SSRF**: 1
- **RCE**: 1
- **Password Reset**: 1

## How to use

1. Browse [CATEGORIES.md](./CATEGORIES.md) or [INDEX.md](./INDEX.md).
2. Open a tip file for **How it works** + **Payload / Code** + **Source**.
3. Treat everything as **LEAD**: confirm with evidence on accounts/objects you own.

## Relation to Zero Track / BugBountyCI

High-signal patterns (Magic DNS SSRF, WAF norm-fail, array IDOR, GraphQL mutation BOLA, AI chat conversationID, disclosure paths) feed operator checklists and wordlists in the private automation pipeline — **not** auto-confirmation.

## Sync notes

- Source of truth remains Notion until a full 333/333 export is committed.
- After quota reset, re-export and replace `data/tips.json` + regenerate `tips/`.

---
Generated for Tawffik · Bug bounty research knowledge base
