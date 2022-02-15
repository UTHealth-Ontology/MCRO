# Model Card Sample 2

## Model Card: Incorporating social network information to predict HIV status

### Model Details

* Developed by researchers at University of Texas Health Science Center at Houston, University of Chicago, and Jilin University
* Published 2019
* Graph Convolutional Network
* Detection of previously unknown HIV infections in the young MSM (Men who have Sex with Men) population (16-29) in Houston, Texas

### Intended Use

* Determine an individual’s HIV status using social network data
 
### Factors
* Individual features (sociodemographic characteristics, sexual behavioral characteristics, and biological data)
* Social Network characteristics (number of social venues attended, number of sexual partners, etc.)
* Graph Features (centrality, ratio of positive and negative HIV neighbors)

### Metrics
* Evaluation metrics include Accuracy and F1-Score (balance between Precision and Recall)
  
### Training Data and Evaluation Data
* With a population of 378 male individuals, 300 were used for the training split and 78 were used for the test split
 
### Ethical Considerations
* The MSM cohort used in this study is based in Houston, so the generalizability to other regions or cities in the United States would require additional data

### Caveats and Recommendations
* Small training sample size and sparse features can make model training difficult, especially given challenges in recruiting members of the MSM population for such studies
* Limited graph size also produced significant variation in model performance that showed little improvement of GCN over baseline models (like random forest and logistic regression), and models showed sensitivity to parameters
* Explore incorporation of more or new data to represent venue affiliation ties between nodes on the graph

*Evan Yu, School of Biomedical Informatics, University of Texas Health Science Center at Houston*