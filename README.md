# Tutorial_Vidoes_on_Drugs_Discovery_using_Machine_Learning_with-Festus
This repo contains series of Drugs Discovery using Machine Learning with Festus. I will update it with codes used in each tutorials.

## COMPLETE VIDEO SERIES: MACHINE LEARNING FOR DRUG DISCOVERY

### Total Videos: 55

---

## MODULE 0: SETUP AND INTRODUCTION (Videos 0-5)

| Video | Title | Description |
|-------|-------|-------------|
| **Video 0** | Setup Guide - Installing RDKit, Python, and Required Libraries | Installing Anaconda, Jupyter Notebook, RDKit, pandas, scikit-learn, matplotlib. Testing installation with first molecule. |

---

## MODULE 1: MOLECULAR BASICS (Videos 1-3)

| Video | Title | Description |
|-------|-------|-------------|
| **Video 1** | Your First Molecule in Python - SMILES to Structure | Introduction to SMILES strings. Converting SMILES to molecular structures using RDKit. Visualizing aspirin and ethanol. |
| **Video 2** | Drawing Multiple Drugs - Visualizing Molecular Libraries | Creating grids of multiple drug molecules. Comparing structures of aspirin, ibuprofen, caffeine, paracetamol. |
| **Video 3** | Molecular Properties - Introduction to Descriptors | Calculating molecular weight, LogP, TPSA. Understanding what these properties mean for drug-likeness. |

---

## MODULE 2: LIPINSKI RULE OF FIVE (Videos 4a-4g)

| Video | Title | Description |
|-------|-------|-------------|
| **Video 4a** | Introduction to Lipinski's Rule of Five in Python | Overview of Lipinski's rules: MW < 500, LogP < 5, HBD < 5, HBA < 10. Accessing RDKit's Lipinski module. |
| **Video 4b** | Hydrogen Bond Donors - First Lipinski Rule | Calculating HBD for aspirin, caffeine, ibuprofen. Understanding what constitutes a hydrogen bond donor. |
| **Video 4c** | Hydrogen Bond Acceptors - Second Lipinski Rule | Calculating HBA for multiple drugs. Identifying oxygen and nitrogen acceptors. |
| **Video 4d** | LogP - Third Lipinski Rule | Calculating lipophilicity. Interpreting LogP values for drug absorption. |
| **Video 4e** | Molecular Weight - Fourth Lipinski Rule | Calculating molecular weight. Why heavy molecules struggle to cross membranes. |
| **Video 4f** | Topological Polar Surface Area (TPSA) | Calculating TPSA. Relationship between TPSA and cell permeability. |
| **Video 4g** | Complete Lipinski Analysis | Combining all five properties. Creating a pass/fail table for drug-likeness. |

---

## MODULE 3: MOLECULAR FINGERPRINTS (Videos 5-5g)

| Video | Title | Description |
|-------|-------|-------------|
| **Video 5** | Molecular Fingerprints - Converting Molecules to Numbers | Introduction to Morgan fingerprints. Converting aspirin to 1024-bit fingerprint. Understanding bit strings. |
| **Video 5b** | Understanding Fingerprint Bits | What the 1's and 0's represent. Comparing fingerprints of similar and different molecules. Tanimoto similarity. |
| **Video 5c** | Fingerprint Bits as Features | Creating feature matrices. Multiple molecules as rows, fingerprint bits as columns. |
| **Video 5d** | Interpreting Fingerprint Bits - What Do The 1's Mean? | Detailed explanation of bit positions. Why certain bits are 1 for specific molecules. |
| **Video 5e** | What Substructure Does Each Bit Represent? | Mapping bits back to molecular fragments. Understanding atom environments. |
| **Video 5f** | Visualizing Fingerprint Bit Environments | Highlighting atoms that contribute to specific bits. Visual representation of bit activation. |
| **Video 5g** | Comparing Fingerprints of Different Molecules | Side-by-side comparison of aspirin and ibuprofen fingerprints. Common and unique bits. |

---

## MODULE 4: QSAR FUNDAMENTALS AND DATA ACQUISITION (Videos 6-12)

| Video | Title | Description |
|-------|-------|-------------|
| **Video 6** | What is QSAR? Introduction to Quantitative Structure-Activity Relationships | Definition and history. Basic principle: structure determines activity. Simple MW vs activity demonstration. |
| **Video 7** | Types of Bioactivity Data in Drug Discovery | IC50, pIC50, active/inactive. Converting IC50 to pIC50. Why pIC50 is better for modeling. |
| **Video 8** | Introduction to ChEMBL Database | Overview of ChEMBL. Data types: compounds, targets, assays. Web interface vs API. |
| **Video 9** | Searching ChEMBL by Target Protein (COX-2 Example) | Finding human COX-2 target ID. Understanding confidence scores and assay types. |
| **Video 10** | Downloading ChEMBL Data for COX-2 | Using ChEMBL API. Fetching bioactivity records. Saving raw data to CSV. |
| **Video 11** | Filtering and Cleaning ChEMBL Data | Removing invalid SMILES. Handling duplicates. Keeping only IC50 values in nM. |
| **Video 12** | Defining Active and Inactive Classes | Setting activity threshold (pIC50 > 6 = active). Creating binary classification labels. |

---

## MODULE 5: EXPLORATORY DATA ANALYSIS (Videos 13-17a5)

| Video | Title | Description |
|-------|-------|-------------|
| **Video 13** | Loading Saved ChEMBL Data and Initial Exploration | Loading CSV. Displaying dataframe. Basic statistics. Missing value check. |
| **Video 14** | Filtering and Cleaning ChEMBL Data | Step-by-step filtering. Removing low confidence records. Handling duplicates with median aggregation. |
| **Video 15** | Adding pIC50 Values | Converting IC50 to pIC50. Distribution analysis. Histograms comparing IC50 and pIC50. |
| **Video 16** | Defining Activity Classes for Classification | Creating active/inactive labels. Class balance analysis. Bar charts and pie charts. |
| **Video 17** | Generating Fingerprints for All Molecules | Batch fingerprint generation. Progress tracking. Saving fingerprint matrix. |
| **Video 17a1** | EDA - Understanding Our COX-2 Dataset | Dataset dimensions. Data types. Summary statistics. Memory usage. |
| **Video 17a2** | EDA - Distribution of pIC50 Values | Histograms. Box plots. Normality testing. Outlier detection. |
| **Video 17a3** | EDA - Active vs Inactive Class Balance | Class counts. Percentage distributions. Stratification verification. |
| **Video 17a4** | EDA - Correlation Between Features | Correlation matrix. Highly correlated bit pairs. VIF analysis. PCA preview. |
| **Video 17a5** | EDA - Relationship Between Features and Target | Bit frequency in active vs inactive. Statistical significance tests. Mutual information. Box plots for top bits. |

---

## MODULE 6: MACHINE LEARNING FUNDAMENTALS (Videos 17b-18)

| Video | Title | Description |
|-------|-------|-------------|
| **Video 17b** | Introduction to Machine Learning for Drug Discovery, Bioactivity Prediction and QSAR | Overview of ML in drug discovery. Regression vs classification. What we'll build. |
| **Video 18** | Splitting Data for Machine Learning | Train-test split (80/20). Stratification. Saving split indices. Reproducibility. |

---

## MODULE 7: RANDOM FOREST MODELS (Videos 19a-19e)

| Video | Title | Description |
|-------|-------|-------------|
| **Video 19a** | Training a Random Forest Regressor | Building first regression model. 100 trees, max_depth=10. Predicting pIC50. Saving model. |
| **Video 19b** | Training a Random Forest Classifier | Building first classification model. Probability outputs. Predicting active/inactive. |
| **Video 19c** | Feature Engineering - Adding Molecular Descriptors to Fingerprints | Calculating 10 key descriptors. Combining with fingerprints. Comparing performance improvement. |
| **Video 19c3** | Regression Model Comparison - Benchmarking 5 Algorithms | Linear Regression, Random Forest, XGBoost, SVR, KNN. Cross-validation comparison. R² and MAE. |
| **Video 19c4** | Classification Model Comparison - Benchmarking 5 Algorithms | Logistic Regression, Random Forest, XGBoost, SVM, KNN. AUC, accuracy, F1 comparison. |
| **Video 19d** | Random Forest Classifier - Model Evaluation - Confusion Matrix | True/False positives/negatives. Precision, recall, F1. Drug discovery cost implications. |
| **Video 19e** | Random Forest Classifier - Model Evaluation - ROC Curve and AUC | ROC curves. AUC interpretation. Threshold selection for drug discovery. |

---

## MODULE 8: ADVANCED MODELING AND VALIDATION (Videos 20-23)

| Video | Title | Description |
|-------|-------|-------------|
| **Video 20** | Feature Importance Analysis for Random Forest Regressor and Classifier | Top features from both models. LogP as most important. Fingerprint bit interpretation. |
| **Video 21** | Cross-Validation for Robust Evaluation | 5-fold cross-validation. Stability analysis. Confidence intervals for performance. |
| **Video 22** | Hyperparameter Tuning for XGBoost Regressor and Classifier | Grid search for optimal parameters. Learning rate, max_depth, n_estimators. Performance improvement. |
| **Video 23** | External Validation - Testing on Completely New Data | Held-out test set never used before. Comparing CV estimates with external performance. Generalization assessment. |

---

## MODULE 9: PRACTICAL APPLICATION (Videos 24-25)

| Video | Title | Description |
|-------|-------|-------------|
| **Video 24** | Virtual Screening - Predicting New Molecules | Screening novel compounds. Converting SMILES to features. Priority ranking based on potency and confidence. Exporting results for medicinal chemists. |
| **Video 25** | Complete QSAR Workflow Summary and Next Steps | Recap of entire workflow. Key findings. Performance summary. Next steps: deep learning, GNNs, ADMET. |

---

## MODULE 10: COURSE COMPLETION (Video 26)

| Video | Title | Description |
|-------|-------|-------------|
| **Video 26** | Course Wrap-Up and Career Pathways in Computational Drug Discovery | Skill assessment. Career pathways. Learning roadmap. Certifications. Conferences. Portfolio building. Final certificate. |

---

## SERIES SUMMARY

| Module | Topic | Number of Videos |
|--------|-------|------------------|
| 0 | Setup and Introduction | 1 |
| 1 | Molecular Basics | 3 |
| 2 | Lipinski Rule of Five | 7 |
| 3 | Molecular Fingerprints | 7 |
| 4 | QSAR Fundamentals and Data Acquisition | 7 |
| 5 | Exploratory Data Analysis | 8 |
| 6 | Machine Learning Fundamentals | 2 |
| 7 | Random Forest Models | 7 |
| 8 | Advanced Modeling and Validation | 4 |
| 9 | Practical Application | 2 |
| 10 | Course Completion | 1 |
| **TOTAL** | | **55 Videos** |
