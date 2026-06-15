# SnapKitty Sovereign OS — Architecture Overview

## The Stack

```
┌─────────────────────────────────────────────────────────┐
│                    collectivekitty                       │
│              (Next.js 16 — Sovereign UI)                │
├─────────────────────────────────────────────────────────┤
│                   snapkitty-core                        │
│     (Rust agent runtime, kinetic layer, WORM ledger)    │
├──────────────┬──────────────────┬───────────────────────┤
│  silverback  │     bifrost      │      soul-bus         │
│ (microkernel)│ (Merkle-DAG, WORM│  (inter-agent NATS)   │
├──────────────┴──────────────────┴───────────────────────┤
│                   Bridge Layer (10 languages)            │
│  Haskell·Prolog·Rust·APL·COBOL·C++·Lisp·Elixir·TS·Robots│
├─────────────────────────────────────────────────────────┤
│              Formal Verification Layer                   │
│         Lean 4 (policy) · Prolog (logic) · Haskell (types)│
└─────────────────────────────────────────────────────────┘
```

## Sovereign Chain

Every decision flows through:
```
ANU quantum source
    → ThermalWindow (Haskell, proven lo < hi)
    → QuantumSuperposition (Haskell monad)
    → 5-pass ERE (Prolog / Haskell / JS)
    → METATRON certify (weighted Watchtower majority ≥ 0.5)
    → Born-rule collapse (highest-amplitude branch wins)
    → No-Cloning (LinearTypes — single use)
    → Verdict (Lean 4 algebra)
    → Bifrost commit (WORM-sealed Merkle event)
```

## Key Invariants

| Invariant | Where Proven |
|-----------|-------------|
| `lo(f) < hi(f)` for all `f ∈ [0,1]` | `thermal.hs` smart constructor |
| No temperature observed twice | `no_cloning.hs` LinearTypes GADT |
| `decide_sound`: `decide e s = true → validEvent e s` | `Bifrost/Policy.lean` (sorry → Week 3) |
| `call_49(call_49(X)) = X` | `quantum_monad.pl` `mirror_identity/1` |
| ERE score 0.0 ↔ METATRON:YES | `edaulc_verify.pl` all-pass gate |

## The 49th Call

One operation across three generations of languages:
- APL (1962): `⌽X`
- Prolog (1972): `call_49(X, Y) :- reverse(X, Y).`
- Haskell (1990): `call49 = reverse`

Reading backward reveals what reading forward conceals.

## Workspace Topology

```
bobs control repo/
├── DEVFLOW-FINANCE/         — Rust workspace (4 crates) + 13 JS packages
│   └── bridges/             — 32+ multi-language bridge files
├── snap-os/                 — Rust workspace (16 crates)
├── sovereign-context-tools/ — npm monorepo (6 packages, 2 vsix)
├── tools/                   ← THIS REPO — meta-catalog
├── proofs/                  — formal verification collection
└── resonance-core/          — math engine (RESONANCE-CORE)
```

## Security Boundary

SENTINEL identified three threat vectors (2026-06-06):
1. **Ghost Protocol** — agents callable without reasoning audit
2. **Verification Gap** — zero VERIFY entries between squash clusters
3. **GATE-LOCK SUBSTITUTION** — erase reasoning → retain gate → inject agents

Defense: per-agent content-hash in `mod.rs`, async verification before RETAIN fires.
Shrew attestation (Level 4) covers all bridge binaries.
