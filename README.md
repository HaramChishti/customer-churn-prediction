##### ***Customer Churn Prediction System***

##### *Technical Documentation \& Deployment Manual for Churn Prediction*

&#x20;**1. Project Overview**

This directory houses the software artifacts and complete engineering pipeline for **Customer Churn Prediction**. This system develops a proactive machine learning architecture designed to analyze massive customer engagement parameters and identify high-risk subscription accounts before they initiate service cancellation.

&#x20;**2. Dataset Core Architecture**

The predictive models ingest a large-scale database designed to simulate enterprise transactional behavior patterns:

•	Source File Registry: 'customer\_churn\_dataset.csv' containing exactly **440,832** historical consumer tracking entries.

•	Target Vector (Y): Churn (Binary Classification: **1 = Customer has left the ecosystem**, **0 = Customer remains active**).

•	Predictive Features (X): Demographics (Age, Gender) and Operational activity logs (Tenure, Usage Frequency, Support Calls, Payment Delay, and Contract Type).

&#x20;**3. Critical Data Engineering Interventions**

To guarantee statistical validation and protect the pipelines from systematic bias, the codebase executes two critical optimization transformations:

•	***Stratified Train-Test Split:*** Initial random splitting scripts suffered from an acute class imbalance bias that artificially locked baseline metric accuracy at a capped limit of 57.12%. This was corrected by integrating a Stratified Shuffle Split, maintaining identical minority-to-majority ratio distributions across both training and testing shards.

•	***Standard Feature Vector Scaling:*** Features with extensive numeric bounds (such as multi-month Tenure intervals) naturally skew spatial evaluation models. A StandardScaler normalization mapping was deployed to transform all continuous numerical distributions to a standardized scale (Mean = 0, Variance = 1).

 

&#x20;

**4. System Requirements \& Environment Setup**

The source architecture runs on top of Python 3.8+ execution stacks. To configure the local sandbox workspace with all necessary technical tracking libraries, run the compilation instruction below:

\# Shell installation terminal command:

pip install numpy pandas scikit-learn matplotlib seaborn



\# To verify accurate installation paths within your workspace script:

python -c "import sklearn; print('Scikit-Learn version installed:', sklearn.\_\_version\_\_)"



&#x20;**5. Benchmarked Model Performances**

The evaluation pipeline measures a linear base framework against a localized non-linear neighbor architecture:

•	**Logistic Regression**: Secured a dependable baseline accuracy rating of **89.33%.** However, the model remained structurally capped due to its linear plane limitations, which are unable to register complex, non-linear human churn patterns.

•	**k-Nearest Neighbour-KNN**: Configured via specialized parameter sweeps setting **n\_neighbors=25** with distance-based voting weights. This system successfully isolated dense active cohorts, generating an elite operational accuracy rating of **94.99%** and registering only 6 misclassifications out of tens of thousands of validation records.

&#x20;**6. Step-by-Step Execution Protocol**

Follow this exact operational matrix within your runtime environment to execute and test the prediction system:

Step 1: Ensure 'customer\_churn\_dataset.csv' is saved directly inside the folder root.

Step 2: Initialize Jupyter Notebook, Google Colab, or VS Code terminal tools.

Step 3: Open the analytical notebook file 'Project1\_Churn\_Prediction.ipynb'.

Step 4: Execute all structural code blocks sequentially (Shift + Enter).

Step 5: Review console summaries, generated evaluation tables, and final Confusion Matrices.




