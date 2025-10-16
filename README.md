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
 Include the necessary coding and corresponding screenshots

  import seaborn as sns
  
 import matplotlib.pyplot as plt
 
 import pandas as pd
 
 import numpy as np
 
 x = [1, 2, 3, 4, 5]
 
 y = [3, 6, 2, 7, 1]
 
 sns.lineplot(x=x,y=y)

 <img width="770" height="539" alt="image" src="https://github.com/user-attachments/assets/2a602786-900a-41b1-b767-0e968d0eba4c" />

  df = sns.load_dataset("tips")
  
 df

 <img width="586" height="464" alt="image" src="https://github.com/user-attachments/assets/2eaf724b-a9b0-4fea-a169-087f32dea035" />

  sns.lineplot(x="total_bill",y="tip", data=df, hue="sex", linestyle='solid', legend="auto")

  <img width="758" height="555" alt="image" src="https://github.com/user-attachments/assets/21d691e9-0c22-4bfc-99e3-8bb8db19ae82" />

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

 <img width="634" height="534" alt="image" src="https://github.com/user-attachments/assets/336367ff-85b4-4328-8e6c-42a1ffd39522" />

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

 <img width="670" height="551" alt="image" src="https://github.com/user-attachments/assets/83ec935f-fa74-4492-9061-f7de0e42cffd" />

  avg_total_bill = tips.groupby('time')['total_bill'].mean()
  
 avg_tip=tips.groupby('time') ['tip'].mean()
 
 p1= plt.bar(avg_total_bill.index, avg_total_bill, label='Total Bill', width=0.4)
 
 p2 = plt.bar(avg_tip.index,avg_tip,bottom=avg_total_bill,label='Tip', width=0.4)

 <img width="717" height="548" alt="image" src="https://github.com/user-attachments/assets/b7b1692e-232d-41a0-87c8-eb46a711bacb" />

  years=range(2000, 2012)
  
 apples=[0.895, 0.91, 0.919, 0.926, 0.929, 0.931, 0.934, 0.936, 0.937, 0.9375, 0.9372, 0.939]
 
 oranges = [0.962, 0.941, 0.930, 0.923, 0.918, 0.908, 0.907, 0.904, 0.901, 0.898, 0.9, 0.896, ]
 
 plt.bar(years, apples)
 
 plt.bar(years, oranges, bottom=apples)

 <img width="814" height="647" alt="image" src="https://github.com/user-attachments/assets/27c347e2-cf6b-47c2-a46b-608551000948" />

 dt= sns.load_dataset('tips')
 
 sns.barplot(x='day', y='total_bill', hue='sex', data=dt, palette='Set1')
 
 plt.xlabel('Day of the Week')
 
 plt.ylabel("Total Bill")
 
 plt.title('Total Bill by Day and Gender')

<img width="898" height="701" alt="image" src="https://github.com/user-attachments/assets/731fe885-27ca-44db-8cec-5b033bfc6907" />

 tit=pd.read_csv("titanic_dataset.csv")
 
 tit
 
 <img width="927" height="319" alt="image" src="https://github.com/user-attachments/assets/c731f92d-26f9-48ff-a49c-e69f49e07e0e" />

  plt.figure(figsize=(8,5))
  
 sns.barplot(x='Embarked', y='Fare', data=tit, palette='rainbow')
 
 plt.title("Fare of Passenger by Embarked Town")

 <img width="834" height="601" alt="image" src="https://github.com/user-attachments/assets/1bcf7603-dcb8-40e2-86cb-142f50ce9181" />

tips=sns.load_dataset('tips')

 sns.scatterplot(x='total_bill', y='tip', hue='sex', data=tips)
 
 plt.xlabel('Total Bill')
 
 plt.ylabel("Tip Amount")
 
 plt.title('Scatter Plot of Total Bill vs. Tip Amount')

<img width="873" height="693" alt="image" src="https://github.com/user-attachments/assets/f4cf288a-3068-4840-9ed2-4c4dea9601e3" />

 num_var = np.random.randn(1000)
 
 num_var=pd.Series(num_var, name = "Numerical variable")
 
 num_var

<img width="738" height="358" alt="image" src="https://github.com/user-attachments/assets/b4d76472-f3ca-47d2-9748-58793aca828a" />

sns.histplot(data = num_var, kde = True)
<img width="847" height="692" alt="image" src="https://github.com/user-attachments/assets/607158e9-37b6-448f-879f-53f09a008966" />

 df=pd.read_csv("titanic_dataset.csv")
 
 sns.histplot(data=df,x="Pclass", hue="Survived", kde=True)

 <img width="849" height="645" alt="image" src="https://github.com/user-attachments/assets/ee614f94-c197-42bf-99f4-ac6a469b18c0" />


 tips=sns.load_dataset('tips')
 
 sns.boxplot(x=tips['day'], y=tips ['total_bill'], hue=tips['sex'])

<img width="800" height="653" alt="image" src="https://github.com/user-attachments/assets/92941458-593b-441e-901e-e28fe8d1c956" />
 
 sns.boxplot(x="day", y="total_bill", hue="smoker", data=tips, linewidth=2, width=0.6, boxprops=
 {"facecolor": "lightblue", "edgecolor": "darkblue"}, whiskerprops={"color": "black", "linestyle": "--",
 "linewidth": 1.5}, capprops={"color": "black", "linestyle": "--", "linewidth": 1.5})
 
<img width="854" height="664" alt="image" src="https://github.com/user-attachments/assets/98ea0de5-69b0-4994-b7ec-5612a5e1925d" />

 sns.violinplot(x="day", y="total_bill", hue="smoker", data=tips, linewidth=2, width=0.6, palette="Set3",
 inner="quartile")
 
 plt.xlabel("Day of the Week")
 
 plt.ylabel("Total Bill")
 
 plt.title("Violin Plot of Total Bill by Day and Smoker Status")

<img width="895" height="736" alt="image" src="https://github.com/user-attachments/assets/71b41958-9dee-4abe-8050-5e00ced1e960" />

mart=pd.read_csv("titanic_dataset.csv")

 mart
<img width="992" height="341" alt="image" src="https://github.com/user-attachments/assets/348ddca3-b4ac-4546-bcf8-6f7c25ef60a3" />

 mart=mart[['PassengerId', 'Survived', 'Age', 'Name', 'Ticket', 'Embarked']]
 
 mart.head(10)
<img width="947" height="387" alt="image" src="https://github.com/user-attachments/assets/cdac8232-43ad-43b1-8788-00303ec0a51a" />

 sns.kdeplot(data=mart,x='PassengerId')

 <img width="907" height="655" alt="image" src="https://github.com/user-attachments/assets/ca8dc0b4-7281-4f9a-b799-bfdb56ab0dd3" />

  sns.kdeplot(data=mart,x='Age')
<img width="913" height="687" alt="image" src="https://github.com/user-attachments/assets/022b495b-e135-4619-8af4-ea4341b2dec7" />


 sns.kdeplot(data=mart)

 <img width="848" height="653" alt="image" src="https://github.com/user-attachments/assets/138cff09-7ec5-48fa-bfad-72adf322ecd3" />

 

 









# Result:
  Thus Performed Data Visualization using seaborn python library for the given datas.

