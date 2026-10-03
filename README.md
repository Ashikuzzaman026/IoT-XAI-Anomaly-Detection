<div align="center">

# 🌐 IoT-XAI-Anomaly-Detection

## An Optimized Decision Tree-Based Framework for Explainable IoT Anomaly Detection

<p>
  <strong>
    A machine-learning research framework for detecting anomalous behavior in Internet of Things (IoT) network traffic using an optimized Decision Tree model and explainable artificial intelligence techniques.
  </strong>
</p>

<p>
  <img src="https://img.shields.io/badge/Python-3.x-3776AB?logo=python&logoColor=white" alt="Python"/>
  <img src="https://img.shields.io/badge/Model-Decision%20Tree-6F42C1" alt="Decision Tree"/>
  <img src="https://img.shields.io/badge/Domain-IoT%20Security-0EA5E9" alt="IoT Security"/>
  <img src="https://img.shields.io/badge/XAI-Explainable%20AI-F59E0B" alt="Explainable AI"/>
  <img src="https://img.shields.io/badge/Data-WUSTL%20EHMS%202020-22C55E" alt="WUSTL EHMS 2020"/>
  <img src="https://img.shields.io/badge/Status-Research%20Code-22C55E" alt="Research Code"/>
</p>

<p>
  <b>IoT Security</b> •
  <b>Anomaly Detection</b> •
  <b>Decision Tree Learning</b> •
  <b>Explainable AI</b>
</p>

</div>

## 👥 Contributors

- Ashikuzzaman

## 🌟 Overview

IoT devices continuously generate network traffic and system-level data. Because these devices are often deployed in security-sensitive environments, identifying abnormal or malicious behavior is an important cybersecurity task.

This project presents an explainable machine-learning workflow for IoT anomaly detection. It uses the **WUSTL-EHMS-2020** dataset with attack-category information and applies an optimized **Decision Tree-based classification framework** to distinguish normal traffic from anomalous traffic.

The primary objective is not only to detect anomalies, but also to make the model's decisions easier to understand. Explainable AI methods can help identify the features that contribute most to a prediction and support more transparent security analysis.

## ✨ Highlights

<table>
<tr>
<td width="50%">

### 🧠 Machine Learning

- Decision Tree-based anomaly classification
- Data preprocessing and cleaning
- Feature and target preparation
- Training and testing workflow
- Model evaluation using classification metrics
- Suitable for structured IoT network data

</td>
<td width="50%">

### 🔍 Explainable AI

- Feature-importance analysis
- Interpretation of anomaly predictions
- More transparent security decisions
- Easier investigation of attack-related traffic
- Supports research-focused model analysis

</td>
</tr>
</table>

## 🧩 Project Workflow

```mermaid
flowchart LR
    A[IoT Network Dataset] --> B[Data Loading]
    B --> C[Data Cleaning and Preprocessing]
    C --> D[Feature and Label Preparation]
    D --> E[Train/Test Split]
    E --> F[Optimized Decision Tree]
    F --> G[Anomaly Prediction]
    G --> H[Performance Evaluation]
    F --> I[Explainable AI Analysis]
    I --> J[Feature Importance and Interpretation]
```

## 📊 Dataset

The project uses the following dataset:

- **Dataset:** WUSTL-EHMS-2020 with attack categories
- **File:** `wustl-ehms-2020_with_attacks_categories.csv`
- **Data type:** Structured IoT/network traffic data
- **Purpose:** IoT anomaly and attack-category detection

The dataset is included in this repository for reproducibility. Please review the original dataset documentation and licensing terms before using it in other projects or redistributing it.

## 🧠 Model Description

The project is based on an optimized Decision Tree approach. Decision Trees are useful for tabular cybersecurity data because they can learn nonlinear decision boundaries while producing rules that are comparatively easy to interpret.

The framework includes the following stages:

1. Load the IoT traffic dataset.
2. Inspect the dataset and identify relevant variables.
3. Prepare features and target labels.
4. Apply preprocessing required for model training.
5. Train the Decision Tree classifier.
6. Generate normal/anomalous predictions.
7. Evaluate the model using standard classification metrics.
8. Analyze feature importance to explain the predictions.

## 🔍 Explainable AI

Explainability is an important part of this project. Instead of treating the detector as a black box, the workflow investigates which input features influence the model's decisions.

The explainability analysis can be used to:

- Rank the most influential traffic features.
- Understand why a sample is classified as anomalous.
- Inspect the relationship between important features and attack categories.
- Support security analysts during anomaly investigation.
- Improve trust and transparency in machine-learning-based detection.

## 📈 Evaluation

The notebook is designed to evaluate the classifier using commonly used classification metrics, including:

- Accuracy
- Precision
- Recall
- F1-score
- Confusion matrix
- Classification report
- Feature importance

For security applications, precision and recall should be considered together with accuracy because an imbalanced dataset may make accuracy alone misleading.

## 📁 Repository Structure

```text
IoT-XAI-Anomaly-Detection/
│
├── wustl_data_iot_(2).ipynb
│   ├── Dataset loading
│   ├── Data exploration
│   ├── Data preprocessing
│   ├── Feature preparation
│   ├── Decision Tree training
│   ├── Anomaly prediction
│   ├── Model evaluation
│   └── Explainable AI / feature-importance analysis
│
├── wustl-ehms-2020_with_attacks_categories.csv
│   └── WUSTL-EHMS-2020 IoT traffic dataset with attack categories
│
└── README.md
```

## 🚀 Quick Start

### 1. Clone the repository

```bash
git clone https://github.com/Ashikuzzaman026/IoT-XAI-Anomaly-Detection.git
cd IoT-XAI-Anomaly-Detection
```

### 2. Create a virtual environment

```bash
python -m venv .venv
```

Activate the environment on Linux/macOS:

```bash
source .venv/bin/activate
```

Activate the environment on Windows:

```powershell
.venv\Scripts\activate
```

### 3. Install the required packages

```bash
pip install numpy pandas scikit-learn matplotlib seaborn jupyter
```

### 4. Open the notebook

```bash
jupyter notebook "wustl_data_iot_(2).ipynb"
```

### 5. Run the workflow

Recommended execution order:

```text
Load Dataset
    ↓
Explore and Clean Data
    ↓
Prepare Features and Labels
    ↓
Split the Dataset
    ↓
Train the Decision Tree
    ↓
Evaluate Anomaly Detection Performance
    ↓
Analyze Feature Importance
```

## 🛠️ Technologies

- Python
- Jupyter Notebook
- Pandas
- NumPy
- Scikit-learn
- Matplotlib
- Seaborn
- Explainable AI techniques for model interpretation

## 🎯 Research Goals

This project focuses on the following goals:

- Build a practical anomaly-detection pipeline for IoT traffic.
- Use an interpretable Decision Tree model for structured data.
- Identify important features associated with anomalous behavior.
- Evaluate the model using multiple performance metrics.
- Make IoT security predictions more understandable and trustworthy.

## ⚠️ Limitations

- This repository is primarily notebook-based.
- Results may depend on preprocessing choices, train/test splitting, and hyperparameter settings.
- Dataset performance may not directly represent real-world deployment performance.
- Further validation on external IoT datasets is recommended.
- Explainability results should be interpreted as model behavior, not as definitive causal evidence.

## 🔮 Future Improvements

Potential future extensions include:

- Comparing Decision Tree performance with Random Forest, XGBoost, and LightGBM.
- Adding SHAP and LIME explanations.
- Performing cross-validation and systematic hyperparameter tuning.
- Handling class imbalance with suitable sampling strategies.
- Adding real-time IoT traffic inference.
- Building a lightweight monitoring dashboard.
- Evaluating robustness against changing attack patterns.

## 📜 Citation

If you use this project in academic or research work, please cite the repository and the original WUSTL-EHMS-2020 dataset source.

## 📄 License

No license has currently been specified for this repository. Please contact the repository owner before redistributing or using the code and dataset outside the intended research context.

## 🙏 Acknowledgements

Thanks to the researchers and dataset creators who made the WUSTL-EHMS-2020 IoT security data available for research and experimentation.
