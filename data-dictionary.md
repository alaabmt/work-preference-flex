# Data Dictionary — V17.5

Participant sessions retain research fields needed for pilot analysis, including participant code, administration occasion, item-bank version, item/option order, raw responses, response timing, revisions, profile fields provided by the participant, relative preference indices, Social Coordination choices, Environment Needs ranks, and contextual Flex choices.

The participant code is intended for longitudinal linkage without encoding personally identifying information. The prototype stores sessions locally in the browser; cross-device research collection requires a secure backend.


## Stored score fields used by the V17.5 report

These fields may appear inside `scores` after completion:

- `scores.core.<U|S|A>.index`: relative 0–100 core emphasis index.
- `scores.social.index`: retained descriptive percentage in stored data; the V17.5 participant report does **not** use it as a hero score and instead shows direct counts (e.g., 6/9).
- `scores.needs.indices.<need>`: relative 0–100 environment-need index.
- `scores.flex.shiftCount`: retained for research/export as the number of matched pairs in which the selected response changed; the V17.5 participant report does **not** headline this count or treat it as a Flex score.
