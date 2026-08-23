[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.21842891.svg)](https://doi.org/10.5281/zenodo.21986309)

# EOA-43: A Rank-Collapsed Deterministic Word Representation with a Convergent Recursive Basis

[![License: CC BY-NC 4.0](https://img.shields.io/badge/License-CC%20BY--NC%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by-nc/4.0/)

> A deterministic, training-free word representation with a strange reproducible property: the ratio of consecutive terms in its 43-term basis sequences stabilizes to ≈ 3.173 for the English primary encoding — for **every** letter name and **every** word. The number is **not a universal constant**. Across 5 encodings in 4 languages it shifts from **2.710 (Hebrew)** to **4.128 (Greek)** — a 1.5× spread. The theoretical explanation is **open**.

![LCR variance across 5 encodings, 4 languages](https://github.com/bahaa-budargham/eoa-data/blob/main/figures/lcr_across_encodings.png)

*The English primary encoding bar sits at ≈ 3.037; this value is encoding-dependent, not a universal constant.*

---

**Papers:** [EOA-43 (Part I)](#citation) · [EOA Program, Part 0](https://github.com/bahaa-budargham/eoa-part0-paper) · [EOA Program Main Page](https://github.com/bahaa-budargham/engineering-of-alphabets)

**Benchmark notebook:** [Colab](https://colab.research.google.com/drive/1WvLdr4qqDU_KY8H26DaYnR3N1U6CQIdV?usp=sharing)

---

## What is in this repository

| File | Description |
| :--- | :--- |
| `eoa43-paper.pdf` | Full paper: EOA-43 — A Rank-Collapsed Deterministic Word Representation |
| `notebooks/allcolab.ipynb` | Main Colab notebook containing all benchmark experiments for EOA‑43 (uniform noise, Tables 3–4, PCA, rank diagnostics, and reproducibility) |
| `notebooks/ocrs.ipynb` | Colab notebook for the OCR noise experiment (Table 5) |
| `figures/` | Figures from the paper |
| `data/` | Pre-computed sequences and word vectors |

The internal deterministic operator that generates the basis sequences is **not** in this repository. The generated outputs are available under the terms described in EOA-43, Section 2. See [Disclosure status](#disclosure-status) below.

---

## Open Theoretical Questions

The companion paper (EOA-Recurrence, Part II) formalizes three open questions derived from the released sequences: stability within a fixed encoding, cross-encoding mapping, and inverse design. A bank of seven candidate hypotheses (H1–H7) is provided in the companion paper.

The 43-term sequences are available to qualified researchers under the terms described in EOA-43, Section 2. They are fully measurable by researchers with access. The operator that generated them is the only gated piece. Submissions of theoretical explanations are tracked in [`LEADERBOARD.md`](./LEADERBOARD.md).

---

## Disclosure Status

**Public (this repository and the linked Colab notebook):**

- The letter-name input strings for the five encodings.
- The benchmark code, baselines, and evaluation pipeline.
- The precomputed noisy-word vectors for the OCR experiment.
- The empirical LCR measurements for 5 encodings across 4 languages.
- The cross-encoding consistency experiment.
- The hypothesis bank H1–H7.

**Not public:**

- The 43‑term basis sequences (`english_alphabet.json`) – access restricted.
- The interactive playground – access restricted.
- The internal deterministic operator that produces the basis sequences.
- The closed-form mapping from encoding properties to LCR (open question).

A preliminary least-squares test of the natural linear hypothesis (v<sub>n+1</sub> = M · v<sub>n</sub>) yielded large reconstruction errors on the released sequences. The operator is made available to qualified research collaborators under research-protective terms. Contact the author for the agreement.

---

## How to Cite

If you use any materials from this repository in your research, please cite the relevant EOA paper:

**EOA-43 (Part I):**
Budargham, B. (2026). EOA-43: A Rank-Collapsed Deterministic Word Representation with a Convergent Recursive Basis. GitHub. https://github.com/bahaa-budargham/eoa-part1-paper

**EOA Program, Part 0:**
Budargham, B. (2026). The EOA Program, Part 0: The Engineering of Alphabets as an Open Frontier. GitHub. https://github.com/bahaa-budargham/eoa-part0-paper

**BibTeX:**
```bibtex
@article{Budargham2026EOA43,
  author = {Bahaa Budargham},
  title = {EOA-43: A Rank-Collapsed Deterministic Word Representation with a Convergent Recursive Basis},
  year = {2026},
  note = {GitHub: https://github.com/bahaa-budargham/eoa-part1-paper}
}
