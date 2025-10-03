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

![Team win rates]
<img width="563" height="530" alt="image" src="https://github.com/user-attachments/assets/c5e81877-d948-4869-9dab-7500bb23f61e" />

![Runs distribution]
<img width="571" height="453" alt="image" src="https://github.com/user-attachments/assets/5d82d507-0aa7-4545-97f2-0f6dcf4a0c57" />

![Wickets VS Frequency]
<img width="563" height="453" alt="image" src="https://github.com/user-attachments/assets/6ea7d1ff-0d65-4b36-9000-18620110ac7d" />

![Run vs Frequency]
<img width="1065" height="622" alt="image" src="https://github.com/user-attachments/assets/8a7fa317-340c-4ac2-a4c3-66b59251201b" />

![Season Vs India Wins Frequency]
<img width="563" height="432" alt="image" src="https://github.com/user-attachments/assets/100e64ae-8d48-4177-a08b-9b8d1c9c2a4f" />


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
