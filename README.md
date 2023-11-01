# Ex-09-Data-Visualization-

## AIM
To Perform Data Visualization on a complex dataset and save the data to a file. 

# Explanation
Data visualization is the graphical representation of information and data. By using visual elements like charts, graphs, and maps, data visualization tools provide an accessible way to see and understand trends, outliers, and patterns in data.

# ALGORITHM
### STEP 1
Read the given Data
### STEP 2
Clean the Data Set using Data Cleaning Process
### STEP 3
Apply Feature generation and selection techniques to all the features of the data set
### STEP 4
Apply data visualization techniques to identify the patterns of the data.


# CODE:
```python 
Developed by: Yogeshvar M
Register number:212222230180

import seaborn as sns
import matplotlib.pyplot as plt
tips=sns.load_dataset('tips')
tips

tips.head()

tips.info()

# Which day of the week has the highest total bill amount?

sns.barplot(x='day',y='total_bill',data=tips)
plt.title("Weekly highest total bill amount")

# What is the average tip amount given by smokers and non-smokers?

sns.barplot(x='smoker',y='tip',data=tips, palette='rainbow')
plt.title("Average tip amount given by smokers and non-smokers")

# How does the tip percentage vary based on the size of the dining party?

sns.boxplot(x='size', y='tip',data=tips)
plt.title("Tip percentage based on the sizes of the dining party")

# Which gender tends to leave higher tips?

sns.boxplot(x='sex', y='tip',data=tips)
plt.title("Higher tips based on gender")

# Is there any relationship between the total bill amount and the day of the week?

plt.plot(tips['day'],tips['total_bill'])
plt.title("Relationship between the total bill amount and the day of the week")
plt.show()

# How does the distribution of total bill amounts vary across different time periods (lunch vs. dinner)?

sns.violinplot(x='time',y='total_bill',data=tips)
plt.title("Distribution of total bill amounts vary across different time periods(lunch vs. dinner)")

# Which dining party size group tends to have the highest average total bill amount?

sns.barplot(x='size',y='total_bill',data=tips)
plt.title("Highest average total bill amount based party size")

# What is the distribution of tip amounts for each day of the week?

sns.boxplot(x='day',y='total_bill',data=tips)
plt.title("Distribution of tip amounts for each day of the week")

# How does the tip amount vary based on the type of service (lunch vs. dinner)?

sns.violinplot(x='time',y='tip',data=tips)
plt.title("Tip based on the type of service ")

# Is there any correlation between the total bill amount and the tip amount?

sns.scatterplot(data=tips, x='total_bill', y='tip')
correlation_coefficient = tips['total_bill'].corr(tips['tip'])
print("Correlation Coefficient:", correlation_coefficient)
# heatmap
tips.corr()
plt.subplots(figsize=(7,5))
sns.heatmap(tips.corr(),annot=True)
```

# OUPUT:

## dataset
![image](https://github.com/Yogeshvar005/ODD2023-Datascience-Ex-08/assets/113497367/0e572e45-6c39-42f5-8102-ed837dfe0738)

## tips.head()
![image](https://github.com/Yogeshvar005/ODD2023-Datascience-Ex-08/assets/113497367/09fcf759-6488-4efe-8f5a-a7a0b6b17870)

## tips.info()
![image](https://github.com/Yogeshvar005/ODD2023-Datascience-Ex-08/assets/113497367/c4355629-e993-4887-abba-1df8a930b9dd)

![image](https://github.com/Yogeshvar005/ODD2023-Datascience-Ex-08/assets/113497367/72d35356-b4f6-45c7-a636-fd65bd0c3d45)

![image](https://github.com/Yogeshvar005/ODD2023-Datascience-Ex-08/assets/113497367/5805253f-5afb-42da-afcb-e65c0fb0bcd5)

![image](https://github.com/Yogeshvar005/ODD2023-Datascience-Ex-08/assets/113497367/38c7db60-3764-4bb4-8a54-54299bcd3f26)

![image](https://github.com/Yogeshvar005/ODD2023-Datascience-Ex-08/assets/113497367/cf8a7ace-b86d-4815-93b5-7a5266aa1d96)

![image](https://github.com/Yogeshvar005/ODD2023-Datascience-Ex-08/assets/113497367/899cb0fa-8be5-42e8-ad57-1a6de9a5b069)

![image](https://github.com/Yogeshvar005/ODD2023-Datascience-Ex-08/assets/113497367/0095030d-81be-4475-9b53-fce410667794)

![image](https://github.com/Yogeshvar005/ODD2023-Datascience-Ex-08/assets/113497367/e7650342-8e99-4e64-9b9d-1586ec43e177)

![image](https://github.com/Yogeshvar005/ODD2023-Datascience-Ex-08/assets/113497367/bdc756e1-1582-403e-9dc5-b7a476365244)

![image](https://github.com/Yogeshvar005/ODD2023-Datascience-Ex-08/assets/113497367/2ec16435-54ec-4e26-8c06-bb972c392d9e)

![image](https://github.com/Yogeshvar005/ODD2023-Datascience-Ex-08/assets/113497367/f54cd2db-fdd9-4f2e-ae18-6cb9d90febe8)

![image](https://github.com/Yogeshvar005/ODD2023-Datascience-Ex-08/assets/113497367/5b315d71-a574-404b-849e-834c4538ff2c)

## RESULT:

     Hence,Data Visualization is applied on the complex dataset using libraries like Seaborn and Matplotlib successfully based on tips dataset and the data is saved to file.
