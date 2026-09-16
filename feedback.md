# Build progress — SaraBCA

## What was built

A disruption-care chat agent for Larkspur Airlines, built step by step against the Claude Messages API.

## Steps completed

| Step | Gate | Evidence |
|---|---|---|
| 1.2 — Loop holds | ✓ banked | FA2-FA2 |
| 1.3 — Tools route | ✓ banked | 4F9-56D |
| 1.4 — All five shapes | ✓ banked | B22-5C7 |
| 2.1 — Own tool (next_available_day) | ✓ banked | — |
| 2.2 — Same tool over MCP | ✓ banked | — |
| 3.1 — Eval proof | in progress | — |
| 4.1 — Intelligence lane | not started | — |

## Key decisions made

- Fixed the loop to pass `response.content` (not `text_of(response)`) as the assistant turn, which resolved the `tool_use_id` mismatch error.
- Wrote the `search_alternatives` description from scratch after the gate caught the 6-character placeholder.
- Added `next_available_day` as a local tool in Build 2, then moved it to MCP ownership in step 2.2.
- Wrote eval case `grnd-0201`: K7PQ2M / Marchetti, hurricane question, hard gate — **PASSED**.

## What the evals showed

5/6 cases passed (83%). `tone-0101` failed: the agent gave a normal entitlements rundown on a legal threat instead of escalating. That gap is what Build 4's `TONE_ADDENDUM` closes.

## Still open

- PITCH.md needs `Built`, `Does`, `Guardrail`, `Next` filled in to bank 3.1.
- Build 4 (step 4.1) — intelligence lane, tone addendum.
- Submission: `python3 readout.py` then pod agrees who runs `--push-canon`.
