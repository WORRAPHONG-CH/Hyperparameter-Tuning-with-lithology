# Hyperparameter-tuning-with-lithology-data

-  This project will try to predict a lithologic name from downhole measurement data. <a  href='https://iodp.tamu.edu/labs/ship/Cdeck_downhole.html'>Downhold measurements</a> are done on drilling vessel to supplement or replace coring information: cores are rarely complete, and sometimes are not collected because coring is an expensive process. Instead, a series of measurement tools is sent down the drilling pipe on a cable (a 'string') and collects measurement values from the rock formation.
- The goal will be to fit the best KNN Classifier. And in particular, how many "neighbors" ("K" in KNN) should consider to best predict lithology

![downhole_lab](https://iodp.tamu.edu/labs/ship/photos/dhml.jpg)

## The Features in dataset
*  **Depth_WMSF**: depth of measurements below seafloor for the logging string

*  **HCGR**: Total gamma ray measurement, a bulk measure of radioactivity in the rock

*  **HFK**: Gamma-ray value associated with potassium: a good proxy for clay mineral content

*  **HTHO**: Gamma-ray value associated with thorium: another proxy for mineral content

*  **HURA**: Gamma-ray value associated with uranium: mostly associated with organic matter or phosphorus

*  **HFK**: Gamma-ray value associated with potassium: a good proxy for clay mineral content

*  **IDPH**: Deep induction log from the Phasor Dual Induction–Spherically Focused Resistivity Tool

*  **IMPH**: Medium induction log from the Phasor Dual Induction–Spherically Focused Resistivity Tool

*  **SFLU**: Shallow induction log from the Phasor Dual Induction–Spherically Focused Resistivity Tool

## Concepts
- Preprocessing data by scaled data with standard scaler.
- Perform EDA (Exploratory Data Analysis) to identify keys factor that affect to target.
- Prepared data using Label Encoder to turns label column to numerical classes.
- Create baseline model (KNeihborClassifier) as an initial model utilizing simple "n_neigbors=100" for prediction.
- Identify the best "k" value which provide the best accuracy by using "GridSearch" and "Random Search" to fine-tune hyperparameter in the models
- Evaluate performance model with F1_score.
- Test the best model with test set (unseen dataset).
