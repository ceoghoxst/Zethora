# Zethora™

**Fair money for people and machines.**

Bitcoin left your home. Zethora brings it back.

---

## What Zethora is

Zethora is a proposed Layer-1 blockchain that combines three working properties no single network has brought together — plus privacy, currently under review:

| | Inspired by | In Zethora |
|---|---|---|
| **Scarcity** | Bitcoin | 100,000,000 ZTHR, ever. Every coin mined. No premine. |
| **Speed** | Kaspa / Solana | ~1 block per second (BlockDAG). Everyday payments safe in ~10 seconds. |
| **Home mining** | Monero | CPU-friendly proof-of-work (RandomZ). No warehouses, no special chips. |
| **Privacy** | Zcash | Private by default. Integrated (Orchard 0.16.0). Disabled on public networks until an independent cryptographic review is complete. |

Plus what none of them have built in:

- **Coins you can't lose.** Built-in recovery and inheritance (planned).
- **Wallets for machines.** Cars, robots and AI agents can hold funds under rules their owner sets (planned).

### Programmability — planned research, not a current feature

Zethora does **not** currently support smart contracts. The `simpa` crate in the node repository is a Kaspa network simulator inherited with the fork; it is not a virtual machine.

If programmability is added in the future, the design direction is an object-model language in the Move family (as used by Sui and Aptos). This would require a formal VM specification, independent cryptographic review, wallet tooling, and a dedicated engineering team funded over multiple years.

It is not promised for testnet. It is not promised for mainnet. It may not ship at all.

---

## Status

**Prototype stage. A private Zethora devnet is running on a home PC. There is no public network yet.**

- Specifications: **Draft v0.1, open for public comment**
- Prototype node: **running** ([zethora-node](https://github.com/ceoghoxst/zethora-node), forked from Kaspa's open-source BlockDAG node)
- Public testnet: not live
- Mainnet: not live

What already works on the private devnet:

| | |
|---|---|
| Supply rule | 100M cap, smooth decay, 1,000 ZTHR never-mined reserve |
| Genesis | 0 coins, "Wake Up From The Dream World" |
| Mining | RandomZ (home-CPU proof of work), ~1 block per second |
| Fees | Tips to miners; base fees 60% to the miner fee pool, 40% burned, enforced by consensus |
| Verification | Independent nodes re-check and agree on every block |
| Supply check | Every block proves visible coins + fee pool + burned + private pool = coins issued. A block that is off by even 1 zet is rejected |
| Attack test | A money-printing bug was planted on purpose; the node refused to continue and no fake coin entered the chain |
| Addresses | `zethora:` format |

Privacy design: chosen and specified (Orchard / Halo 2, no trusted setup; see [ZTH-SPEC-006](./specs/ZTH-SPEC-006-privacy.md)). The private pool's public balance (turnstile) is already enforced; private transactions themselves are disabled on testnet and mainnet pending an independent cryptographic review.

Not built yet: private transactions on public networks, wallet app, recovery and inheritance, smart contracts and tokens, RandomX key rotation.

There is **no Zethora token today.** Anything claiming to be one is not Zethora.
The $ZERO token on pump.fun is **not part of Zethora** and will not migrate.

---

## Core rules

- **Fair launch.** Genesis contains 0 coins. No premine, no presale, no founder or investor allocation.
- **No owner.** No admin key, no pause button, no freeze power. Not for anyone, including the builders.
- **Fixed supply.** 100M ZTHR. The money rules can never change.
- **Announced launch.** The launch date and software are published one month in advance so anyone in the world can mine from block one.
- **Provable start.** The first block carries the hash of the latest Bitcoin block at launch, proving no one mined early.
- **Security first.** Mainnet launches only after independent audits, formal verification, and at least six months of public testnet.

---

## Monetary summary

| | |
|---|---|
| Ticker | ZTHR |
| Max supply | 100,000,000 |
| Smallest unit | 1 zet = 0.0000000001 ZTHR |
| Issuance | Mining only, smooth decay (no halving cliffs) |
| Half mined | ~8 years |
| 90% mined | ~27 years |
| Fees | Fractions of a cent; 60% to a miner fee pool, 40% burned |

---

## Documents

- **[Lightpaper v0.3](./Zethora_Lightpaper_v0.3.md)**: the overview
- **[Specifications](./specs/)**: the full rules
- **[Reference tools](./tools/)**: tested supply and fee calculations
- **[zethora-node](https://github.com/ceoghoxst/zethora-node)**: the prototype node (Rust)

| Spec | Topic | Status |
|---|---|---|
| [000](./specs/ZTH-SPEC-000-foundation.md) | Foundation | Active |
| [001](./specs/ZTH-SPEC-001-monetary-policy.md) | Monetary policy | Active |
| [002](./specs/ZTH-SPEC-002-execution.md) | Execution / programmability | **Planned, not implemented** |
| [003](./specs/ZTH-SPEC-003-tokens.md) | Tokens and launchpad standards | **Planned, not implemented** |
| [005](./specs/ZTH-SPEC-005-consensus-speed.md) | Consensus, mining and speed | Active |
| [006](./specs/ZTH-SPEC-006-privacy.md) | Privacy and provable supply | Active |
| [008](./specs/ZTH-SPEC-008-fees.md) | Fees, fee pool and burn | Active |
| [009](./specs/ZTH-SPEC-009-nodes-network.md) | Nodes and network | Active |
| [010](./specs/ZTH-SPEC-010-wallets.md) | Wallets, recovery and inheritance | Active |
| [011](./specs/ZTH-SPEC-011-upgrades.md) | Upgrades and governance | Active |
| [012](./specs/ZTH-SPEC-012-security.md) | Security and launch gates | Active |
| [013](./specs/ZTH-SPEC-013-genesis-launch.md) | Genesis and launch | Active |

---

## Roadmap

1. **Specification**: draft v0.1 published
2. **Prototype**: working devnet node (you are here)
3. **Public testnet**: minimum six months, open to all
4. **Mainnet**: only when every launch gate passes
5. **Ecosystem**: apps, tools
6. **Research**: programmability, if pursued

---

## Get involved

Zethora is built in the open.

- **Read the specs** and open an issue with questions or problems you find.
- **Propose changes** through Zethora Improvement Proposals (ZIPs).
- **Builders wanted**: Rust, cryptography, consensus, wallets, security.

Contributors receive credit. Never coins. The fair launch stays fair.

---

## Disclaimer

This repository describes a proposed design. It is not an offer to sell anything, not investment advice, and makes no claims about the future price or value of any asset.

---

*Wake Up From The Dream World.*

X: [@ZethoraNetwork](https://x.com/ZethoraNetwork) · Built by DeionRaven Labs
