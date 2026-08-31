# Trust Without Verification — reproducible analysis

Companion code for the paper *Trust Without Verification: One in Seven AI-Judged
High-Stakes Tasks Proceeds with Minimal Human Oversight* (Nageshwaran & Ezekiel, 2026),
an independent secondary analysis of Anthropic's public *enabling-independent-research*
dataset (CC-BY-4.0).

## Contents
- `trust_without_verification_analysis.ipynb` — end-to-end analysis notebook. Downloads
  the four dataset CSVs from Hugging Face, defines the statistical helpers, and reproduces
  every number, table, and figure in the paper with narrated explanation. Runs top to
  bottom with no errors; all four figures render inline.
- `trust_without_verification_analysis.html` — a pre-rendered, read-only copy (open in any
  browser; no Jupyter needed).

## Run
```bash
pip install jupyter pandas numpy matplotlib
jupyter nbconvert --to notebook --execute --inplace trust_without_verification_analysis.ipynb
# or open in Jupyter / VS Code and "Run All"
```
Python 3.10+. The first cell fetches the data (needs network once).

## Data & citation
Data (c) Anthropic, released CC-BY-4.0:
Handa et al. (2026), *Enabling independent research on how people use Claude*.
https://huggingface.co/datasets/Anthropic/enabling-independent-research

## Note
All dataset labels ("high-stakes", "minimal human input", "fully autonomous",
"clear success") are model-generated judgements from Anthropic's Insights pipeline and were
not human-validated; every finding is therefore *AI-judged*. See the paper's Limitations.

## License
Code in this repository: MIT. Dataset: CC-BY-4.0 (Anthropic).
