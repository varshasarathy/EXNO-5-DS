```
NAME : VARSHA SARATHY
REG NO : 212223040130
```

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
```
```
x = [1, 2, 3, 4, 5]
y = [3, 6, 2, 7, 1]
```
```
# CREATE A LINE GRAPH FOR X AND Y AND LABEL X axis and Y Axis and create a legend
plt.plot(x, y, label="Line 1")
plt.xlabel("X Axis")
plt.ylabel("Y Axis")
plt.legend()
plt.title("Line Graph for X and Y")
plt.show()
```
![image](https://github.com/user-attachments/assets/66208050-d2eb-4502-804b-0b8b3136e747)
```
# line 1 points
x1 = [1,2,3]
y1 = [2,4,1]
x2 = [1,2,3]
y2 = [4,1,3]
```
```
# plot line 1 and line 2 points in same graph and include the necessary parameters
plt.plot(x1, y1, label="Line 1", color="blue")
plt.plot(x2, y2, label="Line 2", color="orange")
plt.xlabel("X Axis")
plt.ylabel("Y Axis")
# plot the points in the above graph
plt.legend()
plt.title("Two Lines in One Graph")
plt.show()
```
![image](https://github.com/user-attachments/assets/45c30a51-9dd8-46ab-877c-856194582e01)
```
# Creating some random data
x = [1, 2, 3, 4, 5]
y1 = [10, 12, 14, 16, 18]
y2 = [5, 7, 9, 11, 13]
y3 = [2, 4, 6, 8, 10]
```
```
x_values = [0,1,2,3,4,5]
y_values = [0,1,4,9,16,25]
# implement line graph using fill between option
from scipy.interpolate import make_interp_spline
# interpolate data using cubic spline
plt.plot(x, y1, label="Line 1", color="red")
plt.plot(x, y2, label="Line 2", color="blue")
plt.plot(x, y3, label="Line 3", color="green")
plt.fill_between(x, y2, y3, color="grey", alpha=0.2)
plt.fill_between(x, y2, y1, color="pink", alpha=0.2)
plt.xlabel("X Axis")
plt.ylabel("Y Axis")
plt.legend()
plt.title("Line Graph with Fill Between")
plt.show()
```
![image](https://github.com/user-attachments/assets/bbea7981-7287-4d55-8dad-f4d3b0f43f0f)
```
values = [5, 6, 3, 7, 2]
names  = ["A", "B", "C", "D", "E"]
# Create bar graph using the above two variables and include the necessary parameters
plt.bar(names, values, color=['red', 'green', 'blue', 'yellow', 'purple'])
plt.xlabel("Categories")
plt.ylabel("Values")
# plot a bar chart
plt.title("Bar Graph")
plt.show()
```
![image](https://github.com/user-attachments/assets/0ee93ffa-f05c-46b4-b268-a00dccfb3cf4)
```
df = sns.load_dataset("tips")
df
```
![image](https://github.com/user-attachments/assets/c62ec21e-907a-4545-a472-df236724bdae)
```
# Calculate the average total bill and tip by day
avg_total_bill = df.groupby('day')['total_bill'].mean()
avg_tip = df.groupby('day')['tip'].mean()

plt.figure(figsize=(8, 6))
p1 = plt.bar(avg_total_bill.index, avg_total_bill, label='Total Bill')
p2 = plt.bar(avg_tip.index, avg_tip, bottom=avg_total_bill, label='Tip')
# Set the labels and title
plt.xlabel('Day of the Week')
plt.ylabel('Amount')
plt.title('Average Total Bill and Tip by Day')
plt.legend()
plt.show()
```
![image](https://github.com/user-attachments/assets/88449954-ea56-4f91-91ee-f4e1fc055de6)
```
x_values = [0,1,2,3,4,5]
y_values = [0,1,4,9,16,25]
# CREATE A SCATTER PLOT FOR X_VALUES AND Y_VALUES

# x-axis values
x = [1,2,3,4,5,6,7,8,9,10]
# y-axis values
y = [2,4,5,7,6,8,9,11,12,12]
# plot the above points x and y in scatter plot Using the parmeters label= "stars", color="green", marker="*", s=30
plt.scatter(x_values, y_values, label="stars", color="green", marker="*", s=30)
# set x-axis label and y axis label

plt.xlabel("X Axis")
plt.ylabel("Y Axis")
# set the title and legend of the graph
plt.title("Scatter Plot")
plt.legend()
plt.show()
```
![image](https://github.com/user-attachments/assets/44b6cdf0-b7aa-4eab-bf30-0f8b522fdf6b)
```
# defining labels
activities = ['eat', 'sleep', 'work', 'play']
# portion covered by each label
slices = [3, 7, 8, 6]
# color for each label
colors = ['r', 'y', 'g', 'b']
# plot the pie chart using above parameters

plt.pie(slices, labels=activities, colors=colors, startangle=90, autopct='%1.1f%%')
plt.title("Pie Chart")
plt.show()
```
![image](https://github.com/user-attachments/assets/8edfea86-c83a-4d66-9495-1dbfea45e1f6)


# Result:
 Thus, all the data visualization techniques of matplotlib has been implemented.
