# ⚒️ First Foundry Repo: Advanced Testing & Fuzzing

Continuing my **Master in Blockchain Development** at **Blockchain Accelerator Academy**, I have migrated my workflow to **Foundry**, the blazing-fast, portable, and modular toolkit for Ethereum application development written in Rust.

As a **Java Software Engineer**, relying on JavaScript frameworks (like Hardhat) for testing Solidity felt disconnected. Foundry allows me to write tests **in Solidity**, providing a developer experience much closer to JUnit/Mockito.

## 💡 Project Overview

This project implements a Calculator Smart Contract, but the focus is not on the arithmetic. The goal is to explore Foundry's powerful testing capabilities, including **Cheatcodes**, **Traces**, and **Fuzz Testing**.

### 🔍 Key Technical Features:

* **Foundry Framework:**
    * Moved away from Remix/Hardhat to a local, professional development environment.
    * Writing tests in Solidity (`.t.sol` files) ensures type safety and better integration with the contract logic.

* **Advanced Testing Patterns:**
    * **Pranking (`vm.prank`):** Simulating different user identities (like Admin vs. User) to test Access Control (`onlyAdmin` modifiers) without needing multiple private keys.
    * **Custom Error Expectations:** Using `vm.expectRevert(Selector)` to precisely validate *why* a transaction failed, not just *that* it failed.

* **Fuzz Testing (Property-Based Testing):**
    * Instead of testing `10 / 2 = 5`, I implemented **Fuzzing**. Foundry automatically generates thousands of random inputs to try to break the logic.
    * **Input Bounding:** Used `bound()` to handle edge cases (like preventing division by zero during random input generation) while still testing the full range of `uint256`.

## 🛠️ Stack & Tools

* **Framework:** Foundry (Forge, Cast, Anvil).
* **Language:** Solidity `0.8.30` (Modern syntax).
* **Testing:** `forge-std` (Standard Library).
* **Concepts:** Fuzzing, Cheatcodes, Gas Optimization (`immutable`).

---

*This project represents a level-up in my tooling, adopting the industry standard for secure smart contract development.*
