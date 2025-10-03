## Fast Food Consumption – Exploration and Feature Engineering

Exploratory data analysis and feature engineering on U.S. fast food spending by state using Python and Jupyter.

### Repo structure
```text
Fast-food-consumption/
  ├─ Fast_food.ipynb          # Main analysis / feature engineering notebook
  ├─ fast_food_dataset.csv    # Dataset loaded by the notebook
  ├─ requirements.txt         # Python dependencies
  └─ README.md
```

### Prerequisites
- **Python**: 3.9+ recommended
- **OS**: Windows 10/11 (PowerShell commands below)

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
Then open `Fast_food.ipynb` and run cells top-to-bottom.

### Notebook: `Fast_food.ipynb` and key outputs
The notebook performs step-by-step EDA and feature engineering on `fast_food_dataset.csv` with columns: `state`, `region`, `fast_food_millions`.
- Data inspection: `head`, `info`, shape, missing and duplicate checks, `describe`
- Visualizations: histogram of `fast_food_millions`, bar chart `region` vs `fast_food_millions`, box plot
- Ranking and segments: top/bottom states, regional totals, dense ranks, quartiles via `qcut`
- Statistics: mean, median, mode, percent above national average
- Features: `above_avg` flag, synthetic `population_millions`, per-capita `spending`, `spending_Quartile`
- Math demo: SymPy derivative of unhealthiness index \( (Food / Population) * 100 \)

If a cell shows no output, run it to regenerate the tables/plots. Re-running all cells recomputes figures and tables from the CSV.

### Visualizations (saved outputs)
Optionally export figures created in the notebook to a `figures/` folder so they can be embedded here:

Distribution of spending
<img width="563" height="433" alt="image" src="https://github.com/user-attachments/assets/9361542b-aa87-470d-a9b2-acf4ef2e5fdf" />

Spending by region
<img width="563" height="507" alt="image" src="https://github.com/user-attachments/assets/18503c24-d745-433f-a99c-b94a97af7cd4" />

Spending box plot
<img width="520" height="453" alt="image" src="https://github.com/user-attachments/assets/ef3c7118-c5d9-4f0e-a9fc-ff972a60fa34" />


Export from within the notebook, for example:
```python
import matplotlib.pyplot as plt
# after creating a plot
plt.tight_layout()
plt.savefig("figures/spending_distribution.png", dpi=200, bbox_inches="tight")
```
If the `figures/` directory does not exist, create it first or adjust the path.

### Data
- **File**: `fast_food_dataset.csv`
- **Columns**: `state` (str), `region` (str), `fast_food_millions` (int)
  Keep the CSV in the project root so the notebook can load it without path changes.

### Reproduce the analysis
1) Create and activate the virtual environment
2) Install dependencies via `requirements.txt`
3) Launch Jupyter and open `Fast_food.ipynb`
4) Run all cells

### Notes
- The notebook currently reads from a local CSV path; ensure the path points to `fast_food_dataset.csv` in the repo root.
- If you prefer VS Code, install the Python and Jupyter extensions and open `Fast_food.ipynb` directly.
- When adding packages, also update `requirements.txt` for reproducibility.

### License
Dataset source: Kaggle.
