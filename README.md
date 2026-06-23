# Quantum Calculator

This repo consists of a single Jupyter notebook, which implements a **Quantum Calculator** using [qiskit](https://www.ibm.com/quantum/qiskit). This notebook was submitted for mini project #1 at the [Summer 2026 Quantum Computing Boot Camp](https://www.erdosinstitute.org/programs/summer-2026/quantum-computing-boot-camp) run by the [Erdős Institute](https://www.erdosinstitute.org/).

## Implementation

The Jupyter notebook implements a Qiskit function called $\mathrm{QCalc}$. It inputs a positive integer $d$ and outputs a quantum circuit that implements the operation

$$
\text{QCalc} \lvert x \rangle_d \lvert y \rangle_d \lvert z \rangle_1 \lvert 0 \rangle_d = \begin{cases}
\lvert x \rangle_d \lvert y \rangle_d \lvert z \rangle_1 \lvert x + y \mod 2^d \rangle_d, & z = 0 \\
\lvert x \rangle_d \lvert y \rangle_d \lvert z \rangle_1 \lvert x \cdot y \mod 2^d \rangle_d, & z = 1 \\
\end{cases}
$$

That is, if the control gate $z$ is activated then it returns the product of the inputs $x$ and $y$, else it returns their sum. Note that the circuit $\mathrm{QCalc}$ operates on $3d + 1$ qubits.

## Current Status

Currently, the notebook implements the addition and multiplication circuits separately. More work is required to combine them into the single $\mathrm{QCalc}$ circuit with behavior controlled by the $z$ bit. See the notebook for further details.
