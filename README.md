# Zethora™

**Fair money for people and machines.**

Bitcoin left your home. Zethora brings it back.

---

## What Zethora is

Zethora is a proposed Layer-1 blockchain that brings together four properties no single network has combined:

| | Inspired by | In Zethora |
|---|---|---|
| **Scarcity** | Bitcoin | 100,000,000 ZTHR, ever. Every coin mined. No premine. |
| **Speed** | Solana | ~1 block per second (BlockDAG). Everyday payments safe in ~10 seconds. |
| **Programmability** | Ethereum | Safe object-based smart contracts. Anyone can create tokens. |
| **Privacy** | Monero / Zcash | Private by default. Supply always provable. |

Plus what none of them have built in:

- **Home-computer mining.** CPU-friendly proof-of-work. No warehouses, no special chips.
- **Coins you can't lose.** Built-in recovery and inheritance.
- **Wallets for machines.** Cars, robots and AI agents can hold funds under rules their owner sets.

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
| Mining | RandomX (home-CPU proof of work), ~1 block per second |
| Fees | Tips to miners; base fees 60% to the miner fee pool, 40% burned, enforced by consensus |
| Verification | Independent nodes re-check and agree on every block |
| Addresses | `zethora:` format |

Not built yet: privacy, wallet app, recovery and inheritance, smart contracts and tokens, RandomX key rotation.

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

- **[Lightpaper v0.2](./Zethora_Lightpaper_v0.2.pdf)**: the overview
- **[Specifications](./specs/)**: the full rules
- **[Reference tools](./tools/)**: tested supply and fee calculations
- **[zethora-node](https://github.com/ceoghoxst/zethora-node)**: the prototype node (Rust)

| Spec | Topic |
|---|---|
| [000](./specs/ZTH-SPEC-000-foundation.md) | Foundation |
| [001](./specs/ZTH-SPEC-001-monetary-policy.md) | Monetary policy |
| [002](./specs/ZTH-SPEC-002-execution.md) | Execution / programmability |
| [003](./specs/ZTH-SPEC-003-tokens.md) | Tokens and launchpad standards |
| [005](./specs/ZTH-SPEC-005-consensus-speed.md) | Consensus, mining and speed |
| [006](./specs/ZTH-SPEC-006-privacy.md) | Privacy and provable supply |
| [008](./specs/ZTH-SPEC-008-fees.md) | Fees, fee pool and burn |
| [009](./specs/ZTH-SPEC-009-nodes-network.md) | Nodes and network |
| [010](./specs/ZTH-SPEC-010-wallets.md) | Wallets, recovery and inheritance |
| [011](./specs/ZTH-SPEC-011-upgrades.md) | Upgrades and governance |
| [012](./specs/ZTH-SPEC-012-security.md) | Security and launch gates |
| [013](./specs/ZTH-SPEC-013-genesis-launch.md) | Genesis and launch |

---

## Roadmap

1. **Specification**: draft v0.1 published
2. **Prototype**: working devnet node (you are here)
3. **Public testnet**: minimum six months, open to all
4. **Mainnet**: only when every launch gate passes
5. **Ecosystem**: apps, launchpad, AI compute marketplace, devices

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
