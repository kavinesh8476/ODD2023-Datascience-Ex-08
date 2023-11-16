# Ex-08-Data-Visualization-
## AIM
To Perform Data Visualization on a complex dataset and save the data to a file.

## Explanation
Data visualization is the graphical representation of information and data. By using visual elements like charts, graphs, and maps, data visualization tools provide an accessible way to see and understand trends, outliers, and patterns in data.

## ALGORITHM
### STEP 1
Read the given Data

### STEP 2
Clean the Data Set using Data Cleaning Process

### STEP 3
Apply Feature generation and selection techniques to all the features of the data set

### STEP 4
Apply data visualization techniques to identify the patterns of the data.

## CODE and OUTPUT
```
DEVELOPED BY:KAVINESH M
REGISTER NO:212222230064
```
```
import matplotlib.pyplot as plt

x1=[1,2,3]
y1=[2,4,1]
plt.plot(x1,y1,label='line 1')
x2=[1,2,3]
y2=[4,1,3]
plt.plot(x2,y2,label='line 2')
plt.xlabel('x-axis')
plt.ylabel('y-axis')
plt.title('Two lines on same graph')
plt.legend()
plt.show()
```
![282649721-6cdc5e57-9c36-4136-8469-ae44e61e037c](https://github.com/kavinesh8476/ODD2023-Datascience-Ex-08/assets/118466561/961bcb30-2121-45b1-948a-8a9f43b4a964)


```
x=[1,2,3,4,5,6]
y=[2,4,1,5,2,6]
plt.plot(x,y,color='green',linestyle='dashed',linewidth=3,marker='o',markerfacecolor='blue',markersize=12)
plt.xlim(1,8)
plt.ylim(1,8)
plt.xlabel('x-axis')
plt.ylabel('y-axis')
plt.title('some cool customizations')
plt.show()
```
![282649797-7d8663ef-f797-43dc-81d6-bd64aa9f7dea](https://github.com/kavinesh8476/ODD2023-Datascience-Ex-08/assets/118466561/fe952e1b-e762-42d4-860d-0b7e55f25eb9)


```
import seaborn as sns
```
```
x=[1,2,3,4,5]
y=[3,6,2,7,1]
sns.lineplot(x=x,y=y)
```
![282649831-7625cd3a-13e1-4599-9cbf-dabc3cc84b09](https://github.com/kavinesh8476/ODD2023-Datascience-Ex-08/assets/118466561/41b0f14c-5a4e-47a9-885b-d7ae28ccdaf2)


```
df=sns.load_dataset("tips")
df
```
![282649859-12623d04-caa2-4fdb-bef5-fc9fdf3b3600](https://github.com/kavinesh8476/ODD2023-Datascience-Ex-08/assets/118466561/ed386e13-b17d-44e5-af91-b775a7d5ee3d)


```
sns.lineplot(x="total_bill",y="tip",data=df,hue='sex',linestyle='solid',legend='auto')
```
![282649958-7dd27cac-e53e-476a-9741-4d9593a0f2ab](https://github.com/kavinesh8476/ODD2023-Datascience-Ex-08/assets/118466561/9c77d8e5-3597-47f9-9fd2-e5c828accb7e)


```
height=[10,24,36,40,5]
names=['one','two','three','four','five']
c1=['red','green']
c2=['b','g']
plt.bar(names,height,width=0.8,color=c2)
plt.xlabel('x-axis')
plt.ylabel('y-axis')
plt.title('My bar Chart!')
plt.show()
```
![282650143-637961cc-3815-4bbe-9d2b-4d78f5576c81](https://github.com/kavinesh8476/ODD2023-Datascience-Ex-08/assets/118466561/113cbceb-4e83-45d2-a495-2705c0aa6255)


```
x=[0,1,2,3,5,8]
y=[3,5,2,6,8,9]
plt.scatter(x,y,s=30,color='blue')
```

```
sns.scatterplot(x='total_bill',y='tip',hue='sex',data=df)
plt.xlabel('Total bill')
plt.ylabel('Tip amount')
plt.title('Scatter plot of Total bill vs Tip amount')
```

```
ages=[5,3,54,76,53,23,42,22,21,20,21,67,65,87,25,57,22]
bins=10
range=(0,100)
plt.hist(ages,bins,range,color='green',histtype='bar',rwidth=0.8)
plt.xlabel('ages')
plt.ylabel('No. of people')
plt.title('My histogram')
plt.show()
```

```
sns.violinplot(x="tip",data=df)
```
![282650394-c3319771-18e7-417a-a3bd-9e17719c328a](https://github.com/kavinesh8476/ODD2023-Datascience-Ex-08/assets/118466561/8dc09153-5393-4fae-9cd8-2a00830934a5)


```
sns.kdeplot(x="tip", data = df,hue='time')
```
![282650421-dc6df73f-16b6-439a-bc66-fdfe4ebe2ebd](https://github.com/kavinesh8476/ODD2023-Datascience-Ex-08/assets/118466561/35252b00-9452-426f-8fae-bd9bcd439fc5)


```
plt.boxplot(x="tip",data=df)
plt.show()
```
![282650341-35070575-72d7-4403-aabc-0c990501a4bf](https://github.com/kavinesh8476/ODD2023-Datascience-Ex-08/assets/118466561/b02c1996-5d02-49de-b0e6-6e30a6abab79)


```
sns.boxplot(x='tip',data=df)
```
![282650652-b1a440bd-9d0d-434c-8f6d-a00a37282266](https://github.com/kavinesh8476/ODD2023-Datascience-Ex-08/assets/118466561/915400da-3bf4-4293-8367-232b9681ae97)


```
df.corr()
plt.subplots(figsize=(12,7))
sns.heatmap(df.corr(),annot=True)
```
![282650838-22776a93-1450-4fc2-9bc6-150229cf8f82](https://github.com/kavinesh8476/ODD2023-Datascience-Ex-08/assets/118466561/0408b733-ece6-466e-ab3f-5b5ff270ef3d)



## RESULT

Hence, Data Visualization is applied on the complex dataset using libraries like Seaborn and Matplotlib successfully and the data is saved to file.
