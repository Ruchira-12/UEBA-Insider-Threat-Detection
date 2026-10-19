UEBA — User and Entity Behavior Analytics for Insider Threat Detection

Project status: Work in progress.

Overview
This project explores using anomaly detection to identify user activities that differ from expected behavior. The aim is to help surface activity that may warrant further investigation; an anomaly is not, by itself, proof of malicious behavior.

Problem
Traditional rule-based monitoring can miss unusual behavior that does not match a predefined rule. UEBA-style analysis looks at activity patterns and flags outliers for review.

Current project direction
The project is intended to analyze activity such as:
- Login and logon patterns
- Device usage
- File-access behavior
  
Tech stack
- Python
- Pandas and NumPy for data preparation
- scikit-learn Isolation Forest for unsupervised anomaly detection
- Matplotlib for visualizations
- Streamlit for the user interface
  
How Isolation Forest fits
Isolation Forest builds randomized trees that isolate observations. Points that are isolated in fewer splits tend to receive more anomalous scores. The contamination setting influences the expected proportion of outliers; it should be selected and validated against the data rather than treated as a guaranteed attack rate.

Planned Workflow
1. Load the activity dataset.
2. Validate columns, types, timestamps, missing values, and duplicate records.
3. Prepare numeric or encoded features for the model.
4. Fit Isolation Forest and generate anomaly scores or labels.
5. Review flagged records and visualize results.

Current Implementation
The project is currently under development. The implementation status of data preprocessing, Isolation Forest model training, anomaly scoring, and Streamlit visualization is being refined.

Features will be documented as they are implemented and tested.
Roadmap
- Document the dataset and feature schema.
- Add reproducible setup instructions.
- Record the rationale for model parameters.
- Add example outputs and explain false positives.
- Add tests for preprocessing and prediction code.

Security and privacy
Do not commit real user logs, personal data, API keys, credentials, or sensitive incident records. Use synthetic or appropriately anonymized data.
