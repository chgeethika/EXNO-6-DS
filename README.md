# EXNO-6-DS-DATA VISUALIZATION USING SEABORN LIBRARY

# Aim:
  To Perform Data Visualization using seaborn python library for the given datas.

# EXPLANATION:
Data visualization is the graphical representation of information and data. By using visual elements like charts, graphs, and maps, data visualization tools provide an accessible way to see and understand trends, outliers, and patterns in data.

# Algorithm:
STEP 1:Include the necessary Library.

STEP 2:Read the given Data.

STEP 3:Apply data visualization techniques to identify the patterns of the data.

STEP 4:Apply the various data visualization tools wherever necessary.

STEP 5:Include Necessary parameters in each functions.

# Coding and Output:
```
import seaborn as sns
import matplotlib.pyplot as plt
import pandas as pd
import numpy as np
x = [1, 2, 3, 4, 5]
y = [3, 6, 2, 7, 1]
sns.lineplot(x=x,y=y)
```
![o1](https://github.com/chgeethika/EXNO-6-DS/assets/142209368/f06cb1bc-454f-447b-9cbc-9d01509ef267)

```
df = sns.load_dataset("tips")
df
```
![o2](https://github.com/chgeethika/EXNO-6-DS/assets/142209368/b4e19aea-2912-425b-8432-ae2c0d34f7d7)


```
sns.lineplot(x="total_bill",y="tip", data=df,hue="sex", linestyle='solid', legend="auto")
```
![o3](https://github.com/chgeethika/EXNO-6-DS/assets/142209368/84b1c26e-e1f1-4d31-ac78-f5b83cd82c74)

```
x=[1, 2, 3, 4, 5]
y1=[3, 5, 2, 6, 1]
y2=[1, 6, 4, 3, 8]
y3=[5, 2, 7, 1, 4]
sns.lineplot(x=x, y=y1)
sns.lineplot(x=x, y=y2)
sns.lineplot(x=x, y=y3)
plt.title("Multi-Line Plot")
plt.xlabel('X Label')
plt.ylabel("Y Label")
```
![o4](https://github.com/chgeethika/EXNO-6-DS/assets/142209368/0970b5e1-8229-48a5-9fb7-534f95d2e3b2)

```
tips=sns.load_dataset('tips')
avg_total_bill = tips.groupby('day')['total_bill'].mean()
avg_tip = tips.groupby('day')['tip'].mean()
plt.figure(figsize=(8, 6))
p1 = plt.bar(avg_total_bill.index, avg_total_bill, label='Total Bill')
p2 = plt.bar(avg_tip.index, avg_tip, bottom=avg_total_bill, label='Tip')
plt.xlabel('Day of the Week')
plt.ylabel('Amount')
plt.title('Average Total Bill and Tip by Day')
plt.legend()
```
![o5](https://github.com/chgeethika/EXNO-6-DS/assets/142209368/f52b8f50-f26b-46a7-b1b7-3e3d7e579064)

```
avg_total_bill = tips.groupby('time')['total_bill'].mean()
avg_tip=tips.groupby('time') ['tip'].mean()
p1= plt.bar(avg_total_bill.index, avg_total_bill, label='Total Bill', width=0.4)
p2 = plt.bar(avg_tip.index,avg_tip,bottom=avg_total_bill,label='Tip', width=0.4)
```
![o6](https://github.com/chgeethika/EXNO-6-DS/assets/142209368/acd015a7-eb57-4867-be35-9e392fba6908)

```
years=range(2000, 2012)
apples=[0.895, 0.91, 0.919, 0.926, 0.929, 0.931, 0.934, 0.936, 0.937, 0.9375, 0.9372,0.939]
oranges = [0.962, 0.941, 0.930, 0.923, 0.918, 0.908, 0.907, 0.904, 0.901, 0.898, 0.9,0.896]
plt.bar(years, apples)
plt.bar(years, oranges, bottom=apples)
```
![o7](https://github.com/chgeethika/EXNO-6-DS/assets/142209368/00e5144a-cbed-466c-a66c-b82a02a603c5)

```
import seaborn as sns
dt= sns.load_dataset('tips')
sns.barplot(x='day', y='total_bill', hue='sex', data=dt, palette='Set1')
plt.xlabel('Day of the Week')
plt.ylabel("Total Bill")
plt.title('Total Bill by Day and Gender')
```
![o8](https://github.com/chgeethika/EXNO-6-DS/assets/142209368/277f3bfc-8e43-4cd5-9b77-bfab98027de0)

```
tit=pd.read_csv("titanic_dataset.csv")
tit
```
![o9](https://github.com/chgeethika/EXNO-6-DS/assets/142209368/aaf24410-14ba-4f9f-a66b-05ff2a528159)

```
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked', y='Fare', data=tit, palette='rainbow')
plt.title("Fare of Passenger by Embarked Town")
```
![o10](https://github.com/chgeethika/EXNO-6-DS/assets/142209368/54ddd672-29bb-4cb1-9ce8-1532784223e9)
```
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked', y='Fare', data=tit, palette='rainbow', hue='Pclass')
plt.title("Fare of Passenger by Embarked Town, Divided by Class")
```
![o11](https://github.com/chgeethika/EXNO-6-DS/assets/142209368/e46ba771-8880-4938-a6f6-917242691e34)


```
tips=sns.load_dataset('tips')
sns.scatterplot(x='total_bill', y='tip', hue='sex', data=tips)
plt.xlabel('Total Bill')
plt.ylabel("Tip Amount")
plt.title('Scatter Plot of Total Bill vs. Tip Amount')
```
![o12](https://github.com/chgeethika/EXNO-6-DS/assets/142209368/da9d69a6-9b8a-412f-a857-537a8d1f6a89)

```
num_var = np.random.randn(1000)
num_var=pd.Series(num_var, name = "Numerical variable")
num_var
```
![o13](https://github.com/chgeethika/EXNO-6-DS/assets/142209368/7d5095f1-f962-4f45-8042-d850ef3a73ee)

```
sns.histplot(data = num_var, kde = True)
```
![o14](https://github.com/chgeethika/EXNO-6-DS/assets/142209368/513b0d57-e888-4d56-a662-986cd4e32650)

```
df=pd.read_csv("titanic_dataset.csv")
sns.histplot(data=df,x="Pclass", hue="Survived", kde=True)
```
![o15](https://github.com/chgeethika/EXNO-6-DS/assets/142209368/8588bdaf-ad62-4efc-9ed7-c4398ce25eb6)

```
tips=sns.load_dataset('tips')
sns.boxplot(x=tips['day'], y=tips ['total_bill'], hue=tips['sex'])
```
![o16](https://github.com/chgeethika/EXNO-6-DS/assets/142209368/67b42d96-59a4-4b4c-bd8b-594e330f2bc1)
```
sns.boxplot(x="day", y="total_bill", hue="smoker", data=tips, linewidth=2, width=0.6,boxprops={"facecolor":"lightblue","edgecolor":"darkblue"},
whiskerprops={"color": "black", "linestyle": "--", "linewidth": 1.5}, capprops={"color":"black","linestyle":"--","linewidth":1.5})
```

![o17](https://github.com/chgeethika/EXNO-6-DS/assets/142209368/7219ed2e-1c6a-4ec8-88ff-b895038cc25e)

```
sns.violinplot(x="day", y="total_bill", hue="smoker", data=tips, linewidth=2, width=0.6,palette="Set3",inner="quartile")
plt.xlabel("Day of the Week")
plt.ylabel("Total Bill")
plt.title("Violin Plot of Total Bill by Day and Smoker Status")
```
![o18](https://github.com/chgeethika/EXNO-6-DS/assets/142209368/8fd1cf11-f222-48ed-907d-99ef58985e1d)


```
mart=pd.read_csv("titanic_dataset.csv")
mart
```
![o19](https://github.com/chgeethika/EXNO-6-DS/assets/142209368/3b7f76e4-c049-44c7-9ab7-49ced9f0a518)

```
mart=mart[['PassengerId', 'Survived', 'Age', 'Name', 'Ticket', 'Embarked']]
mart.head(10)
```
![o20](https://github.com/chgeethika/EXNO-6-DS/assets/142209368/fdce848a-b9ae-4888-a266-fc040eae704d)

```
sns.kdeplot(data=mart,x='PassengerId')
```
![o21](https://github.com/chgeethika/EXNO-6-DS/assets/142209368/a3897022-3baf-4326-90fb-50c4398cc339)

```
sns.kdeplot(data=mart,x='Age')
```
![o22](https://github.com/chgeethika/EXNO-6-DS/assets/142209368/24c42d59-ae97-400e-906d-702d9c62c616)

```
sns.kdeplot(data=mart)
```
![o23](https://github.com/chgeethika/EXNO-6-DS/assets/142209368/d2bbd091-7880-4187-a725-5ec1afeb035c)

```
sns.kdeplot(data=mart,x='PassengerId',hue='Survived',multiple='stack')
```
![o24](https://github.com/chgeethika/EXNO-6-DS/assets/142209368/2250604b-0f4c-4710-b9a3-c6778a6317ab)

```
sns.kdeplot(data=mart,x='PassengerId',y='Survived')
```
![o25](https://github.com/chgeethika/EXNO-6-DS/assets/142209368/3f4f7c4c-95bf-46fb-a40d-0e0aa10c44e0)

```
data = np.random.randint(low = 1, high = 100, size = (10,10))
hm=sns.heatmap(data=data,annot=True)
```
![o26](https://github.com/chgeethika/EXNO-6-DS/assets/142209368/327ff1ec-3c69-419c-9307-a0ca257c6a10)


```
hm=sns.heatmap(data=data)
```
![o27](https://github.com/chgeethika/EXNO-6-DS/assets/142209368/a39eb48e-0a19-4939-a9fc-fb11ba142917)



# Result:
Thus, all the data visualization techniques of seaborn has been implemented.
