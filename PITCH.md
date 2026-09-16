# PITCH.md

Six lines and a lever. Your words. The last two are scored.

Built: A GenAI disruption-care agent for Larkspur Airlines with a connection protection tool.
Does: Handles rebooking for cancelled and delayed flights so customers don't wait 40 minutes on hold — looks up the booking, checks flight status, applies policy, and offers alternatives.
Number: $0.11 per resolved contact vs $6.90 for a human agent (98% cheaper). X% of contacts still escalate to a human for refunds, groups, minors, and out-of-scope cases.
Guardrail: Agent escalates to a human for refunds, groups of 12+, unaccompanied minors, and anything outside scope. Confirmation tokens — only the customer's own click — are required to finalise any rebooking.
Next: Tone detection for abusive or distressed messages (Build 4 intelligence lane).
Still broken: The agent can search alternatives and hold seats but cannot complete a booking — it cannot produce the confirmation token only the customer's click generates.
Lever: cost

## Priya asked

Costs: $0.11 per resolved contact against $6.90 human cost — but only for contacts the agent resolves on its own. A share still escalate to a human; the blended cost depends on that escalation rate.
Wrong: It can hallucinate or state false data — flight times, delay causes, and policy quotes come from the data it has. If that data is stale or wrong, the agent states it confidently anyway.
Runs it: Three functions need an owner after the team leaves — a policy/reference data steward to keep the data current, a technical operator to monitor and maintain the system, and an escalation/threshold owner to decide when the automation boundaries need to change.
Left out: The agent cannot complete a rebooking. It searches alternatives and holds seats, but finalising requires a confirmation token only the customer's own Confirm-click produces.
