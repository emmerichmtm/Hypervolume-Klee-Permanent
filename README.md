# Hypervolume Indicator and Klee Measure Problem through the Permanent

**Michael T.M. Emmerich** <br>
Faculty of Information Technology, University of Jyväskylä <br>
**25 November 2026**

[Read the report (PDF)](hypervolume_klee_permanent.pdf) · [LaTeX source](hypervolume_klee_permanent.tex) · [Reference checks and novelty assessment](REFERENCE_CHECKS.md)

This technical report explains how an explicit union of anchored boxes encodes a partial permanent. Extracting its leading coefficient recovers the permanent and transfers arithmetic circuit lower bounds to the Hypervolume Indicator and the Klee Measure Problem.

The reduction is unconditional. **The main lower-bound conclusion is conditional on VP ≠ VNP over the real numbers:** the constructed hypervolume family then has no polynomial-size arithmetic circuits. This concerns growing dimension and the specified exact arithmetic model.

The discussion considers the recent Claude (Anthropic) preprint separately. Its particular quantitative lower bound is a stronger premise than VP ≠ VNP alone.

## What the report covers

- Counting complexity versus arithmetic circuit complexity.
- Both directions of reduction, including rational Klee measure to the integer permanent.
- The explicit box construction, interpolation proof, and a numerical example.
- Exact relationships between hypervolume and ordinary ℓ₁ magnitude of dominated sets.
- The limits of the conclusions for fixed dimension, approximation, and symbolic representations.
- Prior work, a qualified novelty assessment, and checks of all ten bibliography entries.

The conflict graph and its partial-permanent polynomial are credited to Briquel and Koiran (2009). The review did not locate the precise geometric corollary as stated here, but does not establish priority.

## Build the PDF

Use a LaTeX installation providing the packages listed in the source. The bibliography is included in the `.tex` file; no BibTeX step is needed.

```sh
pdflatex -interaction=nonstopmode -halt-on-error hypervolume_klee_permanent.tex
pdflatex -interaction=nonstopmode -halt-on-error hypervolume_klee_permanent.tex
pdflatex -interaction=nonstopmode -halt-on-error hypervolume_klee_permanent.tex
```

## Licence

Copyright © 2026 Michael T.M. Emmerich.

The report, its LaTeX source, and accompanying documentation are licensed under [Creative Commons Attribution 4.0 International (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/). The full legal text is in [LICENSE](LICENSE).

Suggested attribution: Michael T.M. Emmerich, *Hypervolume Indicator and Klee Measure Problem through the Permanent*, 25 November 2026, [this repository](https://github.com/emmerichmtm/Hypervolume-Klee-Permanent), CC BY 4.0. Identify any changes when sharing an adaptation. Linked third-party works retain their own licences.
