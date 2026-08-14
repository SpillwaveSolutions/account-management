---
name: acm-validate
description: Validate Account Management concepts: required fields, types, and in-bundle links.
---

# acm-validate

```bash
python3 "${CLAUDE_PLUGIN_ROOT}/scripts/acm_common.py" validate --bundle knowledge
```

Fail on missing `type`/`title` or broken absolute links.
