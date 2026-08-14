---
name: acm-init
description: Scaffold the Account Management catalogs in a shared second-brain bundle.
---

# acm-init

Create the catalogs this plugin owns inside a shared knowledge root.

## Process

1. Confirm target (default `knowledge/`).
2. Run:

```bash
python3 "${CLAUDE_PLUGIN_ROOT}/scripts/acm_common.py" init-bundle \
  --bundle knowledge \
  --title "Account Management" \
  --catalogs "clients,contacts,stakeholders,account-plans,deliverables,milestones,issues,commitments,meetings,risks"
```

3. Point the user at `sample-knowledge/` for a fictional demo.

## Done when

- `knowledge/index.md` exists
- Each owned catalog has `index.md`
