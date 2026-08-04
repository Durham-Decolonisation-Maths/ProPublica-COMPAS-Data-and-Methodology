                  Low  High
                 +---------+
Didn't Reoffend  |____|____|
Reoffended       |    |    |
                 +---------+


This repository contains a Jupyter notebook and data for the ProPublica story "Machine Bias."

Story:
https://www.propublica.org/article/machine-bias-risk-assessments-in-criminal-sentencing/

Methodology:
https://www.propublica.org/article/how-we-analyzed-the-compas-recidivism-algorithm/

Notebook (you'll probably want to follow along in the methodology):
https://github.com/propublica/compas-analysis/blob/master/Compas%20Analysis.ipynb

Main Dataset:
compas.db: a sqlite3 database containing criminal history, jail and prison time, demographics and COMPAS risk scores for defendants from Broward County.

Other files as needed for the analysis.

## Workshop extensions

Two additional notebooks extend the original ProPublica analysis for this course. Both are plain Python/pandas unlike `Compas Analysis.ipynb`, they don't need R or `rpy2`, and both reuse the exact same filtering criteria as the original notebook so their numbers are directly comparable.

| Notebook | Extends the audit to... |
| --- | --- |
| `intersectional_subgroups.ipynb` | Race × sex intersections, with Wilson confidence intervals, some cells are too small to support a metric at all; others reveal disparities the race-only view hides. |
| `feedback_loops.ipynb` | What happens *after* a single snapshot: how `priors_count` accumulates from historical enforcement, and a simulation of how allocation decisions based on observed (not true) rates can run away over time. |

```bash
pip install -r requirements.txt
jupyter notebook .
```
