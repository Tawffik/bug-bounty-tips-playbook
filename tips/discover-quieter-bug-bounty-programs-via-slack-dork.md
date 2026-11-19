# Discover quieter bug bounty programs via Slack dork

**Rating:** ⭐ جيدة  
**Category:** Recon, General  
**Status:** Not started  

## How It Works

Many companies publish security/bug bounty status on Slack directories or pages indexed by Google. A simple dork finds program mentions that are less crowded than top HackerOne lists.

## Payload / Code

```
site:slack.com "Has a bug bounty program"
site:slack[.]com "Has a bug bounty program"

Then open official policy URL from the page (example pattern: responsible-disclosure pages).
```

## Source

AnmolSecSavvy — site:slack.com Has a bug bounty program · Oct 2025

---

_Synced from Notion: Bug Bounty Tips and Tricks. Authorized testing only._
