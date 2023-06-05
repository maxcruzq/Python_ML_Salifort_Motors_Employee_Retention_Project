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

![Captura de Pantalla 2023-06-05 a la(s) 10 33 37](https://github.com/maxcruzq/Python_ML_Salifort_Motors_Employee_Retention_Project/assets/132103792/74fe6e6f-d2f7-4b8b-83d9-55826deaa0a4)


Some initial observation on the data: 
- Variables are categorical but are in numerical type. 
- Some name columns are not in the expected format and have some misspellings. 

![Captura de Pantalla 2023-06-05 a la(s) 11 35 32](https://github.com/maxcruzq/Python_ML_Salifort_Motors_Employee_Retention_Project/assets/132103792/cc68935d-a49a-442c-b65a-ba035dd7edf4)


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

#### Logistic Regression

The logistic regression model achieved the following wighter average scores, on the test set:


![Captura de Pantalla 2023-06-05 a la(s) 11 29 42](https://github.com/maxcruzq/Python_ML_Salifort_Motors_Employee_Retention_Project/assets/132103792/6d8dc0a3-fc67-4788-976b-1fc21b750092)



![Captura de Pantalla 2023-06-05 a la(s) 11 08 28](https://github.com/maxcruzq/Python_ML_Salifort_Motors_Employee_Retention_Project/assets/132103792/8c49009e-8fa3-49de-af30-b3f0f0fc6b8c)




#### Decision-tree based model


![Captura de Pantalla 2023-06-05 a la(s) 11 12 51](https://github.com/maxcruzq/Python_ML_Salifort_Motors_Employee_Retention_Project/assets/132103792/1c2eb484-2f1f-45b5-97e3-0828ee9183d6)



Scores

![Captura de Pantalla 2023-06-05 a la(s) 11 22 47](https://github.com/maxcruzq/Python_ML_Salifort_Motors_Employee_Retention_Project/assets/132103792/6f34e88d-df0d-4f79-807a-8b90f4bf870b)


Features Importance:

![Captura de Pantalla 2023-06-05 a la(s) 10 44 12](https://github.com/maxcruzq/Python_ML_Salifort_Motors_Employee_Retention_Project/assets/132103792/ac2e6ddf-eaa0-4965-9eae-598bb29e0a1f)



#### Random Forest

Scores

##### The random forest model slightly outperformed the decision tree model.

![Captura de Pantalla 2023-06-05 a la(s) 11 17 51](https://github.com/maxcruzq/Python_ML_Salifort_Motors_Employee_Retention_Project/assets/132103792/d5020733-d984-4aa4-ab5c-3a3add0a077b)

##### The random forest model slightly outperformed the decision tree model.

Features Importance:

![Captura de Pantalla 2023-06-05 a la(s) 10 44 34](https://github.com/maxcruzq/Python_ML_Salifort_Motors_Employee_Retention_Project/assets/132103792/e90d0ddd-6f6c-41e5-baf6-0f5b32782afd)



On the test set, the Random Forest model, performed as follows:

![Captura de Pantalla 2023-06-05 a la(s) 11 19 29](https://github.com/maxcruzq/Python_ML_Salifort_Motors_Employee_Retention_Project/assets/132103792/32ef5f3a-9f6c-43c3-8cb9-dbb8f83cb891)

![Captura de Pantalla 2023-06-05 a la(s) 11 12 39](https://github.com/maxcruzq/Python_ML_Salifort_Motors_Employee_Retention_Project/assets/132103792/9ff0ef38-19c6-455d-bd36-76dc4ec1a2eb)

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

