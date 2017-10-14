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
About the Zero-knowledge of zkSNARKs: it requires during the interaction, the verifier does not know the witness string. <br>

Transaction Example: <br>
f(σ_1, σ_2, address_a, address_b, v_a, p_a, p_b, v_a)
σ_1: root hash of account merkle trees(before transaction)<br>
σ_2: root hash of account merkle trees(after transaction)<br>
address_a: address of account a<br>
address_b: address of account b<br>
v_a: balance of a before transaction<br>
Pa: merkle tree proof to test if balance of a >= v_a before transaction and hash to σ_1<br>
Pb: merkle tree proof to test if balance of b >= v_a after transaction and hash to σ_2<br>

It is relatively easy to verify the computation of f if all inputs are known. Because of that, we
can turn f into a zkSNARK where only σ_1 and σ_2 are publicly known and (address_a, address_b, v_a, Pa , Pb, v) is the
witness string. The zero-knowledge property now causes the verifier to be able to check that the
prover knows some witness that turns the root hash from σ_1 to σ_2 in a way that does not violate
any requirement on correct transactions, but she has no idea who sent how much money to whom.
```
The formal definition (still leaving out some details) of zero-knowledge is that there is a simulator
that, having also produced the setup string, but does not know the secret witness, can interact with
the verifier – but an outside observer is not able to distinguish this interaction from the interaction
with the real prover.
```

##### Succinctness, prover shift,  QSP(multiply of polynomials, target polynomial of degree d),  <br>
common reference string(CRS), <br>
Witness: reduction function(any NP -> NPC, 3-SAT), <br>

anew: again
