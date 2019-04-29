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
  
## Notations

All gates are of the following form

        :G [target(s)] [control(s)] {classical control(s)} Angle

* ":" := Prefix for a gate
* "G" := Gate type
* "[]" := Qubit register
* "{}" := Classical register
* "Angle" := Optional angle (default pi)

Available gate types are

* i := Initialization to 0
* m := Measurement
* h := Hadamard gate
* rz := RZ gate
* s := S gate
* si := Inverse S gate
* t := T gate
* ti := Inverse T gate

The exceptional case in the notation is a CNOT gate.
In this special case, the notation is

        :cnot [control] [target] {classical control(s)}

Note that the control qubit comes first.


To express the circuit, we use the following notation.

* "seq $NAME" denotes a quantum gate sequence with $NAME as the name.
* "exp $NAME" expands the $NAME quantum gate sequence.
* "repeat #" repeats the codeblock # times.

A codeblock, in this notation, is defined according to the off-side rule.

## Circuits

The circuits are given in the ASCII format. The circuit optimizations 
were carried out using the techniques detailed in the following paper.

* Yunseong Nam, Neil J. Ross, Yuan Su, Andrew M. Childs, and Dmitri
  Maslov. Automated optimization of large quantum circuits with
  continuous parameters. October 2017. Available from
  https://arxiv.org/abs/1710.07345.
  npj:Quantum Information 4, 23 (2018).
  
Filenames for the LCR-optimized quantum simulation circuits are

        LCR_Postoptim_(graph_name)_(pFT/FT)_(Order#)

Filenames for the non-LCR optimized quantum simulation circuits are

        Postoptim_(graph_name)_(pFT/FT)_(Order#)
        
The first () is the connectivity graph (k_d_n): k = degree, d = diameter, n = number of vertices.
The second () denotes whether the circuit is targeted towards pre-fault tolerant or fault tolerant implementations.
The third () denotes the order of the product formula algorithm used to develop the simulation circuit.

## Contributors

* Yunseong Nam
* Dmitri Maslov

## Contact

Questions and comments can be addressed to: nam@ionq.co
