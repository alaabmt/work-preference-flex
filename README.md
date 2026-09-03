# Work Preference–Environment–Flex — V17 Theory-Aligned Pilot

This GitHub Pages package is a rebuild aligned to the revised theoretical architecture discussed on 2026-09-02/03.

## What changed
- Core preference model reduced to three provisional work-regulation orientations: **Understanding the Situation**, **Structuring the Work**, and **Starting Action**.
- **Working with Others / Social Coordination** is measured separately as a cross-cutting social focus rather than forced into the same rank profile.
- **Adapting the Approach** moved out of the core preference model. Flex is now described from response shifts across matched context pairs; there is no right/wrong Flex key and no Flex competence score.
- Environment Needs remain a separate pilot layer grounded conceptually in person–environment fit. Their internal structure is still provisional.
- The item bank now lives in one bilingual `item-bank.json`, so Arabic and English share the same IDs and scoring keys.
- All item and option order is deterministic from participant code + administration + bank version.
- Participant name is not collected.
- Coach packets use browser localStorage only; `coach.html` is a static prototype gate, not production security.

## Files
- `index.html` — language landing page
- `ar.html` — Arabic participant experience (RTL)
- `en.html` — English participant experience (LTR)
- `coach.html` — local prototype coach dashboard
- `item-bank.json` — bilingual single source of truth
- `assets/app.js`, `assets/app.css`, `assets/coach.js`
- approved homepage infographics in `assets/`
- `technical-notes.md` — construct and scoring notes
- `language-review.md` — bilingual writing standard and audit notes

## GitHub Pages
Upload the contents of this folder to the repository root, commit, and enable GitHub Pages from the branch/root you use. Do not open `ar.html`/`en.html` directly with `file://` because the browser may block loading `item-bank.json`; serve it through GitHub Pages or a local HTTP server.

## Prototype password
The coach password remains the user-specified prototype password. Only its SHA-256 hash is in the public JavaScript. This is **not** secure authentication.

## Research status
This is a **research pilot, not a validated or standardized assessment**. Core preference indices are ipsative/relative within an administration. Do not use them for hiring, promotion, firing, diagnosis, or other high-stakes decisions. Thurstonian/MFC calibration, content-validity evidence, desirability studies, cognitive interviews, reliability, test–retest, convergent/discriminant validity, invariance/DIF, and replication are still required.
