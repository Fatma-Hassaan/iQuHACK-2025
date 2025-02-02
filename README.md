# iQuHACK-2025

Shor's Algorithm accelerates the process of finding the prime factorization of semiprime numbers by utilizing quantum superposition. For example, factoring a 2048-bit public key, which would traditionally take millions of years even with the most powerful supercomputers [1], can be accomplished in sub-polynomial time using Shor's Algorithm. The algorithm's first notable application was the factorization of 15 into 3 and 5 [1]. While Shor's Algorithm offers a significant speedup over classical methods, there are still cases where the factorization process can take hours [2] or even days [3] to complete.In this project, we aim to implement Shor's Algorithm for the factorization of larger numbers than 15. We explored various techniques to optimize the implementation, such as Quantum Annealing and Pollard's Method, but unfortunately, we were unable to achieve successful implementations with these approaches.

Key Functions:

  y_times_21_mod_143(qc, q[i]): 
  A placeholder for the modular exponentiation part of Shor's algorithm. It should be defined to handle the modular operations necessary for the algorithm.
  The implementation is based on eq(4) and Fig. 9 in the paper [1] for 8 bit factorization.
  According to Fig. 4 in [1], q0 to q6 correspond to x which will act as a control qubit
  Qubits q7 to q14 are the target qubits.
Implementation of a function g(y) = y x a mod N; where a=21, N=143 is also provided in fig. 9 in [1].
 We use the same implementation
 Next is accordinhg to Fig 4 the lower circuits are of the form y x a^i mod N which if further simplifies in equation 4 by just repeating g(y) multiple times base on the corresponding control x bit we use. This part is implemented when we call the function y_times_21_mod_143(qc, q[i])


iqft_cct(qc, q, 7): 
A placeholder for the Quantum Fourier Transform (QFT) implementation.
Rest part is the same, we use IQFT to the x qubits and get the results
Next is we find the period and the factors based on the period calculated.
      
                                





   

  [1] J. Tomčala, “On the Various Ways of Quantum Implementation of the Modular Exponentiation Function for Shor’s Factorization,” Int J Theor Phys, vol. 63, no. 1, p. 14, Jan. 2024,                                     doi: 10.1007/s10773-023-05532-4.
  [2] Gidney, Craig, and Martin Ekerå. "How to factor 2048 bit RSA integers in 8 hours using 20 million noisy qubits." Quantum 5 (2021): 433.
  [3] Gouzien, Élie, and Nicolas Sangouard. "Factoring 2048-bit rsa integers in 177 days with 13 436 qubits and a multimode memory." Physical review letters 127, no. 14 (2021): 140503.
