# What Makes a Chess Puzzle Hard? Predicting Lichess Puzzle Difficulty

This project predicts the difficulty rating of chess puzzles from the Lichess open puzzle database, using six features computed from each puzzle's position and solution. It compares linear regression with a random forest.

## Files

| File | Description |
|---|---|
| `puzzle_difficulty.ipynb` | The full project: data loading, preprocessing, feature extraction, exploratory analysis, models, results, and supporting experiments |
| `lichess_puzzles_sample.csv` | A sample of 51,200 puzzles from the Lichess puzzle database (see Data below) |
| `requirements.txt` | Python libraries needed to run the notebook |

## How to run

1. Install the required libraries:
   ```
   pip install -r requirements.txt
   ```
2. Open `puzzle_difficulty.ipynb` in Jupyter (JupyterLab or Jupyter Notebook), with `lichess_puzzles_sample.csv` in the same folder.
3. Run all cells. The notebook runs in about a minute.

## Data

The puzzles come from the [Lichess open puzzle database](https://database.lichess.org/#puzzles), released under CC0 (public domain). The sample consists of the first 51,200 puzzles by puzzle ID from a September 2022 copy of the database, obtained from [mcognetta/lichess-combined-puzzle-game-db](https://github.com/mcognetta/lichess-combined-puzzle-game-db).

## Results

On the held-out test set, the random forest predicts puzzle ratings with a mean absolute error of 305.5 rating points (R² = 0.41), compared with 318.2 (R² = 0.37) for linear regression and 412.7 for a baseline that always predicts the average rating.
