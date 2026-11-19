# Genetic Algorithm Strategies for Enhanced Pattern Detection

A small research prototype that explores using a genetic algorithm (DEAP) with OHLCV price data and a Plotly candlestick chart to demonstrate harmonic-pattern detection.

## Repository contents

- `execute.ipynb` — the original project notebook.
- `dataset.csv` — OHLCV data with currency symbols in the price columns.
- `dataset1.csv` — another OHLCV dataset with numeric price columns.
- `requirements.txt` — Python packages used by the notebook.

## Setup

Use Python 3.10 or newer, then install the dependencies:

```bash
python -m pip install -r requirements.txt
```

Open `execute.ipynb` in Jupyter Notebook or JupyterLab to review the experiment.

## Current limitations

The notebook is an early prototype and its results should be treated as illustrative:

1. It tries to load `dataset4.csv`, which is not included in the supplied project archive. The included CSVs have the expected OHLCV columns; update the notebook's input filename to `dataset.csv` or `dataset1.csv` before running.
2. The genetic algorithm evolves four random values, but the fitness checks are placeholders and do not calculate harmonic ratios from the price series.
3. The plotted detection points are fixed example indices, not points found by the algorithm.

These limitations mean the notebook does not yet provide validated pattern detections. The project needs a real pattern-fitness function and evaluation against labeled data before its results can be interpreted as detection performance.

## Data notes

The supplied CSVs contain date, close, volume, open, high, and low columns. The archive does not include data-source or license information; add those details before redistributing the datasets if you have them.
