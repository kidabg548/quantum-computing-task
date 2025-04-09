# Quantum Entanglement Playground

Welcome to the **Quantum Entanglement Playground**, a hands-on collection of quantum computing experiments built using **Qiskit**. This project explores fundamental quantum phenomena such as **superposition**, **entanglement**, and **quantum measurement** through interactive simulation tasks and statistical verification.

---

## Project Overview

This project simulates and visualizes key quantum mechanics concepts through four experiments:

1.  **Forced Superposition & Entanglement**
2.  **Entanglement Witness with Probabilistic Noise**
3.  **Opposite-Measurement Entanglement**
4.  **Quantum Coin Flip Game with Measurement Entanglement**

Each task is executed over hundreds or thousands of trials to gather meaningful measurement statistics. The project is built using **Python**, **Qiskit**, and **Matplotlib**, and runs in **Google Colab** or Jupyter Notebooks.

---

## Setup Instructions

> ✅ Requires Python 3.7+, Qiskit, and Matplotlib.

### Install Dependencies

```bash
pip install qiskit matplotlib

# Quantum Circuit Experiments

This document outlines a series of quantum circuit experiments designed to explore fundamental quantum concepts like superposition, entanglement, and quantum measurement. The experiments are designed to be run using a quantum computing simulator like Qiskit.

## Running the Code

You can execute the code in the following environments:

*   **Google Colab (Recommended):** Provides a readily accessible environment with all necessary libraries pre-installed.
*   **Jupyter Notebook (Locally):** Requires installing the necessary libraries (e.g., Qiskit, NumPy, Matplotlib).

## Experiments

### 🧪 Task 1: Forced Superposition & Opposite Entanglement

**Description:**

This task explores the creation of an entangled state where qubits are perfectly anti-correlated. Qubit 0 is initialized in superposition (|0⟩ + |1⟩)/√2, and Qubit 1 is forced to the |1⟩ state. A CNOT gate is then applied to entangle the qubits in such a way that their measurement results are always opposite.

**Gates Used:** `H` (Hadamard), `X` (Pauli-X), `CX` (CNOT)

**Expected Output:**

The resulting histogram should only show the states `01` and `10`. The states `00` and `11` should not appear, indicating the qubits are perfectly anti-correlated.

### 🔍 Task 2: Entanglement Witness with Probabilistic Error

**Description:**

This task investigates the robustness of entanglement in the presence of noise. A Bell state (|00⟩ + |11⟩)/√2 is prepared.  A probabilistic error is introduced by applying an X-gate to one of the qubits with a 20% probability, simulating noise that can disrupt entanglement. Only one qubit is measured across 1000 shots.

**Goal:**

The goal is to determine if the entanglement is preserved despite the error. If the output distribution is random (50/50), it suggests the entanglement has been broken. A non-random distribution would indicate that entanglement is still present, albeit potentially weakened.

### 🔄 Task 3: Opposite-Measurement Entanglement

**Description:**

This task aims to create a circuit where two qubits are perfectly anti-correlated. This means that if Qubit 0 is measured as 0, Qubit 1 must be 1, and vice versa.

**Expected Output:**

The histogram should display only `01` and `10`. This represents a maximally entangled anti-correlated state.


### 🎮 Task 4: Quantum Coin Flip Game

**Game Logic:**

*   Alice prepares a qubit in the |+⟩ state (superposition).
*   Bob randomly chooses to measure the qubit in either the X-basis (|+⟩/|−⟩) or the Z-basis (|0⟩/|1⟩).
*   Bob wins if he measures |+⟩ (in the X-basis) or |0⟩ (in the Z-basis).
*   Alice wins otherwise.

**Simulation:**

*   The game is simulated for 500 rounds.
*   Win rates for both Alice and Bob are tracked.

**Twist:**

Bob's measurement choice (X or Z basis) is entangled with another qubit to explore if a quantum-enhanced strategy can alter the win probabilities.

**Goal:**

The analysis focuses on determining whether entangling Bob's basis choice with another qubit impacts the win probabilities for Alice and Bob compared to a classical random choice.
