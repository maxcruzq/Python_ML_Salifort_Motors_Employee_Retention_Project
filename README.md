# Python_ML_Salifort_Motors_Employee_Retention_Project

## Overview
A project overview should be a few sentences long stating the problem you solved, what data was used in the project, 
and your modeling results.

- Salifort Motors seeks to improve employee retention and answer the following question:
What’s likely to make the employee leave the company?
- If we can predict employees likely to quit, it might be possible to identify factors that contribute to their leaving. Because it is time-consuming and expensive to find, interview, and hire new employees, increasing employee retention will be beneficial to the company.
- The company collected data from employees.
- The variable we are looking to predict is categorical. So we will build a Logistic Regression model and Tree-Based Machine Learning model.
- The Random Forest model slightly outperforms the Decision Tree model.
- This model helps predict whether an employee will leave and identify which factors are most influential. 
- These insights can help HR make decisions to improve employee retention.


## Business Understanding
You should have a section that showcases the stakeholder(s) and the business problem you tried to solve. 
Feel free to add citations of research you did on your business problem here as well. 

- Salifort Motors is a fictional French-based alternative energy vehicle manufacturer.
- They have received the results of a recent employee survey. The senior leadership team has wants to analize the data 
to come up with ideas for how to increase employee retention. 
- They would like to design a model that predicts whether an employee will leave the company based on their  
department, number of projects, average monthly hours, and any other data points you deem helpful.

## Data Understanding
Explain what data you used in your analysis, the timeframe of the data, and any data limitations. 
This is also a good section to add visualizations of your exploratory data analysis. 

The dataset will be using contains 15,000 rows and 10 columns for the following variables:


Some initial observation on the data: 
- Variables are categorical but are in numerical type. 
- Some name columns are not in the expected format and have some misspellings. 

![Captura de Pantalla 2023-06-05 a la(s) 10 58 04](https://github.com/maxcruzq/Python_ML_Salifort_Motors_Employee_Retention_Project/assets/132103792/8d148099-8594-45df-8712-7a9071e00b9a)
![Captura de Pantalla 2023-06-05 a la(s) 10 58 24](https://github.com/maxcruzq/Python_ML_Salifort_Motors_Employee_Retention_Project/assets/132103792/93b8fc0a-b50c-4a09-adea-45c2c2038b36)


- There are no null-values. 
- ~20% of the observartions are duplicates, this is a big proportion. 
- ~5% (~800 rows) are outliers in tenure. Some models are suceptible to outliers.

![Captura de Pantalla 2023-06-05 a la(s) 10 59 09](https://github.com/maxcruzq/Python_ML_Salifort_Motors_Employee_Retention_Project/assets/132103792/e25bbdc5-99b2-41dd-ba86-4069afdccb6f)


- Data has strong indicative of data manipulation or synthetic data for the following reasons:
  - Unnatural Clusters: data points form unnaturally perfect clusters, real world data tends to have more irregular and diverse clustering patterns.
  - Uniform Spacing: data points are uniformaley arrange in a highly regular pattern. In real world scenarios data points are often distributed unevenly.
  
  ![Captura de Pantalla 2023-06-05 a la(s) 10 59 41](https://github.com/maxcruzq/Python_ML_Salifort_Motors_Employee_Retention_Project/assets/132103792/85125c68-240d-4ef2-ba1b-c3c4795e7b2e)

  
- Ethical consideration: the model could be missused. For example, the model predicts that a employee will leave, so the company decides to start taking some responsabilities or outcasting them instead of giving that person more incentives. The model also can have false results so we must be very clear about that.

## Modeling Evaluation
This section should detail what models you used and the corresponding evaluation metrics. 

#### Logistic Regression

The logistic regression model achieved the following wighter average scores, on the test set:
- Precision = 80%
- Recall = 83%
- F1-score = 80% 
- Accuracy = 83%


Feature Importance:

![Captura de Pantalla 2023-06-05 a la(s) 10 44 12](https://github.com/maxcruzq/Python_ML_Salifort_Motors_Employee_Retention_Project/assets/132103792/ac2e6ddf-eaa0-4965-9eae-598bb29e0a1f)


#### Tree-based Machine Learning

After conducting feature engineering, the decision tree model achieved the following results on the test set: 
- AUC: 94.3% 
- Precision: 86.5%
- Recall: 91.5%
- F1-score: 88.9%
- Accuracy: 96.2%


Feature Importance:

![Captura de Pantalla 2023-06-05 a la(s) 10 44 34](https://github.com/maxcruzq/Python_ML_Salifort_Motors_Employee_Retention_Project/assets/132103792/e90d0ddd-6f6c-41e5-baf6-0f5b32782afd)



##### The random forest model slightly outperformed the decision tree model.

## Conclusion

- Control and limit the number of projects that an employee can work on simultaneously.
- Conduct further investigations about why 4 year tenure employees are so dissatisfied.
- Reward employees that work long hours and give them some kind of recognition (promotion, salary, bonuses, company awards).
- Create  culture, incentives and polocies of healthier work/life balance.
- High evaluation scores shouldn´t be reserved only for eployees who work long hours.

#### Next Steps
- Address and conduct further verifications for data leakage.
- Consider how predictions change when last_evaluation is removed from the data. It´s possible that evaluations aren´t performed frequently.It colud be 
useful to predict retention whithout this feature.
- There could further analysis building K-means model and analyzing the clusters, this may give valuable insights.

