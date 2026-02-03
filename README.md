# ⏱️ Crypto_Algorithms_Benchmark

[![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://www.python.org/)
[![Cryptography](https://img.shields.io/badge/Library-Cryptography-red.svg)](https://cryptography.io/en/latest/)

## 📄 Project Overview
This project benchmarks the performance of three fundamental cryptographic algorithms to analyze how file size impacts processing speed. Using Python, I measured the execution time for:

1.  **AES (Symmetric Encryption):** Fast, single-key encryption used for data transfer.
2.  **RSA (Asymmetric Encryption):** Slower, dual-key encryption used for key exchange.
3.  **SHA-256 (Hashing):** One-way data integrity verification.

The goal is to provide a clear, empirical comparison of computational overhead between symmetric and asymmetric systems.

---

## 📊 Key Findings
The tests measured processing time across file sizes ranging from **8 bytes to 2 MB**.

| Algorithm | Type | Performance Verdict |
| :--- | :--- | :--- |
| **AES-128** | Symmetric | **Fastest.** Scales linearly and handles large files efficiently. |
| **SHA-256** | Hashing | **High Efficiency.** Very fast, with predictable performance growth. |
| **RSA-2048** | Asymmetric | **Slowest.** Significant bottleneck, especially during decryption. |

**Conclusion:** RSA is computationally expensive and unsuited for large files, validating the real-world practice of using RSA only to encrypt small AES keys, while AES handles the actual data payload.

---

## 📈 Visualization
*Note: Run the notebook to generate these plots locally.*

The project includes Matplotlib scripts to visualize:
* **Time vs. File Size** (Linear and Logarithmic scales).
* **Encryption vs. Decryption** speed disparities (specifically for RSA).

---

## 🛠️ Installation & Usage

### 1. Clone the Repository
```bash
git clone [https://github.com/YourUsername/Crypto-Algorithms-Benchmark.git](https://github.com/YourUsername/Crypto-Algorithms-Benchmark.git)
cd Crypto-Algorithms-Benchmark
