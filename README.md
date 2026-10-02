# ChatGPT Session Workspace Study

Empirical study of whether a ChatGPT session can serve as a practical, evidence-preserving software project workspace.

> **Result:** yes, conditionally — when execution, durable evidence, repository state, external compute, and publication are treated as separate systems with explicit handoff and verification boundaries.

## Highlights

- **Project workflow and persistence** — session-local work, artifact handoff, connectors, Drive backup, GitHub operations
- **Meta-observability** — what session history can be observed and how much chronology can be recovered
- **Execution workspace** — runtime limits, dependency provisioning, native build, test, and debug work
- **Pilots** — CPython (build, test, debug, rebuild) and Foundry PR #306 / LigandMPNN (inference, validation, recovery, scaling)

## Key findings

- Repository-oriented project work is viable through explicit state boundaries and connector or API operations
- The sandbox can build, test, and debug native software and run realistic CPU scientific workflows within resource limits
- Runtime continuity is not guaranteed; execution state is not durable storage
- Resource visibility, authorization, connector actions, and file representation fail independently
- Large raw evidence can be preserved off-runtime and verified by download, hashing, reassembly, and integrity checks
- The useful model is hybrid: compose session execution, local workstations, CI, GPU or HPC systems, Git, and durable storage by workload

## Repository

- `docs/` — study narrative in three parts, method, and assessment
- `experiments/` — procedures and experiment records
- `evidence/` — compact evidence kept in Git
- `playbook/` — workflow-selection guidance for new projects
- `release-assets/` — bundle metadata, checksums, and notices
- `legacy/`, `artifacts/`, `archive/` — historical compatibility trees

## Start here

- [Overview](docs/00-study-overview.md) · [Method](docs/01-method-and-evidence-policy.md) · [Assessment](docs/99-overall-assessment.md)
- [Playbook](playbook/README.md) · [Bootstrap brief](playbook/CHATGPT_SESSION_BOOTSTRAP.md)

## Evidence

- **Git** — narrative, methods, compact evidence, playbook
- **Release `study-v1.0.0`** — complete CPython and Foundry bundles with verification sidecars; see [third-party notices](release-assets/THIRD_PARTY_NOTICES.md)

## Related

- [chatgpt-session-ops](https://github.com/daylight-00/chatgpt-session-ops) — operating protocol and tools

## License

- [MIT](LICENSE) for original material
- Third-party materials in the bundles keep their own licenses; see [RIGHTS.md](RIGHTS.md)
