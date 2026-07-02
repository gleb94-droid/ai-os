---
type: project
status: 🟡
---
# 📱 Wello

Gleb's app. **7-agent audit verdict: the bottleneck is OUTREACH, not the app.**

## Status
🟡 Agreed plan: mom as the 1st daily user · one-tap `?demo=1` (LIVE) · 15-sec video outreach · a kill/continue rule.

## Where the code lives (solved 2026-07-02)
- **Live:** `wello.sfalimshop.com` (Vercel project `wello` under the sfalimshop team; deployment URLs `wello-*-sfalimshop.vercel.app`; Vercel MCP hides the project — same as mehiron-haxam).
- **Local repo:** `C:/Users/Gleb/Documents/GitHub/wello` — created 2026-07-02 from a full live download (24 files, matches sw.js precache; the app is now MULTI-FILE: index.html + js/{data,state,utils,quotes,tasks,calendar,stock,ui,crm,help,nav,team,sb}.js + style.css + sw.js). The old Desktop copy (`Desktop/wello/wello version 1.0`, single-file, 2026-06-08) is OBSOLETE — never edit it.
- No GitHub remote yet.

## 2026-07-02 — Quick-start onboarding fixes (committed `efd432f`, NOT deployed)
Gleb's bug: "set my discount but the step didn't check off." Root cause: tier control shows default **50% already selected** → users never tap → `sfalim_tier` never saved. Fixes: **one-tap confirm button** («אשרו 50% ✓» + «לשנות») in the tier row · tier taps refresh the CRM checklist live + «שלב הושלם ✓» toast (first set only) · **5/5 celebration card** (trophy + existing qsDoneMsg + «הבנתי») instead of silent hide; demo account excluded. he/ru/en. Verified in browser (logic checks + RTL screenshot + RU, 0 console errors).

## Next
- **DEPLOY the quick-start fixes** (needs Gleb's go + establish the deploy path: Vercel CLI login or dashboard drag-drop).
- Next improvement blocks (agreed direction, non-technical users): **text-size control** (many .74–.9rem labels) → **login simplification** (invite links / persistent session).
- Outreach plan unchanged — app polish ≠ distribution ([[wello-outreach-not-app-problem]] still governs).

## Related
- [[Idea bank]]
