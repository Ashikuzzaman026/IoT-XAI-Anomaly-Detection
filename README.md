<div align="center">

# 🌐 IoT-XAI-Anomaly-Detection

## An Optimized Decision Tree-Based Framework for Explainable IoT Anomaly Detection

<p>
  <img src="https://img.shields.io/badge/Python-3.x-3776AB?logo=python&logoColor=white" alt="Python" />
  <img src="https://img.shields.io/badge/Model-Decision%20Tree-6F42C1" alt="Decision Tree" />
  <img src="https://img.shields.io/badge/Domain-IoT%20Security-0EA5E9" alt="IoT Security" />
  <img src="https://img.shields.io/badge/XAI-Explainable%20AI-F59E0B" alt="Explainable AI" />
  <img src="https://img.shields.io/badge/Dataset-WUSTL%20EHMS%202020-22C55E" alt="WUSTL EHMS 2020" />
  <img src="https://img.shields.io/badge/Status-Research%20Code-34D399" alt="Research Code" />
</p>

<p>
  <b>IoT Security</b> •
  <b>Anomaly Detection</b> •
  <b>Decision Tree Learning</b> •
  <b>Explainable AI</b>
</p>

</div>

---

## 👥 Contributors

- Ashikuzzaman

## ✨ Overview

IoT devices continuously generate network traffic and system-level data. In security-sensitive environments, even a small abnormal pattern may indicate malware, botnet activity, compromise, or operational faults. Detecting these anomalies early is essential for protecting connected systems.

This repository presents an explainable machine-learning workflow for IoT anomaly detection. It uses the WUSTL-EHMS-2020 dataset and an optimized Decision Tree model to classify network behaviors and highlight the most influential features behind each prediction.

The project aims to go beyond simple detection by supporting interpretability. In real-world security systems, understanding why a sample is flagged as anomalous is often as important as the prediction itself.

---

<table>
  <tr>
    <td width="50%">

### 🧠 Core ML Capabilities

- Decision Tree-based anomaly classification
- Data cleaning and preprocessing
- Feature and label preparation
- Train/test splitting workflow
- Model evaluation with standard metrics
- Structured IoT network data support

    </td>
    <td width="50%">

### 🔍 Explainable AI Focus

- Feature-importance analysis
- Transparent anomaly reasoning
- Better interpretation of security alerts
- Improved investigation of abnormal patterns
- Research-oriented model understanding

    </td>
  </tr>
</table>

---

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

---

## 📊 Dataset

The project uses the following research dataset:

- Dataset: WUSTL-EHMS-2020 with attack categories
- File: `wustl-ehms-2020_with_attacks_categories.csv`
- Data type: Structured IoT / network traffic data
- Purpose: IoT anomaly detection and attack-category analysis

> Please review the original dataset documentation and licensing terms before redistributing or using the data in other projects.

---

## 🧠 Model Description

The framework is based on an optimized Decision Tree classifier. Decision Trees are especially useful for tabular cybersecurity data because they can model nonlinear decision boundaries while preserving interpretability.

The workflow includes the following stages:

1. Load the IoT traffic dataset.
2. Inspect the dataset and identify relevant variables.
3. Prepare features and target labels.
4. Apply preprocessing needed for model training.
5. Train the Decision Tree classifier.
6. Generate anomaly predictions.
7. Evaluate performance using standard metrics.
8. Analyze feature importance to explain outputs.

---

## 🔎 Explainable AI

Explainability is a central part of this project. Instead of treating the detector as a black box, the workflow identifies which input features contribute most to the model's decisions.

This can help:

- Rank the most relevant traffic features
- Understand why a sample is classified as anomalous
- Interpret relationships between important features and attack categories
- Support security analysts during investigation
- Improve trust and transparency in model-based detection

---

## 📈 Evaluation Metrics

The notebook is designed to assess the classifier using widely used classification metrics, including:

- Accuracy
- Precision
- Recall
- F1-score
- Confusion matrix
- Classification report
- Feature importance

For security applications, precision and recall should be interpreted alongside accuracy, since class imbalance can make raw accuracy misleading.

---

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
├── README.md
│
└── .gitignore (if present)
```

---

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

Activate it:

- Linux/macOS:

```bash
source .venv/bin/activate
```

- Windows:

```powershell
.venv\Scripts\activate
```

### 3. Install required packages

```bash
pip install numpy pandas scikit-learn matplotlib seaborn jupyter
```

### 4. Open the notebook

```bash
jupyter notebook "wustl_data_iot_(2).ipynb"
```

### 5. Run the workflow

Recommended flow:

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

---

## 🛠️ Technologies

- Python
- Jupyter Notebook
- Pandas
- NumPy
- Scikit-learn
- Matplotlib
- Seaborn
- Explainable AI techniques

---

## 🎯 Research Goals

This project focuses on the following objectives:

- Build a practical anomaly-detection workflow for IoT traffic
- Use an interpretable Decision Tree model for structured data
- Identify features associated with anomalous behavior
- Evaluate performance using multiple metrics
- Make IoT security predictions more transparent and trustworthy

---

## ⚠️ Limitations

- The repository is primarily notebook-based.
- Results may depend on preprocessing choices, train/test splits, and hyperparameters.
- Dataset performance may not generalize directly to all real-world deployment scenarios.
- Additional validation on external IoT datasets is recommended.
- Explainability results represent model behavior, not definitive causal proof.

---

## 🔮 Future Improvements

Possible extensions include:

- Comparing Decision Tree performance with Random Forest, XGBoost, and LightGBM
- Adding SHAP and LIME explanations
- Conducting cross-validation and systematic hyperparameter tuning
- Handling class imbalance with suitable sampling strategies
- Supporting real-time IoT traffic inference
- Building a lightweight monitoring dashboard
- Evaluating robustness against evolving attack patterns

---

## 📜 Citation

If you use this project in academic or research work, please cite both the repository and the original WUSTL-EHMS-2020 dataset source.

---

## 📄 License

No explicit license has been specified for this repository. Please contact the repository owner before redistributing or reusing the code and dataset outside the intended research context.

---

## 🙏 Acknowledgements

Thanks to the researchers and dataset creators who made the WUSTL-EHMS-2020 IoT security dataset available for research and experimentation.

<div align="center">

<p><i>Built for interpretable and trustworthy IoT anomaly detection.</i></p>

</div>
