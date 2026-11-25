# lib-rand

Random **port types** for the Handl platform — the contract side of
the port/impl split. Backends `rand-c` (C entropy) and `rand-js`
implement the same interface.

## Layout

| path | role |
| --- | --- |
| `src/index.hnl` | the contract |
| `pkg.hnl` | manifest — dep `type`, `modules: ["rand"]` |
| `scripts/hnl-gate.sh`, `workflows/gate.yaml` | the gate / bupha entry |

## Contract

- Port types for randomness; see `src/index.hnl` for the signature
  surface (unseeded + `seeded_*` families).

## Verification

```bash
HNL=../host-cli/target/debug/hnl scripts/hnl-gate.sh
```

## License

MIT.

<!-- myco:agent-awareness -->

## Agent awareness

- Session start / any work discussion: run `myco status --prompt`
  before proposing next steps — know the board first.
- User describes new work → offer to capture it (`myco todo add`,
  `issue new`, `proposal new`). Don't wait to be asked.
- Picking up a task: `myco resume <ID>` is the briefing.
- Wrapping up: `myco handoff <ID>` anything resumable; keep statuses
  honest (claimed → in-progress → blocked/done).

<!-- /myco:agent-awareness -->
