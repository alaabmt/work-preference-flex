# Data Dictionary — V17.4

Participant sessions retain research fields needed for pilot analysis, including participant code, administration occasion, item-bank version, item/option order, raw responses, response timing, revisions, profile fields provided by the participant, relative preference indices, Social Coordination choices, Environment Needs ranks, and contextual Flex choices.

The participant code is intended for longitudinal linkage without encoding personally identifying information. The prototype stores sessions locally in the browser; cross-device research collection requires a secure backend.


## V17.4 report-derived indicators

These fields may appear inside `scores` after completion:

- `scores.core.<U|S|A>.index`: relative 0–100 core emphasis index.
- `scores.social.index`: descriptive percentage of direct social-coordination choices.
- `scores.needs.indices.<need>`: relative 0–100 environment-need index.
- `scores.flex.shiftCount`: number of matched pairs in which the selected core response changed; not a Flex score.
