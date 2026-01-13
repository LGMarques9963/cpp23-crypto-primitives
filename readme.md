# 🔐 C++23 Cryptographic Primitives

[![C++23](https://img.shields.io/badge/Standard-C%2B%2B23-00599C?logo=c%2B%2B&logoColor=white)](https://en.cppreference.com/w/cpp/23)
[![Build](https://img.shields.io/badge/Build-CMake-064F8C?logo=cmake&logoColor=white)](https://cmake.org/)
[![License](https://img.shields.io/badge/License-MIT-green)](LICENSE)

## 📌 Project Overview

This repository contains a collection of **cryptographic algorithms and attacks implemented in modern C++**, focused on understanding **how cryptography behaves in real software systems**.

It is designed as a **cryptography engineering lab**, not as a production crypto library.

---

## Purpose

Most security failures do not come from broken math — they come from:
- incorrect implementations  
- unsafe memory handling  
- misuse of cryptographic primitives  
- weak key management  

This project exists to study **cryptography as software**, including:
- how ciphers are implemented  
- how they fail  
- and how they are attacked  


> *Designed to demonstrate how modern C++ features (RAII, Smart Pointers, String Views) can optimize legacy cryptographic implementations.*

---

## 🚀 Technical Highlights

Unlike standard textbook implementations, this project leverages modern language features to ensure robustness:

- **⚡ C++23 Standards:** Utilizes modern containers and algorithms to avoid raw pointer manipulation.
- **🛡️ Cryptanalysis Engine:** Includes modules for **brute-force**, **frequency analysis**, and **pattern recognition** to simulate attack vectors.
- **🧪 Unit Testing:** Comprehensive test coverage using `ctest` to validate mathematical correctness.
- **🏗️ Modular Architecture:** Clean separation of concerns with header-only utilities and compiled logic.

---

## 🛠️ Implemented Algorithms

| Category | Algorithm | Technical Focus |
| :--- | :--- | :--- |
| **Substitution** | **Caesar / Rot13** | Modular arithmetic & character set shifting. |
| **Substitution** | **Vigenère** | Polyalphabetic substitution using keyword cycles. |
| **Substitution** | **Affine** | Linear algebra concepts ($ax + b \pmod m$). |
| **Transposition** | **Columnar Transposition** | Matrix-based data manipulation and memory layout optimization. |
| **Symmetric** | **XOR Cipher** | Bitwise operations and key stream generation. |
| **Asymmetric** | **Public-Key (RSA Prototype)** | Basics of prime number generation and modular exponentiation. |
| **Stream** | **One-Time Pad** | Information-theoretic security implementation. |

---

## 📂 Project Structure

```text
cpp23-crypto-primitives/
├── src/                # Core implementation logic
│   ├── symmetric/      # Substitution and Transposition ciphers
│   ├── asymmetric/     # Public Key infrastructure
│   └── utils/          # Math and String helpers
├── tests/              # Unit tests (GTest/CTest)
├── include/            # Header files
└── CMakeLists.txt      # Build configuration

```

---

## ⚙️ Build & Benchmarking

### Prerequisites

* C++ Compiler supporting C++20/23 (GCC 11+, Clang 14+, MSVC)
* CMake 3.10+

### Compilation

```bash
# Clone the repository
git clone [https://github.com/LGMarques9963/cpp23-crypto-primitives.git](https://github.com/LGMarques9963/cpp23-crypto-primitives.git)
cd cpp23-crypto-primitives

# Build with optimizations
mkdir build && cd build
cmake -DCMAKE_BUILD_TYPE=Release ..
make

# Run the test suite
ctest --verbose

```

---

## 🛡️ Security Research Context

This library includes **offensive security modules** used for educational cryptanalysis:

* **Frequency Analysis:** Statistical attack on monoalphabetic substitution.
* **Brute-Force Multithreading:** Leveraging concurrency to exhaust key spaces.
* **Known-Plaintext Attacks:** Reverse engineering keys from partial data.

*Note: While implemented with efficiency in mind, this is a research library. It has not been audited for side-channel resistance (timing attacks, power analysis) and should not be used to secure production data.*

## Why this matters for security engineering

In real systems, cryptography is embedded inside:
- authentication tokens  
- APIs  
- secure storage  
- TLS stacks  
- distributed systems  

Understanding how crypto **fails in code** is essential for:
- AppSec  
- secure backend design  
- vulnerability research  
- protocol analysis  

This project trains the ability to reason about:
> **cryptography at the level where exploits actually happen: in memory and code.**

---

## Engineering focus

Beyond cryptography, this project emphasizes:

- clean C++ APIs  
- memory safety  
- test-driven development  
- predictable behavior  
- reproducibility  

These are the same properties required in:
- secure services  
- key management systems  
- identity platforms  
- encryption pipelines  

---

## 📄 References & Credits

This project builds upon concepts from:

* *Cracking Codes with Python* (Al Sweigart) - Adapted for System Level Programming.
* *The C++ Standard Library* (Josuttis) - For best practices in STL usage.

---

## 🤝 Contributing

Contributions focused on **optimization**, **Post-Quantum algorithms**, or **memory safety improvements** are welcome.

---

## 💌 Author

**Lorran Marques** *Systems & Security Engineer | M.Sc. Candidate* [LinkedIn](https://www.linkedin.com/in/lgmarques/) • [GitHub](https://github.com/LGMarques9963)
