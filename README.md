# Caglar Varcin Portfolio
<!--- Data Science Portfolio Projects --->

# [Project 1: United States Energy Demand Forecasting by Sector](https://github.com/Varcin/Business-Problems/tree/master/054_energy_forecast_xgboost)
* Forecasted United States energy demand by using XGBoost, Support Vector Machines, and Recursive Linear Regression Model. 
* Created cross-validation set to compare different models and selected the best performing model for each sector.  
* Used historical energy generation data from [EIA](https://www.eia.gov/electricity/data/browser/)

![](https://varcin.github.io/Portfolio/images/energy_forecast.png)
<span style="font-size:1.2em;">*[interactive plot](https://varcin.github.io/Portfolio/images/energy_forecast.html)*</span>

# [Project 2: A/B Testing with Google Optimize](https://github.com/Varcin/Business-Problems/tree/master/024_ab_testing_for_website_optimization)
* The goal of the A/B test was to increase the number of emails collected through a sign up page by updating the sign-up window. 
* Reviewed treatment and control customers and removed leakage.
* Analyzed conversion rate (people who sign-up over people who visited the website) over time. 
* Calculated confidence interval by bootstrapping the sample and did not find enough evidence to update the website. 

<p float="left">
  <img src="https://varcin.github.io/Portfolio/images/ab_test_conversion_overtime.png"  width="300" />
  <img src="https://varcin.github.io/Portfolio/images/ab_test_conversion_bootstrap.png"  width="300" />
</p>

<!--- ![](https://varcin.github.io/Portfolio/images/ab_test_conversion_bootstrap.png) --->

# [Project 3: Telecom Company Customer Churn Survival Analysis](https://github.com/Varcin/Business-Problems/tree/master/014_customer_churn_survival_h2o)
* The goal of the project is to understand the reasons of customer churn and immplement retention strategies ([kaggle data](https://www.kaggle.com/datasets/blastchar/telco-customer-churn)). 
* Identified important predictors of customer attrition by doing correlation analysis. Below table ranks the correlation with churn of each feature. 
<!--- <img src="https://varcin.github.io/Portfolio/images/corr_funel_1.png" width="600"> --->

![](https://varcin.github.io/Portfolio/images/corr_funel_1.png)

* Used Cox Proportional Hazard and Survival Regression models to create survival curves however it performed worse than H2O (auto-machine learning) model when it comes to predicting churn. 
* Survival curve shows that half of the month-to-month contracts are leaving in the first 50 days. 

![](https://varcin.github.io/Portfolio/images/014_churn_survical_fit.png)

* The company can analyse more why half of their month-to-month subscribers leave in less than two months to develop strategies to increase contract length. 

# [Project 4: Detecting Fraudelant Transactions with Isolation Forest (IF)](https://github.com/Varcin/Business-Problems/tree/master/017_anomaly_detection_h2o)
* The dataset contains transactions made by credit cards in September 2013 by European cardholders. The dataset is highly unbalanced, the positive class (frauds) account for 0.172% of all transactions. ([kaggle data](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud)). 
* Isolation forest is an unsupervised machine learning algorithm that is easily scalable. IF uses a random forest algorithm to randomly selects a feature. It randomly splits, separates, and classifies the data. The key concept is outliers have fewer splits to isolate in the decision tree. 
* IF randomly selects a single target, therefore it is important to run it multiple times by changing the seed parameter and averaging the results. 

![](https://varcin.github.io/Portfolio/images/fraud_roc_auc_plot.png)

* Since the dataset is highly unbalanced, I measured the accuracy using the Area Under the Precision-Recall Curve (AUPRC) as confusion matrix accuracy is not meaningful for unbalanced classification. 
* Anomalies (Outliers) are more often than not Fraudulent Transactions. 
* Isolation Forest did a good job at detecting anomalous behaviour. 
