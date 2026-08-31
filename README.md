# patyproj
# QSS 20 Final Project: Social Security Claiming, Gender, and Wealth

**Author:** Ellenia Paty  
**Institution:** Dartmouth College  
**Data:** RAND Health and Retirement Study Longitudinal File 2022 

Social Security pays you more if you delay claiming. So why is 62 still the most popular age to claim? This project uses 30 years of survey data to look at whether early claiming is basically just a cash-flow problem (household wealth), or if it's tied heavier to demographics (gender).

You can read the full write-up on the [live project website](https://elleniaspaty28-cyber.github.io/patyproj/).

# Repository Structure
To ensure clean data hygiene and full reproducibility, this repository is organized into distinct directories:

*   **`code/`**: Contains the sequentially numbered Jupyter Notebooks used to process the data and run the analysis.
*   **`output/`**: Contains the generated Matplotlib/Seaborn figures (`g1patyproj.png` and `g2patyproj.png`).
*   **`index.html`**: The source code for the public-facing GitHub Pages website.

## Replication Instructions
All code is executed via Jupyter Notebooks. The notebooks must be run in the following sequential order:

1.  **`00_pull.ipynb`**: Subsets the massive raw RAND HRS Stata file down to the targeted 86 columns necessary for the analysis. 
2.  **`01_merge.ipynb`**: Handles the wave-to-person aggregation, constructs the `claim_age` and `avg_wealth` proxy variables, and filters out missing values to create the complete-case regression sample.
3.  **`02_analyze.ipynb`**: Runs the OLS and Logistic regression models and generates the final data visualizations.
