# EXNO-5-DS-DATA VISUALIZATION USING MATPLOT LIBRARY

# Aim:
  To Perform Data Visualization using matplot python library for the given datas.

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
import pandas as pd
import numpy as np
import seaborn as sns
import matplotlib.pyplot as plt
from scipy.interpolate import make_interp_spline
x_values=[0,1,2,3,4,5]
y_values=[0,1,4,9,16,25]
plt.plot(x_values,y_values)
plt.show()
```
<img width="1389" height="763" alt="image" src="https://github.com/user-attachments/assets/9bc559ca-894e-497a-b87b-7676974009c3" /><br>
```
x = [1, 2, 3, 4, 5]
y = [3, 6, 2, 7, 1]
plt.plot(x, y, label="Line Graph", color="blue", marker="o")
plt.xlabel("X Axis")
plt.ylabel("Y Axis")
plt.legend()
plt.title("Simple Line Graph")
plt.show()
```
<img width="1390" height="758" alt="image" src="https://github.com/user-attachments/assets/667a0d04-5d1c-4e62-bfbc-ba8f15610c1f" /><br>
```
x1 = [1,2,3]
y1 = [2,4,1]
x2 = [1,2,3]
y2 = [4,1,3]
plt.plot(x1, y1, label="line 1", color="red")
plt.plot(x2, y2, label="line 2", color="green")
plt.scatter(x1, y1, color="red")
plt.scatter(x2, y2, color="green")
plt.xlabel("X Axis")
plt.ylabel("Y Axis")
plt.legend()
plt.title("Two Line Graph")
plt.show()
```
<img width="1383" height="771" alt="image" src="https://github.com/user-attachments/assets/c45e6ca2-3ebb-4254-88f0-60baaa46b870" /><br>
```
x=[1,2,3,4,5,6]
y=[2,4,1,5,2,6]
plt.plot(x,y,color='green',linestyle='dashed',linewidth=3,marker='o',markerfacecolor='blue') 
plt.ylim(1,8)
plt.xlim(1,8)
plt.xlabel('x-axis')
plt.ylabel('y-axis')
plt.title('Some cool customizations')
plt.show()
```
<img width="1385" height="756" alt="image" src="https://github.com/user-attachments/assets/5ac0f545-bcb2-4612-a232-07308a704e86" /><br>
```
x_values = [0,1,2,3,4,5]
y_values = [0,1,4,9,16,25]
plt.plot(x_values, y_values)
plt.fill_between(x_values, y_values, color="lightblue", alpha=0.5)
plt.title("Fill Between Graph")
plt.show()
```
<img width="1383" height="714" alt="image" src="https://github.com/user-attachments/assets/be7ab550-be3e-4763-b58a-45f9a05a3c6c" /><br>
```
x = np.array([1,2,3,4,5,6,7,8,9,10])
y = np.array([2,4,5,7,8,8,9,10,11,12])
x_new = np.linspace(x.min(), x.max(), 300)
spl = make_interp_spline(x, y, k=3)
y_smooth = spl(x_new)
plt.plot(x_new, y_smooth)
plt.title("Smooth Curve")
plt.show()
```
<img width="1385" height="755" alt="image" src="https://github.com/user-attachments/assets/647b1359-20f9-4d55-9cb8-d25addee61b4" /><br>
```
values = [5, 6, 3, 7, 2]
names  = ["A", "B", "C", "D", "E"]
plt.bar(names, values, color='orange')
plt.xlabel("Names")
plt.ylabel("Values")
plt.title("Bar Graph")
plt.show()
```
<img width="1385" height="763" alt="image" src="https://github.com/user-attachments/assets/448b7554-da04-47ae-911f-28fc1a32c145" /><br>
```
c1 = ['red', 'green', 'blue', 'yellow', 'purple']
plt.bar(names, values, color=c1)
plt.show()
```
<img width="1389" height="622" alt="image" src="https://github.com/user-attachments/assets/be8f13b0-6f81-40f4-9b9d-4775e40f8ae8" /><br>
```
df = sns.load_dataset("tips")
avg_total_bill = df.groupby("day")["total_bill"].mean()
avg_tip = df.groupby("day")["tip"].mean()
plt.figure(figsize=(8, 6))
p1 = plt.bar(avg_total_bill.index, avg_total_bill, label='Total Bill')
p2 = plt.bar(avg_tip.index, avg_tip, bottom=avg_total_bill, label='Tip')
plt.xlabel('Day of the Week')
plt.ylabel('Amount')
plt.title('Average Total Bill and Tip by Day')
plt.legend()
plt.show()
```
<img width="1368" height="783" alt="image" src="https://github.com/user-attachments/assets/17f2b7eb-6f2c-400b-85fb-e598d39b730a" /><br>
```
x_values = [0,1,2,3,4,5]
y_values = [0,1,4,9,16,25]
plt.scatter(x_values, y_values)
plt.title("Scatter Plot")
plt.show()
```
<img width="1354" height="686" alt="image" src="https://github.com/user-attachments/assets/1cebc383-ecff-466f-838c-d44f0e4fc070" /><br>
```
x = [1,2,3,4,5,6,7,8,9,10]
y = [2,4,5,7,6,8,9,11,12,12]
plt.scatter(x, y, label="stars", color="green", marker="*", s=30)
plt.xlabel("X Axis")
plt.ylabel("Y Axis")
plt.title("Scatter Plot with Stars")
plt.legend()
plt.show()
```
<img width="1394" height="750" alt="image" src="https://github.com/user-attachments/assets/aa9474b6-0f6f-4795-86c5-bc3655b2d67f" /><br>
```

activities = ['eat', 'sleep', 'work', 'play']
slices = [3, 7, 8, 6]
colors = ['r', 'y', 'g', 'b']
plt.pie(slices, labels=activities, colors=colors, autopct='%1.1f%%', startangle=90)
plt.title("Pie Chart")
plt.show()
```
<img width="1396" height="688" alt="image" src="https://github.com/user-attachments/assets/39293d24-11c9-4825-90b5-08b841fb74d8" /><br>
```
x=np.arange(0,4*np.pi,0.1)
y=np.sin(x)
plt.title("sine wave form")
plt.plot(x,y)
plt.show()
```
<img width="1388" height="696" alt="image" src="https://github.com/user-attachments/assets/191d87b1-e791-47ff-9256-674105a4e42c" /><br>

```
x=[1,2,3,4,5]
y1=[10,12,14,16,18]
y2=[5,7,9,11,13]
y3=[2,4,6,8,10]
plt.fill_between(x,y1,color='blue')
plt.fill_between(x,y2,color='green')
plt.plot(x,y1,color='red')
plt.plot(x,y2,color='black')
plt.legend(['y1','y2'])
plt.show()
```
<img width="1386" height="763" alt="image" src="https://github.com/user-attachments/assets/c4890e2a-61c9-4e1b-abb7-fab85121a9a6" /><br>
```
plt.stackplot(x,y1,y2,y3,labels=['Line 1','Line 2','Line 3'])
plt.legend(loc='upper left')
plt.title('Stacked Line Chart')
plt.xlabel('X-axis')
plt.ylabel('Y-axis')
plt.show()
```
<img width="1383" height="741" alt="image" src="https://github.com/user-attachments/assets/d37d5675-6027-40ec-a848-bfb4c6199fab" /><br>
```
import numpy as np
import matplotlib.pyplot as plt
from scipy.interpolate import make_interp_spline
x=np.array([1,2,3,4,5,6,7,8,9,10])
y=np.array([2,4,5,7,8,8,9,10,11,12])
spl=make_interp_spline(x,y)
x_smooth=np.linspace(x.min(),x.max(),100)
y_smooth=spl(x_smooth)
plt.plot(x,y,'o',label='data')
plt.plot(x_smooth,y_smooth,'-',label='Spline')
plt.legend()
plt.show()
```
<img width="1386" height="778" alt="image" src="https://github.com/user-attachments/assets/21038e9f-04ea-4386-800e-1b7b9fb048d3" /><br>
```
values=[5,6,3,7,2]
names=["A","B","C","D","E"]
plt.barh(names,values,color="yellowgreen")
plt.show()
```
<img width="1391" height="643" alt="image" src="https://github.com/user-attachments/assets/260124e3-5a24-4a34-8c0c-7022000eccb6" /><br>
```
x=[2,8,10]
y=[11,16,9]
x2=[3,9,11]
y2=[6,15,7]
plt.bar(x,y,color='r')
plt.bar(x2,y2,color='g')
plt.title('Bar graph')
plt.ylabel('Y axis')
plt.xlabel('X axis')
plt.show()
```
<img width="1382" height="783" alt="image" src="https://github.com/user-attachments/assets/8ad0b855-cfec-450c-a1d6-ab7e2af43b29" /><br>
```
x=[2,1,6,4,2,4,8,9,4,2,4,10,6,4,5,7,7,3,2,7,5,3,5,9,2,1]
plt.hist(x,bins=10,color='blue',alpha=0.5)
plt.show()
```
<img width="1418" height="652" alt="image" src="https://github.com/user-attachments/assets/aa5511c7-b505-4988-9066-a642fc41577c" /><br>
```
data = [42, 55, 67, 68, 70, 72, 75, 79, 81, 88, 95, 102, 140, 160]
plt.boxplot(data)
plt.title("Simple Boxplot")
plt.ylabel("Values")
plt.show()
```

<img width="1426" height="697" alt="image" src="https://github.com/user-attachments/assets/03ce2310-98f5-481c-b739-cd6c3e47513e" /><br>






# Result:
Thus, all the data visualization techniques of matplotlib has been implemented.
