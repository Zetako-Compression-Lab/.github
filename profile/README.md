# Zetako Compression Lab

**Sovereign deep tech, built from original research.**

Zetako Compression Lab is the public research and engineering showcase for Zetako's lossless compression work.

We develop specialized compression architectures for three different problem classes: general-purpose data, blockchain infrastructure, and constrained embedded telemetry. The proprietary production implementations remain private; the public repositories focus on measurable engineering progress, reproducible benchmark methodology, integration models, and clearly scoped technical claims.

**Luxembourg · [zetako.ai](https://zetako.ai/) · contact@zetako.ai**

---

## Compression research lines

| Project | Focus | Public positioning |
|---|---|---|
| **ZCaps** | General-purpose lossless compression | Adaptive contextual prediction and statistical entropy coding research |
| **ZChain** | Blockchain-native lossless compression | Payload-aware compression for blockchain clients, validators, RPC, execution-layer and consensus data |
| **ZNano** | Embedded telemetry compression | Lossless compression for metering, IoT, telemetry and constrained MCU environments |

---

## ZCaps

### General-purpose adaptive lossless compression research

ZCaps explores a general-purpose compression architecture centered on **adaptive context modeling, prediction and statistical entropy coding** rather than a conventional dictionary-first design.

The public research record documents:

- lossless validation on established public corpora;
- compression-density and throughput measurements;
- research profiles for balanced, fast and maximum-compression directions;
- architecture explanations at a non-proprietary level;
- the distinction between raw codec performance and complete product-path overhead.

**Public repository:** [ZCaps](https://github.com/Zetako-Compression-Lab/Zcaps-Adaptive-lossless-statistical-compressor)

---

## ZChain

### Blockchain-native lossless compression engine

ZChain is built specifically for structured blockchain data paths rather than as a generic "compress everything" library.

Its public engineering history shows the evolution from the original v3 compatibility profile through v4 optimization, Speed_First, blockchain-aware models, schema-assisted experiments and the current Blockchain Engine direction.

The public repository includes dedicated benchmark and methodology pages for:

- Ethereum / Reth;
- Solana mainnet RPC;
- Agave validator integration experiments;
- Cosmos / CometBFT;
- selected codec comparisons;
- version-to-version performance deltas and compatibility boundaries.

The goal is simple: **reduce the bytes moved or stored by blockchain infrastructure while keeping reconstruction exact and processing cost low enough for the target path.**

**Public repository:** [ZChain](https://github.com/Zetako-Compression-Lab/ZChain-blockchain-native-lossless-compression-engine)

---

## ZNano

### Lossless compression for embedded telemetry

ZNano targets structured telemetry and constrained systems where bandwidth, flash, RAM and deterministic reconstruction all matter.

The public evidence set covers metering and telemetry workloads, multi-frame processing, MCU-oriented footprint measurements and functional validation across Cortex-M class targets.

Public documentation deliberately separates host benchmark timing from MCU runtime claims and distinguishes measured, calculated and target-dependent metrics.

Typical domains include:

- smart metering;
- industrial telemetry;
- GNSS / positioning;
- IoT and LPWAN payloads;
- embedded systems with tight memory and transport constraints.

**Public repository:** [ZNano](https://github.com/Zetako-Compression-Lab/Znano-Structured-Telemetry-Compression)

---

## How we publish research

The public GitHub organization is designed as an **evidence layer**, not as a source-code dump of the proprietary compression cores.

We aim to publish:

- reproducible benchmark methodology;
- public datasets or dataset-fetch instructions where appropriate;
- round-trip integrity evidence;
- compression ratio and throughput together;
- hardware/build context for performance measurements;
- version evolution and engineering deltas;
- integration architecture and clear readiness boundaries;
- limitations and failed assumptions when they materially affect interpretation.

We intentionally keep private:

- proprietary codec core implementations;
- protected production builds and release engineering;
- internal tuning data and sensitive datasets;
- customer-specific integrations.

---

## Research principles

**Lossless first.** Compression improvements are only valid when the original payload is reconstructed exactly.

**Ratio and speed belong together.** A smaller output with unacceptable latency is a different engineering tradeoff, not automatically a better result.

**Native codec and integration overhead are measured separately.** Build profile, I/O, hashing, wrappers and host application behavior can materially change observed throughput.

**Claims stay scoped.** A benchmark on one blockchain payload, MCU target or corpus is not presented as a universal guarantee.

**Continuous iteration matters.** Public version histories are intended to show measurable progress in compression density, throughput, compatibility and deployment readiness.

---

## About Zetako

Zetako S.à r.l. is a Luxembourg deep-tech company developing sovereign software and original data-compression technologies.

**Website:** [zetako.ai](https://zetako.ai/)  
**Contact:** contact@zetako.ai  
**Location:** Luxembourg

---

<sub>Public benchmark figures in the linked repositories represent specific test environments, datasets, codec profiles and build configurations. They should always be interpreted together with their documented methodology and scope.</sub>
