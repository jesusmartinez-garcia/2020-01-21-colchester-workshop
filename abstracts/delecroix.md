---
layout: default
permalink: /abstracts/delecroix
---

## Vincent Delecroix

### Galois group of polynomials

Computing Galois group of an irreducible polynomial P of degree d can be done by assembling two subroutines

a) (number theory) manipulating (arbitrary precision) roots of the polynomial `r1, ..., rd` and checking that given a polynomial `R(x1, ..., xd)` with rational coefficients whether `R(r1, r2, ..., rd)` is a rational number.

b) (permutation groups) exploring the lattice of transitive subgroups of the symmetric group `S_d`.

The task a) can be efficiently done for example in PARI/GP. Thanks to the transitive group database, one can compute the lattice of transitive groups up to degree 31 and hence hardcoding task b).  This is an approach that has been implemented in collaboration with B. Allombert (Bordeaux) and M. Pfeiffer (St Andrews). However, this procedure would ideally be dynamical. The algorithmic problem I would like to address is the following:

Given a transitive subgroup of `S_d`, give the list of its maximal transitive subgroups.

That would (potentially) allow us to make our algorithm work in degrees >= 32.
