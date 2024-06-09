# SpeakX Assignment
Assignment for speakx. The deliverable include: a jupyter file containing the code and models, and a report containing my findings, results and conclusions. 

## EDA findings
1. The dataset is imbalanced in regards with the target variable. There are far 77% negative values and only 23% positive values. Oversampling had to be done to solve this issue.
2. There isnt a lot of correlation between numerical values. Only Monthly charges and total charges are slightly correlated because monthly charges is a subset of total charges.
3. There are 16.2% senior citiens, along with only 29.8% people who have dependents. THere are equal number of people who are male and female, there are equal number of people who have partners and who don't
4. There is a minor correlation between the variables and the target variable. To further check the correlation between categorical columns we will have to use chi-square test.
5. Ydata profiling showed which columns have a data imbalance.


## Data cleaning and prep
- It is important to convert categorical values to numerical before moving on with models. So I used, label encoder from sklearn to encode the categorical columns. ![image](https://github.com/drblack0/speakxassignment/assets/97089794/2fbfd2ae-ccc5-4823-8390-3a61917a7f74)
- Since majority of our dataset is categorical values we will have to normalize our numerical columns so that they don't skew the data. ![image](https://github.com/drblack0/speakxassignment/assets/97089794/444e3bee-077e-4588-a729-51872022c9f0)
- We will also drop all the null values from the dataset (our dataset is big enough to drop null values without any conseuqnece. There are 11 null values and total records amount up to 7000+)


## Model selection 
- We are using 4 models in this assignemnt:
   1. Logistic Regression Classifier
   2. SVC
   3. Random Forest Classifier
   4. Gradient Boosting Classifier
- Logistic Regression Classifier: Accuracy score of this model is 77%. Logistic regression models fits the data using a sigmoid function, and is often helpful in binary classification problems. They work by transforming a linear relationship between variables into a probability using a sigmoid function. This function outputs a value between 0 and 1, representing the likelihood of the positive outcome ![image](https://github.com/drblack0/speakxassignment/assets/97089794/08df0f93-353a-4cae-af09-caa00e9dea07)

- Random Forest Classifier: Accuracy score is 78%, a 1% increase from logistic regression model. RF classifier uses a group of decision trees to make the classification. Each tree analyzes a random subset of data and features.  The final prediction is made by majority vote (classification) or averaging (regression) of the individual tree predictions ![image](https://github.com/drblack0/speakxassignment/assets/97089794/21eb717b-9775-44da-a426-9b8cff0c1614)

- Gradient Boost classifier: GB classifier gave an accuracy rating of 76%. Gradient boosting classifiers build a powerful model by combining weaker ones.  These models are trained sequentially, focusing on correcting the errors of the previous model.  This step-wise approach allows them to handle complex data and reduce overall prediction error ![image](https://github.com/drblack0/speakxassignment/assets/97089794/87c8bea2-9d8c-4cd8-aa03-dabc60f7b8c7)

- SVC: Accuracy given by SVC is 77%. They find a hyperplane that best separates different classes in high-dimensional space.  This separation aims to maximize the margin between the data points and the hyperplane, leading to good generalization on unseen data ![image](https://github.com/drblack0/speakxassignment/assets/97089794/659fde99-dcd1-412c-9ab5-e859697dccc5)

### Model conclusions: 
All of the models have almost same accuracy and other metrics. We can achieve better accuracy by feature engineering but being a dataset of almost all categorical values, its difficult to find which columns is more correlated to the target, or even which columns are highly correlated with each other, which makes it difficult to add or remove columns from this dataset. 

## Challenges 
- Almost all categorical values, makes it difficult to find correlation between target and other columns
- Data was imbalanced and heavy oversampling was used
- EDA proved to be a challenge because there were many categorical values and finding a way to plot them meaningfully was challenging
## Conclusion
- I achieved a final accuracy of 78% using Random Forest Classifier.
- There is not much data to work with if we want to create new features or even figure out how columns are correlated with each other.
- EDA and inital analysis lead to finding some interesting trends such as how different demogrpahics affect the churn prediction. 

