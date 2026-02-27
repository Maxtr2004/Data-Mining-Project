# Data Mining Projekt 
## Unterrepräsentierte Champion-Archetypen in League of Legends

Autor: Max Trummer

Modul: DMI01 – Data Mining

Angabe: 27.02.2026

## Überblick

Ziel dieses Projekts ist die datengetriebene Identifikation unterrepräsentierter Champion-Kombinationen im aktuellen League of Legends Meta.

### Forschungsfrage:

Welche Kombination aus Rolle und Klasse weist bei durchschnittlichen Leistungswerten die niedrigste prognostizierte Pickrate auf und eignet sich somit als Grundlage für ein neues Champion-Design?

Die Analyse folgt dem CRISP-DM-Prozess.

## Methodik

Datenquellen: METAsrc & League of Legends Wiki (via Kaggle)

Zielvariable: Pickrate

Train/Test-Split: 80/20

Cross-Validation: 5-Fold

Hyperparameter-Tuning: GridSearchCV

## Getestete Modelle

Lineare Regression (Baseline)

Random Forest

Neuronales Netz (MLP)

XGBoost (bestes Modell)

### Modellperformance (XGBoost):

R² ≈ 0,964

Niedrigster RMSE im Vergleich

## Zentrales Ergebnis

Das Modell identifiziert folgende Kombination als unterrepräsentiert:

Rolle: Top-Lane

Klasse: Tank

Prognostizierte Pickrate bei durchschnittlichen Werten: ≈ 4 %

## Projektstruktur

    Trummer_Max_DMI01.pdf

    Screencast_Data_Mining.mp4

    Eigenständigkeitserklärung_TRUMMER_DataMining

    Code and Data/
    │
    ├── Code und Output/
    │   ├── DataMiningProject-Notebook.ipynb
    │   ├── lol_pickrate_model.pkl
    │   └── ydata_profiling_report.html
    │
    └── Daten/
        ├── 200125_LoL_champion_data.csv
        └── League of Legends Champion Stats 12.1.csv

## Wesentliche Bibliotheken:

pandas

numpy

scikit-learn

xgboost

seaborn

ydata-profiling