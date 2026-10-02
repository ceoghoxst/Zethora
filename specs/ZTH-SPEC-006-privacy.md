# ZTH-SPEC-006: Privacy and Provable Supply

**Project:** Zethora (ZTHR). Built by DeionRaven Labs.
**Status: Direction LOCKED (Oct 2, 2026).** Cryptographic parameters OPEN.
**Depends on:** ZTH-SPEC-000, ZTH-SPEC-001, ZTH-SPEC-005.

## 1. Purpose
Make Zethora private by default without ever allowing hidden inflation.

## 2. Locked decisions

| Decision | Value |
|---|---|
| What is hidden | Sender, receiver, and amount (Monero-level) |
| Default | Private by default in every standard wallet |
| Transparent mode | Optional, for parties who need it (e.g. exchanges, businesses). Using it exposes only that party's own activity. Wallets must show: "Transparent mode: anyone in the world can see this address's balance and history. This cannot be undone for past transactions." |
| View keys | Users may create read-only keys and share them voluntarily (taxes, audits). No master key exists for anyone |
| Technology | Zero-knowledge proofs with no trusted setup (Halo 2 family or successor) |
| Network privacy | Dandelion++-style relaying plus Tor/I2P support, hiding transaction origin IPs |
| Supply | Always provable; privacy can never hide inflation |

## 3. How privacy works for a user (plain language)
3.1 Inside your wallet: balances, senders, receivers and amounts are hidden from everyone, including DeionRaven.
3.2 Exchanges and payment providers know their own customers (ID checks), as with every coin. They do not see what happens after coins reach a private wallet.
3.3 Nobody, including governments or the founder, can use the chain to see a private wallet's history unless its owner shares a view key.

## 4. Hack protections (LOCKED)
History shows privacy can hide inflation bugs: Bytecoin 2017 (exploited, ~693M coins), Firo/Zcoin 2017 (exploited, ~370K coins), Zcash 2018 (counterfeiting bug, fixed quietly), Zcash Orchard 2026 (unlimited-counterfeit bug undetected 4 years; exploitation cannot be ruled out), Firo Spark 2026 (forgery flaw, emergency fork). Zethora therefore requires:

4.1 **Turnstile accounting.** All value entering and leaving the private pool is counted publicly. The private pool can never release more than entered it. A hidden counterfeit can never escape into circulation.
4.2 **Continuous supply proof.** Nodes verify every block that total supply matches the SPEC-001 schedule, using commitment sums anyone can recompute.
4.3 **Multiple independent audits** of privacy circuits before launch and after every change, including AI-assisted review.
4.4 **Formal verification** of core privacy circuits (machine-checked proofs that constraints are complete).
4.5 **Bug bounty** sized so reporting pays more than exploiting.
4.6 **Staged rollout.** Limits on private-pool flow early, raised as confidence grows. OPEN: limit values and schedule.

## 5. Threats

| Threat | Mitigation |
|---|---|
| Counterfeit coins via circuit bug | Turnstile 4.1, supply proof 4.2, audits, formal verification |
| Small private crowd | Private by default |
| Exchanges delisting | Transparent mode for exchanges |
| IP tracking | Dandelion++ / Tor / I2P |
| Coerced disclosure | No master key; view keys only by owner |
| Wallet bugs leaking data | Wallet audits; open-source reference wallet |

## 6. Interactions
- SPEC-001: supply must stay provable; prohibition on privacy hiding inflation.
- SPEC-002 (Execution): private smart contracts are FUTURE (SPEC-000 6.2).
- SPEC-003 (Assets): user tokens may be private; same turnstile rule applies per asset.
- SPEC-010 (Wallets): view keys, recovery, device wallets.

## 7. Open issues
1. Exact proof system and curves.
2. Turnstile design per pool and per asset.
3. Staged-rollout limits.
4. Fee and size impact of private transactions.
5. Transparent-mode address format.

## 8. Changelog
- Oct 2, 2026: Direction LOCKED: full privacy by default, optional transparent mode, view keys, ZK without trusted setup, network privacy, six hack protections.
