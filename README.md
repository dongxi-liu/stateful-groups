
# Stateful Groups 

We introduce a new algebraic structure, stateful group, and uses it as the foundation to construct the Schnorr signature scheme, the Diffie–Hellman key agreement protocol,  and threshold schemes (a FROST-based threshold signature scheme, a MuSig2-style multi-signature scheme, and a distributed Diffie–Hellman key agreement protocol). 

In a stateful group,  each element is attached with a binary state tag and the group operation depends on not only element values but also their tags.  A stateful group is cyclic and hence still vulnerable to Shor's algorithm. 
However, by employing features of stateful groups, a structure requirement is enforced onto the secret exponents in public keys and ciphertexts. This requirement makes Quantum Fourier Transform in Shor's algorithm not applicable to produce meaningful linear equations over the secret components.  

The current SageMath implementation  instantiates the stateful groups over several underlying groups: the ones to be introduced here, the additive group  of integers, two elliptic-curve groups  P-256  and Curve25519. The resulting schemes will be quantum-safe and  provide competitive public-key, signature, and ciphertext sizes (less than 400B for some instances).

