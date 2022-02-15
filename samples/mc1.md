# Model Card Sample 1

## Model Card – Adverse endpoints prediction for patients undergoing PCI 

### Model details
* Developed by researchers at University of Texas Health Science Center at Houston
* Recurrent neural networks (RNN)
* Binary classification for adverse endpoints after coronary artery stent implantation 

### Intended Use
* Intended to be used for disease risk prediction and treatment optimization using longitudinal sequence data, e.g., electronic health records (EHRs)

### Factors  
* The potentially relevant factors include age, gender, history (e.g., prior bleeding, prior myocardial infarction), comorbidities and risk factors (diabetes mellites, smoking, congestive heart failure), as well as comedications (e.g., statins, beta-blockers)

### Metrics
* Evaluation metrics include the area under the receiver operating characteristic curve (AUC) and Precision-Recall Curve (PRC)

### Training and Validation Data
* Cerner, training and validation data split (70% and 10% respectively, out of the total selected cohort) 

### Evaluation Data
* Cerner, test data split (20% out of the total selected cohort) 

### Ethical Considerations
* Since the Cerner cohort is from the US hospitals, the generalizability to other countries or regions might need more data to validate.

### Caveats and Recommendations
* Imbalance distribution of case and control is common in the real-world data, which might bring negative impacts for prediction performance. Could apply some data sampling strategies to make the data more balanced 
* Data incompleteness and missingness are also evident in EHRs data, which might cause serious prediction bias particularly when important information is missing. Try to select the higher quality dataset and multimodality data to make an well-informed prediction. 

*Fang Li, School of Biomedical Informatics, University of Texas Health Science Center at Houston*