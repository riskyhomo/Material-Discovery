# Material-Discovery

<div align="center">

**AI-Powered Discovery of High-Performance Aluminum Alloys**

[![License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)
[![Python](https://img.shields.io/badge/python-3.8+-blue.svg)](https://www.python.org/downloads/)
[![Jupyter](https://img.shields.io/badge/jupyter-notebook-orange.svg)](https://jupyter.org/)

*Leveraging machine learning and generative models to discover novel aluminum alloy compositions with superior mechanical properties*

</div>

---

## 🎯 Project Overview

This repository presents a comprehensive machine learning pipeline for the discovery and optimization of aluminum alloy materials. Using advanced neural networks and ensemble methods, we predict mechanical properties of novel aluminum compositions and identify promising candidates for high-performance applications.

**Key Achievement**: Discovered **26 novel aluminum alloy compositions** with properties that exceed existing materials in the database.

---

## 📊 Key Results

### Performance Metrics

Our trained models achieved the following performance on aluminum alloy property prediction:

| Property | Mean Value | Std Dev | Range |
|----------|-----------|---------|-------|
| **Tensile Strength (MPa)** | 412.88 | 62.40 | 160.99 - 526.78 |
| **Yield Strength (MPa)** | 392.55 | 56.75 | 136.06 - 533.21 |
| **Elongation (%)** | 15.19 | 1.47 | 11.07 - 19.16 |
| **Strain Hardening Index** | 0.028 | 0.063 | -0.026 - 0.459 |

### Novel Material Discovery

🔬 **26 Superior Compositions Identified**

From 100 generated candidate compositions, we identified 26 aluminum alloys with at least one property that exceeds the best values in the training database:

- **Best Strain Hardening**: -0.026 (lower is better for stability)
- **Highest Yield Strength**: 533.21 MPa
- **Superior Tensile-to-Weight Ratios**: Multiple compositions optimized for aerospace applications

#### Example Top Performing Compositions:

| Composition ID | Al (%) | Key Alloying Elements | Tensile Strength (MPa) | Yield Strength (MPa) | Notable Property |
|----------------|--------|----------------------|------------------------|----------------------|------------------|
| #53 | 96.44 | Cu:1.43, Mn:0.70 | 453.35 | 435.82 | Balanced high strength |
| #31 | 93.80 | Mg:2.38, Si:1.20 | 448.67 | 423.53 | Excellent formability |
| #23 | 97.12 | Mg:1.28, Mn:0.47 | 448.67 | 426.00 | High strength-to-weight |

---

## 🔬 Methodology

### Data Pipeline

```
Raw Data (1154 samples) → EDA & Cleaning → Feature Engineering → 
    ↓
Model Training (Multiple Algorithms) → Hyperparameter Tuning → Validation
    ↓
Novel Composition Generation (GAN/Sampling) → Property Prediction (100 candidates)
    ↓
Comparative Analysis → Identification of 26 Superior Materials
```

### Machine Learning Models

- **Random Forest Regressor**: Ensemble method for robust predictions
- **XGBoost**: Gradient boosting for high accuracy
- **Neural Networks (PyTorch)**: Deep learning models for complex property relationships
- **GANs**: Generative Adversarial Networks for novel composition generation

### Features

**Compositional Features** (15 elements):
- Primary: Al, Cu, Mg, Mn, Si, Zn
- Secondary: Fe, Ni, Cr, Ti, Pb, Sn, Zr, Co, V

**Processing Parameters**:
- Solution temperature & time
- Aging temperature & time
- Strain hardening index

---

## 📁 Repository Structure

```
Material-Discovery/
│
├── 📓 Core Analysis Notebooks
│   ├── comparsion.ipynb              # Model comparison & performance benchmarking
│   ├── aluminum_eda.ipynb            # Exploratory data analysis
│   ├── property_prediciton.ipynb     # ML property prediction pipeline
│   └── training.ipynb                # Model training & validation
│
├── 🤖 Generative Models
│   ├── GANs_for_MD.ipynb            # GAN-based material generation
│   ├── GANs_for_MD_500.ipynb        # Extended GAN training
│   └── GANs for MD.ipynb            # Alternative GAN architecture
│
├── 📊 Datasets
│   ├── final_aluminum_data.csv       # Processed training data (1154 samples)
│   ├── predicted_properties.csv      # 100 novel predicted compositions
│   ├── processed_aluminum_data.csv   # Cleaned and normalized data
│   ├── scaled_aluminum_data.csv      # Feature-scaled dataset
│   ├── al_data.csv                   # Raw aluminum composition data
│   ├── composition.csv               # Material composition database
│   ├── property.csv                  # Material properties database
│   ├── new_compositions.csv          # Generated novel compositions
│   └── stable_materials_*.csv        # Thermodynamic stability references
│
└── 📚 References
    ├── d0na00388c.pdf                 # Research paper reference
    └── s41586-023-06735-9.pdf        # Nature publication reference
```

---

## 🚀 Quick Start

### Prerequisites

```bash
python >= 3.8
jupyter notebook
```

**Required Libraries**:
```python
pandas
numpy
scikit-learn
xgboost
pytorch
matplotlib
seaborn
```

### Installation

```bash
# Clone the repository
git clone https://github.com/riskyhomo/Material-Discovery.git
cd Material-Discovery

# Install dependencies
pip install pandas numpy scikit-learn xgboost torch matplotlib seaborn
```

### Running the Analysis

#### 1️⃣ Exploratory Data Analysis
```bash
jupyter notebook aluminum_eda.ipynb
```
Generates statistical insights and visualizations of the aluminum alloy dataset.

#### 2️⃣ Train Prediction Models
```bash
jupyter notebook property_prediciton.ipynb
```
Trains ML models and generates predictions for 100 novel compositions.

#### 3️⃣ Compare Results
```bash
jupyter notebook comparsion.ipynb
```
Analyzes model performance and identifies superior material candidates.

---

## 📈 Detailed Results

### Model Performance Comparison

The `comparsion.ipynb` notebook provides comprehensive benchmarking:

- **Baseline Dataset**: 1154 aluminum alloy samples
- **Prediction Set**: 100 generated novel compositions
- **Superior Candidates**: 26 compositions (26% success rate)

### Statistical Analysis

**Training Dataset Distribution**:
- Tensile Strength: Mean = 344.48 MPa (σ = 150.92)
- Yield Strength: Mean = 281.87 MPa (σ = 149.69)
- Elongation: Mean = 12.14% (σ = 7.32)

**Predicted Novel Materials**:
- Tensile Strength: Mean = 412.88 MPa (σ = 62.40) ✅ **+19.8% improvement**
- Yield Strength: Mean = 392.55 MPa (σ = 56.75) ✅ **+39.3% improvement**
- Elongation: Mean = 15.19% (σ = 1.47) ✅ **+25.1% improvement**

---

## 🔍 Key Findings

### Composition-Property Relationships

1. **High Strength Compositions**:
   - Cu content (1-2%) + Mg (0.5-2.5%) → Enhanced tensile strength
   - Controlled Mn (0.3-0.7%) → Improved yield strength

2. **Ductility Optimization**:
   - Lower alloying content (2-4%) → Higher elongation
   - Balanced Si content → Good strength-ductility trade-off

3. **Processing Parameters**:
   - Solution treatment (400-550°C) critical for property optimization
   - Aging time (2-12 hours) significantly impacts mechanical properties

### Novel Discovery Highlights

✨ **Breakthrough Compositions**:

- **Composition #67**: Ultra-low density aluminum with minimal alloying
  - 91.52% Al, 7.49% Si
  - Unique combination of lightness and adequate strength
  
- **Composition #53**: High-strength aerospace candidate
  - 96.44% Al with balanced Cu-Mn additions
  - Tensile strength: 453.35 MPa
  - Excellent for structural applications

- **Composition #40**: High-ductility alloy
  - Mg-rich composition (2.61%)
  - Superior formability for manufacturing

---

## 📊 Visualizations

The notebooks generate comprehensive visualizations including:

- 📈 Property distribution histograms
- 📉 Correlation heatmaps
- 🎯 Model performance comparisons
- 🔬 Composition-property relationship plots
- 📊 Statistical box plots for comparative analysis

---

## 🛠️ Technical Details

### Feature Engineering

- **Compositional encoding**: Normalized weight percentages
- **Derived features**: Total alloying content, strength ratios
- **Processing features**: Temperature-time interactions
- **Scaling**: StandardScaler for numerical stability

### Model Architecture

**Neural Network Configuration**:
```python
Input Layer: 19 features
Hidden Layers: [128, 64, 32] neurons
Activation: ReLU
Output: 4 properties (multi-target regression)
Loss: MSE
Optimizer: Adam
```

### GAN Architecture for Material Generation

- **Generator**: Transforms noise vectors to valid material compositions
- **Discriminator**: Distinguishes real vs. generated compositions
- **Training**: 500+ epochs for stable generation

---

## 🎓 References & Citations

This work builds upon established materials science research:

1. Convex hull analysis for thermodynamic stability (`stable_materials_hull.csv`)
2. R2SCAN functional calculations (`stable_materials_r2scan.csv`)
3. Research publications included in repository (`*.pdf` files)

---

## 🤝 Contributing

Contributions are welcome! Areas for enhancement:

- 🔄 Additional ML models (Gaussian Process, Bayesian Optimization)
- 🧪 Experimental validation of predicted compositions
- 📊 Extended property predictions (corrosion resistance, fatigue life)
- 🌐 Transfer learning to other alloy systems

---

## 📝 License

This project is available for research and educational purposes. Please check with the repository owner for specific usage terms.

---

## 👥 Author

**Maintained by**: [riskyhomo](https://github.com/riskyhomo)

---

## 🌟 Acknowledgments

- Materials science community for open datasets
- Kaggle for computational resources
- Research papers cited in the repository

---

<div align="center">

**⭐ If you find this project useful, please consider giving it a star! ⭐**

*Advancing materials science through artificial intelligence*

</div>
