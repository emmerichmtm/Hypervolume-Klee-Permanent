# Reference checks and novelty assessment

Report: *Hypervolume Indicator and Klee Measure Problem through the Permanent* <br>
Author: Michael T.M. Emmerich <br>
Affiliation: Faculty of Information Technology, University of Jyväskylä <br>
Checked: **25 November 2026**

The checks cover all ten bibliography entries: bibliographic identity, accessible primary sources, and the passages supporting the report's use of each reference. They do not constitute an independent audit of every proof in the cited works. In particular, the Claude paper is treated as a preprint; the report's main lower-bound result remains conditional on VP ≠ VNP over the reals.

## Bibliography audit

| Key | Verified source and passage | Outcome |
| --- | --- | --- |
| `ValiantCounting` | L. G. Valiant, *The complexity of computing the permanent*, Theoretical Computer Science **8**(2), 189–201 (1979), [DOI](https://doi.org/10.1016/0304-3975(79)90044-6). [University-hosted original scan](https://sites.math.washington.edu/~billey/colombia/references/valiant.permanent.1979pdf.pdf), Theorem 1, printed p. 189; Theorem 3, p. 190. | Metadata agrees with the DOI record. The zero–one permanent counts accepting computations up to polynomial reductions; the modulo-two observation is explicit. |
| `ValiantAlgebra` | L. G. Valiant, *Completeness classes in algebra*, STOC 1979, 249–261, [DOI](https://doi.org/10.1145/800135.804419). [University-hosted original scan](https://sites.math.washington.edu/~billey/colombia/references/valiant.completeness.1979.pdf), Theorem 2, printed p. 254. | Metadata and permanent completeness outside characteristic two verified. This is a separate paper from the counting result. |
| `BringmannFriedrich` | K. Bringmann and T. Friedrich, *Approximating the volume of unions and intersections of high-dimensional geometric objects*, Computational Geometry **43**(6–7), 601–610 (2010), [DOI](https://doi.org/10.1016/j.comgeo.2010.03.004). [Author manuscript](https://people.mpi-inf.mpg.de/~kbringma/paper/J2010CGTA.pdf), §2.1, Theorem 1, manuscript pp. 3–4; approximation bound in the introduction, p. 3. | Verified origin anchor, coordinates 1 and 2, and counting reduction. The box approximation bound is O(nd/ε²) at constant success probability. |
| `BriquelKoiran2009` | I. Briquel and P. Koiran, *A dichotomy theorem for polynomial evaluation*, MFCS 2009, 187–198, [DOI](https://doi.org/10.1007/978-3-642-03816-7_17). [Author manuscript](https://perso.ens-lyon.fr/pascal.koiran/Publis/mfcs09.dichotomy_theorem.pdf), §3, Theorems 3 and 5, manuscript pp. 6–7. | Added after the literature check. Theorem 5 uses exactly the matrix-position conflict graph and identifies its independent-set polynomial with the partial permanent. |
| `Chan2013` | T. M. Chan, *Klee's measure problem made easy*, FOCS 2013, 410–419, [DOI](https://doi.org/10.1109/FOCS.2013.51). [Author manuscript](https://tmc.web.engr.illinois.edu/easyklee8_13.pdf), abstract and §1, p. 1; [author's institutional publication record](https://experts.illinois.edu/en/publications/klees-measure-problem-made-easy/). | Metadata, fixed-dimension assumption, O(n^(d/2)) Klee-measure bound and O(n^(d/3) polylog n) orthant bound verified. |
| `BringmannEtAl2025` | K. Bringmann, K. G. Larsen, A. Nusser, E. Rotenberg and Y. Wang, *Approximating Klee's Measure Problem and a Lower Bound for Union Volume Estimation*, LIPIcs **332**, 25:1–25:16 (SoCG 2025). [Publisher record](https://drops.dagstuhl.de/entities/document/10.4230/LIPIcs.SoCG.2025.25), [full paper](https://drops.dagstuhl.de/storage/00lipics/lipics-vol332-socg2025/LIPIcs.SoCG.2025.25/LIPIcs.SoCG.2025.25.pdf), Theorem 2 at p. 25:7 and §§4–5. | Authors, title, pages and DOI verified. Theorem 2 gives O((n + ε⁻²) log^(2d+1) n), constant d, success probability at least 0.9. The lower bound uses object oracles, not explicit box coordinates. |
| `Emmerich2026` | M. T.M. Emmerich, *The Magnitude of Dominated Sets: A Pareto Compliant Indicator Grounded in Metric Geometry*, [arXiv:2604.18147v1](https://arxiv.org/abs/2604.18147v1), 20 April 2026; [Theorem 3.3 in the versioned full text](https://arxiv.org/html/2604.18147v1). | Author, title, date, identifier and projection formula verified. The report also gives its own direct kernel proof rather than relying on an unproved additivity assertion. |
| `Claude2026` | Claude (Anthropic), *VP ≠ VNP over every field*, [Hexagon version 1](https://hexagonmath.org/2611.00954v1), 23 November 2026; [paper and formalization](https://github.com/anthropics/formal-math/tree/11b6c7e3c927df2658f513b6b68ea7f8929c62c5/vp-vnp). | Version/date and the claimed permanent bound verified in the primary posting. The author attribution is also given by the repository. Preprint status retained. This is a Hexagon identifier, not an arXiv identifier. |
| `ClaudeRepo` | Anthropic, [repository README at the inspected commit](https://raw.githubusercontent.com/anthropics/formal-math/11b6c7e3c927df2658f513b6b68ea7f8929c62c5/vp-vnp/README.md). | The project description, paper attribution and stated scope were checked. The README is a status source, not an independent proof verification. |
| `ClaudeStatement` | Anthropic, [Statement.lean at the inspected commit](https://raw.githubusercontent.com/anthropics/formal-math/11b6c7e3c927df2658f513b6b68ea7f8929c62c5/vp-vnp/Statement.lean), definitions `Computes`, `Beyond`, `MainTheorem`, `Approximates` and `MainTheoremApprox`. | Checked the gate-count convention, characteristic restriction, quantitative exponent, and formal Laurent-series meaning of approximation. No Lean build or full formal-proof audit was performed. |

For DOI landing pages that denied browser access, bibliographic data was checked against the publisher-deposited Crossref record, and the relevant theorem was read in an accessible primary scan or author manuscript. Mutable repository links were replaced with links pinned to commit `11b6c7e3c927df2658f513b6b68ea7f8929c62c5`.

## Both directions of reduction

For binary-encoded rational box endpoints, multiply each axis by a product of its endpoint denominators and translate to nonnegative integer endpoints. The scaled volume is the number of covered unit lattice cells. A nondeterministic polynomial-time computation guesses a cell index once and checks whether any input box covers it. Overlaps are counted once. All indices and scaling factors have polynomial bit length.

This supplies the additional argument needed to apply Valiant's counting completeness theorem: **rational Klee measure reduces to the integer permanent under polynomial-time oracle reductions**, followed by exact rescaling. The report proves this consequence; it does not attribute the geometric unit-cell formulation itself to Valiant.

Conversely, the established counting hardness of anchored box volume already yields a counting reduction from the zero–one permanent to Klee measure. That does not by itself transfer arithmetic circuit lower bounds for the generic permanent polynomial. The report's weighted realization and interpolation provide that algebraic step.

## What the literature check establishes

**Explicitly documented:** Briquel and Koiran's Theorem 5 contains the same conflict graph and partial-permanent polynomial. Bringmann and Friedrich's Theorem 1 contains the anchored Boolean-cell encoding. Neither should be presented as a newly discovered object or hardness classification here.

**Additional derivation in this report:** replacing vertex weights by `t a_e` and realizing a selected coordinate interval with length `t a_e`, and its unselected complement with length one, turns the known partial-permanent sum into a residual volume. Its top coefficient is the permanent, and interpolation transfers circuit bounds. This connects the verified antecedents; it is not a quotation of a geometric theorem from either source.

**Novelty remains unconfirmed:** the precise positive-coordinate construction and conditional geometric corollary were not located as explicit statements in the sources examined. Searches combined “Klee measure” / “Klee's measure” / “hypervolume” with “permanent”, “partial permanent”, “VNP”, “arithmetic circuit”, and the names Briquel and Koiran. These searches and the primary sources above do not constitute an exhaustive historical survey. Failure to locate an earlier statement does not establish priority.

The report therefore uses the description **an explicit geometric realization of a known algebraic construction, with a conditional complexity consequence**, without a claim to the first proof.

## Conditional statements

- The exact identities, geometric construction, and circuit reduction are unconditional.
- Assuming **VP ≠ VNP over the reals** excludes polynomially bounded circuit size for the constructed families.
- The numerical rate **2^Ω((log r)^(4/3))** needs the stronger quantitative permanent premise stated in the Claude preprint. VP ≠ VNP alone does not specify that rate.
- The relevant lower bounds concern growing dimension and exact arithmetic computation. They do not establish a fixed-dimensional optimum or a lower bound for every bit-model algorithm.

Copyright © 2026 Michael T.M. Emmerich. Licensed under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/).
