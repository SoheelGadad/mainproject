# nodejsworkshopon

import pandas as pd
import matplotlib.pyplot as plt

#To read file
data=pd.read_csv('C:\\Users\\mujahidxec\\Desktop\\DStest\\Book1.csv')
print(data)
# to remove index filecolumn
data=pd.read_csv('C:\\Users\\mujahidxec\\Desktop\\DStest\\Book1.csv',index_col=0)
print(data)
# to replace missing value(??,???? with nan values)
data=pd.read_csv('C:\\Users\\mujahidxec\\Desktop\\DStest\\Book1.csv',index_col=0, na_values=["??","????"])
print(data)
# to print scatter graph
plt.scatter(data['Class'], data['Percentage']) 
plt.xlabel('Class')
plt.ylabel('Percentage')
# bar graph
x=data['Class']
y=data['Percentage']
plt.bar(x,y,color=['red','green'])


print(data['Percentage'].mean()) # prints mean 
print(data['Percentage'].mode()) # prints mode

print(data.head(2))# print first 2 lines
# print last 2 lines
print(data.tail(2))

# to print information
data.info()
# to print rows and column
data.shape
      # to print all the columns
data.columns

plt.show