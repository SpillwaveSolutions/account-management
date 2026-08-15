---
name: acm-capture
description: Capture a Account Management noun into the shared second brain via the deterministic write helper.
---

# acm-capture

## Process

1. Identify the noun type from the allowed list (see README).
2. Resolve identity: run `whoami`. If unclaimed, ask the user what to sign as, then `whoami --claim`. Do not invent a Grok Bot name.
3. Collect title, status, and optional typed links.
3. Write with the helper — do not hand-author frontmatter unless the user insists:

```bash
python3 "${CLAUDE_PLUGIN_ROOT}/scripts/acm_common.py" write \
  --bundle knowledge \
  --type Client \
  --folder clients \
  --title "Example Client" \
  --author "${SECOND_BRAIN_IDENTITY:?claim an identity first: brain.py whoami --claim}" \
  --tags "acm"
```

4. Add typed links in a follow-up edit if needed (`rel` values from `docs/typed-edges.md`).
5. Validate.

Allowed types: Client, Contact, Stakeholder, RelationshipHealth, AccountPlan, StatementOfWork, Deliverable, Milestone, Issue, Risk, Opportunity, Meeting, CallNote, EmailThread, Commitment, InvoiceStatus, ExpansionOpportunity, SatisfactionSignal, Escalation, RenewalDate, SuccessMetric.
