Burn Area Analysis – Pantanal 2024

This project uses GeoAI to study wildfires in the Pantanal wetlands during May–July 2024.
It combines satellite data, climate reanalysis, and land-use information to build models that predict where fires are likely to occur.

What’s Included

Data preprocessing (MODIS Burn Area, WorldCover, NASADEM, ERA5)

Baseline models: Random Forest, XGBoost, TabNet

Spatiotemporal model: ConvLSTM for burn progression

Scripts and notebooks for training, evaluation, and visualization

How to Run

Use the Jupyter notebooks in notebooks/ to follow the workflow step by step.
0.final_notebook_v3(2).ipynb
The consolidated notebook for the I-GUIDE Summer School 2025 (Team 2) project. Combines preprocessing, model training, and evaluation into a single, streamlined workflow for sharing and reproducibility.

1.1.Tabular_data_processing.ipynb
Prepares and processes raw tabular datasets for modeling. Includes data cleaning, feature engineering, and formatting steps to ensure compatibility with multiple machine learning models.

2.1.RF_basic_features.ipynb
Trains and evaluates a baseline Random Forest classifier using only the core tabular features (without burn or embedding information).

2.2.RF_basic with burn.ipynb
Extends the Random Forest baseline by incorporating burn area data as an additional feature set to improve classification performance.

2.3.RF_basic with burn+embeddings.ipynb
Builds on the previous Random Forest setup by adding both burn data and learned embeddings, testing whether combined features improve model accuracy.

3.1.XGB_basic_features.ipynb
Implements a baseline XGBoost model using the same basic tabular features for classification, serving as a comparison point with Random Forest.

3.2.XGB_basic with burn.ipynb
Enhances the XGBoost model by including burn area information to evaluate its effect on predictive performance.

3.3.XGB_basic with burn+embeddings.ipynb
Further extends XGBoost by integrating both burn features and embeddings, testing the benefits of richer input features.

4.1.TabNet_basic_features.ipynb
Introduces the TabNet deep learning model trained on the basic tabular feature set, offering a neural network–based approach to classification.

4.2.TabNet_basic with burn.ipynb
Trains TabNet with burn features added to the input data, evaluating the effect of fire-related predictors.

4.3.TabNet_basic with burn+embeddings.ipynb
Runs TabNet with the full feature set, including basic features, burn data, and embeddings, providing the most complex model configuration.
Or run scripts (e.g. train_baseline.py, train_convlstm.py) for model training.

5.1.ResConvLSTM_training.ipynb
Defines and trains a Residual Convolutional LSTM (ResConvLSTM) architecture for spatiotemporal sequence modeling. Focuses on capturing both spatial and temporal dependencies in the input data.
Key actions:

5.2.ResConvLSTM_test.ipynb
Evaluates the trained ResConvLSTM model on test data, generating inference plots and performance metrics.
Key actions:


Outputs (figures, gifs, model results) will be saved in the outputs/ folder.