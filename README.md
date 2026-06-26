# SNAPKIT — SnapKitty Tools Meta-Catalog

Comprehensive inventory of all artifacts across the SnapKitty Sovereign OS ecosystem:
22 Rust crates · 21 npm packages · 6 VS Code extensions · 7 compiled binaries · 10 bridge languages

## Quick Reference

| Category | Count | Key Examples |
|----------|-------|--------------|
| Rust Crates | 22 | snapkitty-core, silverback, bifrost, soulvm |
| npm Packages | 21 | collectivekitty, api-bucket, woz-vault, abzu |
| VS Code Extensions | 6 | vscode-edaulc, vscode-woz-vault, forge-completions |
| Binary Executables | 7 | ahmad-meta, quantum-governance, nova-signal |
| Bridge Languages | 10 | Haskell, Prolog, Rust, APL, COBOL, C++, Lisp, Elixir, TypeScript, Robotics |
| Bridge Files | 32+ | 11 Haskell, 7 Prolog, 5 Rust, 2 APL, 2 COBOL, 1 C++, 1 Lisp |

## Structure

```
catalog/
├── index.yaml       — machine-readable master index
├── crates.yaml      — all Rust crates (workspaces: DEVFLOW-FINANCE, snap-os)
├── npm.yaml         — all npm packages (monorepos: sovereign-context-tools, DEVFLOW-FINANCE/packages)
├── extensions.yaml  — VS Code extensions (publisher: snapkitty)
├── binaries.yaml    — compiled ELF binaries in bridges/bin
└── bridges.yaml     — multi-language bridge integrations
```

## Repositories

| Repo | Purpose |
|------|---------|
| **DEVFLOW-FINANCE** | Sovereign OS runtime, Next.js UI (collectivekitty), bridge layer |
| **snap-os** | Microkernel (silverback), SoulVM, Bifrost audit chain |
| **sovereign-context-tools** | EDAULC linter, ABZU context GC, IDE extensions |
| **RESONANCE-CORE** | Math engine — entropy, quantum monad, thermal, ERE |
| **civicmind** | Civic intelligence Next.js application |
| **snapkitty-bot** | Discord bot |
| **vault-fundability-engine** | Fundability analysis engine |

## License

Sovereign Source License v1.0. Individual packages may carry MIT or Apache 2.0 — see each package manifest.

![](https://sovereign-analytics.snapkittywest.workers.dev/canary/SNAPKIT)
