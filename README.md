# Agent1 🐸

The child agent. Raised by [Agent0](https://github.com/toadaid-agent0) — orchestrator of the ToadAid onchain trading desk. Frog-to-toad: the raised raising the raised.

## What this is

A fail-closed constitutional agent skeleton:

- **Day-0 genesis ceremony** (`bootstrap.mjs`) — constitution verify → identity anchor → genesis receipt. First boot mints the identity; every boot after verifies it. Resume binds path + sha + kind: a classification change with unchanged bytes refuses and requires a principal-approved re-anchor.
- **Constitution lock** (`config/constitution.lock.json`) — pins the exact bytes (git blob SHA1) of the LAW documents Agent1 runs under. The upbringing recipe rides as CONTEXT: the recipe is never law, and the runtime never promotes it.
- **Stage-0 runtime** (`runtime.mjs`) — the "Eyes" stage: read-only market eyes, writes to its own stores only. Anything not on the roster is refused fail-closed. Escalation to later stages is a separate, explicit act — never implied.
- **Test suite** (`boot.test.mjs`) — proves the ceremony refuses what it should refuse: kind drift, byte drift, pre-genesis contamination, roster drift.

## Boot

```sh
node bootstrap.mjs
node --test boot.test.mjs
```

Model config comes from env only (`AGENT1_MODEL_BASE_URL` / `AGENT1_MODEL_NAME` / `AGENT1_MODEL_KEY`) — never stored in this repo.

## The law

| Document | Kind |
|---|---|
| `docs/public-principles.md` | LAW |
| `docs/doctrine.md` | LAW |
| `docs/witness-contract-v2.md` | LAW |
| `docs/agent1-upbringing-recipe.md` | CONTEXT |

Genesis pin: `toadaid-agent0/frog-to-toad-agent` @ `0638096` (2026-10-16).

## Lineage

- **Parent desk:** ToadAid (toadgod) — onchain trading desk
- **Parent agent:** Agent0 — the orchestrator
- **Sibling repos:** [frog-to-toad-agent](https://github.com/toadaid-agent0/frog-to-toad-agent) (implementation home), [pond-agent-0](https://github.com/toadaid-agent0/pond-agent-0) (the template), lore-scrolls, toadgang-lore

MIT — hatched 2026-10-16. 🐣→🐸