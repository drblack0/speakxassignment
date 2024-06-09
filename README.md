# SpeakX Assignment
Assignment for speakx. The deliverable include: a jupyter file containing the code and models, and a report containing my findings, results and conclusions. 

## EDA findings
1. The dataset is imbalanced in regards with the target variable. There are far 77% negative values and only 23% positive values. Oversampling had to be done to solve this issue.
2. There isnt a lot of correlation between numerical values. Only Monthly charges and total charges are slightly correlated because monthly charges is a subset of total charges.
3. There are 16.2% senior citiens, along with only 29.8% people who have dependents. THere are equal number of people who are male and female, there are equal number of people who have partners and who don't
4. There is a minor correlation between the variables and the target variable. To further check the correlation between categorical columns we will have to use chi-square test.
5. Ydata profiling showed which columns have a data imbalance.


## Data cleaning and prep
- It is important to convert categorical values to numerical before moving on with models. So I used, label encoder from sklearn to encode the categorical columns.
                        ![image](https://github.com/drblack0/speakxassignment/assets/97089794/2fbfd2ae-ccc5-4823-8390-3a61917a7f74)
