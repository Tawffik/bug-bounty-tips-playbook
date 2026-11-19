# Cloudflare Worker/API Key Exposure → Edge JavaScript Supply-Chain Injection

**Rating:** ⭐ جيدة  
**Category:** Recon, API Hacking, General  
**Status:** Not started  

## How It Works

A September 2026 incident showed how a broad Cloudflare API key exposed in application source could be used to create Workers, routes, and DNS changes, allowing JavaScript to be modified at the edge without changing the origin. The hunting lesson is to treat exposed CDN/edge credentials and third-party script delivery as a chain: source/config leak → edge control-plane access → route or Worker modification → customer-facing script integrity impact. Study Tab: JS/config/source maps → search for CDN or edge-provider credentials and deployment references → edge control-plane abuse → validate scope, permissions, and harmless response-integrity differences. Use when: a target uses Cloudflare Workers, Pages, CDN-managed scripts, or embeds third-party JavaScript across many customer sites.

## Source

BreachHistory / Brevo incident analysis — 14–15 Sep 2026 — https://breachhistory.com/blog/brevo-cloudflare-clickfix-supply-chain-september-2026

---

_Synced from Notion: Bug Bounty Tips and Tricks. Authorized testing only._
