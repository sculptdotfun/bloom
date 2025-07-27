# BLOOM 🌸

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=flat-square)](http://makeapullrequest.com)
[![Discussions](https://img.shields.io/badge/GitHub-Discussions-blue?style=flat-square)](https://github.com/sculptdotfun/bloom/discussions)

An open blueprint for a community-driven, decentralized GPU network to provide high-throughput proving for large, general-purpose Zero-Knowledge (ZK) circuits on Solana.

---

## The Vision: The "Unsolved Frontier" of ZK

The ZK landscape on Solana has split into two worlds:

1.  **The "Solved" World (Tiny Circuits):** For tasks like State Compression, the ZK circuits are small (<15k constraints) and proofs are incredibly fast (~5-15ms) even on standard CPUs. The problem of proving simple, standardized operations is largely solved.

2.  **The "Unsolved" World (Large Circuits):** For the next wave of innovation—private DeFi, on-chain games, complex identity systems—the ZK circuits are massive (100k to 1M+ constraints). For these applications, proof generation on CPUs is still a major bottleneck, taking **10-30 seconds** and making interactive experiences impossible.

**BLOOM is a blueprint for the "Unsolved" world.** It aims to provide the critical infrastructure for developers building novel applications with large, complex, and custom ZK circuits.

The goal is to build a decentralized marketplace connecting these developers with a global network of Solana validators who use consumer-grade GPUs to generate these complex proofs at scale.

## Core Concepts

-   ⚡️ **High-Throughput GPU Proving:** While a CPU is fine for a tiny circuit, GPUs are essential for the massive, parallel workloads of large circuits. BLOOM is designed to reduce proof times for complex circuits from **30 seconds down to an interactive ~100-400ms**.
-   🌍 **Decentralized & Credibly Neutral:** By leveraging a network of independent validators, BLOOM creates a censorship-resistant and resilient public utility. There is no single point of failure or control.
-   💰 **Sustainable Validator Economics:** Create a new, reliable revenue stream for Solana validators who contribute their GPU hardware to the network, fostering a self-sustaining ecosystem.
-   🛡️ **Security & Incentive Alignment:** The design assumes validators will stake SOL to participate. This stake can be slashed for malicious behavior (e.g., submitting invalid proofs) or downtime, keeping the network honest and reliable.

## ⚠️ Current Status: An Idea in Need of Builders

This project is currently in the **idea and design phase**.

This repository contains the refined blueprint, technical concepts, and a place for community discussion. **There is no functional code yet.** The purpose of this repository is to serve as a public home for this idea, with the hope that the community will embrace it, refine it, and build it together.

## How to Contribute

This is a community-driven project, and we need your help to make it a reality. Whether you're a developer, a validator, a cryptographer, or an enthusiast, there are many ways to contribute:

-   **🗣️ Join the Discussion:** The best place to start is the [**Discussions Tab**](https://github.com/sculptdotfun/bloom/discussions). Challenge the assumptions, ask questions about the economic model, or propose new features.
-   **📝 Refine the Architecture:** Open an [**Issue**](https://github.com/sculptdotfun/bloom/issues) to propose changes to the core design, such as the slashing mechanism, trusted setup process, or proof aggregation strategy.
-   **💻 Write Some Code:** If you're ready to start building, fork the repo and open a Pull Request. Foundational components needed include:
    -   Performance benchmarks for large Groth16 circuits on various GPUs.
    -   A reference implementation of a GPU prover using a library like [ICICLE](https://github.com/ingonyama-zk/icicle).
    -   Initial designs for the network protocol.

## High-Level Roadmap

This is a potential path forward, open to community input.

-   [ ] **Phase 1: Foundational Research & Prover**
    -   [ ] Benchmark performance of **large** Groth16 circuits (100k-1M+ constraints) on consumer GPUs.
    -   [ ] Implement a reference GPU prover optimized for throughput.
    -   [ ] Design a secure and scalable process for per-circuit trusted setups (CRS).

-   [ ] **Phase 2: Network Protocol & Security**
    -   [ ] Design the P2P network for routing proof requests.
    -   [ ] Formalize the staking and slashing mechanism to ensure validator honesty.
    -   [ ] Develop a simple onboarding script for validators.

-   [ ] **Phase 3: SDK & Ecosystem Integration**
    -   [ ] Build a developer SDK for submitting proof requests for custom circuits.
    -   [ ] Explore proof aggregation techniques (e.g., KZG-based) to reduce on-chain verification costs for users.
    -   [ ] Partner with early-adopter projects building applications with complex ZK needs.

## License

This project is licensed under the **MIT License**. See the `LICENSE` file for details.
