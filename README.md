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

NAME : SANTHOSE AROCKIARAJ J

REG NO : 212224230248

```
import seaborn as sns
import matplotlib.pyplot as plt
df=sns.load_dataset("tips")
df
```
![image](https://github.com/user-attachments/assets/de207201-eb40-4b7f-8932-94e0484f772c)
```
sns.lineplot(x="total_bill",y="tip",data=df,hue='sex',linestyle="solid",legend="auto",palette="Set1")
```
![image](https://github.com/user-attachments/assets/2d2623ee-c19a-4eee-b3b5-a716a1001ab3)
```
import seaborn as sns
import matplotlib.pyplot as plt
tips=sns.load_dataset("tips")
avg_total_bill=tips.groupby("day")["total_bill"].mean()
avg_tip=tips.groupby("day")["tip"].mean()
avg_total_bill
```
![image](https://github.com/user-attachments/assets/208b514c-876f-4243-8866-caadd48c6c5f)
```
plt.figure(figsize=(8,6))
p1=plt.bar(avg_total_bill.index,avg_total_bill,label="Total Bill")
p2=plt.bar(avg_tip.index,avg_tip,bottom=avg_total_bill,label="Tip")
plt.xlabel("Day of the week")
plt.ylabel("Amount")
plt.title("Average Total Bill and Tip by Day")
plt.legend()
plt.show()
```
![image](https://github.com/user-attachments/assets/ca060561-2449-46e9-864f-766a2dc774f4)
```
avg_total_bill=tips.groupby("time")["total_bill"].mean()
avg_tip=tips.groupby("time")["tip"].mean()
p1=plt.bar(avg_total_bill.index,avg_total_bill,label="Total Bill")
p2=plt.bar(avg_tip.index,avg_tip,bottom=avg_total_bill,label="Tip")
plt.xlabel("Day of the week")
plt.ylabel("Amount")
plt.title("Average Total Bill and Tip by Day")
plt.legend()
```
![image](https://github.com/user-attachments/assets/506d0f7e-c01a-4f1e-bc36-c7d7138f6d91)
```
import seaborn as sns
df=sns.load_dataset("tips")
sns.barplot(x='day',y='total_bill',data=df,hue='sex',palette='Set3')
plt.xlabel("Day of the week")
plt.ylabel("Total Bill")
plt.title("Total Bill by Day and Gender")
```
![image](https://github.com/user-attachments/assets/6c233eab-d9fd-4285-9b50-67d45e43edcc)
```
import seaborn as sns
df=sns.load_dataset("tips")
sns.scatterplot(x='total_bill',y='tip',data=df,hue='sex',palette='Set1')
```
![image](https://github.com/user-attachments/assets/5f5a0d6b-d041-4aea-b73b-c01f6d30addf)
```
sns.histplot(data=df,x='total_bill',hue="smoker",kde=True,palette="Set2")
plt.xlabel("Total Bill")
plt.ylabel("Frequency")
plt.title("Distribution of Total Bill by Smoker Status")
```
![image](https://github.com/user-attachments/assets/2d3b0cc8-36f4-4848-a5c7-bc32232b7340)
```
import pandas as pd
df=sns.load_dataset('tips')
sns.boxplot(x='day',y='total_bill',data=df,hue='sex',palette='Set2')
```
![image](https://github.com/user-attachments/assets/ac7755a1-043c-41a5-b0e5-d7822411d8b9)
```
sns.boxplot(x='day',y='total_bill',hue='smoker',
            data=df,linewidth=2,width=0.6,
            fliersize=7,flierprops={"marker":"o","markerfacecolor":"grey"}, # Changed 'makerfacecolor' to 'markerfacecolor'
            boxprops={"facecolor":"red","edgecolor":"black"},
            whiskerprops={"color":"darkblue","linestyle":"--","linewidth":2},
            capprops={"color":"darkblue","linestyle":"-","linewidth":2},palette="Set1")
```
![image](https://github.com/user-attachments/assets/cf2d2a5e-bb6b-4217-9885-30ad8c11682b)
```
sns.violinplot(x='day',y='total_bill',data=tips,hue='smoker',linewidth=2,width=0.6,palette="Set1",inner="quartile")
plt.xlabel("Day of the week")
plt.ylabel("Total Bill")
plt.title("Distribution of Total Bill by Day and Smoker Status")
```
![image](https://github.com/user-attachments/assets/aa702264-afe5-48ef-b19d-768d089ecb2a)
```
sns.set(style="whitegrid")
tip=sns.load_dataset('tips')
sns.violinplot(x='day',y='tip',data=tip,palette="Set2")
```
![image](https://github.com/user-attachments/assets/03bb9653-0785-48c7-8a62-1873f8de2e74)
```
sns.set(style='whitegrid')
tip=sns.load_dataset('tips')
sns.violinplot(x=tip['total_bill'],data=tip,palette="Set1")
```
![image](https://github.com/user-attachments/assets/3d033722-0bd7-4777-8881-ad10a25ce36d)
```
sns.set(style='whitegrid')
tips=sns.load_dataset('tips')
sns.violinplot(x='tip',y='day',data=tip,palette="Set2")
```
![image](https://github.com/user-attachments/assets/33966e4c-b864-4fb9-b3dd-72e532545354)
```
sns.kdeplot(data=tips,x='total_bill',hue='time',multiple='layer',linewidth=3,palette='Set2',alpha=0.8)
```
![image](https://github.com/user-attachments/assets/d16f8bde-d6ec-4991-a4c1-5e545fdbcb0e)
```
sns.kdeplot(data=tips,x='total_bill',hue='time',multiple='stack',linewidth=3,palette='Set3',alpha=0.8)
```
![image](https://github.com/user-attachments/assets/453af435-2632-42a8-a5da-bb9b1a0a1a89)
```
sns.kdeplot(data=tips,x='total_bill',hue='time',multiple='fill',linewidth=3,palette='Set1',alpha=0.8)
```
![image](https://github.com/user-attachments/assets/780517c7-1866-4aca-a11e-feb0d4266f6f)
```
tip=sns.load_dataset('tips')
num=tips.select_dtypes(include=['float64','int64']).columns
corr=tips[num].corr()
sns.heatmap(corr,annot=True,cmap='YlGnBu')
```
![image](https://github.com/user-attachments/assets/6dfdd823-7ee9-40f0-a058-bea3525cf042)
```
sns.heatmap(corr,cmap='YlGnBu')
```
![image](https://github.com/user-attachments/assets/871f031b-ee2c-4d5b-99d7-436a097020ef)


# Result:
 Thus, performed Data Visualization using seaborn python library for the given datas.

