# Zero Knowledge Proof
It is possible for a prover to convince verifier that  a statement is true without leaking any information.
It must satisfy 3 conditions:
1. Completeness:  If the statement is true, the honest verifier is convinced truth of this statement by the honeset prover
2. Soundness: If the statement is false, no cheating prover cannot convince the honest verifier the the truth of this statement.[ref](https://en.wikipedia.org/wiki/Soundness)
3. Zero-Knowledge: If the statement is true, no cheating verifier learns any information except the truth of the statement.

# Non-interactive zero-knowledge proof
No interaction is necessary between prover and verifier


# Quadratic Span Programs
Characterization of the NP complexity class. It's exten of span programs.

# Terminalogy
Sound: reasonable
Soundness: Justifiability. Rightfulness
Witness: prover of relevant  event
succinctness: concision
SNARKs: succinct non-interactive arguments of knowledge: 简洁的非交互性知识论证

#
# Points
##### Encoding: quadratic equation of polynomials: t(x)(h(x) = w(x)v(x), find the coefficient of the quadratic equation on both sides.<br>
Succinctness by random sampling, <br>
homomorphic encoding/encryption:  Computing E(t(s)) with known E(s), not knowing s.<br>
Encryption can be taken as encoding.  <br>

##### Zero Knowledge: prover obfuscates the values E(t(s)), E(h(S)), E(w(s)), E(v(s)) by multiplying a random value k such that verifier does not the original encoded values: E(t(s)).<br>
checking t(s)h(s)=v(s)w(s) is equivalent to checking t(s)h(s)k=v(s)w(s)k for random secret k(non-zero). prover sends verifier the obfuscated values t(s)h(s)k, verifier can not infer the value of t(s)h(s).<br>

##### RSA for Zero-Knowledge proof<br>
E(x):= encryption value of x<br>
E(x)E(y) = E(xy)(mod n).<br>
Application: Prover knows x and y, now he want to convince the verifier that he knows X and Y without leaking them.<br>
Prover send verifier E(x), E(y) and E(xy). the verifier check if E(x)E(y) equals to E(xy) modulo N. N is the public key.<br>

##### zkSNARKs
of Knowledge: it is **NOT** possible for the prover to construct a proof/argument without knowing a certain so-called witness(address the prover want to spend, or transfer money from). <br>
About the Zero-knowledge of zkSNARKs: it requires during the interaction, the verifier does not know the witness string.


##### Succinctness, prover shift,  QSP(multiply of polynomials, target polynomial of degree d),  <br>
common reference string(CRS), <br>
Witness: reduction function(any NP -> NPC, 3-SAT), <br>

anew: again
