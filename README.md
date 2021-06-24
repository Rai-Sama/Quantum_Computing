# Quantum_Computing
A repository for storing my files as I learn quantum computing

# Topics covered so far
## Quantum bits(qbits) vs Classical bits(cbits)
* Cbits are special cases of qbits
* for a qbit represented by the vector (a  b)<sup>T</sup>; a & b are complex numbers and ||a|<sup>2</sup> + |b|<sup>2</sup>| = 1 and the probability of the qbit collapsing to 0 is |a|<sup>2</sup> and it collapsing to 1 is |b|<sup>2</sup>

## Operations and Gates
* All operations in quantum computing are reversible and inverse of themselves i.e. given the output of an operation it is possible to know what the input was (reversible) and performing the same operation on the output gives the input again (inverse)
* Matrix operators model the effect of some device (like gates) which manipulates qbit spin/polarization without measuring/collapsing it.
* Bitflip: It flips the qbit. 
  
  Matrix 
  
  ![image](https://user-images.githubusercontent.com/48092867/123316799-e4ed8680-d54a-11eb-8b2a-c2327c43e024.png)

Eg.: ![image](https://user-images.githubusercontent.com/48092867/123316827-ec149480-d54a-11eb-9579-8f29e64a65ac.png) ![image](https://user-images.githubusercontent.com/48092867/123316526-8f18de80-d54a-11eb-87a2-44ccff92f34b.png) ![image](https://user-images.githubusercontent.com/48092867/123320198-1405f700-d54f-11eb-951b-27f45b4f232d.png)

25% chance of collapsing to 0 and 75% chance of collapsing to 1 gets converted to 75% chance of collapsing to 0 and 25% chance of collapsing to 1

* Hadamard gate: Puts a qbit into equal superposition.

  Matrix
  
  ![image](https://user-images.githubusercontent.com/48092867/123317687-ebc8c900-d54b-11eb-91a4-c54ce431dd38.png)
  
  Note => The -1/√2 at the bottom of the matrix is there to ensure that we get different values for 0 and 1 and so, the operation remains reversible
  
  Since all operations are inverse of themselves, the Hadamard gate on a qbit with equal probability of collapsing to 0 or 1 collapses to exactly 0 or 1
* CNOT gate: Also called Controlled not. It works on a pair of bits called control bit and target bit. The not operation (negation) here is performed only on the second bit and only if the first bit is 1

## Quantum entanglement
* If the product state of 2 qbits cannot be factored, they are said to be entangled.
* Two qbits can be entangled by apply Hadamard gate on the first bit and CNOT on both with the first bit acting as the control bit - This all is better explained with eg. in the jupyter notebook (Quantum_computing_1.ipynb)

## Quantum Teleportation
* We can entangle 3 qbits by entangling our target bit to be transfered with one of the qbits of an already entangled pair and then measuring the target qbit makes the others collapse as well (teleportation). The entanglement of a number of pairs of qbits can be done beforehand and so teleportation of a bunch of qbits could be carried out.
* Quantum entanglement is also one of the reasons quantum computation cannot be simulated on classical computers. It takes exponential memory since, if n qbits are entangled, you have to keep their full product state stored i.e a vector of size 2<sup>n</sup> 
