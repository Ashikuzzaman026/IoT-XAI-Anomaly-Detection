# An Optimized Decision Tree-Based Framework for Explainable IoT Anomaly Detection

## About the Project

This repository contains the research artifacts for an explainable machine learning framework designed to detect anomalies in Internet of Things (IoT) network traffic.

The project investigates how an optimized Decision Tree-based machine learning approach can be used for IoT anomaly detection while maintaining model interpretability. In addition to classifying normal and anomalous traffic, the framework provides feature-level explanations that help identify the characteristics responsible for each prediction.

Unlike a conventional software application or continuously running detection service, this repository represents a completed research project. It includes the dataset, experiment notebook, and the published research paper associated with the proposed framework.

## Research Objectives

The primary objectives of this project are:

- To detect anomalous behavior in IoT network traffic.
- To develop an optimized Decision Tree-based classification framework.
- To evaluate the model using a publicly available IoT healthcare dataset.
- To identify the most influential traffic features for anomaly classification.
- To improve the interpretability of machine learning-based IoT security systems.
- To provide human-understandable explanations for model predictions.

## Key Contributions

The project focuses on the following contributions:

1. **Optimized Decision Tree-Based Detection**

   A Decision Tree-based classification approach is developed and optimized for detecting anomalies in IoT network traffic.

2. **Explainable IoT Security Analytics**

   The framework emphasizes interpretability so that the reasons behind individual predictions can be inspected and analyzed.

3. **Feature-Level Analysis**

   Important network traffic characteristics are examined to understand their contribution to anomaly detection.

4. **Research-Based Evaluation**

   The proposed approach is evaluated using the WUSTL-EHMS-2020 dataset with attack-category information.

5. **Reproducible Experimental Notebook**

   The complete experimental workflow is provided through a Jupyter Notebook, including data loading, preprocessing, model training, evaluation, and explainability analysis.

## Dataset

The experiments use the **WUSTL-EHMS-2020** dataset, which contains network traffic collected from an IoT-enabled healthcare environment.

The dataset used in this repository includes attack-category information and is provided in CSV format:

```text
wustl-ehms-2020_with_attacks_categories.csv
```

The dataset contains network traffic observations associated with normal and anomalous activities. It is used to train and evaluate the proposed anomaly detection model.

> Please refer to the original dataset documentation and the accompanying research paper for details about data collection, feature definitions, and attack categories.

## Methodology

The overall experimental workflow follows the steps below:

```text
Dataset
   │
   ▼
Data preprocessing
   │
   ▼
Feature preparation
   │
   ▼
Train-test data splitting
   │
   ▼
Optimized Decision Tree training
   │
   ▼
Anomaly classification
   │
   ▼
Performance evaluation
   │
   ▼
Explainable AI analysis
```

### 1. Data Preparation

The dataset is loaded and prepared for machine learning. The preprocessing stage includes:

- Loading the IoT network traffic data.
- Inspecting the dataset structure.
- Handling the target label.
- Preparing input features.
- Separating normal and anomalous samples.
- Splitting the data into training and testing subsets.

### 2. Model Training

A Decision Tree-based classifier is trained using the processed IoT network traffic features.

Decision Trees are particularly suitable for this research because their decision paths can be inspected directly. This makes it possible to understand how different feature conditions contribute to the final classification decision.

### 3. Model Evaluation

The trained model is evaluated using standard classification metrics, including:

- Accuracy
- Precision
- Recall
- F1-score
- Confusion matrix
- Classification report

The exact experimental results are reported in the published paper included in this repository.

### 4. Explainable AI Analysis

The project includes explainability analysis to investigate why the model classifies a particular traffic sample as normal or anomalous.

The explainability component is used to:

- Identify important features.
- Analyze feature influence on predictions.
- Understand model decision patterns.
- Provide human-readable interpretations of anomaly classifications.
- Support security analysts in investigating suspicious IoT traffic.

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
| `IoT Anomaly Detection.pdf` | Published research paper describing the proposed IoT anomaly detection framework. |
| `wustl-ehms-2020_with_attacks_categories.csv` | IoT network traffic dataset with attack-category labels. |
| `wustl_data_iot_(2).ipynb` | Jupyter Notebook containing data processing, model development, evaluation, and explainability analysis. |
| `README.md` | Project documentation and reproducibility guide. |

## Running the Experiments

This repository is organized as a notebook-based research project.

### Requirements

The experiments can be reproduced using Python and the following commonly used libraries:

```text
Python 3.x
Jupyter Notebook
pandas
numpy
scikit-learn
matplotlib
seaborn
```

Additional libraries may be required depending on the explainability methods used in the notebook.

### Installation

Create and activate a Python environment:

```bash
python -m venv iot-xai-env
source iot-xai-env/bin/activate
```

For Windows:

```bash
iot-xai-env\Scripts\activate
```

Install the required packages:

```bash
pip install numpy pandas scikit-learn matplotlib seaborn jupyter
```

Start Jupyter Notebook:

```bash
jupyter notebook
```

Then open:

```text
wustl_data_iot_(2).ipynb
```

Run the notebook cells sequentially to reproduce the preprocessing, training, evaluation, and explainability workflow.

## Research Paper

The complete research paper is available in this repository:

```text
IoT Anomaly Detection.pdf
```

The paper provides detailed information about:

- The research motivation.
- IoT anomaly detection challenges.
- Dataset characteristics.
- Proposed machine learning framework.
- Model optimization process.
- Experimental setup.
- Evaluation results.
- Explainable AI analysis.
- Research findings and limitations.

## Results

The experimental results and visualizations generated during the research process are available in the Jupyter Notebook and are discussed in detail in the published paper.

The results should be interpreted together with the paper because the paper provides the complete experimental context, including:

- Dataset preparation.
- Evaluation protocol.
- Model configuration.
- Performance measurements.
- Explainability findings.
- Comparison with relevant approaches.

## Explainability and Interpretability

A major focus of this project is not only detecting anomalies but also understanding the model's decisions.

For an IoT security system, a prediction without an explanation may be difficult to validate or trust. Therefore, the proposed framework analyzes the relationship between the input network features and the model output.

The explainability analysis helps answer questions such as:

- Which features contributed most to an anomaly prediction?
- What feature values are associated with suspicious behavior?
- How does the Decision Tree separate normal and anomalous traffic?
- Can security analysts interpret the model's classification logic?
- Which traffic characteristics should be investigated further?

## Scope of the Repository

This repository is intended for:

- Academic research.
- IoT cybersecurity experiments.
- Explainable machine learning studies.
- Reproducibility of the published work.
- Educational use of IoT anomaly detection techniques.
- Further development of interpretable intrusion detection systems.

The repository is not intended to represent a production-ready, continuously running IoT monitoring service. The provided notebook represents the experimental implementation used for the research study.

## Limitations

The current repository has the following limitations:

- The implementation is provided primarily as a research notebook.
- The framework is evaluated using a specific IoT healthcare dataset.
- Performance may vary on other IoT environments or network configurations.
- The notebook-based workflow does not provide a real-time deployment interface.
- Further validation may be required before applying the model in operational security environments.
- Dataset quality and label distribution may affect the final model performance.

## Reproducibility

To reproduce the experiments:

1. Clone or download this repository.
2. Install the required Python dependencies.
3. Keep the dataset file in the repository directory.
4. Open `wustl_data_iot_(2).ipynb`.
5. Run the notebook cells in sequence.
6. Review the generated metrics, visualizations, and explainability outputs.
7. Compare the reproduced results with the results reported in the research paper.

## Citation

If you use this repository, dataset preparation, methodology, or research findings in your work, please cite the associated publication available in:

```text
IoT Anomaly Detection.pdf
```

A complete BibTeX citation can be added here based on the final publication information:

```bibtex
@article{
  iot_xai_anomaly_detection,
  title     = {An Optimized Decision Tree-Based Framework for Explainable IoT Anomaly Detection},
  author    = {Author Names},
  journal   = {Journal or Conference Name},
  year      = {Publication Year}
}
```

## Acknowledgment

This work is based on the WUSTL-EHMS-2020 IoT network traffic dataset and builds upon research in IoT security, machine learning-based anomaly detection, and explainable artificial intelligence.

## License

No separate open-source license has been specified for this repository yet. Please contact the repository owner before redistributing the code, dataset, or research materials.

## Author

**Ashikuzzaman026**

GitHub: [Ashikuzzaman026](https://github.com/Ashikuzzaman026)
