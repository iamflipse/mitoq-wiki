# MitoQ & Age-Related Physiological Dysfunction — Wiki

A curated wiki distilling the 2026 *GeroScience* (Springer) review:
**Therapeutic potential of MitoQ, a mitochondria-targeted antioxidant, in age-related physiological dysfunction**
(Kim et al., GeroScience 2026, DOI 10.1007/s11357-026-02515-1).

**Public copy:** https://iamflipse.github.io/mitoq-wiki/ (read-only; static build served from the `gh-pages` branch)

## Contents

- **6 concept pages**: mitochondrial aging hallmarks & ROS generation (ETC, dynamics, Ca²⁺, NLRP3 inflammaging); MitoQ chemistry & mitochondrial targeting (TPP⁺, CoQ10 comparison, redox cycle); organ-system effects — [cardiovascular](src/concepts/cardiovascular.md), [neuronal](src/concepts/neuronal.md), [skeletal muscle](src/concepts/skeletal-muscle.md), [lower urinary tract (LUTS)](src/concepts/lower-urinary-tract.md).
- **Source of truth:** full paper text at `src/sources/mitoq-fulltext.md`.

## Layout

- `src/` — markdown source pages
- `book/` — mdbook-generated static site (committed for GitHub Pages)
- `tools/mdbook` — mdbook v0.4.21 binary (aarch64 Linux, built from source)

## Rebuild + republish

```sh
./tools/mdbook build -d book
git add -A && git commit -m "update" && git push origin main
# republish: recreate orphan gh-pages branch with book files at root + tools/mdbook, force push
```
