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
df=sns.load_dataset("tips")
df
```

![image](https://github.com/user-attachments/assets/4efa41f1-708c-4af2-b3ea-d6c4a2b860b6)

```
sns.lineplot(x="total_bill",y="tip",data=df,hue="sex",linestyle='solid',legend="auto")
```
![image](https://github.com/user-attachments/assets/7bcdf676-c482-4198-abbc-0456076a9bb6)

```
import seaborn as sns
import matplotlib.pyplot as plt
tips=sns.load_dataset("tips")
avg_total_bill=tips.groupby("day")["total_bill"].mean()
avg_tip=tips.groupby('day')["tip"].mean()
```
![image](https://github.com/user-attachments/assets/224c75ae-8321-4865-9cd4-96e4f6d376fc)

```
plt.figure(figsize=(8,6))
p1=plt.bar(avg_total_bill.index,avg_total_bill,label='Total Bill')
p2=plt.bar(avg_tip.index,avg_tip,bottom=avg_total_bill,label='Tip')
plt.xlabel('Day of the week')
plt.ylabel('Amount')
plt.title('Average Total Bill and Tip by Day')
plt.legend()
plt.show()
```
![image](https://github.com/user-attachments/assets/625ff243-37b8-4f4e-adc3-295371ab4151)

```
avg_total_bill=tips.groupby("time")["total_bill"].mean()
avg_tip=tips.groupby("time")["tip"].mean()
p1=plt.bar(avg_total_bill.index,avg_total_bill,label='Total Bill',width=0.4)
p2=plt.bar(avg_tip.index,avg_tip,bottom=avg_total_bill,label='Tip',width=0.4)
plt.xlabel('Time of Day')
plt.ylabel('Amount')
plt.title('Average Total Bill and Tip by Time of Day')
plt.legend()
plt.show()
```
![image](https://github.com/user-attachments/assets/77a5db49-60a2-4b15-a155-ef32cd8bf711)

```
import seaborn as sns
df=sns.load_dataset("tips")
sns.barplot(x="day",y="total_bill",hue="sex",data=df,palette="Set1")
plt.xlabel('Day of the Week')
plt.ylabel('Total Bill')
plt.title('Average Total Bill by Day and Gender')
plt.show()
```
![image](https://github.com/user-attachments/assets/87b853e6-2a0a-4d24-9fe5-c0219d84bef6)

```
import seaborn as sns
tips=sns.load_dataset("tips")
sns.scatterplot(x="total_bill",y="tip",hue="sex",data=tips)
plt.xlabel('Total Bill')
plt.ylabel('Tip Amount')
plt.title('Relationship Plot of Total Bill vs. Tip Amount')
plt.show()
```
![image](https://github.com/user-attachments/assets/5fe5d163-8a32-4118-87eb-3461fdf13865)

```
sns.histplot(data=tips,x="total_bill",hue="smoker",kde=True,palette="Set1")
plt.xlabel('Total Bill')
plt.ylabel('Frequency')
plt.title('Distribution of Total Bill by Gender')
plt.show()

```
![image](https://github.com/user-attachments/assets/5e6386b9-dbf6-423e-9f17-602cc3b19822)

```
import seaborn as sns
import matplotlib.pyplot as pd
tips=sns.load_dataset("tips")
sns.boxplot(x=tips['day'],y=tips['total_bill'],hue=tips['sex'])
```

```
sns.boxplot(x="day", y="total_bill", hue="smoker", data=tips, linewidth=2, width=0.6, boxprops={"facecolor": "lightblue", "edgecolor": "darkblue"},
            whiskerprops={"color": "black", "linestyle": "--", "linewidth": 1.5}, capprops={"color": "black", "linestyle": "--", "linewidth": 1.5})
```
![image](https://github.com/user-attachments/assets/43f07a6d-dc79-43a0-8a08-096134890f23)

```
sns.violinplot(x="day", y="total_bill", hue="smoker", data=tips, linewidth=2, width=0.6, palette="Set3",inner="quartile")
plt.xlabel('Day of the Week')
plt.ylabel('Total Bill')
plt.title('Distribution of Total Bill by Day and Smoker Status')
plt.show()
```
![image](https://github.com/user-attachments/assets/a526bdb3-88f5-4785-964a-26c81e9e8418)

```
import seaborn as sns
sns.set(style='whitegrid')
tips=sns.load_dataset("tips")
sns.violinplot(x="day",y="tip",data=tips,palette="Set2")

```
![image](https://github.com/user-attachments/assets/dcf360b5-5c67-4293-b11a-a43eb25b6558)

```
sns.kdeplot(data=tips,x="total_bill",hue="time",multiple="fill",linewidth=3,palette="Set2",alpha=0.8)
```
![image](https://github.com/user-attachments/assets/abba749f-401d-4343-a8b7-a67f953f6fc0)

```
sns.kdeplot(data=tips,x="total_bill",hue="time",multiple="stack",linewidth=3,palette="Set2",alpha=0.8)
```
![image](https://github.com/user-attachments/assets/698f120c-6cce-4289-8479-6bd1bf36e72b)

```
sns.kdeplot(data=tips,x="total_bill",hue="time",multiple="layer",linewidth=3,palette="Set2",alpha=0.8)
```
![image](https://github.com/user-attachments/assets/49a22e44-7b61-4d66-b97d-d28c6a12dc76)

```
import numpy as np
data=np.random.randint(low=1,high=100,size=(10,10))
print("The data to be plotted is:\n")
print(data)
```
![image](https://github.com/user-attachments/assets/aff73dae-2cc7-49a2-b636-fc360d082a54)

```

hm=sns.heatmap(data=data,annot=True)
```
![image](https://github.com/user-attachments/assets/8a46373d-d8b6-4c54-9b8c-c114a9077a69)

# Result:
Thus, all the data visualization techniques of seaborn has been implemented.
