# Explainability-in-Hospital-Mortality-Prediction

Report on
‘Comparative analysis of explainable machine learning
prediction models for hospital mortality’
from
Eline Stenwig, Giampiero Salvi, Pierluigi Salvo Rossi and Nils Kristian Skjærvold
BMC Medical Research Methodology
Presented by Mjema Christina John
COSC 590B Graduate Seminar
2023W2
The University of British Columbia
Kelowna
August 20, 2024

This study addresses a classification task in ICU mortality prediction using logistic regression, random forests, ADA boost, and naive Bayes classifiers, trained and tested on the electronic ICU (eICU) dataset. In the replication of the study, the four machine learning algorithms are trained and tested on another ICU dataset, the MIMIC-III ICU dataset of patients with heart failure. An XGBoost classifier, not included in the original study, is introduced and achieves the highest AUC of 0.872 on the eICU dataset, with a calibration curve close to the line $y=x$. This model also demonstrates competitive class distinction abilities, achieving an AUC score of 0.83 on the MIMIC-III dataset, underscoring its robustness.

    While all models exhibit comparable AUC scores on both datasets, significant differences are observed in their calibration curves. Fine-tuning the XGBoost classifier on the MIMIC-III dataset results in a higher AUC score of 0.849. However, this adjustment leads to changes in calibration, evident in summary plots where features influence predictions towards mortality.
    
    Furthermore, examination of explainability using the SHAP tool reveals that models with similar AUC scores may employ distinct decision-making processes, potentially lacking alignment with established medical theory. For instance, logistic regression models indicate that temperatures higher than 36°C consistently correlate with higher chances of survival, a trend contrary to medical knowledge.
