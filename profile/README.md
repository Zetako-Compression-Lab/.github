# Zetako Compression Lab

**Sovereign deep tech, built from original research.**

Zetako Compression Lab is the public research and engineering showcase for Zetako’s proprietary lossless compression technologies.

We are developing three specialized compression lines for three different constraints: **general-purpose data**, **blockchain infrastructure**, and **embedded telemetry**. The production codec cores remain private; this GitHub organization publishes the engineering evidence around them — benchmarks, methodology, architecture, version evolution, integration experiments, and clearly scoped technical claims.

**Luxembourg · [zetako.ai](https://zetako.ai/) · contact@zetako.ai**

---

## Research portfolio

| Project | Focus | Public repository |
|---|---|---|
| **ZCaps** | General-purpose adaptive lossless compression research | [Zcaps-Adaptive-lossless-statistical-compressor](https://github.com/Zetako-Compression-Lab/Zcaps-Adaptive-lossless-statistical-compressor) |
| **ZChain** | Blockchain-native lossless compression engine | [ZChain-blockchain-native-lossless-compression-engine](https://github.com/Zetako-Compression-Lab/ZChain-blockchain-native-lossless-compression-engine) |
| **ZNano** | Lossless compression for embedded telemetry | [Znano-Structured-Telemetry-Compression](https://github.com/Zetako-Compression-Lab/Znano-Structured-Telemetry-Compression) |

---

## ZCaps

### General-purpose adaptive lossless compression research

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

## ZChain

### Blockchain-native lossless compression engine

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

## ZNano

### Lossless compression for embedded telemetry

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

A blockchain validator, a general-purpose archive, and a Cortex-M telemetry device operate under very different constraints. Zetako Compression Lab therefore develops separate architectures instead of forcing one codec to compromise across every workload.

| Constraint | ZCaps | ZChain | ZNano |
|---|---:|---:|---:|
| General-purpose data | **Primary** | Secondary | No |
| Blockchain structure awareness | No | **Primary** | No |
| Embedded / MCU constraints | No | Limited | **Primary** |
| Adaptive statistical modeling | **Core research** | Used where relevant | Lightweight / constrained |
| Throughput-sensitive infrastructure | Yes | **Primary** | Target-dependent |
| Tiny implementation footprint | No | No | **Primary** |

---

## How we publish research

This organization is an **evidence layer**, not a source-code dump of the proprietary codec cores.

We publish material that allows an external engineer, researcher, partner, or investor to understand what has been built and how the claims are supported:

- reproducible benchmark methodology;
- public datasets or dataset-fetch instructions where appropriate;
- exact round-trip integrity evidence;
- compression ratio and throughput reported together;
- hardware and build context for performance measurements;
- version evolution and measurable engineering deltas;
- integration architecture and readiness boundaries;
- limitations when they materially affect interpretation.

We intentionally keep private:

- proprietary codec core implementations;
- production builds and release engineering;
- internal tuning data;
- sensitive or customer-specific datasets;
- customer-specific integrations.

---

## Research principles

**Lossless first.** A compression improvement only counts when the original payload is reconstructed exactly.

**Ratio and speed belong together.** A smaller output with unacceptable latency is not automatically a better engineering result.

**Native codec and integration overhead are separate measurements.** Build profile, wrappers, I/O, hashing, serialization, and host application behavior can materially affect observed throughput.

**Claims stay scoped.** A result on one corpus, blockchain payload, MCU target, or hardware configuration is not presented as a universal guarantee.

**Continuous iteration matters.** Public version histories are intended to show measurable progress in compression density, throughput, compatibility, and deployment readiness.

---

## About Zetako

**Zetako S.à r.l.** is a Luxembourg deep-tech company developing sovereign software and original data-compression technologies.

**Website:** [zetako.ai](https://zetako.ai/)  
**Contact:** contact@zetako.ai  
**Location:** Luxembourg

---

<sub>Public benchmark figures in the linked repositories represent specific test environments, datasets, codec profiles, and build configurations. They should always be interpreted together with their documented methodology and scope.</sub>
