---
name: acm-pack
description: Build a bounded ContextPack from a Account Management root concept (default 2 hops, 20 nodes).
---

# acm-pack

## Process

```bash
python3 "${CLAUDE_PLUGIN_ROOT}/scripts/acm_common.py" pack \
  --bundle knowledge \
  --root "/clients/example.md" \
  --hops 2 \
  --max-nodes 20
```

Use `--hops 1` for a tiny pack. Outbound edges only. Do not dump the whole tree.
