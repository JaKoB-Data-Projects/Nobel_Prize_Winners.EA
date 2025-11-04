# Nobel Prize Winners — Exploratory Analysis

Short description
A small exploratory project that analyzes a dataset of Nobel Prize winners. The script computes and visualizes:
- Which gender has the most Nobel laureates.
- The most common birth country among laureates.
- The proportion of U.S.-born laureates by decade (line plot).
- The proportion of female laureates by decade and category (line plot).
- The first woman to win a Nobel Prize (name and category).
- A list of laureates who won multiple Nobel Prizes.

Files
- analysis.py — example script that performs the analysis and plots

Requirements
- Python 3.8+
- pandas
- numpy
- seaborn
- matplotlib

Install
pip install pandas numpy seaborn matplotlib

Usage
1. Place the dataset at data/nobel.csv (or update the path in the script).
2. Run the script:
   python analysis.py
3. The script prints summary values and creates two seaborn relplot line charts:
   - proportion of U.S.-born winners by decade
   - proportion of female winners by decade (with category hue)

Outputs
- top_gender — the gender with the most Nobel laureates
- top_country — the most common birth country among laureates
- prop_usa_winners — proportion of U.S.-born winners for each decade
- max_decade_usa — the decade with the highest proportion of U.S.-born winners
- prop_female_winners — proportion of female laureates by decade and category
- max_female_decade_category — decade and category with highest female proportion
- first_woman_name / first_woman_category — the first female laureate found in the dataset
- repeat_list — list of laureates who appear two or more times (multiple prizes)

Notes & Fixes
- Fix print statements to call print(...) instead of assigning (current code sets print variable).
- Consider saving plots instead of only displaying them, e.g.:
  fig1 = ax1.fig
  fig1.savefig("outputs/usa_by_decade.png")
  fig2 = ax2.fig
  fig2.savefig("outputs/female_by_decade_category.png")
- Validate that data/nobel.csv contains expected columns: year, sex, birth_country, full_name, category.
- Handle ties when selecting max values (current code picks first match).
- Add argument parsing or a small notebook to make the project more user-friendly.
- Add a requirements.txt or environment.yml for reproducibility.

License
Add a license file if you want to make the project public (e.g., MIT).# Nobel_Prize_Winners.EA
Analysis of Nobel Prize winners: loads Nobel winners data, computes trends by decade for U.S.-born and female laureates, finds the first female laureate and repeated winners, and produces simple line plots."
