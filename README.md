# Simulating spins with quantum computers

ARTICLE INFORMATION 

Title:  [Simulating spin dynamics using quantum computers](https://arxiv.org/abs/2207.10567)

SUPPLEMENTARY MATERIALS INFORMATION 

Description: The .ipynb files are (Python 3) Jupyter notebooks, and the .m file is a MATLAB script

Total No. of Files: There are 7 files, including the README.TXT files

File Names:  README.TXT, SingleSpin.ipynb, MultipleSpins.ipynb, threespins.m, SingletTriplet.ipynb, SpinChainQASM.ipynb, DomainWallSparse.m

File Types:  txt, ipynb, m

Instructions: 

(I) This notebook was written using the (free) Anaconda Individual Python Distribution (https://www.anaconda.com/)

(II) The Python notebooks import Qiskit 1.x, which must be installed locally to run the notebooks. Alternatively, one can upload these notebooks to the IBM Quantum Lab

(III) The file [SingleSpin.ipynb](SingleSpin.ipynb) allows the user to reproduce the data shown in Figs. 3-5 of the main text. Users can also change parameters to explore cases not considered explicitly in the paper. In summary, the user can measure spin expectation values for a single spin in an arbitrary magnetic field and explore how the number of Trotter steps affects the final results in a simple situation. Commands are given for executing jobs on the simulator as well as on actual IBM Quantum hardware (IBM Quantum account required for the latter).

(IV) The file [MultipleSpins.ipynb](MultipleSpins.ipynb) gives users the ability to simulate interacting systems of two and three spins. Instructions are included for using actual IBM devices, as the notebook is set up to return simulator results only. Users can adjust system parameters (initial configuration, couplings, Trotter steps, etc.) to explore cases not considered explicitly as well as reproducing data depicted in Figs. 5-7 of the main text.

(V) The file [threespins.m](threespins.m) is a MATLAB script for performing exact diagonalization in a three-spin system. This routine was used to create the theoretical predictions in Fig. 7. Instead of obtaining the eigenvalues and eigenvectors of the Hamiltonian matrix, the function ```expm()``` is used to directly exponentiate the Hamiltonian in order to compute the time evolution operator.

(VI) The file [EntangledState.ipynb](EntangledState.ipynb) creates the family of states 

$$|\psi\rangle = \frac{1}{\sqrt{2}}\left(|+-\rangle+e^{i \phi}|-+\rangle\right)$$

for a range $0 < \phi < \pi$. Three circuits are constructed to measure the three spin-spin correlations $\langle \hat{S}^{x}\otimes\hat{S}^{x}\rangle$, $\langle \hat{S}^{y}\otimes\hat{S}^{y}\rangle$, $\langle \hat{S}^{z}\otimes\hat{S}^{z}\rangle$ needed to measure the total squared spin operator. Cases $\phi = 0, \pi$ correspond to eigenstates of total spin with eigenvalues $s(s+1)\hbar^2$ with $s = 1, 0$, respectively.

(VII) The file [SpinChainSim.ipynb](SpinChainSim.ipynb) uses the QASM simulator to calculate $\langle\hat{S}^{z}\rangle$ as a function of time on all sites in a system with $N=20$ beginning from a domain wall state. Aside from looping over the $N$ spins and creating a domain wall, the backbone of this script is essentially the same as the script for computing dynamics in a three-spin system (Trotter steps).

(VIII) The file [DomainWallSparse.m](DomainWallSparse.m) is a MATLAB script for computing time evolution in a spin chain. The function ```expv()``` must be downloaded and saved to the same directory for this script to run ([https://www.maths.uq.edu.au/expokit/](https://www.maths.uq.edu.au/expokit/)).


The authors acknowledge the use of IBM Quantum services for this work. The views expressed are those of the authors, and do not reflect the official policy or position of IBM or the IBM Quantum team. Additionally, the authors acknowledge the access to advanced services provided by the IBM Quantum Researchers Program.
