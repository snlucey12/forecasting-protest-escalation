# Forecasting Protest Escalation

This repository contains code and analysis for my STAT 4915 research project on forecasting when protests escalate into political violence.

The project constructs a country–month panel dataset using ACLED event data and macro-political indicators, then applies statistical and machine learning models to estimate short-term escalation risk.

---

## Data

This project relies on three datasets:

- **ACLED Event Data (2015–2025)** – not included in the repository due to size and licensing restrictions. Data can be downloaded from https://acleddata.com/
- **Democracy Index data**
- **GINI inequality data**

All datasets should be placed in a `data/` folder before running the analysis.

---

## Repository Structure

- `code/datacleaning.qmd` – Cleans and aggregates ACLED event-level data into a country–month panel and merges macro variables  
- `code/modeling.qmd` – Constructs the escalation variable, fits models, and evaluates predictive performance  
- `data/` – Input datasets (not included for ACLED)  
- `output/` – Generated figures, tables, and model results  

---

## Reproducibility

To reproduce the analysis:

1. Download and place all required datasets in the `data/` folder  
2. Run the data cleaning script:
```bash
   quarto render code/datacleaning.qmd
```
3. Run the modeling script:
```bash
quarto render code/modeling.qmd
```
All figures and results used in the final paper will be generated in the output/
folder.

## Notes
The analysis uses time-ordered training, validation, and test splits (2015–2025) to preserve forecasting integrity.
ACLED data are excluded from the repository due to licensing and size constraints.
Results may vary slightly depending on data version and updates.

## Author

Sonia Lucey  
B.S. Statistical Data Science, University of Connecticut  
