---
type: project
status: 🟡
---
# 🏷️ mehiron-haxam (= Wello)

"Smart Price List" / CRM PWA for Herbalife consultants — Gleb's separate project (NOT sfalimshop).
App title: **Wello — העוזר העסקי שלך**

- **Live:** mehiron-haxam.vercel.app · **Repo:** GitHub `gleb94-droid/mehiron-haxam`
- **Deploy:** GitHub → Vercel **auto-deploy**. ⚠️ Vercel MCP hides it — use the CLI.
- **Stack:** Vanilla JS PWA (no build step), Supabase, offline-first, SW caching

## Architecture (as of 2026-06-30)
Single-file app split into modular files (no ES modules — classic `<script src>`):
```
index.html    (~546 lines) — HTML only + 13 <script> tags
style.css     (1351 lines) — all CSS
js/data.js    ( ~402 lines) — products catalog, T i18n dict, ICONS, WHATS_NEW
js/state.js   (  84 lines) — shared state + all localStorage load/save
js/utils.js   (  15 lines) — ic(), t(), LOC(), fmt(), helpers
js/quotes.js  (  58 lines) — motivational quotes
js/tasks.js   (  67 lines) — personal tasks
js/calendar.js( 313 lines) — calendar & events
js/stock.js   ( 172 lines) — inventory
js/ui.js      ( 405 lines) — rendering, filters, cart
js/crm.js     (1415 lines) — clients, orders, WhatsApp
js/help.js    ( 614 lines) — help, AI assistant, onboarding
js/nav.js     ( 306 lines) — bottom nav, More, install
js/team.js    ( 810 lines) — team mode, pickers, pull-to-refresh
js/sb.js      ( 648 lines) — Supabase auth, DB sync, boot
```
SW cache: `v187-domain-split` (all files cached for offline).

## Status
🟡 Live. Modular refactor complete (2026-06-30). Step 2 (Supabase price editing) **pending**.

## Next
- Build step 2 — price editing via Supabase.
- Deeper feature work (reorder prediction, delight UX patterns).

## Related
- [[Idea bank]]
