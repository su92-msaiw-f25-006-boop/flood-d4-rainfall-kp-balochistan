# Subnational Rainfall Forecasting for Khyber Pakhtunkhwa and Balochistan (1981–2025)

This repository provides long-term monthly and decadal precipitation time-series (1981–2025) across Pakistan with focused analysis on the flash-flood vulnerable regions of Khyber Pakhtunkhwa (KP) and Balochistan. It benchmarks classical statistical models (SARIMAX) against machine learning algorithms (Linear Regression, Random Forest, XGBoost, and LSTM neural networks) for next-month rainfall forecasting.

## Folder Structure

```
flood-d4-rainfall-kp-balochistan/
├── 1_code/
│   └── Rainfall_Forecast_KP_Balochistan.ipynb  # Data cleaning, aggregation, SARIMA & ML models
├── 2_kaggle_input/
│   └── ABD_Rainfall_1981_2025.csv              # Decadal (10-day) rainfall observations (1981–2025)
├── 3_kaggle_output/
│   └── Dataset_4_Rainfall_OUTPUT.ipynb         # Executed notebook with model outputs and plots
├── 4_doc/
│   └── Dataset 4 - Rainfall Forecasting KP and Balochistan - Results.docx # Experimental summary report
├── .gitignore
├── LICENSE
├── README.md
└── requirements.txt
```

## How to Run

1. **Prerequisites:** Python 3.10 or higher.
2. **Install Dependencies:**
   ```bash
   pip install -r requirements.txt
   ```
3. **Run the Notebook:**
   ```bash
   jupyter notebook 1_code/Rainfall_Forecast_KP_Balochistan.ipynb
   ```

The pipeline aggregates 10-day records across 535 continuous months, handles multi-gauge station averages for KP, and evaluates out-of-time forecasting by training on 1981–2014 and testing on 2015–2025.

## Data Source and Licence

- **Primary Source:** Kaggle dataset *"Citywise Pakistan Rainfall by QTR (1981–2025)"* uploaded by Abdullah Imran ([Kaggle dataset](https://www.kaggle.com/datasets/abdullahimranr2/citywise-pakistan-rainfall-by-qtr-19812025)).
  - Upstream data provider: World Food Programme (WFP) / Humanitarian Data Exchange (HDX) subnational rainfall indicators, derived from the Climate Hazards Group InfraRed Precipitation with Station data (CHIRPS) and Pakistan Meteorological Department (PMD) station records.
- **Data Licence:** Database: Open Database License ([ODbL 1.0](http://opendatacommons.org/licenses/odbl/1.0/)) / Underlying contents: [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/).
- **Code Licence:** The code in this repository is released under the [MIT License](LICENSE).

## Citation

```bibtex
@misc{anwar2026_rainfall_kp_balochistan,
  author = {Shahan Anwar},
  title = {Subnational Rainfall Forecasting for Khyber Pakhtunkhwa and Balochistan (1981--2025)},
  year = {2026},
  publisher = {GitHub},
  howpublished = {\url{https://github.com/su92-msaiw-f25-006-boop/flood-d4-rainfall-kp-balochistan}}
}
```
