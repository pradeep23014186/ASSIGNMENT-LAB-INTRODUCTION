# ASSIGNMENT-LAB-INTRODUCTION
## AIM:
To find the code for Activity 1 and 2
## Procedure:
1. Check the Question
2. Analyse the Problem
3. Enter the code for Activity 1 and 2
4. Run the program
## Program:
### Activity 1:
```
import pandas as pd
import numpy as np

exam_data = {
    'name': ['Anastasia', 'Dima', 'Katherine', 'James', 'Emily', 'Michael', 'Matthew', 'Laura', 'Kevin', 'Jonas'],
    'score': [12.5, 9, 16.5, np.nan, 9, 20, 14.5, np.nan, 8, 19],
    'attempts': [1, 3, 4, 3, 5, 3, 6, 1, 7, 1]
}

df = pd.DataFrame(exam_data)

result = df[['name', 'score']]
print(result)
filtered_df = df[df['attempts'] > 3]
print(filtered_df)
data = {
    'name': ['Alice', 'Bob', 'Charlie', 'Dave'],
    'age': [25, 35, 40, 28],
    'gender': ['F', 'M', 'M', 'M'],
    'salary': [50000, 70000, 60000, 80000]
}

df = pd.DataFrame(data)

# a. Select rows where age is greater than 30
age_filtered = df[df['age'] > 30]
print(age_filtered)

# b. Select rows where name contains 'e'
name_filtered = df[df['name'].str.contains('e', case=False, na=False)]
print(name_filtered)

# c. Select rows where gender is 'M' and salary is greater than 65000
gender_salary_filtered = df[(df['gender'] == 'M') & (df['salary'] > 65000)]
print(gender_salary_filtered)

# d. Select columns 'name' and 'age'
selected_columns = df[['name', 'age']]
print(selected_columns)
```

## Activity 2:

```
import pandas as pd

# Sample DataFrame
data = {
    'name': ['Alice', 'Bob', 'Charlie', 'Dave', 'Eva', 'Frank'],
    'education': ['primary', 'secondary', 'tertiary', 'primary', 'secondary', 'tertiary'],
    'deposit': ['yes', 'no', 'yes', 'no', 'no', 'yes'],
    'housing': ['no', 'yes', 'yes', 'no', 'yes', 'no'],
    'personal_loan': ['yes', 'no', 'no', 'yes', 'no', 'yes'],
    'job': ['unemployed', 'admin', 'technician', 'management', 'unemployed', 'admin'],
    'campaign_outcome': ['success', 'failure', 'success', 'failure', 'failure', 'success'],
    'age': [25, 45, 35, 29, 50, 30],
    'salary': [40000, 50000, 60000, 45000, 70000, 55000]
}

df = pd.DataFrame(data)

# a. Select rows where clients with primary education have subscribed to a deposit
primary_edu_deposit = df.loc[(df['education'] == 'primary') & (df['deposit'] == 'yes')]
print(primary_edu_deposit)

# b. Select rows where clients who have not subscribed to a deposit
no_deposit = df.loc[df['deposit'] == 'no']
print(no_deposit)

# c. Select rows where clients who have subscribed to a deposit either have a housing or a personal loan
deposit_with_loans = df.loc[(df['deposit'] == 'yes') & ((df['housing'] == 'yes') | (df['personal_loan'] == 'yes'))]
print(deposit_with_loans)

# d. Select rows where clients with secondary education who have not subscribed to a deposit
secondary_no_deposit = df.loc[(df['education'] == 'secondary') & (df['deposit'] == 'no')]
print(secondary_no_deposit)

# e. Select rows where clients who have subscribed to a deposit as an outcome of a successful marketing campaign
successful_campaign = df.loc[(df['deposit'] == 'yes') & (df['campaign_outcome'] == 'success')]
print(successful_campaign)

# f. Select rows where unemployed clients who have not subscribed to a deposit
unemployed_no_deposit = df.loc[(df['job'] == 'unemployed') & (df['deposit'] == 'no')]
print(unemployed_no_deposit)

# g. Select columns 'name' and 'salary' where age is less than or equal to 30
name_salary_age = df.loc[df['age'] <= 30, ['name', 'salary']]
print(name_salary_age)
```
## Output:
### Output 1:
![image](https://github.com/user-attachments/assets/27be14aa-bb25-425a-aa50-a9d9d5c57deb)
![image](https://github.com/user-attachments/assets/8b365fce-9b69-4e2a-b7d9-115806db5097)
![image](https://github.com/user-attachments/assets/7b62f646-8118-4996-9ebe-340ca72bc3ca)

### Output 2:
![image](https://github.com/user-attachments/assets/44863d38-4d94-466c-a890-c4bd355520be)
