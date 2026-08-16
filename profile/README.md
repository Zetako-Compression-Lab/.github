# Zetako Compression Lab

**Sovereign software infrastructure and original deep-tech research.**

Zetako Compression Lab is the public engineering and research showcase for **Zetako S.à r.l.**

The organization documents two complementary areas of work:

- **ZNode** — sovereign workspace infrastructure for private organizational communication, collaboration, governance and controlled operations;
- **Zetako compression research** — proprietary lossless-compression technologies for blockchain infrastructure, general-purpose data and embedded telemetry.

Production source code and proprietary codec cores remain private. This GitHub organization publishes the engineering evidence around the products: architecture, methodology, benchmark results, deployment models, product evolution, operational boundaries, integration experiments and clearly scoped technical claims.

**Luxembourg · [zetako.ai](https://zetako.ai/) · contact@zetako.ai**

---

## Engineering portfolio

| Project | Focus | Public repository |
|---|---|---|
| **ZNode** | Sovereign workspace infrastructure | [Znode-sovereign-workspace-infrastructure](https://github.com/Zetako-Compression-Lab/Znode-sovereign-workspace-infrastructure) |
| **ZCaps** | General-purpose adaptive lossless compression research | [Zcaps-Adaptive-lossless-statistical-compressor](https://github.com/Zetako-Compression-Lab/Zcaps-Adaptive-lossless-statistical-compressor) |
| **ZChain** | Blockchain-native lossless compression engine | [ZChain-blockchain-native-lossless-compression-engine](https://github.com/Zetako-Compression-Lab/ZChain-blockchain-native-lossless-compression-engine) |
| **ZNano** | Lossless compression for embedded telemetry | [Znano-Structured-Telemetry-Compression](https://github.com/Zetako-Compression-Lab/Znano-Structured-Telemetry-Compression) |

---

## ZNode

### Sovereign workspace infrastructure

ZNode is Zetako's **self-hosted, single-node sovereign workspace** for organizations that want to retain control over communications, collaboration, data, administration and operational access.

The platform combines product surfaces such as:

- direct and group messaging;
- workspace and file collaboration;
- voice, video and meetings;
- administrative and policy controls;
- audit and security event records;
- compliance-oriented governance;
- controlled support and maintenance models;
- agent-ready infrastructure with scoped execution, visible principals and auditability.

The public ZNode repository is an **engineering evidence layer**, not the proprietary application source repository.

It currently documents:

- product evolution;
- single-node architecture and deployment boundaries;
- reference deployment profile;
- SQLite + local-filesystem data model;
- operating and support models;
- Compliance Center and governance model;
- security and test evidence;
- performance methodology;
- live external-vs-backend latency decomposition;
- future capacity, SFU, storage and pilot benchmark campaigns.

Current public engineering evidence includes a **1,613-test automated suite**, **327 HTTP routes**, **6 read-only agent tools**, **9 scoped compliance export data types**, and an instrumented live-development latency baseline that separates external TCP/TLS/network time from ZNode application processing.

The supported V1 profile is intentionally **single-node by design**: one controlled deployment boundary, local transactional state, local filesystem storage, dedicated Z-Connect/SFU services where enabled, and explicit backup/recovery ownership.

**Positioning:** *Sovereign workspace infrastructure.*

[Explore ZNode →](https://github.com/Zetako-Compression-Lab/Znode-sovereign-workspace-infrastructure)

---

## Compression research portfolio

Zetako develops three specialized compression lines for three different engineering constraints: **general-purpose data**, **blockchain infrastructure**, and **embedded telemetry**.

### ZCaps

#### General-purpose adaptive lossless compression research

ZCaps explores a general-purpose codec architecture built around **adaptive context modeling, prediction, and statistical entropy coding**.

The research direction is deliberately different from a conventional dictionary-first compressor: instead of primarily searching for repeated byte sequences, ZCaps continuously learns from the stream and models what is likely to occur next.

Public work includes:

- exact lossless validation on established compression corpora;
- compression-density and throughput measurements;
- adaptive context-modeling research;
- Balanced / Fast / Max optimization directions;
- architecture documentation at a non-proprietary level;
- clear separation between codec-only speed and full product-path overhead.

**Positioning:** *General-purpose adaptive lossless compression research.*

[Explore ZCaps →](https://github.com/Zetako-Compression-Lab/Zcaps-Adaptive-lossless-statistical-compressor)

---

### ZChain

#### Blockchain-native lossless compression engine

ZChain is designed for **structured blockchain data paths**, where the runtime already knows whether it is processing blocks, receipts, transactions, signatures, RPC payloads, account keys, consensus results, or storage records.

Rather than treating every payload as generic bytes, ZChain increasingly uses that structural knowledge to choose the right compression model for the serialization family being processed.

Its public engineering history deliberately shows the evolution of the product:

**v3 → v4 → Speed_First → blockchain-aware models → schema-assisted models → current Blockchain Engine direction**

The public repository contains dedicated benchmark and methodology pages for:

- **Ethereum / Reth**;
- **Solana mainnet RPC**;
- **Agave validator integration**;
- **Cosmos / CometBFT**;
- version-to-version performance deltas;
- compatibility boundaries;
- selected codec comparisons.

The goal is straightforward: **reduce the bytes moved or stored by blockchain infrastructure while preserving exact reconstruction and keeping processing cost practical for the target path.**

**Positioning:** *Blockchain-native lossless compression engine.*

[Explore ZChain →](https://github.com/Zetako-Compression-Lab/ZChain-blockchain-native-lossless-compression-engine)

---

### ZNano

#### Lossless compression for embedded telemetry

ZNano targets **structured telemetry and constrained devices**, where bandwidth, flash, RAM, deterministic reconstruction, and implementation footprint all matter.

The public evidence set covers metering and telemetry payloads, multi-frame processing, host validation, MCU-oriented footprint measurements, and functional evidence across Cortex-M class targets.

Typical domains include:

- smart metering;
- industrial telemetry;
- IoT and LPWAN;
- GNSS / positioning;
- embedded systems with constrained memory and transport budgets.

The documentation explicitly separates **host benchmark timing** from **MCU runtime claims**, and distinguishes measured, calculated, and target-dependent metrics.

**Positioning:** *Lossless compression for embedded telemetry.*

[Explore ZNano →](https://github.com/Zetako-Compression-Lab/Znano-Structured-Telemetry-Compression)

---

## Why three compression lines?

Compression is not one problem.

A blockchain validator, a general-purpose archive, and a Cortex-M telemetry device operate under very different constraints. Zetako therefore develops separate architectures instead of forcing one codec to compromise across every workload.

| Constraint | ZCaps | ZChain | ZNano |
|---|---:|---:|---:|
| General-purpose data | **Primary** | Secondary | No |
| Blockchain structure awareness | No | **Primary** | No |
| Embedded / MCU constraints | No | Limited | **Primary** |
| Adaptive statistical modeling | **Core research** | Used where relevant | Lightweight / constrained |
| Throughput-sensitive infrastructure | Yes | **Primary** | Target-dependent |
| Tiny implementation footprint | No | No | **Primary** |

---

## How we publish engineering evidence

This organization is an **evidence layer**, not a source-code dump of proprietary implementations.

We publish material that allows an external engineer, researcher, customer, security team, partner, or investor to understand what has been built and how the claims are supported:

- architecture and deployment boundaries;
- reproducible benchmark methodology;
- public datasets or dataset-fetch instructions where appropriate;
- exact round-trip integrity evidence for compression research;
- compression ratio and throughput reported together;
- hardware and build context for performance measurements;
- version evolution and measurable engineering deltas;
- integration architecture and readiness boundaries;
- security and governance evidence at a non-sensitive level;
- limitations when they materially affect interpretation.

We intentionally keep private:

- proprietary ZNode production source code;
- proprietary codec core implementations;
- production credentials and secrets;
- customer data and customer-specific deployment details;
- exploit-relevant security implementation details;
- internal tuning data;
- sensitive or customer-specific datasets;
- protected commercial integrations.

---

## Engineering principles

**Measured claims should be inspectable.** Public performance claims should retain enough methodology and scope to be interpreted correctly.

**Sovereignty requires operational clarity.** Deployment boundaries, data ownership, support access and recovery responsibilities should be explicit.

**Lossless means exact reconstruction.** A compression improvement only counts when the original payload is reconstructed exactly.

**Ratio and speed belong together.** A smaller output with unacceptable latency is not automatically a better engineering result.

**Native codec and integration overhead are separate measurements.** Build profile, wrappers, I/O, hashing, serialization, network paths and host application behavior can materially affect observed throughput or latency.

**Claims stay scoped.** A result on one deployment, corpus, blockchain payload, MCU target or hardware configuration is not presented as a universal guarantee.

**Continuous iteration matters.** Public version histories are intended to show measurable progress in performance, capability, compatibility, governance and deployment readiness.

---

## About Zetako

**Zetako S.à r.l.** is a Luxembourg deep-tech company developing sovereign software infrastructure and proprietary data-compression technologies.

**Website:** [zetako.ai](https://zetako.ai/)  
**Contact:** contact@zetako.ai  
**Location:** Luxembourg

---

<sub>Public benchmark and operational figures in the linked repositories represent specific test environments, datasets, product versions, profiles and measurement boundaries. They should always be interpreted together with their documented methodology and scope.</sub>
