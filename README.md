# Genetic Algorithm Strategies for Enhanced Pattern Detection

This project explores genetic search for X-A-B-C-D harmonic-pattern candidates in OHLCV price history. The notebook extracts alternating swing points, evolves five-point sequences with a genetic algorithm, scores their price ratios against configurable Gartley, Bat, Butterfly, and Crab bands, and plots the top candidates.

## Repository contents

- `execute.ipynb` — data preparation, swing extraction, genetic search, scoring, and visualizations.
- `dataset.csv` — OHLCV data whose price fields include currency symbols.
- `dataset1.csv` — a second OHLCV dataset with numeric price fields.
- `requirements.txt` — notebook dependencies.

## Run the notebook

Use Python 3.10 or newer:

```bash
python -m pip install -r requirements.txt
jupyter notebook execute.ipynb
```

Set `DATASET_FILE` near the top of the notebook to `dataset.csv` or `dataset1.csv`.

## How scoring works

The notebook identifies local highs and lows, filters out smaller moves, then uses a genetic algorithm to search alternating swing-point sequences. Candidate sequences are scored by their fit to the ratio bands defined in `PATTERN_BANDS`. The random seed and search settings are configurable in the notebook.

## Limitations

- The supplied datasets have no expert labels. The reported score measures ratio fit to the configured bands; it is **not** detection accuracy, predictive performance, or evidence of a profitable trading strategy.
- The ratio ranges are heuristic settings and should be documented, reviewed, and evaluated against labeled examples.
- Swing extraction uses centered windows that look ahead in time. This is suitable for historical exploration but would need redesign for real-time detection.
- Dataset source and redistribution terms were not included in the supplied archive. Confirm and document them before redistributing the CSV files.
- This is a research prototype, not financial advice.

