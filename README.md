# BT4012 Kaggle Competition

Code for the two submissions I selected for the private leaderboard. The method and results are described in the report.

| Output file | Submission |
|---|---|
| `M26_M18_M24_1to1.csv` | Final submission: Model A (binary graph ensemble) + Model B (3-class ensemble) |
| `M21_M18_M19_1to1.csv` | Second selected submission: Model A + a single 3-class LightGBM |

## Reproducing both submissions
1. Create the environment (Python 3.11):
   ```bash
   conda create -n bt4012 -c conda-forge python=3.11 llvm-openmp
   conda activate bt4012
   pip install -r requirements.txt
   ```
2. Put the four competition files in a folder named `data/` next to the notebook (the dataset is not included in this repository):
   ```
   data/train.csv
   data/test.csv
   data/txs_edgelist.csv
   data/sample_submission.csv
   ```
3. Run the notebook.
   It writes both submission files to the repository root. To only regenerate the two submission files (training on steps 1–35 and predicting the test set), set `RUN_CV = False` in the first code cell.
