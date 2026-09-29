# Employee Retention Analysis: Predicting Staff Turnover

I built an automated workforce analytics framework to model the core operational and systemic drivers behind voluntary employee attrition across an enterprise database of 14,999 records.

### Model Evaluation & Selection Logic
The predictive architecture was evaluated across linear baselines and non-linear ensemble pipelines. While simple Logistic Regression struggled to map complex, non-linear human behavioral boundaries (like sudden burnout spikes when an employee crosses a specific project or hourly ceiling), tree-based models handled the data thresholds with absolute precision.

Here is how the final test set metrics came out:
* **Logistic Regression Baseline:** 83.0% Accuracy | 80.0% Precision | 83.0% Recall | 80.0% F1-Score
* **Decision Tree (Tuned via Grid Search):** 97.2% Accuracy | 91.5% Precision | 91.7% Recall | 91.6% F1-Score
* **Random Forest Classifier (Champion Model):** **98.1% Accuracy | 96.4% Precision | 92.0% Recall | 94.1% F1-Score**

**Engineering Analysis:** The **Random Forest Classifier** was selected as our final operational champion, delivering a top-tier **98.1% classification accuracy** and a robust **92.0% Recall score** on unseen test data. For workforce retention tracking, prioritizing Recall is crucial to guarantee that HR teams actively flag 92% of high-risk, burning-out talent before they voluntarily resign.

### Core Discoveries & Actions for Organizational Leadership
* **Implement Automated Project Caps:** Attrition in this dataset is heavily driven by system over-saturation rather than generic dissatisfaction. 100% of employees assigned to 5-7 concurrent tasks or working over **200+ monthly working hours** show critical burnout risks. Management should implement system guardrails restricting engineering allocations to an optimal ceiling of **3 to 4 concurrent projects** per person.
* **Address the 4-Year Career Bottleneck:** A distinct voluntary tenure drop-off occurs right at the **4-year mark**, driven by promotion stagnation or lack of progression. Human Resource business partners should launch structured milestone progression reviews and role-rotation gates precisely at the 3-year and 4-year anniversaries to mitigate veteran turnover.

### Environment & Reproducibility Requirements
* **Data Processing:** `numpy`, `pandas`
* **Plotting & Visuals:** `matplotlib`, `seaborn`
* **Modeling Infrastructure:** `scikit-learn` (DecisionTreeClassifier, RandomForestClassifier, GridSearchCV)
* **Model Serialization:** `pickle`

### 📄 License
This repository is licensed under the open-source **MIT License**—feel free to use, modify, and distribute the code baseline as needed.
