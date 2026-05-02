# Credit Card Fraud Detection using K-Means Clustering
 ### Project Description

This project focuses on detecting fraudulent credit card transactions using unsupervised machine learning techniques. Since fraud cases are extremely rare, the problem is approached as an anomaly detection task rather than a traditional classification problem.

The model uses K-Means clustering to group similar transactions and identifies anomalies based on their distance from cluster centroids.

### Objective
Apply clustering to group transactions
Detect anomalies (potential fraud)
Compare predicted anomalies with actual fraud labels
Evaluate performance using appropriate metrics
### Dataset
Source: Kaggle – Credit Card Fraud Detection Dataset
Total Records: 284,807 transactions
Fraud Cases: 492 (~0.17%)
### Features:
Time – Time elapsed between transactions
Amount – Transaction amount
V1–V28 – Transformed features using Principal Component Analysis
Class – Target variable (0 = Normal, 1 = Fraud)
### Project Workflow
### Data Understanding
Checked dataset shape and structure
Verified no missing values
Analyzed class imbalance
### Data Preprocessing
Applied Standard Scaling to Time and Amount
Removed Class column during clustering
### Clustering (K-Means)
Used Elbow Method to determine optimal clusters
Selected K = 2
Trained K-Means model
### Anomaly Detection
Calculated distance of each point from cluster centroid
Selected top 1% farthest points as anomalies
### Evaluation
Compared predicted anomalies with actual labels
Metrics used:
Confusion Matrix
Precision
Recall
### Visualization
Applied PCA for dimensionality reduction
Visualized:
Clusters
Anomalies vs Normal transactions
### Results & Insights
Dataset is highly imbalanced
K-Means successfully groups transactions into patterns
Distance-based method identifies unusual transactions
Model achieves reasonable recall for fraud detection
### Limitations
K-Means assumes spherical clusters
Sensitive to scaling and outliers
Not ideal for complex anomaly detection
### Future Improvements
Use advanced models:
Isolation Forest
DBSCAN
Autoencoders
Tune anomaly threshold
Feature engineering
### Tech Stack
Python
Pandas
NumPy
Scikit-learn
Matplotlib / Seaborn
### Project Structure
credit-card-fraud-detection/
│
├── data/
│   └── creditcard.csv
│
├── notebooks/
│   └── fraud_detection.ipynb
│
├── src/
│   └── clustering_model.py
│
├── outputs/
│   ├── plots/
│   └── results/
│
├── requirements.txt
└── README.md
### Conclusion

This project demonstrates how unsupervised learning can be applied to detect anomalies in highly imbalanced datasets. While K-Means provides a simple baseline approach, combining clustering with distance-based methods helps identify potential fraud cases effectively.

### Video Presentation


### Contribution

Feel free to fork this repository and improve the model using advanced anomaly detection techniques.
