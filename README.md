# Ex-08-Data-Visualization-

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


# CODE

```
NAME:R.Vignesh
REGISTER NUMBER:212222230172
```

```
import pandas as pd

import seaborn as sns

import matplotlib.pyplot as plt

df = sns.load_dataset("tips")

df.head()

df.isnull().sum()

plt.figure(figsize=(5,5))

plt.title("Data with Outliers")

df.boxplot()

plt.show()

plt.figure(figsize=(5,5))

cols = ['size','tip','total_bill']

Q1 = df[cols].quantile(0.25)

Q3 = df[cols].quantile(0.75)

IQR = Q3 - Q1

df = df[~((df[cols] < (Q1 - 1.5 * IQR)) |(df[cols] > (Q3 + 1.5 * IQR))).any(axis=1)]

plt.title("Dataset after removing outliers")

df.boxplot()

plt.show()

sns.barplot(x=df['day'], y=df['total_bill'])

plt.title("Highest Total Bill Amount by day")

plt.show()

sns.boxplot(x=df['smoker'], y=df['tip'],hue=df['smoker'])

plt.title("Average Tip Amount given by smokers and non-smokers")

plt.show()

df["tip_percent"] = df["tip"] / df["total_bill"]

sns.barplot(x=df['size'],y=df['tip_percent'],data=df)

plt.title("Tip Percentage by Dining Party Size")

plt.show()

sns.barplot(x=df['sex'], y=df['tip'])

plt.title("Highest tips based on gender")

plt.show()

sns.barplot(x=df['day'],y=df['total_bill'])

plt.title("Total bill amount by day of the week")

plt.show()

sns.histplot(data=df, x="total_bill", hue="time", element="step", stat="density")

plt.title("Distribution of Total Bill Amounts by Time of Day")

plt.show()

sns.barplotdata=df,(x=df['size'],y=df['total_bill'])

plt.title("Average Total Bill Amount by Dining Party Size")

plt.show()

sns.violinplot(x="day", y="tip", data=df)

plt.title("Tip Amount by Day of Week")

plt.show()

sns.barplot(x="time", y="tip", data=df)

plt.title("Tip Amount by Time of Day")

plt.show()

sns.scatterplot(x="total_bill", y="tip", data=df)

plt.title("Correlation between Tip Amount and Total Bill Amount")

plt.show()
```

# OUPUT

![240808166-16739396-95f5-4718-a12e-880819742785](https://github.com/Praveenkumar2004-dev/Ex-08-Data-Visualization_1/assets/119559827/56be36fd-a1a3-4ca5-aada-cbca08ecc04a)

![240808173-dae48bff-8de6-4e08-84dd-61e4f14a7eb0](https://github.com/Praveenkumar2004-dev/Ex-08-Data-Visualization_1/assets/119559827/6cc30905-34fe-482a-bfe4-07ba70f01821)

![240808177-7ba5c454-d644-4cf0-b411-7b5e0485c846](https://github.com/Praveenkumar2004-dev/Ex-08-Data-Visualization_1/assets/119559827/a1aa59e8-3057-4d70-9e03-ee6e6e8fac75)

![240808182-96d1bb76-d76f-42e5-b08d-dc0e4a031048](https://github.com/Praveenkumar2004-dev/Ex-08-Data-Visualization_1/assets/119559827/dc9ca824-0a75-4545-978b-497e100414b6)

![240808187-94d2c80e-a80e-438c-b6ec-ae417e02ba75](https://github.com/Praveenkumar2004-dev/Ex-08-Data-Visualization_1/assets/119559827/65e9eecb-8831-4bdf-a82c-80a86b271a74)

![240808191-c7bf9439-1e14-4279-805b-5c0815d37e01](https://github.com/Praveenkumar2004-dev/Ex-08-Data-Visualization_1/assets/119559827/fb4d0645-0f35-4062-b5e6-a6991d08fe7e)

![240808196-cf98f293-f141-4ac1-9fa2-f553293e4e42](https://github.com/Praveenkumar2004-dev/Ex-08-Data-Visualization_1/assets/119559827/04a6da36-713a-4d7e-a448-f768a3d989d9)

![240808199-fbfb11e2-74ea-459d-b52e-be7932245d6a](https://github.com/Praveenkumar2004-dev/Ex-08-Data-Visualization_1/assets/119559827/31925f76-2f99-4be1-8c4a-ea83185d6616)

![240808201-bcc40e04-5014-4b97-b813-c4b0d06cd863](https://github.com/Praveenkumar2004-dev/Ex-08-Data-Visualization_1/assets/119559827/38a2c0df-100a-4fa6-8dc7-74be55b98f09)

![240808203-ad6fd5d5-3925-4e69-befc-038259e853ba](https://github.com/Praveenkumar2004-dev/Ex-08-Data-Visualization_1/assets/119559827/b6d03861-cf10-4c10-be7d-1987b0cf82d6)

![240808204-2697bfcf-34d0-4787-a5f5-96303553c79d](https://github.com/Praveenkumar2004-dev/Ex-08-Data-Visualization_1/assets/119559827/3a333a1e-a2b3-4a79-bf71-e0a3944f2f6e)

![240808207-a2cfca9c-939f-48ed-8949-e546680bf70c](https://github.com/Praveenkumar2004-dev/Ex-08-Data-Visualization_1/assets/119559827/79aab964-d76d-41f4-822e-7c5900da9917)

![240808210-c0900349-72fc-49bf-88a2-93aa308add2f](https://github.com/Praveenkumar2004-dev/Ex-08-Data-Visualization_1/assets/119559827/2b2d5da6-2ad1-40e2-bcb4-7ae54ba71e39)

![240808217-10848604-6780-4307-addc-83f59f3ea702](https://github.com/Praveenkumar2004-dev/Ex-08-Data-Visualization_1/assets/119559827/9aea45f1-2439-45db-896c-bef8edfdc883)

# RESULT:
Thus data visualization on complex dataset was performed successfully.
