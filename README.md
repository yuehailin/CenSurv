# CenSurv
## Bipartite Patient-Modality Graph Learning with Event-Conditional Modelling of Censoring for Cancer Survival Prediction
Accurately predicting the survival of cancer patients is crucial for personalized treatment. However, existing studies focus solely on the relationships between samples with known survival risks, ignoring the value of censored samples, which is inevitable in clinical practice. Furthermore, these studies may suffer performance degradation in modality-missing scenarios and even struggle during the inference process. In this study, we propose a bipartite patient-modality graph learning with event-conditional modelling of censoring for cancer survival prediction (CenSurv). Specifically, we first use graph structure to model multimodal data and obtain representation. Then, to alleviate performance degradation in modality-missing scenarios, we design a bipartite graph to simulate the patient-modality relationship in various modality-missing scenarios and leverage a complete-incomplete alignment strategy to explore modality-agnostic features. Finally, we design a plug-and-play event-conditional modeling of censoring (ECMC) that selects reliable censored data using dynamic momentum accumulation confidences, assigns more accurate survival times to these censored data, and incorporates them as uncensored data into training. Comprehensive evaluations on 5 publicly cancer datasets showcase the superiority of CenSurv over the best state-of-the-art by 3.1% in terms of the mean C-index, while also exhibiting excellent robustness under various modality-missing scenarios. In addition, using the plug-and-play ECMC module, the mean C-index of 8 baselines increased by 1.3% across 5 datasets.

![image](https://github.com/user-attachments/assets/d021d1a1-493c-411e-b918-d4ff1d8cc98e)

## 1. Data Acquisition
Pathological slide and clinical records are available at https://portal.gdc.cancer.gov/. Genomic profile is available at https://www.cbioportal.org/.
The extracted features of the clinical records, pathology and genetic will be uploaded as soon as possible.

## 2. Data Partitioning
In the 5-fold cross validation folder, we provide the details of data splitting for each disease.

## 3. Train
```
train-for-graph.py
```

## Acknowledge
This project is based on [HGCN](https://github.com/lin-lcx/HGCN) and [MUSE+](https://github.com/zzachw/MUSE). We have great thanks for these awesome projects.



