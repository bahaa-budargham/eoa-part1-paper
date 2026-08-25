[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.21842891.svg)](https://doi.org/10.5281/zenodo.21986309)

# EOA-43: A Rank-Collapsed Deterministic Word Representation with a Convergent Recursive Basis

[![License: CC BY-NC 4.0](https://img.shields.io/badge/License-CC%20BY--NC%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by-nc/4.0/)

> A deterministic, training-free word representation with a strange reproducible property: the ratio of consecutive terms in its basis sequences stabilizes after the 43rd iteration. For the English primary phonetic mapping, this limiting constant ratio (LCR) is approximately **3.037**. Under a different mapping, the LCR shifts to **2.689**. Under a third mapping, it is **3.306**. The number is **not a universal constant**. Across 5 encodings in 4 languages it shifts from **2.710 (Hebrew)** to **4.128 (Greek)** — a 1.5× spread. The theoretical explanation is **open**

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

EOA materials are released on a tiered basis. See the table below for what is open, restricted, or available by request.
| Tier | Access | Agreement | Materials | Purpose |
| :--- | :--- | :--- | :--- | :--- |
| **0** | Public | None | Published papers, basis groupings, LCR values (3.037, 2.689, 3.173, 2.486, 3.306), benchmark code, Colab notebooks | Priority and scientific disclosure; fully verifiable empirical claims |
| **1** | Restricted | DUA (Data Use Agreement) | 43‑term basis sequences (`english_alphabet_LCR3.173_v1.0.json`) | Independent verification of empirical claims; research use only, no redistribution, citation required |
| **2** | Restricted | ELA (Evaluation License Agreement) + click-through ToS | Interactive playground (`eoa43-playground.html`) | Interactive testing; hosted, rate-limited, no scraping, no ML training on outputs |
| **3** | Restricted | Research API License | Batch API (text file → CSV of sequences) | Bulk evaluation; named-user, rate-limited, no data extraction |
| **4** | Restricted | MTA (Material Transfer Agreement) + Mutual NDA | Oracle binary (black-box callable) | Run on collaborator hardware; no source, no formula, anti-reverse-engineering clause, audit rights |
| **5** | Restricted | TLA (Technology License Agreement) + optional JDA | Full operator beta and closed-form formula | Commercial or funded collaboration; royalties, equity, or lump sum; co-inventorship on resulting patents |
| **6** | Future | TBD | Hypothesis bank H1–H7 | Will be released in a future paper or update |

---

### Notes

- This graduated disclosure structure mirrors established practice at NIH (DUA), DeepMind AlphaFold (ELA/API), and pre-1997 RSA Laboratories (TLA).
- The operator is withheld under a staged disclosure policy while its theoretical scope is being mapped.
- Empirical claims (rank collapse, cross-encoding LCR variation, memory footprint) are fully verifiable from the released sequences and black-box oracle.
- A full specification will be released once the encoding-to-LCR mapping is theoretically characterized.
- For academic collaborators, access to Tiers 1–4 is available under standard academic agreements that permit research use and publication of derived results with appropriate citation.
- No agreement is required for Tier 0 materials.

For access to Tiers 1 through 5, contact: **bdarghamneurolabs@gmail.com**

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
