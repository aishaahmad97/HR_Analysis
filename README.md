# HR_Promotions
> HR analytics is revolutionising the way human resources departments operate, leading to higher efficiency and better results overall. Human resources has been using analytics for years. However, the collection, processing and analysis of data has been largely manual, and given the nature of human resources dynamics and HR KPIs, the approach has been constraining HR. Therefore, it is surprising that HR departments woke up to the utility of machine learning so late in the game. Here is an opportunity to try predictive analytics in identifying the employees most likely to get promoted. *You can find the original dataset [here](https://www.kaggle.com/datasets/bhrt97/hr-analytics-classification?select=train_LZdllcl.csv).*

# Business Problem:
One of the problems a large MNC is facing is around identifying the right people for promotion (only for manager position and below) and prepare them in time.
Currently the process, they are following is:
1. Identifying a set of employees based on recommendations/ past performance.
2. Selected employees go through a separate training and evaluation program.
3. At the end of the program, based on various factors such as training performance, KPI completion (only employees with KPIs completed greater than 60% are considered) etc., employee gets promotion.

For above mentioned process, the final promotions are only announced after the evaluation, and this leads to delay in transition to their new roles. Hence, company needs help in identifying the eligible candidates at a particular checkpoint so that they can expedite the entire promotion cycle.

# Data Wrangling:
After assessing the dataset visually and programmatically the following  quality issues were found and cleaned:
*	Outliers in [‘trainings’, ‘experience’] columns.
*	Nulls in [‘education’, ‘prev_year_rating’] columns.
*	Erroneous data types.

# Analysis Key Findings:

- Although 15.7% of previously promoted employees received one or more additional training, the promotion process is more concerned about their passing the main training. 
- It seems the process was gender biased as men are 68.6% more likely to get promoted.
- 30.8% of promoted employees hold a Master's degree, 67.8% have a Bachelor's degree, while only 1.5% hold a below secondary certification in some departments that don't require an undergraduate degree for promotion.
- The previous year's performance is important as having a high rating and KPI > 80 can increase the promotion possibility by 69.8%. But despite that fact, winning an award doesn't have the same impact as only 12.2% of them had won an award the previous year yet still got promoted.


# Predictions:
* Random Forest model F1 score: 0.95
  - Most important features:
    - avg_training_score              0.271455
    - prev_year_rating                0.182330
    - age                             0.117181
    - KPI_80                          0.090425
    - experience                      0.076732
    - gender_m                        0.038189
    - gender_f                        0.027297
    - trainings          
* Logistic Regression F1 score: 0.82
