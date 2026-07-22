# Manufacturing Defect Root Cause Analysis

## Overview
This project investigates the root causes of part failures in a manufacturing environment. I initially set out to test if human factors or process durations were driving defects, but the data told a different story. By applying data-driven analysis to manufacturing metrics, this project identifies the true operational bottlenecks and demonstrates how to bridge the gap between operational assumptions and actual machine health.

## The Hypothesis vs. The Data
My initial hypothesis was that **Worker Productivity** or **Additive Process Time** were the primary variables causing defects. 

To test this, I conducted an Exploratory Data Analysis (EDA). The correlation results disproved the initial hypothesis:
* Worker Productivity showed a near-zero correlation (-0.005) with the defect status.
* Additive Process Time also had a negligible impact (0.005).

## Key Findings
After eliminating process times and human error, I expanded the correlation analysis across all system metrics. The real drivers of defects turned out to be related to machine health and production load:
* **Maintenance Hours (0.297):** The strongest predictor of defects. Higher maintenance hours strongly correlate with failure rates, pointing toward machine wear, calibration drift, or issues stabilizing the line after maintenance.
* **Defect Rate (0.245) & Production Volume (0.128):** Higher volumes and batch-level defect rates also showed positive correlations, suggesting machine fatigue or rushed cycle times during peak production.

## Tech Stack
* Python
* Pandas (Data manipulation)
* Matplotlib (Data visualization)
* Jupyter Notebook

## How to Run This Project
1. Clone this repository to your local machine.
2. Install the required Python libraries using the command: `pip install -r requirements.txt`
3. Open `manufacturing_defect_analysis.ipynb` in Jupyter Notebook or VS Code.
4. Ensure the `manufacturing_defect_dataset.csv` is in the same directory.
5. Run the cells to reproduce the correlation analysis and visual distributions.