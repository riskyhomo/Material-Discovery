# Material-Discovery

## Repository Purpose
This repository contains databases, Jupyter notebooks, and analysis tools for discovering and predicting properties of novel aluminum alloy materials. The project focuses on exploring aluminum composition data, performing exploratory data analysis, and building machine learning models for material property prediction.

## Repository Structure

### Recent Analysis Notebooks (Last 10 minutes)

#### 1. **comparsion.ipynb**
- **Purpose**: Compares different machine learning models and their performance metrics for material property prediction
- **Key Features**:
  - Model performance comparison across different algorithms
  - Evaluation metrics analysis
  - Visualization of model accuracies
- **Usage**: Run cells sequentially to compare model performances

#### 2. **aluminum_eda.ipynb**
- **Purpose**: Exploratory Data Analysis (EDA) of aluminum alloy composition and properties
- **Key Features**:
  - Data loading and cleaning from al_data.csv
  - Statistical analysis of material properties
  - Distribution analysis and correlation studies
  - Visualization of composition-property relationships
- **Usage**: Execute cells to generate insights about aluminum alloy datasets

#### 3. **property_prediciton.ipynb** (Note: filename has typo - 'prediciton')
- **Purpose**: Build and train machine learning models to predict material properties
- **Key Features**:
  - Feature engineering from composition data
  - Model training (Random Forest, XGBoost, Neural Networks)
  - Property prediction for new compositions
  - Model evaluation and validation
- **Outputs**: predicted_properties.csv with property predictions for new materials
- **Usage**: Run to train models and generate predictions for novel compositions

### Processed Data Files (Recently Updated)

#### CSV Datasets
- **processed_aluminum_data.csv**: Cleaned and preprocessed aluminum alloy data ready for ML models
- **al_data.csv**: Raw aluminum composition and property data
- **composition.csv**: Material composition specifications
- **property.csv**: Material property measurements
- **predicted_properties.csv**: ML model predictions for material properties
- **final_aluminum_data.csv**: Final processed dataset after all transformations
- **scaled_aluminum_data.csv**: Normalized/scaled features for model training
- **new_compositions.csv**: Novel composition candidates for property prediction

### Legacy Notebooks (Older Work)
- **GANs for MD.ipynb** / **GANs_for_MD.ipynb** / **GANs_for_MD_500.ipynb**: Generative Adversarial Networks for Material Discovery
- **ok1.ipynb**: Early experimental notebook
- **work_on_this.ipynb**: Development/scratch notebook

### Reference Data
- **stable_materials_hull.csv**: Thermodynamically stable materials from convex hull analysis
- **stable_materials_r2scan.csv**: Materials stability data using r2SCAN functional

### Documentation
- **d0na00388c.pdf**: Research paper reference
- **s41586-023-06735-9.pdf**: Nature journal article reference

## Workflow

### Standard Analysis Pipeline

1. **Data Preparation** (aluminum_eda.ipynb)
   - Load raw data from al_data.csv
   - Perform exploratory analysis
   - Clean and preprocess data
   - Output: processed_aluminum_data.csv

2. **Property Prediction** (property_prediciton.ipynb)
   - Load processed data
   - Engineer features from composition
   - Train ML models
   - Predict properties for new compositions
   - Output: predicted_properties.csv

3. **Model Comparison** (comparsion.ipynb)
   - Compare different model architectures
   - Evaluate prediction accuracy
   - Select best performing model

## How to Use

### Prerequisites
```python
# Required libraries
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
from sklearn.ensemble import RandomForestRegressor
from sklearn.model_selection import train_test_split
import xgboost as xgb
```

### Quick Start

1. **Clone the repository**
```bash
git clone https://github.com/riskyhomo/Material-Discovery.git
cd Material-Discovery
```

2. **Run EDA notebook**
```bash
jupyter notebook aluminum_eda.ipynb
```
This will generate visualizations and insights about the aluminum alloy dataset.

3. **Train prediction models**
```bash
jupyter notebook property_prediciton.ipynb
```
This will train ML models and output predicted_properties.csv with predictions.

4. **Compare model performance**
```bash
jupyter notebook comparsion.ipynb
```
Review model comparison metrics to select the best approach.

## Results and Outputs

### Generated Files
- **predicted_properties.csv**: Contains predicted material properties for novel compositions
- **processed_aluminum_data.csv**: Clean dataset ready for analysis
- **scaled_aluminum_data.csv**: Normalized features for ML models
- **final_aluminum_data.csv**: Complete processed dataset with all transformations

### Expected Insights
- Composition-property relationships for aluminum alloys
- ML model performance metrics (R², RMSE, MAE)
- Novel material composition candidates with predicted properties
- Comparative analysis of different prediction algorithms

## Update Log

### Recent Updates (Last 10 minutes)
- ✅ Added **comparsion.ipynb** - Model comparison and evaluation notebook
- ✅ Added **aluminum_eda.ipynb** - Comprehensive exploratory data analysis
- ✅ Added **property_prediciton.ipynb** - ML-based property prediction pipeline
- ✅ Added **processed_aluminum_data.csv** - Cleaned dataset
- ✅ Added **predicted_properties.csv** - ML model predictions
- ✅ Added **al_data.csv** - Raw aluminum alloy data
- ✅ Added **composition.csv** - Material composition data
- ✅ Added **property.csv** - Material property measurements
- ✅ Added **new_compositions.csv** - Novel composition candidates
- ✅ Added **final_aluminum_data.csv** - Final processed dataset
- ✅ Added **scaled_aluminum_data.csv** - Normalized features

### Previous Updates
- Added GAN-based material discovery notebooks
- Included reference papers for material science context
- Added stable materials databases (hull and r2scan)

## Contact
Repository maintained by [riskyhomo](https://github.com/riskyhomo)

## License
Public repository - please check with the owner for usage terms
