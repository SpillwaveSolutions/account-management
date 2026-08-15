---
name: grok-bot-account-management
description: Bind a Grok Bot agent to the account-management ContentPack. Isolation, identity, deterministic writes.
---

# Grok Bot / Account Manager

Read `docs/ONBOARDING.md` first, then follow `docs/GROK_BOT.md`.

1. Identity: `grok-bot/account-management`
2. Open an isolation session before writes (`scripts/brain_session.py open`) unless the human already pointed `SECOND_BRAIN_ROOT` at a session worktree.
3. Pack 2 hops, then write owned types only via `scripts/acm_common.py write --author`.
4. Close the session to PR. Report path + SHA.
5. Never document a private remote. Never write raw Markdown into the tree.
