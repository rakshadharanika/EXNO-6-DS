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
### name : V Raksha dharanika
### reg : 212223230167
```
import seaborn as sns
import matplotlib.pyplot as plt
import pandas as pd
import numpy as np
x = [1, 2, 3, 4, 5]
y = [3, 6, 2, 7, 1]
sns.lineplot(x=x,y=y)
```
![383102371-83ce7b0b-bedd-4ad5-bf10-30859bca0972](https://github.com/user-attachments/assets/240de06a-eb91-4bee-aa74-5cc61df3ea80)
```
df = sns.load_dataset("tips")
df
```
![383102584-cf8d8a3a-6e58-4306-83d5-bd4d848ff78f](https://github.com/user-attachments/assets/adb5ee82-62ba-47cb-85e9-0b5b25e29100)
```
sns.lineplot(x="total_bill",y="tip", data=df, hue="sex", linestyle='solid', legend="auto")
```
![383102808-e39f85e8-f125-4587-94a1-b0042646bb5c](https://github.com/user-attachments/assets/a7ae9be5-6c37-4e50-b97a-5e71f23c565e)
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
![383103291-0101c9d3-6a11-4ebf-98d0-223e2b493b70](https://github.com/user-attachments/assets/d59079f1-1a49-472c-a8d7-f82fc1e85cda)
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
![383103796-0a9326f1-92a7-4ee7-9290-28a569044f20](https://github.com/user-attachments/assets/cf5ee2cd-2322-494a-9887-c096bf8e5627)
```
avg_total_bill = tips.groupby('time')['total_bill'].mean() 
avg_tip=tips.groupby('time') ['tip'].mean()
p1= plt.bar(avg_total_bill.index, avg_total_bill, label='Total Bill', width=0.4)
p2 = plt.bar(avg_tip.index,avg_tip,bottom=avg_total_bill,label='Tip', width=0.4)
```
![383103912-56aeb398-b2ed-4d83-8d80-95d12a56b73e](https://github.com/user-attachments/assets/0629710e-097f-4e57-b054-6d6b2efdc7f7)
```
years=range(2000, 2012)
apples=[0.895, 0.91, 0.919, 0.926, 0.929, 0.931, 0.934, 0.936, 0.937, 0.9375, 0.9372, 0.939] 
oranges = [0.962, 0.941, 0.930, 0.923, 0.918, 0.908, 0.907, 0.904, 0.901, 0.898, 0.9, 0.896, ]
plt.bar(years, apples)
plt.bar(years, oranges, bottom=apples)
```
![383104097-a097bde2-fe75-409b-89e0-8b39f7aeb033](https://github.com/user-attachments/assets/932c7faf-dc22-4d27-a933-022f9ead1af1)
```
import seaborn as sns
dt= sns.load_dataset('tips')
sns.barplot(x='day', y='total_bill', hue='sex', data=dt, palette='Set1')
plt.xlabel('Day of the Week')
plt.ylabel("Total Bill")
plt.title('Total Bill by Day and Gender')
```
![383104197-cf8ef7e0-177d-40f7-af21-989a944baae9](https://github.com/user-attachments/assets/d73ef6dd-62f8-4af8-8ec3-2fc50567ffb0)
```
tit=pd.read_csv("titanic_dataset.csv")
tit
```
![383104340-5328bf34-4b56-4445-8c94-5f4105322275](https://github.com/user-attachments/assets/40cfa1b9-4efc-4aaa-8d61-c8669236d166)
```
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked', y='Fare', data=tit, palette='rainbow') 
plt.title("Fare of Passenger by Embarked Town")
```
![383104567-e27d66ca-8e7b-4441-b318-342a04514b5d](https://github.com/user-attachments/assets/911d5cb8-45a0-4bce-8852-af01c403a116)
```
tips=sns.load_dataset('tips')
sns.scatterplot(x='total_bill', y='tip', hue='sex', data=tips)
plt.xlabel('Total Bill')
plt.ylabel("Tip Amount")
plt.title('Scatter Plot of Total Bill vs. Tip Amount')
```
![383104679-ac5744fd-c9df-4ba7-a0bd-1acabe0da002](https://github.com/user-attachments/assets/f3f7a20b-602d-48c3-b70a-7669d9bf36f4)
```
num_var = np.random.randn(1000)
num_var=pd.Series(num_var, name = "Numerical variable")
num_var
```
![383104856-4d523a54-40f4-4323-aaf4-68d40364e367](https://github.com/user-attachments/assets/a0575ad5-8dca-479f-9619-d4144bfd3699)
```
sns.histplot(data = num_var, kde = True)
```
![383105051-a67e4df4-7dd1-4955-92f5-7c31db45492d](https://github.com/user-attachments/assets/dc4993cb-1882-43ef-8529-285e5ed55cec)
```
df=pd.read_csv("titanic_dataset.csv")
sns.histplot(data=df,x="Pclass", hue="Survived", kde=True)
```
![383105202-2426649f-f7aa-47f1-a44f-d5b0ee39f4ea](https://github.com/user-attachments/assets/67912fa3-ee6c-4fd0-bf50-b0456147d54c)
```
tips=sns.load_dataset('tips')
sns.boxplot(x=tips['day'], y=tips ['total_bill'], hue=tips['sex'])
```
![383105329-cbd8f7b8-e8e4-4a37-90fe-32433fac60a4](https://github.com/user-attachments/assets/73e82086-8b77-44c8-ba5f-0b7ddbe6e624)
```
sns.boxplot(x="day", y="total_bill", hue="smoker", data=tips, linewidth=2, width=0.6, boxprops={"facecolor": "lightblue", "edgecolor": "darkblue"},
whiskerprops={"color": "black", "linestyle": "--", "linewidth": 1.5}, capprops={"color": "black", "linestyle": "--", "linewidth": 1.5})
```
![383105417-347fb971-e82b-451d-b01e-da38e6b465e7](https://github.com/user-attachments/assets/33d7bcda-f63b-4ff7-8c94-4a1a48af9ba0)
```
sns.violinplot(x="day", y="total_bill", hue="smoker", data=tips, linewidth=2, width=0.6, palette="Set3", inner="quartile")
plt.xlabel("Day of the Week")
plt.ylabel("Total Bill")
plt.title("Violin Plot of Total Bill by Day and Smoker Status")
```
![383105530-39d79e4c-7670-4138-b29c-2036d8bfe2c0](https://github.com/user-attachments/assets/ba34039c-9504-4a02-be43-dd1d17f17d61)
```
mart=pd.read_csv("titanic_dataset.csv")
mart
```
![383105667-6c82cdc6-1b53-4ef4-a324-4536126f4ef5](https://github.com/user-attachments/assets/5be23a19-7f48-4c8d-bfd9-7843e381832f)
```
mart=mart[['PassengerId', 'Survived', 'Age', 'Name', 'Ticket', 'Embarked']] 
mart.head(10)
```
![image](https://github.com/user-attachments/assets/b9717748-c885-40a0-a050-b1e6866c62f3)
```
sns.kdeplot(data=mart,x='PassengerId')
```
![image](https://github.com/user-attachments/assets/eb8c91c9-962e-4bb3-9d33-3c661d025b38)
```
sns.kdeplot(data=mart)
```
![383106446-a6ba5a79-d82f-4f8a-9c53-a0a9707e0846](https://github.com/user-attachments/assets/6f3c543f-d96d-4a36-bfe6-5799e010fdeb)
```
sns.kdeplot(data=mart,x='PassengerId',hue='Survived',multiple='stack')
```
![383106585-dfcd8ca2-4bd5-491f-a75a-88e32f508f3b](https://github.com/user-attachments/assets/440d25c1-110e-4bb2-8b03-104b1560a438)
```
sns.kdeplot(data=mart,x='PassengerId',y='Survived')
```
![383106708-3567353e-3b96-4c8e-9df3-72daa607910e](https://github.com/user-attachments/assets/1a8199ab-3521-4782-9e1f-f3b47ae9941f)
```
data = np.random.randint(low = 1, high = 100, size = (10,10))
hm=sns.heatmap(data=data,annot=True)
```
![383106844-71217126-ccb2-4396-adff-81017f3f4b49](https://github.com/user-attachments/assets/bcf2764e-3494-47c8-8487-626bc5517982)
```
hm=sns.heatmap(data=data)
```
![383106967-9b92ccc7-20c8-4f24-8d98-b68af2519816](https://github.com/user-attachments/assets/7ee229f9-af0d-4afd-abbd-f8961ce05223)


# Result:
 Thus, all the data visualization techniques of seaborn has been implemented.
