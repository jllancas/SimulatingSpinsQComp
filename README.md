# Simulating spins with quantum computers

These files are to accompany [arXiv:2207.10567](https://arxiv.org/abs/2207.10567) as supplemental material.

- The Python notebooks import Qiskit, which must be installed locally to run the notebooks. Alternatively, one can upload these notebooks to the IBM Quantum Lab

- The file [SingleSpin.ipynb](SingleSpin.ipynb) allows the user to reproduce the data shown in Figs. 3-5 of the main text. Users can also change parameters to explore cases not considered explicitly in the paper. In summary, the user can measure spin expectation values for a single spin in an arbitrary magnetic field and explore how the number of Trotter steps affects the final results in a simple situation. Commands are given for executing jobs on the QASM simulator as well as on actual IBM Quantum hardware (IBM Quantum account required for the latter).

- The file [MultipleSpins.ipynb](MultipleSpins.ipynb) gives users the ability to simulate interacting systems of two and three spins. Instructions are included for using actual IBM devices, as the notebook is set up to return QASM simulator results only. Users can adjust system parameters (initial configuration, couplings, Trotter steps, etc.) to explore cases not considered explicitly as well as reproducing data depicted in Figs. 6-7 of the main text.

- The file [threespins.m](threespins.m) is a MATLAB script for performing exact diagonalization in a three-spin system. This routine was used to create the theoretical predictions in Fig. 7. Instead of obtaining the eigenvalues and eigenvectors of the Hamiltonian matrix, the function expm() is used to directly exponentiate the Hamiltonian in order to compute the time evolution operator.

-------------------------------------------------

The authors acknowledge the use of IBM Quantum services for this work. The views expressed are those of the authors, and do not reflect the official policy or position of IBM or the IBM Quantum team. Additionally, the authors acknowledge the access to advanced services provided by the IBM Quantum Researchers Program.
