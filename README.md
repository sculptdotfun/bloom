# BLOOM 🌸

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=flat-square)](http://makeapullrequest.com)
[![Discussions](https://img.shields.io/badge/GitHub-Discussions-blue?style=flat-square)](https://github.com/sculptdotfun/bloom/discussions)

An open blueprint for a community-driven, decentralized GPU network to provide fast, low-cost Zero-Knowledge (ZK) proofs on Solana.

---

## The Vision

BLOOM is a shared vision for critical infrastructure that the Solana ecosystem needs to unlock the full potential of Zero-Knowledge technology. The goal is to build a decentralized, high-performance proving network by activating the most underutilized resource in the ecosystem: globally distributed validator hardware.

The core problem is that current ZK proving is **slow** (10-30 seconds on CPUs), **centralized**, and **expensive**. This makes it impossible to build truly interactive and scalable applications that require privacy.

BLOOM aims to solve this by creating a decentralized marketplace where dApps can purchase proofs from a network of Solana validators who use GPUs to generate them at lightning speed.

## Core Concepts

-   💨 **GPU Acceleration:** Leverage GPUs to reduce proof generation times by over 100x, from 10-30 seconds down to **~100 milliseconds**.
-   🌍 **Geographic Distribution:** Route proof requests to the nearest validator to provide a sub-150ms experience for users anywhere in the world.
-   🤝 **Decentralized Marketplace:** Create a sustainable economic flywheel where validators can earn a new stream of revenue (e.g., 2-10 SOL/day) for providing proving services, making the network robust and censorship-resistant.
-   🧩 **Protocol Agnostic:** Design a modular system that can eventually support multiple ZK proof systems (Groth16, PLONK/Halo2, STARKs) as the ecosystem evolves.

## ⚠️ Current Status: An Idea in Need of Builders

This project is currently in the **idea and design phase**.

This repository contains the initial blueprint, technical concepts, and a place for community discussion. **There is no functional code yet.** The purpose of this repository is to serve as a public home for this idea, with the hope that the community will embrace it, refine it, and build it together.

## How to Contribute

This is a community-driven project, and we need your help to make it a reality. I (`sculptdotfun`) am seeding this idea but want the community to take ownership. Whether you're a developer, a validator, a researcher, or just an enthusiast, there are many ways to contribute:

-   **🗣️ Join the Discussion:** The best place to start is the [**Discussions Tab**](https://github.com/sculptdotfun/bloom/discussions). Share your thoughts, ask questions, and challenge the assumptions in this blueprint.
-   **📝 Refine the Architecture:** Open an [**Issue**](https://github.com/sculptdotfun/bloom/issues) to propose changes to the core design, economic model, or technical roadmap.
-   **💻 Write Some Code:** If you're ready to start building, fork the repo and open a Pull Request. We can start with foundational components like prover performance benchmarks or network protocol designs.
-   **📢 Spread the Word:** Share this repository with others in the Solana ecosystem who might be interested in contributing.

## High-Level Roadmap

This is a potential path forward. Let's build it together.

-   [ ] **Phase 1: Foundational Research & Prover**
    -   [ ] Benchmark performance of ZK proof systems (starting with Groth16) on various consumer GPUs.
    -   [ ] Implement a reference GPU prover using a library like [ICICLE](https://github.com/ingonyama-zk/icicle).
    -   [ ] Finalize V1 of the network architecture and economic model.

-   [ ] **Phase 2: Network Protocol & Validator Onboarding**
    -   [ ] Design and build the peer-to-peer network protocol for routing proof requests.
    -   [ ] Develop a simple "one-click" setup script for validators to join the network.
    -   [ ] Create a public dashboard for network analytics and validator profitability.

-   [ ] **Phase 3: SDK & Ecosystem Integration**
    -   [ ] Build a simple SDK for dApp developers to easily request proofs from the BLOOM network.
    -   [ ] Partner with early-adopter projects on Solana to integrate and test the network.
    -   [ ] Begin research on supporting additional proof systems (PLONK, Halo2, etc.).

## License

This project is licensed under the **MIT License**. See the `LICENSE` file for details.
