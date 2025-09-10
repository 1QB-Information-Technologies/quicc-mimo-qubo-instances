## License 
1QBit QuICC Phase II MIMO Dataset
VERSION v2025-08-11.1

This dataset is licensed under the Creative Commons Attribution 4.0 International License (CC BY 4.0). 
https://creativecommons.org/licenses/by/4.0/

This dataset was created under the support of the Defense Advanced Research Projects Agency (DARPA), Microsystems Technology Office (MTO), Quantum-Inspired Classical Computing Program (QuICC) and conducted for Phase II of this program during the period 2025-2027.

Work was performed by members of the QuICC team at:

-	1QB Information Technology (1QBit)

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
- M: number of M-QAM constellation points 
- EbN0: signal-to-noise in dB  

The files are structured as following: 

- First line: the number of variables in the QUBO 
- Second line: the transmitted bits used to generate the problem. This is not the optimal solution of the QUBO, but it is used to derive the optimal solution. The QUBO optimal solutions are stored in the file gs.txt. 
- Following lines: the QUBO terms as they would appear in a triangular matrix, in a dictionary format: if the key has only 1 term, it is a diagonal term. 
