# Arithmetic Lower Bounds for the Time Complexity of the Hypervolume Indicator and Klee Measure Problem through the Permanent

**Technical Report**

**Michael T.M. Emmerich** <br>
Faculty of Information Technology, University of Jyväskylä <br>
26 November 2026

[Read the Technical Report (PDF)](hypervolume_klee_permanent.pdf) · [LaTeX source](hypervolume_klee_permanent.tex)

For a shorter exposition, see the companion WordPress article: [What Would VP ≠ VNP Mean for Hypervolume and Klee Measure?](https://emmerix.net/2026/11/26/what-would-vp-neq-vnp-mean-for-hypervolume-and-klee-measure/).

An explicit family of anchored boxes realizes the partial permanent as a residual volume. Coefficient extraction recovers the permanent, giving an unconditional arithmetic reduction from the permanent to the Hypervolume Indicator and the Klee Measure Problem.

**Conditional on VP ≠ VNP over the real numbers**, the constructed hypervolume family has no polynomial-size arithmetic circuits. The report gives self-contained proofs, the reverse reduction for rational inputs in the bit model, and connections with ordinary ℓ₁ magnitude. The row–column conflict graph and partial-permanent polynomial are due to Briquel and Koiran (2009).

A worked three-dimensional example illustrates how two conflict boxes leave five matching cells uncovered. The figures show both the distinction between Klee measure and hypervolume in two dimensions and the matching construction in three dimensions. The lower bound concerns growing dimension; for multiobjective optimization, where the number of objectives is normally fixed, its value is primarily theoretical.

## Build

The report is typeset on A4 paper in 12-point type. Run from the repository directory with a standard LaTeX installation; the bibliography is included in the source.

```sh
pdflatex -interaction=nonstopmode -halt-on-error hypervolume_klee_permanent.tex
pdflatex -interaction=nonstopmode -halt-on-error hypervolume_klee_permanent.tex
```

## Licence

Copyright © 2026 Michael T.M. Emmerich. The report, source, and original figures are licensed under [Creative Commons Attribution 4.0 International (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/). See [LICENSE](LICENSE) for the full text.

Suggested attribution: Michael T.M. Emmerich, *Arithmetic Lower Bounds for the Time Complexity of the Hypervolume Indicator and Klee Measure Problem through the Permanent*, Technical Report, 26 November 2026, [this repository](https://github.com/emmerichmtm/Hypervolume-Klee-Permanent), CC BY 4.0. Linked third-party works retain their own licences.
