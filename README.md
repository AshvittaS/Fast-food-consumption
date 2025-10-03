## Men's T20 Cup – Feature Engineering

Feature engineering and exploration for Men's T20 World Cup match data using Python and Jupyter.

### Repo structure
```text
Men-s-cup-T20/
  ├─ Men_T20.ipynb                  # Main analysis / feature engineering notebook
  ├─ all_t20_world_cup_matches_results.csv  # Dataset used by the notebook
  ├─ requirements.txt               # Python dependencies
  └─ README.md
```

### Prerequisites
- **Python**: 3.9+ recommended
- **OS**: Windows 10/11 (commands below use PowerShell)

### Setup (Windows PowerShell)
```powershell
# From the repo root
python -m venv .venv
.\.venv\Scripts\Activate
pip install --upgrade pip
pip install -r requirements.txt
```

### Launch the notebook
```powershell
python -m pip install jupyter
jupyter notebook
```
Then open `Men_T20.ipynb` and run cells top-to-bottom.

### Notebook: `Men_T20.ipynb` and outputs
The notebook contains step-by-step exploration and feature engineering. Key outputs are rendered inline so you can see results without exporting files:
- Summary previews of the dataset and selected columns
- Cleaning and transformation steps with before/after samples
- Visualizations (Seaborn/Matplotlib) such as distributions, comparisons, and trends
- Engineered features with intermediate checks and descriptive stats

To view outputs, open the notebook and scroll through executed cells. If any cell shows no output, run it to regenerate the plots/tables. Re-running all cells will recompute every figure and table from the CSV.

### Visualizations (saved outputs)
Below are example plots produced by the notebook. Save figures from the notebook to a `figures/` folder with these filenames so the README renders them automatically:

![Outcome distribution](figures/outcome_distribution.png)
![Team win rates](figures/team_win_rates.png)
![Runs distribution](figures/runs_distribution.png)
![Toss decision vs win rate](figures/toss_vs_win.png)
![Venue-wise results](figures/venue_results.png)

Export figures from the notebook using, for example:
```python
import matplotlib.pyplot as plt
# after creating a plot
plt.tight_layout()
plt.savefig("figures/outcome_distribution.png", dpi=200, bbox_inches="tight")
```
If the `figures/` directory does not exist, create it first or adjust the path.

### Data
- **File**: `all_t20_world_cup_matches_results.csv`
- **Source**: T20 World Cup match results (columns include teams, scores, outcomes, etc.)
  Ensure the CSV remains in the project root so the notebook can load it without path changes.

### Reproduce the analysis
1) Create and activate the virtual environment
2) Install dependencies via `requirements.txt`
3) Launch Jupyter and open `Men_T20.ipynb`
4) Run all cells

### Notes
- If you prefer VS Code, install the Python and Jupyter extensions and open `Men_T20.ipynb` directly.
- To add packages, also update `requirements.txt` so others can reproduce your environment.

### License
Got this dataset from Kaggle.
