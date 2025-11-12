# Quantum Error Correction: Implementation and Analysis

Implementation of fundamental quantum error correction codes including noise models, repetition codes, Shor's 9-qubit code, and CSS codes.

##  Overview

This project implements and analyzes three quantum error correction codes:

1. **3-Qubit Repetition Code** - Protects against bit-flip (X) errors
2. **Shor's 9-Qubit Code** - Protects against all single-qubit Pauli errors (X, Y, Z)
3. **CSS [[7,1,3]] Code** - Efficient stabilizer code for single-qubit error correction

All implementations include:
- Custom noise models with configurable X and Z error rates
- Syndrome measurement circuits
- Error correction logic
- Comprehensive testing and visualization
- Comparative performance analysis

##  Features

-  Pauli noise model (X and Z errors)
-  Complete error correction implementations
-  Syndrome measurement and decoding
-  Circuit visualization and statistics
-  Performance comparison and efficiency analysis
-  LaTeX-rendered quantum notation

##  Repository Structure

```
.
├── error_correction_complete.ipynb    # Main implementation notebook
├── README.md                           # This file
├── LICENSE                             # MIT License
└── .gitignore                          # Git ignore file
```

##  Requirements

- Python 3.8+
- Qiskit 
- NumPy
- Matplotlib

Install dependencies:
```bash
pip install qiskit qiskit-aer numpy matplotlib
```

##  Quick Start

1. Clone the repository:
```bash
git clone https://github.com/Vanshaj0429/quantum-error-correction.git
cd quantum-error-correction
```

2. Install dependencies:
```bash
pip install qiskit qiskit-aer numpy matplotlib
```

3. Open the Jupyter notebook:
```bash
jupyter notebook error_correction_complete.ipynb
```

4. Run all cells to see implementations, tests, and visualizations.

##  Key Results

| Code | Physical Qubits | Logical Qubits | Code Rate | Corrects X | Corrects Z |
|------|----------------|----------------|-----------|------------|------------|
| Repetition [[3,1,3]] | 3 | 1 | 0.33 | Yes | No |
| Shor [[9,1,3]] | 9 | 1 | 0.11 | Yes | Yes |
| CSS [[7,1,3]] | 7 | 1 | 0.14 | Yes | Yes |

**Key Finding:** CSS [[7,1,3]] code provides the same error protection as Shor's code with 22% fewer qubits.

##  What's Implemented

### Task 1: Noise Model
Custom function to introduce random Pauli X and Z errors into quantum circuits with configurable probabilities.

### Task 2: Repetition Code
3-qubit repetition code with:
- Encoding circuit
- Syndrome measurement
- Error correction for X errors
- Analysis of why it fails for Z errors

### Task 3: Shor's 9-Qubit Code
First quantum error correction code capable of correcting arbitrary single-qubit errors:
- Two-level encoding (phase-flip + bit-flip protection)
- 8-bit syndrome measurement
- Correction logic for X and Z errors
- Circuit visualization

### Task 4: CSS [[7,1,3]] Code
Efficient stabilizer code based on classical Hamming codes:
- CSS construction with 6 stabilizers
- Detects and corrects X, Y, and Z errors
- More efficient than Shor's code
- Complete syndrome decoding


##  Contributing

This is a screening task submission. For questions or suggestions, please open an issue.

##  License

This project is licensed under the MIT License.

##  Author

**Vanshaj Bindal**
- MSc Physics (Distinction), Cardiff University
- GSoC 2025 @ QuTiP

##  References

- [Error Correction Zoo](https://errorcorrectionzoo.org/)
- [Qiskit Documentation](https://docs.quantum.ibm.com/)
- Nielsen & Chuang, "Quantum Computation and Quantum Information"
- Gottesman, D. "Stabilizer Codes and Quantum Error Correction"

---

**Note:** This implementation uses a [[7,1,3]] CSS code rather than the Hamming [[7,4,3]] code for clarity and tractability while demonstrating the same CSS construction principles.
