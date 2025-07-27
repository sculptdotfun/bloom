# The BLOOM Blueprint 🌸

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=flat-square)](http://makeapullrequest.com)
[![Discussions](https://img.shields.io/badge/GitHub-Discussions-blue?style=flat-square)](https://github.com/sculptdotfun/bloom/discussions)

A proposal for a community-driven, decentralized GPU network on Solana, focused on providing high-throughput proving for large, general-purpose ZK circuits.

---

## The Vision: Scaling the "Unsolved Frontier" of ZK

The ZK landscape has a great divide:

1.  **The "Solved" World (Tiny Circuits):** For tasks like State Compression, ZK circuits are small (<15k constraints) and proofs are fast (**5–15ms** on a modern CPU). This is not the focus of BLOOM.

2.  **The "Unsolved" World (Large Circuits):** For innovative applications like private DeFi and on-chain gaming, circuits are massive (100k-1M+ constraints). Proving these on a CPU takes **10-30 seconds**, making them unviable.

**BLOOM is a proposed solution for the "Unsolved" world.** It outlines a decentralized marketplace where developers can access a global network of GPU provers to handle these complex workloads.

## Core Concepts

-   ⚡️ **High-Throughput GPU Proving:** Leverage GPUs to crush the massive, parallel workloads of large circuits. Early ICICLE tests on an RTX 4090 show proof times of **120–250 ms for a 1M-constraint Groth16 circuit**.
-   💰 **Constant On-Chain Cost:** A key benefit of Groth16 on Solana is that the on-chain verification cost is cheap and constant (**~180k CU** via native precompiles), regardless of circuit complexity.
-   🛡️ **Decentralized & Credibly Neutral:** The network is designed as a public good, operated by independent validators who stake SOL. This stake can be slashed for malicious behavior, ensuring the network remains honest and reliable.

## ⚠️ Current Status: A Whiteboard-Stage Proposal

This project is in the **idea and design phase**. The numbers are projections, and the architecture needs refinement. This repository exists to host the blueprint and facilitate community discussion and development. **There is no functional code yet.**

## How to Contribute

This project needs a community of builders and skeptics to move forward.

-   **🗣️ Join the Discussion:** The best place to start is the [**Discussions Tab**](https://github.com/sculptdotfun/bloom/discussions).
-   **📝 Challenge the Blueprint:** Think a number is off or have a better idea for the architecture? **Open an Issue!** Every assumption should be questioned.
-   **💻 Write Some Code:** Foundational work needed includes benchmarking large circuits, designing the network protocol, and creating a reference prover implementation.

## Frequently Asked Questions

**Q: Why start with Groth16 vs. PLONK/STARKs?**
**A:** Path-of-least-resistance. The ecosystem tooling (Circom) and developer knowledge are centered on Groth16. Critically, since Solana v1.18, the chain has native syscalls for Groth16's `alt-bn254` curve, allowing a constant 128-byte proof to be verified for just ~180k CU. PLONK/STARKs are a future goal, pending dedicated precompiles to make their larger proofs economically viable on-chain.

**Q: Do wallets or front-ends have to download the big proving key?**
**A:** No. Only the GPU prover nodes ("BLOOM validators") store the key. The end-user wallet sends a small witness (a few kilobytes) to a node and gets back the tiny 128-byte proof.

**Q: That proving key can be 40–60 GB—won’t that be a problem for validators?**
**A:** It’s a one-time infrastructure download. The proposed solution is to ship the key Zstd-compressed (~15 GB) via a P2P swarm or pre-layered container image. On a standard connection, this is a ~15-minute one-time setup. Future work can adopt universal setups to shrink this further.

**Q: What stops a malicious prover from submitting bad proofs?**
**A:** Validators must stake SOL to participate. An invalid proof submitted on-chain can trigger a process to slash that validator's stake. High-value applications can also request redundant proving (two independent nodes generate the same proof) for extra security.

## License

This project is licensed under the **MIT License**. See the `LICENSE` file for details.
