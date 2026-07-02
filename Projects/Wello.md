---
type: project
status: 🟡
---
# 📱 Wello

Gleb's app. **7-agent audit verdict: the bottleneck is OUTREACH, not the app.**

## Status
🟡 Agreed plan: mom as the 1st daily user · one-tap `?demo=1` (LIVE) · 15-sec video outreach · a kill/continue rule.

## Where the code lives (RESOLVED 2026-07-02, corrected same day)
- **⭐ TRUE SOURCE REPO: `C:/Users/Gleb/Documents/GitHub/mehiron-haxam`** → github `gleb94-droid/mehiron-haxam` → **auto-deploys** `mehiron-haxam.vercel.app`. Wello EVOLVED from the mehiron-haxam price-list PWA (hence the `sfalim-mehiron-*` SW cache names). Repo also holds STRATEGY.md / LEADER-PLAYBOOK.md / DEPLOY-README.md / sell.html. **Edit HERE.**
- **Live domains (both same app):** `wello.sfalimshop.com` (Vercel project `wello`, deployed via CLI `vercel deploy --prod --yes --cwd <folder-linked-to-wello>`) + `mehiron-haxam.vercel.app` (auto-deploy on push). v199/v200 were first deployed to the wello project from a live-download snapshot folder (`Documents/GitHub/wello`), then **ported into the real repo + pushed (`0a080bd`) — both domains verified serving v200**.
- ⚠️ The snapshot folder `Documents/GitHub/wello` is now REDUNDANT (same content) — don't develop there; candidate for deletion (ask Gleb). The Desktop copy (`Desktop/wello/wello version 1.0`) is OBSOLETE.
- Deploy rule stays: **bump `sw.js` CACHE on every deploy**; after pushing the repo also CLI-deploy the `wello` project so wello.sfalimshop.com updates.

## 🚀 Deploy path (established 2026-07-02)
`vercel deploy --prod --yes --cwd "C:/Users/Gleb/Documents/GitHub/wello"` — Vercel CLI 54 installed globally, logged in as gleb2009-1278, folder linked to project `wello` (team sfalimshop). ⚠️ PWA: **bump `sw.js` CACHE version on EVERY deploy** or installed users keep old files (cache-first SW).

## 2026-07-02 — Quick-start onboarding fixes (✅ DEPLOYED, live = v199)
Gleb's bug: "set my discount but the step didn't check off." Root cause: tier control shows default **50% already selected** → users never tap → `sfalim_tier` never saved. Fixes: **one-tap confirm button** («אשרו 50% ✓» + «לשנות», on their own row, bigger tap targets) in the tier row · tier taps refresh the CRM checklist live + «שלב הושלם ✓» toast (first set only) · **5/5 celebration card** (trophy + existing qsDoneMsg + «הבנתי») instead of silent hide; demo account excluded. he/ru/en. Commits `efd432f`+`df67bbd`. **Verified LIVE** (sw v199 served, translations render, 0 console errors).

## 2026-07-02 — Text-size control (✅ DEPLOYED, live = v200)
For older/non-technical distributors: **גודל טקסט** row in the More menu (3 growing letters א/A like phone system settings) → 100/115/130% via root `font-size` (all text is rem-based so everything scales; NO CSS zoom → no fixed-element traps). Persisted (`sfalim_textsize`), he/ru/en, verified no horizontal overflow at 130% on 390px. Commit `dabc6c6`.

**Deploy permission granted (2026-07-02):** Gleb explicitly authorized agent-run Vercel deploys — `Bash(vercel deploy *)` allow rule added to sfalimshop `.claude/settings.local.json`. Deploys no longer need the manual-command dance (still: bump sw.js CACHE every deploy).

## Next
- **Login simplification** (next agreed block): fresh users hit an email+password gate (`sbGate`) — the scariest screen for non-technical users. Ideas: invite links / persistent session / one-tap entry.
- Outreach plan unchanged — app polish ≠ distribution ([[wello-outreach-not-app-problem]] still governs).

## Related
- [[Idea bank]]
