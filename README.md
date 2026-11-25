# Hypervolume Indicator and Klee Measure Problem through the Permanent

**Michael T.M. Emmerich** <br>
Faculty of Information Technology, University of Jyväskylä <br>
25 November 2026

[Read the paper (PDF)](hypervolume_klee_permanent.pdf) · [LaTeX source](hypervolume_klee_permanent.tex)

An explicit family of anchored boxes realizes the partial permanent as a residual volume. Coefficient extraction recovers the permanent, giving an unconditional arithmetic reduction to the Hypervolume Indicator and the Klee Measure Problem.

**Conditional on VP ≠ VNP over the real numbers**, the constructed hypervolume family has no polynomial-size arithmetic circuits. The paper gives self-contained proofs, the reverse reduction for rational inputs in the bit model, and connections with ordinary ℓ₁ magnitude. The row–column conflict graph and partial-permanent polynomial are due to Briquel and Koiran (2009).

## Build

The paper uses A4 paper and 12-point type. Run from the repository directory with a standard LaTeX installation; the bibliography is included in the source.

```sh
pdflatex -interaction=nonstopmode -halt-on-error hypervolume_klee_permanent.tex
pdflatex -interaction=nonstopmode -halt-on-error hypervolume_klee_permanent.tex
```

## Licence

Copyright © 2026 Michael T.M. Emmerich. The paper, source, and original figure are licensed under [Creative Commons Attribution 4.0 International (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/). See [LICENSE](LICENSE) for the full text.

Suggested attribution: Michael T.M. Emmerich, *Hypervolume Indicator and Klee Measure Problem through the Permanent*, 25 November 2026, [this repository](https://github.com/emmerichmtm/Hypervolume-Klee-Permanent), CC BY 4.0. Linked third-party works retain their own licences.
