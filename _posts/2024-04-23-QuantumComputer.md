# Quantum Computer

The CHSH, named after the authors Clauser, Horne, Shimony is an inequality that proving Bell's theorem. But in 2022's Physics Nobel Prize, John Clauser, Alain Aspect and Anton Zeilinger find that there is violation of Bell’s inequalities through experiments. We are runing an experiment on a quantum computer to demonstrating the violation.

## Two CHSH inequalities

We will create an entangled pair. And we measure it on two bases.We set the first base as $A$ and $a$, the second one as $B$ and $b$. Then we have the two CHSH inequalities:
$$
S_1 = A(B-b) + a(B+b).
$$

$$
S_2 = A(B+b) - a(B-b),
$$
And we should have $|\langle S_1 \rangle|\leq 2$,  $|\langle S_2 \rangle|\leq 2$ if the inequalities are right.

## Violation

The experiment including these steps:

1. Create a CHSH circuit which is like the real circuit but in the quantum. Create a set of phase value as circuit parameters. Create two observables which can observe the CHSH equations results.
2. To reduce the work loading, transfer the original circuit to instruction set architecture (ISA) circuits. We transfer observation to ISA as well.
3. We use `EstimatorV2` which can interact with Qiskit Runtime Estimator primitive service, in other words Quantum processors and simulators. So we are running the CHSH circuit now.
4. We can get the observation data and virtualize our results. We can find that `S1` and `S2` sometimes exceed $\pm2$ and are approximately $\pm 2\sqrt{2}$. So we find an violation!
