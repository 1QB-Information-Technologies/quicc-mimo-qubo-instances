## License 
1QBit QuICC Phase II MIMO Dataset
VERSION v2026-05-13.1

This dataset is licensed under the Creative Commons Attribution 4.0 International License (CC BY 4.0). 
https://creativecommons.org/licenses/by/4.0/

This dataset was created under the support of the Defense Advanced Research Projects Agency (DARPA), Microsystems Technology Office (MTO), Quantum-Inspired Classical Computing Program (QuICC) and conducted for Phase II of this program during the period 2025-2027.

Work was performed by members of the QuICC team at:

-	1QB Information Technologies (1QBit)

You are free to:
-	Share — copy and redistribute the material in any medium or format
-	Adapt — remix, transform, and build upon the material for any purpose, even commercially under the condition of attribution.  You must give appropriate credit, provide a link to the license, and indicate if changes were made 

## Citation 
If you use any aspect of this this dataset, please cite it as: 

MIMO Problem Instances in QUBO Formulation, Elisabetta Valiante, Khashayar
Hashemi, Moslem Noori, Ignacio Rozada,
2025.  Licensed under CC BY 4.0.

## Description

This repository contains instances of MIMO problems formulated as QUBO. 

The folder name provides information on the problem parameters, in particular: 

- Nt: number of transmitters 
- Nr: number of receivers 
- M: number of $M$-QAM constellation points 
- EbN0: signal-to-noise defined as energy per bit $E_{\rm b}$ over power of noise $N_0$ in
  dB

The number of bits transmitted by each symbol is $r= \log_2 M$. We consider
that $M$ is an even power of two and the QAM constellation has a standard square
shape. We set the minimum distance between two symbols in the constellation to
be 
$$d_{\min} = \sqrt{\frac{6}{M-1}}$$ 
to normalize the average energy of the transmitted QAM signal to unity. This normalization ensures
that all modulations transmit with the same power per symbol, allowing a fair
comparison of performance, and that the energy per bit $E_{\rm b}$ is always $1/r$.  

The `qubo_*.txt` files are structured as following: 

- First line: the number of variables in the QUBO 
- Second line: the transmitted bits used to generate the problem. This is not the optimal solution of the QUBO, but it is used to derive the optimal solution. The QUBO optimal solutions are stored in the files `gs.txt`. 
- Following lines: the QUBO terms as they would appear in a triangular matrix,
  in a dictionary format: if the key has only 1 term, it is a diagonal term. 

The `y_H_*.npz` files can be restored using the `numpy.load` method. They
include the `y` vector of the received symbols and the channel matrix `H`.

Similarly, the `mimo_*.npz` files can be restored using the `numpy.load` method. They
include the `y` vector of the received symbols, the channel matrix `H`, the
`opt_solution_gray` vector, which is the vector of transmitted bits, and the
`mmse_soltuion_gray` vector, which is the vector of the bits detected by the
MMSE method.
