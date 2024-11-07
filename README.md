# Online retail clustering using Machine Learning
#### Video Demo:  <URL HERE>
#### Description: 
This project, **Online Retail Clustering Using Machine Learning**, implements customer segmentation through an RFM-based KMeans clustering model. Inspired by the research paper, "Data mining for the online retail industry: A case study of RFM model-based customer segmentation using data mining," this project demonstrates the application of clustering techniques to a dataset of customer transactions, creating insights for targeted marketing strategies.

The goal is to segment customers based on their behavior, focusing on Recency, Frequency, and Monetary (RFM) metrics—a widely used approach for identifying different types of customers in the retail industry. By clustering customers into distinct groups, businesses can better understand their audience, leading to data-driven decisions in marketing, sales, and customer relationship management.

###### Project Structure
The project consists of several key files and folders:

1. **data_clustering.ipynb:**

- This Jupyter notebook serves as the core of the project, where all steps for data preparation, feature engineering, model development, and analysis are conducted.
- Steps in the notebook include:
Data Importation: Loading the customer dataset into the environment.
- Exploratory Data Analysis (EDA): Visualizing and summarizing data to uncover patterns and trends in customer behaviors.
- Data Cleaning: Addressing missing values, handling outliers, and standardizing variables.
- Feature Engineering: Calculating RFM scores by measuring:
  - Recency (how recently a customer made a purchase)
  - Frequency (how often they made purchases)
  - Monetary Value (total spending amount)
- Model Training: Using the KMeans algorithm to create customer clusters. The elbow method and silhouette scores guide the selection of an optimal cluster count.
- Results Analysis: Identifying and interpreting each customer segment based on clustering results, providing insights into customer behavior patterns.
2. **data:**

- This folder contains the dataset used in the project. The dataset includes transactional data, which is essential for calculating the RFM metrics that serve as input features to the model.
3. **requirements.txt:**

- A file listing all Python libraries required to run this project, such as pandas, numpy, matplotlib, scikit-learn, and seaborn. This file ensures that any user can set up the necessary environment by installing the required dependencies.
4. **data_mining_paper:**

This folder contains a PDF copy of the research paper, which serves as the basis for this project. The paper outlines the theoretical foundation for RFM-based clustering in the retail industry. It provides context and validates the model implementation choices, ensuring the project aligns with industry-standard techniques in data mining and customer segmentation.
5. **README.md:**

- This README file provides a detailed description of the project, including its purpose, structure, and the steps required to run the project. It also elaborates on design choices and discusses the theoretical basis of RFM segmentation as derived from the research paper.
###### Design Choices and Justifications
**Data Cleaning and Preprocessing**
Given the transactional nature of customer data, it was essential to ensure data quality by handling missing values and outliers. Outliers, particularly in monetary values, could distort the clustering results, so we either capped or transformed extreme values to reduce skewness.

**Feature Engineering**
The RFM model was chosen as it is an industry-proven metric for customer segmentation. By calculating recency, frequency, and monetary values, the clustering algorithm receives input that captures the diversity of customer behavior. Each RFM feature was scaled to prevent larger values from disproportionately influencing the KMeans algorithm.

**Model Selection and Optimization**
The KMeans clustering algorithm was selected for its simplicity and interpretability. It allowed us to define specific numbers of clusters, making it easier to identify customer segments as distinct groups. Several potential values for k were tested, with the elbow method and silhouette score guiding the optimal choice.

**Implementation of Research Paper**
By following the methods outlined in the reference paper, we created a reproducible model aligned with best practices in customer segmentation for retail. The research paper's approach validated our design choices, from feature selection to the clustering technique, ensuring the implementation was not only theoretically sound but also applicable to real-world retail data.

**Running the Project**
To run this project locally, follow these steps:

1. Clone the repository and navigate to the project directory.
2. Install dependencies by running:
"pip install -r requirements.txt"
3. Open the Jupyter Notebook data_clustering.ipynb and execute each cell sequentially to load the data, perform EDA, preprocess the data, engineer features, and train the model.
This will produce visualizations of the clusters and customer segments, providing insights based on the RFM metrics.

**Conclusion**
This project successfully demonstrates the implementation of an RFM-based clustering model for customer segmentation. By utilizing unsupervised machine learning techniques on transactional data, we’ve provided a foundation for businesses to better understand their customers and tailor marketing strategies accordingly. The project validates the theoretical foundation laid out in the research paper and showcases a practical approach to customer clustering in the retail domain.