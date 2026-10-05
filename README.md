# An Optimized Decision Tree-Based Framework for Explainable IoT Anomaly Detection

## About the Project

This repository contains the research artifacts for the paper **“An Optimized Decision Tree-Based Framework for Explainable IoT Anomaly Detection.”**

The project presents a machine learning-based framework for detecting anomalous activities in Internet of Things (IoT) network traffic using an optimized Decision Tree approach. The framework also focuses on explainability, allowing the model's decisions to be analyzed and interpreted.

This repository includes the dataset, experimental Jupyter Notebook, and the published research paper associated with the project.

## Contributors

- Ashikuzzaman
- Md. Shawkat Hossain
- Jubayer Abdullah Joy
- Md Zahid Akon
- Dr. Md Manjur Ahmed
- Md. Naimul Islam

## Research Publication

The project is associated with the following research publication:

> **An Optimized Decision Tree-Based Framework for Explainable IoT Anomaly Detection**

**Authors:** Ashikuzzaman, Md Shawkat Hossain, Jubayer Abdullah Joy, Md Zahid Akon, Md Manjur Ahmed, Md Naimul Islam

**Conference:** 2025 IEEE 2nd International Conference on Computing, Applications and Systems (COMPAS)



**Publisher:** IEEE

**IEEE Xplore:**  
[https://ieeexplore.ieee.org/document/11502458](https://doi.org/10.1109/COMPAS67506.2025.11381766)

## Research Overview

The rapid growth of IoT devices has increased the attack surface of connected systems. IoT environments generate diverse and high-dimensional network traffic, making it challenging to detect malicious or abnormal activities accurately.

Traditional intrusion detection systems may provide a prediction without clearly explaining the reason behind that prediction. This project addresses this issue by combining anomaly detection with explainable machine learning.

The proposed framework is designed to:

- Detect anomalous IoT network traffic.
- Classify different traffic categories.
- Use an optimized Decision Tree-based model.
- Improve the interpretability of anomaly detection decisions.
- Identify important features associated with suspicious behavior.
- Support security analysis in resource-constrained IoT environments.

## Key Contributions

The main contributions of this research are:

1. An optimized Decision Tree-based framework for IoT anomaly detection.

2. A classification approach capable of distinguishing normal traffic from different attack categories.

3. An explainable machine learning workflow for analyzing model decisions.

4. Feature-level analysis to identify the characteristics that contribute to anomaly predictions.

5. An experimental evaluation using the WUSTL-EHMS-2020 IoT healthcare network traffic dataset.

6. A reproducible Jupyter Notebook containing the data preprocessing, model training, and evaluation workflow.

## Dataset

The project uses the **WUSTL-EHMS-2020** dataset, which contains network traffic collected from an IoT-enabled healthcare environment.

The dataset used in this repository includes attack-category labels for:

- Normal traffic
- Spoofing attacks
- Data Alteration attacks

The dataset file is:

```text
wustl-ehms-2020_with_attacks_categories.csv
```

The dataset contains **16,318 records** and **45 columns** before preprocessing. The features include network-flow information, packet statistics, traffic-load information, and healthcare-related sensor attributes.

Examples of available features include:

- Source and destination addresses
- Source and destination ports
- Source and destination bytes
- Source and destination load
- Packet statistics
- Packet loss and rate
- Source and destination MAC addresses
- Temperature
- SpO2
- Pulse rate
- Systolic and diastolic blood pressure
- Heart rate
- Respiration rate
- ST value
- Attack category

## Attack Categories

The dataset contains the following attack categories:

| Attack Category | Description |
|----------------|-------------|
| `normal` | Normal IoT network traffic |
| `Spoofing` | Traffic associated with spoofing behavior |
| `Data Alteration` | Traffic associated with data alteration behavior |

The observed class distribution in the dataset is:

| Category | Number of Samples |
|----------|------------------:|
| Normal | 14,272 |
| Spoofing | 1,124 |
| Data Alteration | 922 |

## Methodology

The experimental workflow follows the steps below:

```text
IoT Network Traffic Dataset
            │
            ▼
Data Loading and Inspection
            │
            ▼
Feature Cleaning
            │
            ▼
Categorical Feature Encoding
            │
            ▼
Target Label Encoding
            │
            ▼
Train-Test Data Preparation
            │
            ▼
Machine Learning Model Training
            │
            ▼
Performance Evaluation
            │
            ▼
Explainability Analysis
```

### Data Preprocessing

The preprocessing stage includes:

- Loading the CSV dataset using pandas.
- Inspecting the data structure and feature types.
- Removing unnecessary columns.
- Separating categorical and numerical features.
- Encoding categorical network features.
- Encoding attack-category labels.
- Preparing the dataset for machine learning experiments.

The notebook removes the following columns from the working dataset:

```text
Label
Dir
Flgs
```

The following categorical features are encoded:

```text
SrcAddr
DstAddr
Sport
SrcMac
DstMac
```

The attack category is encoded for model training using label encoding.

## Machine Learning Models

The notebook imports and supports multiple machine learning algorithms for experimentation, including:

- Decision Tree
- Random Forest
- K-Nearest Neighbors
- Multi-Layer Perceptron
- Support Vector Machine

The central focus of the published research is the optimized Decision Tree-based framework.

Decision Trees are useful for this research because their decision paths can be inspected and interpreted more easily than many black-box models.

## Explainable AI Analysis

Explainability is an important component of this project.

The purpose of the explainability analysis is to understand how the model reaches a particular prediction. This is especially important in IoT security, where analysts may need to verify why a traffic sample has been classified as anomalous.

The analysis can help answer questions such as:

- Which features contributed to an anomaly prediction?
- What traffic characteristics distinguish normal and malicious behavior?
- Which feature thresholds are used by the Decision Tree?
- How can the model's decision path be interpreted?
- Can the prediction be explained to a security analyst?

The explainable analysis improves the transparency and trustworthiness of the anomaly detection process.

## Repository Contents

```text
.
├── IoT Anomaly Detection.pdf
├── README.md
├── wustl-ehms-2020_with_attacks_categories.csv
└── wustl_data_iot_(2).ipynb
```

### File Descriptions

| File | Description |
|------|-------------|
| `IoT Anomaly Detection.pdf` | Published paper presented at IEEE COMPAS 2025. |
| `wustl-ehms-2020_with_attacks_categories.csv` | WUSTL-EHMS-2020 IoT network traffic dataset with attack categories. |
| `wustl_data_iot_(2).ipynb` | Jupyter Notebook containing preprocessing, model development, evaluation, and analysis. |
| `README.md` | Project documentation and reproducibility instructions. |

## Requirements

The notebook uses Python-based data science and machine learning libraries.

Recommended environment:

```text
Python 3.x
Jupyter Notebook
```

Required packages include:

```bash
pip install pandas numpy scikit-learn imbalanced-learn matplotlib seaborn jupyter
```

## Running the Notebook

### 1. Clone the Repository

```bash
git clone https://github.com/Ashikuzzaman026/IoT-XAI-Anomaly-Detection.git
cd IoT-XAI-Anomaly-Detection
```

### 2. Create a Virtual Environment

```bash
python -m venv iot-xai-env
```

For Linux or macOS:

```bash
source iot-xai-env/bin/activate
```

For Windows:

```bash
iot-xai-env\Scripts\activate
```

### 3. Install the Dependencies

```bash
pip install --upgrade pip
pip install pandas numpy scikit-learn imbalanced-learn matplotlib seaborn jupyter
```

### 4. Start Jupyter Notebook

```bash
jupyter notebook
```

### 5. Open the Notebook

Open the following file:

```text
wustl_data_iot_(2).ipynb
```

Run the notebook cells sequentially to reproduce the data loading, preprocessing, encoding, machine learning, and evaluation workflow.

## Experimental Evaluation

The model evaluation uses standard classification metrics, including:

- Accuracy
- Precision
- Recall
- F1-score
- Confusion matrix
- Classification report



## Research Paper and Project Relationship

The PDF included in this repository contains the published research paper. The Jupyter Notebook and dataset provide the computational materials related to the study.

The repository is intended to preserve and share:

- The research paper.
- The experimental dataset.
- The data preprocessing workflow.
- The machine learning implementation.
- The explainability-related analysis.
- The supporting research artifacts.

## Project Status

This repository contains the completed research materials associated with the published paper.

It is not a continuously running production service or real-time IoT monitoring platform. The implementation is provided as a notebook-based research artifact for experimentation, analysis, and reproducibility.

## Limitations

The current project has the following limitations:

- The experiments are based on a specific IoT healthcare dataset.
- The implementation is primarily notebook-based.
- The framework has not been packaged as a real-time deployment service.
- Performance may vary on other IoT datasets and network environments.
- Additional validation may be required before production use.
- The class distribution may influence model performance.

## Future Work

Possible future extensions include:

- Real-time IoT traffic monitoring.
- Deployment on edge and resource-constrained devices.
- Integration with live network traffic streams.
- Evaluation on additional IoT datasets.
- Comparison with deep learning and ensemble approaches.
- Improved explainability visualization.
- Automated alert generation for security analysts.
- Development of a web-based monitoring interface.

## Citation

If you use this project, dataset preparation, methodology, or research findings, please cite the associated publication included in this repository.

```bibtex
@inproceedings{Ashikuzzaman2025IoTAnomaly,
  author    = {Ashikuzzaman and
               Hossain, Md. Shawkat and
               Joy, Jubayer Abdullah and
               Akon, Md. Zahid and
               Ahmed, Md. Manjur and
               Islam, Md. Naimul},
  title     = {An Optimized Decision Tree-Based Framework for Explainable IoT Anomaly Detection},
  booktitle = {2025 IEEE 2nd International Conference on Computing, Applications and Systems (COMPAS)},
  pages     = {1--7},
  year      = {2025},
  publisher = {IEEE},
  doi       = {10.1109/COMPAS67506.2025.11381766}
}
```

## Acknowledgment

The authors acknowledge the use of the WUSTL-EHMS-2020 dataset for conducting the IoT anomaly detection experiments.

## License

No separate open-source license has been specified for this repository. Please contact the repository owner before redistributing or reusing the research materials.

