# Shor's Algorithm using Quantum Computing

## Overview

This project implements **Shor's Algorithm** using **IBM Qiskit** to demonstrate quantum integer factorization. Shor's Algorithm is one of the most significant quantum algorithms, offering an exponential speedup over the best known classical algorithms for integer factorization and highlighting the potential impact of quantum computing on modern cryptography.

In this project, the algorithm is used to factor **N = 15**, illustrating the fundamental concepts behind quantum period finding, the Quantum Fourier Transform (QFT), and quantum circuit execution.

---

## Objective

The primary objectives of this project are to:

* Understand the working principles of Shor's Algorithm.
* Build the quantum circuit using IBM Qiskit.
* Implement the Quantum Fourier Transform (QFT) and its inverse.
* Perform modular exponentiation using quantum oracles.
* Execute the circuit on the IBM Qiskit Aer Simulator.
* Extract the period of a modular function and compute the factors of the integer.

---

## Technologies Used

* Python
* IBM Qiskit
* Qiskit Aer
* NumPy
* Matplotlib
* Jupyter Notebook

---

## Theory

Shor's Algorithm reduces the problem of integer factorization to **period finding**.

For an integer (N):

1. Choose an integer **a** such that `gcd(a, N) = 1`.

2. Define the function:

   **f(x) = aˣ mod N**

3. Use a quantum circuit to determine the period **r** of the function.

4. Compute the factors using:

   * gcd(a^(r/2) − 1, N)
   * gcd(a^(r/2) + 1, N)

For this implementation:

* Integer to factor: **15**
* Chosen value: **a = 7**

---

## Project Workflow

### 1. Environment Setup

* Installed the required Qiskit libraries.
* Imported the necessary quantum computing and visualization modules.

### 2. Modular Exponentiation

* Implemented the modular exponentiation oracle.
* Applied controlled unitary operations required by Shor's Algorithm.

### 3. Quantum Fourier Transform

* Constructed the Inverse Quantum Fourier Transform (Inverse QFT).
* Applied Hadamard, controlled phase rotation, and SWAP gates.

### 4. Shor's Circuit Construction

* Built the complete quantum circuit consisting of:

  * Counting register
  * Target register
  * Modular exponentiation
  * Inverse QFT
  * Measurement operations

### 5. Quantum Simulation

* Executed the circuit using the **IBM Qiskit Aer Simulator**.
* Collected measurement results.
* Visualized the output distribution.

### 6. Period Extraction

* Converted measurement outcomes into phase values.
* Estimated the period using continued fractions.
* Determined the factors of the integer using classical post-processing.

---

## Repository Structure

```text
.
├── Shors Algorithm using Quantum Computing.ipynb
├── README.md
├── requirements.txt
└── images/
    ├── quantum_circuit.png
    ├── measurement_histogram.png
    └── period_estimation.png
```

---

## Installation

Clone the repository:

```bash
git clone https://github.com/your-username/shors-algorithm-qiskit.git
```

Install the required dependencies:

```bash
pip install -r requirements.txt
```

Launch Jupyter Notebook:

```bash
jupyter notebook
```

---

## Results

The notebook demonstrates:

* Construction of Shor's Algorithm using IBM Qiskit.
* Quantum circuit implementation for modular exponentiation.
* Inverse Quantum Fourier Transform.
* Execution on the IBM Qiskit Aer Simulator.
* Measurement histogram visualization.
* Period estimation using quantum measurements.
* Successful factorization of **15** through quantum period finding.

---

## Key Learning Outcomes

* Fundamentals of Quantum Computing
* Quantum Gates and Quantum Circuits
* Quantum Fourier Transform (QFT)
* Modular Exponentiation
* Quantum Phase Estimation
* Shor's Algorithm
* IBM Qiskit Framework
* Quantum Circuit Simulation
* Hybrid Quantum-Classical Computation

---

## Future Improvements

* Execute the algorithm on IBM Quantum hardware.
* Extend the implementation to factor larger composite numbers.
* Optimize quantum circuits for reduced gate depth.
* Explore noise-aware and error-mitigated execution.
* Compare simulator results with real quantum hardware.

---

## Author

**Soham Gosavi**

B.Tech Indian Institute of Technology Guwahati

---

## Acknowledgements

* IBM Quantum
* IBM Qiskit
* Qiskit Aer
* Qiskit Documentation
* 4i Labs Quantum Computing Domain
* Indian Institute of Technology Guwahati
