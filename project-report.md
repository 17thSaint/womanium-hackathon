# Analysis of Digital-Analog Variational Quantum Eigensolver
In this hackathon project we examine the behavior of a variational quantum eigensolver (VQE) in two different ways. The main behavior that we want to analyze is the use of a digital-analog VQE where the analog block uses a Hamiltonian to perform the multi-qubit entanglement.  Current VQEs typically are fully digital meaning that they use digital gates to generate entanglement.  However, this can be quite hardware intensive.  By using analog blocks for entanglement, the native properties of the hardware can be used thus generating entanglement much more efficiently.

In the first section, we directly look at how the fully digital VQE compares to a digital-analog one by simulating a hydrogen molecule.  This molecule can be simulated with just two qubits, and in the second section we examine larger systems of qubits.  With four qubits, the connections between each of the qubits generates six different networks with a range on connectivity.  We will analyze the performance of the digital-analog VQE as a function of the qubit connectivity.

## Simulation of H2 atom
In the file called "da_vqe.ipynb" there are a variety of functions which include a fully digital ansatz and a digital-analog ansatz.  The file labelled "h2code.ipynb" contains code that exectues the simulation of a hydrogen molecule.  Unfortuntely, with the time constraints I was not able to perform thorough analysis of the performance of the two different methods.  However, the code is built such that it can be utilized.

There are some issues in that it appears that the fully digital ansatz chosen does not accurately calculate the eigenvalue of the hydrogen Hamiltonian.  More analysis needs to be done to discover why this is.  The code is built now to iterate the full digital block multiple times, the idea being that with sufficient depth, the correct value would be returned.  However, it is not clear that this procedure works either.  The digital-analog ansatz finds the correct eigenvalue even at depth one, already showing its power.

## Impact of Connectivity

