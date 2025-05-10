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
LINE CHART
```
#line graph
import matplotlib.pyplot as plt
x_value = [0,1,2,3,4,5]
y_value = [0,1,4,9,16,25]
plt.plot(x_value,y_value)
plt.show()
```
![image](https://github.com/user-attachments/assets/140b4506-fbfd-4e7c-b6b2-99e10c451942)
```
import matplotlib.pyplot as plt
x = [1,2,3]
y = [2,4,1]              #simple line
plt.plot(x,y)
plt.xlabel('x-axis')
plt.ylabel('y-axis')
plt.title('My First Graph');
plt.show()
```
![image](https://github.com/user-attachments/assets/ed4bea12-0d39-4bf5-832f-8fa1dd88cdb9)
```
import matplotlib.pyplot as plt
x1 = [1,2,3]
y1 = [2,4,1]
plt.plot(x1,y1,label="line 1")
x2 = [1,2,3]                         #simple 2 lines
y2 = [4,1,3]
plt.plot(x2,y2,label = "line 2")
plt.xlabel('x-axis')
plt.ylabel('y-axis')
plt.title('Two lines on same graph')
plt.legend()
plt.show()
```
![image](https://github.com/user-attachments/assets/4245bc60-16b1-40b3-a6ef-bc83276bc61b)
```
import matplotlib.pyplot as plt
x = [1,2,3,4,5,6]
y=[2,4,1,5,2,6]
plt.plot(x,y,color = 'green',linestyle='dashed',linewidth=3,marker='o',markerfacecolor = 'blue',markersize=12)
plt.ylim(1,8)
plt.xlim=(1,8)                  #customization of plots
plt.xlabel('x-axis')
plt.ylabel('y-axis')
plt.title('Some cool customization')
plt.show()
```
![image](https://github.com/user-attachments/assets/095d7d32-75b0-4aa0-a5c3-376c7de90e43)
```
yield_apples = [0.895,0.91,0,919,0.926,0.929,0.931]
plt.plot(yield_apples)
```
![image](https://github.com/user-attachments/assets/f0bbacd1-307f-40c9-bd61-9e0dfd75ab0e)
AREA CHART
```
#area chart
import matplotlib.pyplot as plt
x = [1,2,3,4,5]
y1 =[10,12,14,16,18]
y2 = [5,7,9,11,13]
y3 = [2,4,6,8,10]
plt.fill_between(x,y1,color='blue')
plt.fill_between(x,y2,color='green')
plt.plot(x,y1,color='red')
plt.plot(x,y2,color='black')
plt.legend(['y1','y2'])
plt.show()
```
![image](https://github.com/user-attachments/assets/b425d2e0-4858-4ed3-aa2d-46ed3d17aa90)
```
# Area Chart
import matplotlib.pyplot as plt

x = [1, 2, 3, 4, 5]
y1 = [10, 12, 14, 16, 18]
y2 = [5, 7, 9, 11, 13]
y3 = [2, 4, 6, 8, 10]

plt.fill_between(x, y1, color='blue', alpha=0.6)
plt.fill_between(x, y2, color='green', alpha=0.6)
plt.fill_between(x, y3, color='yellow', alpha=0.6)

plt.plot(x, y1, color='red')
plt.plot(x, y2, color='black')
plt.legend(['y1', 'y2'])
plt.show()
```
![image](https://github.com/user-attachments/assets/fa176146-1212-4abe-9ad3-3e5b22cc2a15)
SPLINE CHART
```
# Spline Chart
import numpy as np
import matplotlib.pyplot as plt
from scipy.interpolate import make_interp_spline

x = np.array([1, 2, 3, 4, 5, 6, 7, 8, 9, 10])
y = np.array([2, 4, 5, 7, 8, 8, 9, 10, 11, 12])

# Interpolate data using cubic spline
spl = make_interp_spline(x, y)

# Define new x values for spline line
x_smooth = np.linspace(x.min(), x.max(), 100)

# Create spline line
y_smooth = spl(x_smooth)

# Plot original data and spline line
plt.plot(x, y, 'o', label='data')
plt.plot(x_smooth, y_smooth, '-', label='spline')
plt.legend()
plt.show()

```
![image](https://github.com/user-attachments/assets/245c7c67-a488-4934-b20b-18008b382727)
BAR CHART
```
#Bar graph
import matplotlib.pyplot as plt
values =[5,6,3,7,2]
names = ["A","B","C","D","E"]
plt.bar(names,values,color="green")
plt.show()
```
![image](https://github.com/user-attachments/assets/f60d6306-f9e4-4672-9f8f-a4d433d69760)
```
#Bar graph
import matplotlib.pyplot as plt
values =[5,6,3,7,2]
names = ["A","B","C","D","E"]
plt.barh(names,values,color="yellowgreen")
plt.show()
```
![image](https://github.com/user-attachments/assets/db94f1b3-8f87-4e51-b741-5af8c47c34ec)
```
import matplotlib.pyplot as plt
height =[10,24,36,40,5]
names = ['one','two','three','four','five']
c1 =['red','green']
c2 = ['b','g']
plt.bar(names,height,width=0.8,color=c1)
plt.xlabel('x - axis')
plt.ylabel('y - axis')
plt.title('My bar chart')
plt.show()
```
![image](https://github.com/user-attachments/assets/a9590822-df57-4aad-8f03-568e6baf0197)
SCATTER PLOT
```
#Scatter plots
import matplotlib.pyplot as plt
x_values = [0,1,2,3,4,5]
y_values = [0,1,4,9,16,25]
plt.scatter(x_values,y_values,s=30,color="blue")
```
![image](https://github.com/user-attachments/assets/990c1749-c940-4da0-919a-b9374bc3494f)
```
import matplotlib.pyplot as plt
x = [1,2,3,4,5,6,7,8,9,10]
y = [2,4,5,7,6,8,9,11,12,12]
plt.scatter(x,y,label="stars",color = "green",marker="*",s=30)
plt.xlabel('x - axis')
plt.ylabel('y-axis')
plt.title('My scatter plot')
plt.legend()
plt.show()
```
![image](https://github.com/user-attachments/assets/15984e13-1adf-4ab6-8303-f9c9552978d6)
HISTOGRAM
```
#Histogram
import matplotlib.pyplot as plt
ages = [2,5,70,40,30,45,50,45,43,40,44,60,7,13,57,18,90,77,32,21,20,40]
range =(0,100)
bins =10
plt.hist (ages,bins,range,color='green',histtype='bar',rwidth=0.8)
plt.xlabel('age')
plt.ylabel('NO of people')
plt.title('My histogram')
plt.show()
```
![image](https://github.com/user-attachments/assets/dafd2af5-4245-4fe0-8ff2-76e891ff9cae)
```
import matplotlib.pyplot as plt
x = [2,1,6,4,2,8,9,4,2,4,10,6,4,5,7,7,3,2,7,5,3,5,9,2,1]
plt.hist(x,bins= 10,color='blue',alpha=0.5)
plt.show()
```
![image](https://github.com/user-attachments/assets/acf2e6cf-72f2-40ac-ab1d-917d07d6b242)
BOX PLOT
```
import matplotlib.pyplot as plt
import numpy as np
np.random.seed(0)
data = np.random.normal(loc=0,scale =1,size=100)
data
fig, ax =plt.subplots()
ax.boxplot(data)
ax.set_xlabel('Data')
ax.set_ylabel('Values')
ax.set_title('Box Plot')
```
![image](https://github.com/user-attachments/assets/fcd25f0f-d1e3-43b6-bc02-35dfb2ff4048)
```
import matplotlib.pyplot as plt
activates = ['eat','sleep','work','play']
slice = [3,7,8,6]
colors = ['r','y','g','b']
plt.pie(slice,labels = activates ,colors = colors,startangle = 90,shadow = True,explode = (0,0,0.1,0),radius = 1.2,autopct = '%1.1f%%')
plt.legend()
plt.show()
```
![image](https://github.com/user-attachments/assets/9f76b678-0e5c-467e-beec-9b07c2b3bfe0)

# Result:
 Thus the given data visualization using matplot Library is executed successfully. 
