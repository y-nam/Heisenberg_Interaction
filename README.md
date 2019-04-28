# Heisenberg_Interaction

Low cost quantum circuits for classically intractable instances of the Hamiltonian dynamics simulation problem

This repository contains:

* Quantum circuits that simulate spin systems evolving
  according to the Hamiltonian that consists of Heisenberg
  interactions between spins and random magnetic field in
  z direction.
  
Explicit descriptions of the algorithms, implementation details, and
original references can be found in the following paper.

* Yunseong Nam and Dmitri Maslov
  Low cost quantum circuits for classically intractable instances of the Hamiltonian dynamics simulation problem
  May 2018. Available from
  https://arxiv.org/abs/1805.04645.

## License

* The code is released under the Apache License. See the LICENSE and
  NOTICE files for more information.


## Circuits

The circuits are given in the ASCII format. The circuit optimizations 
were carried out using the techniques detailed in the following paper.

* Yunseong Nam, Neil J. Ross, Yuan Su, Andrew M. Childs, and Dmitri
  Maslov. Automated optimization of large quantum circuits with
  continuous parameters. October 2017. Available from
  https://arxiv.org/abs/1710.07345.
  npj:Quantum Information 4, 23 (2018).
  
Filenames for the quantum simulation circuits are

        LCR_Postoptim_(graph_name)_(pFT/FT)_(Order#)
        
The first () is the connectivity graph (k_d_n): k = degree, d = diameter, n = number of vertices.
The second () denotes whether the circuit is targeted towards pre-fault tolerant or fault tolerant implementations.
The third () denotes the order of the product formula algorithm used to develop the simulation circuit.

## Contributors

* Yunseong Nam
* Dmitri Maslov

## Contact

Questions and comments can be addressed to: nam@ionq.co
