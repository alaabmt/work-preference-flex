# QA Report — V17.5 Report Architecture

## Scope

V17.5 is a participant-report architecture and language revision built directly on the uploaded V17.4 Rich Report package. It does not change the 56-item assessment content, item IDs, core scoring calculations, coach storage logic, or approved infographic images.

## Automated/static checks

| Check | Result | Detail |
|---|---|---|
| Preference items | PASS | 30/30 retained |
| Social items | PASS | 9/9 retained |
| Environment-need blocks | PASS | 9/9 retained |
| Flex items | PASS | 8/8 retained |
| Item-bank IDs/content | PASS | Standalone `item-bank.json` unchanged from V17.4 |
| Approved infographic images | PASS | Both image files unchanged from V17.4 |
| Arabic/English participant pages | PASS | V17.5 report renderer present in both |
| Report sections | PASS | 10 report sections defined |
| JavaScript syntax | PASS | `node --check` passed for every inline script in `ar.html` and `en.html` |
| JSON validity | PASS | `item-bank.json` and `manifest.json` parse successfully |
| Duplicate static HTML IDs | PASS | None detected in `index.html`, `ar.html`, `en.html`, or `coach.html` |
| GitHub root structure | PASS | `index.html` is at ZIP root; `.nojekyll` present |

## V17.5 report safeguards verified in source

- Core participant results retain numeric indices but no longer use `/100` in the report display.
- Core scale uses 50 only as an explicitly labeled within-scoring-format reference, not a population mean.
- Participant report language uses **approach / أسلوب** rather than difficult participant-facing terms such as orientation/tendency/prominent/less-relative.
- Section 6 retains the visual priority sequence and explicitly states that it is **not** a fixed behavioral sequence.
- Social Coordination is reported as direct counts across the 9 sampled situations, plus process breakdown, rather than a 0–100 hero score.
- Environment Needs are rank-first; numeric priority indices are secondary.
- Flex is reported factor-by-factor without a participant-facing total score or shift-count headline.
- Shifted and consistent Flex responses use neutral status styling; change is not visually rewarded as inherently better.
- The Development & Coaching section no longer selects the lowest Core result as the automatic development target.
- Coaching is organized around real evidence, context, contribution, fit/cost, impact, alternative response, and a small experiment.
- Report sections are labeled **Section / قسم** rather than Page until browser/PDF pagination is visually verified.

## Preservation checks

Compared with the uploaded V17.4 package, the following were intentionally retained unchanged at content/logic level:

- `item-bank.json` item content and IDs
- participant assessment/scoring calculations
- `coach.html` logic (display version label only updated)
- `workplace_response_decision_map.png`
- `how_do_you_respond_at_work.png`
- localStorage/session architecture
- raw JSON/CSV export logic (download filename updated to V17_5)

## Browser/print limitation in this environment

A real headless-browser navigation attempt was made, but local/file navigation is blocked by the execution environment administrator. Therefore a complete browser-driven 56-screen click-through and visual print/PDF verification could not be completed here. JavaScript/JSON/static structure checks passed. After deployment, perform a final visual check in Chrome/Edge/Safari, especially Arabic RTL print-to-PDF pagination and mobile layout.
