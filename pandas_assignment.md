# PandasAssignment

Q1. How do you load a CSV file into a Pandas DataFrame?<br>
Ans.<br>
```
import pandas as pd
data = pd.read_csv("data.csv") 
```
Q2. How do you check the data type of a column in a Pandas DataFrame?<br>
Ans. <br>
```
import pandas as pd

data = {'Products': ['AAA','BBB','CCC','DDD','EEE'],
          'Prices': [200,700,400,1200,900]
        }

df = pd.DataFrame(data)
print (df.dtypes)
print (df['Prices'].dtypes)
```

Q3. How do you select rows from a Pandas DataFrame based on a condition?<br>
Ans.<br>
```
# importing pandas
import pandas as pd

record = {
'Name': ['Ankit', 'Amit', 'Aishwarya', 'Priyanka', 'Priya', 'Shaurya' ],
'Age': [21, 19, 20, 18, 17, 21],
'Stream': ['Math', 'Commerce', 'Science', 'Math', 'Math', 'Science'],
'Percentage': [88, 92, 95, 70, 65, 78]}

# create a dataframe
dataframe = pd.DataFrame(record, columns = ['Name', 'Age', 'Stream', 'Percentage'])

print("Given Dataframe :\n", dataframe)

# selecting rows based on condition
rslt_df = dataframe.loc[dataframe['Percentage'] != 95]

print('\nResult dataframe :\n', rslt_df)

```
Q4. How do you rename columns in a Pandas DataFrame?<br>
Ans.<br>
```
import pandas as pd
dictionary={ 'Name':['Hardik','Narendra'], 'Age':[25,52]}
df=pd.DataFrame(dictionary)
print("Dataframe before renaming")
print(df)
df.rename(columns={'Name':'FirstName'} , inplace=True)
print("Dataframe after renaming")
print(df)
```
output:<br>
```
PS C:\Users\Dell> & C:/Users/Dell/AppData/Local/Programs/Python/Python311/python.exe "c:/Users/Dell/OneDrive/Desktop/Ineuron Big Data Bootcamp/Python Assignment/python pandas assignment/pandas_assignment.py"
Dataframe before renaming
       Name  Age
0    Hardik   25
1  Narendra   52
Dataframe after renaming
  FirstName  Age
0    Hardik   25
1  Narendra   52
```
Q5. How do you drop columns in a Pandas DataFrame?<br>
Ans.<br>
```
import pandas as pd
dictionary={ 'Name':['Hardik','Narendra'], 'Age':[25,52]}
df=pd.DataFrame(dictionary)
df.drop(['Name'] , axis=1, inplace=True)
print(df)
```
Output:<br>
```
PS C:\Users\Dell> & C:/Users/Dell/AppData/Local/Programs/Python/Python311/python.exe "c:/Users/Dell/OneDrive/Desktop/Ineuron Big Data Bootcamp/Python Assignment/python pandas assignment/pandas_assignment.py"
   Age
0   25
1   52
```
Q6. How do you find the unique values in a column of a Pandas DataFrame?<br>
Ans.<br>
```
import pandas as pd
dictionary={ 'Name':['Hardik','Narendra','Hardik'], 'Age':[25,52,78]}
df=pd.DataFrame(dictionary)
print(df['Name'].unique())

```
Output:<br>
```
PS C:\Users\Dell> & C:/Users/Dell/AppData/Local/Programs/Python/Python311/python.exe "c:/Users/Dell/OneDrive/Desktop/Ineuron Big Data Bootcamp/Python Assignment/python pandas assignment/pandas_assignment.py"
['Hardik' 'Narendra']
```
Q7. How do you find the number of missing values in each column of a Pandas DataFrame?<br>
Ans.<br>
```
import pandas as pd
dictionary={ 'Name':['Hardik','Narendra','Hardik',None], 'Age':[25,52,None,78]}
df=pd.DataFrame(dictionary)
print(df.isna().sum())

```
Output:<br>
```
PS C:\Users\Dell> & C:/Users/Dell/AppData/Local/Programs/Python/Python311/python.exe "c:/Users/Dell/OneDrive/Desktop/Ineuron Big Data Bootcamp/Python Assignment/python pandas assignment/pandas_assignment.py"
Name    1
Age     1
dtype: int64
```

Q8. How do you fill missing values in a Pandas DataFrame with a specific value?<br>
Ans.we can use the fillna(),replace(),interpolate() function<br>
```
import pandas as pd
import numpy as np

dict = {'First Score':[100, 90, np.nan, 95],
		'Second Score': [30, 45, 56, np.nan],
		'Third Score':[np.nan, 40, 80, 98]}

# creating a dataframe from dictionary
df = pd.DataFrame(dict)

# filling missing value using fillna()
df.fillna(0,inplace=True)

```
Output:<br>
```
PS C:\Users\Dell> & C:/Users/Dell/AppData/Local/Programs/Python/Python311/python.exe "c:/Users/Dell/OneDrive/Desktop/Ineuron Big Data Bootcamp/Python Assignment/python pandas assignment/pandas_assignment.py"
   First Score  Second Score  Third Score
0        100.0          30.0          0.0
1         90.0          45.0         40.0
2          0.0          56.0         80.0
3         95.0           0.0         98.0
```

Q9. How do you concatenate two Pandas DataFrames?<br>
Ans. we can use concat function.<br>
```

import pandas as pd

data1 = {'d1_Name':['Tom', 'nick', 'krish', 'jack'],
        'd1_Age':[20, 21, 19, 18]}

data2 =  { 'd2_Name':['Hardik','Narendra','Hardik',None], 'd2_Age':[25,52,None,78]}

# creating a dataframe from dictionary
df1 = pd.DataFrame(data1)
df2 = pd.DataFrame(data2)
df3 = pd.concat([df1,df2] , axis=1)
print(df3)
```
output:<br>
```
PS C:\Users\Dell> & C:/Users/Dell/AppData/Local/Programs/Python/Python311/python.exe "c:/Users/Dell/OneDrive/Desktop/Ineuron Big Data Bootcamp/Python Assignment/python pandas assignment/pandas_assignment.py"
  d1_Name  d1_Age   d2_Name  d2_Age
0     Tom      20    Hardik    25.0
1    nick      21  Narendra    52.0
2   krish      19    Hardik     NaN
3    jack      18      None    78.0
```
Q10. How do you merge two Pandas DataFrames on a specific column?<br>
Ans. we can use merge()<br>
```
import pandas as pd

data1 = {'Name':['Hardik', 'Narendra', 'krish', 'jack'],
        'Age':[20, 21, 19, 18]}

data2 =  { 'Name':['Hardik','Narendra','krish',None], 'Age':[25,52,None,78]}

# creating a dataframe from dictionary
df1 = pd.DataFrame(data1)
df2 = pd.DataFrame(data2)

print(df1.merge(df2[['Name','Age']], on='Name' ,how='left'))
```
Output:<br>
```
PS C:\Users\Dell> & C:/Users/Dell/AppData/Local/Programs/Python/Python311/python.exe "c:/Users/Dell/OneDrive/Desktop/Ineuron Big Data Bootcamp/Python Assignment/python pandas assignment/pandas_assignment.py"
       Name  Age_x  Age_y
0    Hardik     20   25.0
1  Narendra     21   52.0
2     krish     19    NaN
3      jack     18    NaN
```

Q11. How do you group data in a Pandas DataFrame by a specific column and apply an aggregation function?<br>
Ans.<br>
```
import pandas as pd
data = {"Team": ["Red Sox", "Red Sox", "Red Sox", "Red Sox", "Red Sox", "Red Sox", "Yankees", "Yankees", "Yankees", "Yankees", "Yankees", "Yankees"],
		"Pos": ["Pitcher", "Pitcher", "Pitcher", "Not Pitcher", "Not Pitcher", "Not Pitcher", "Pitcher", "Pitcher", "Pitcher", "Not Pitcher", "Not Pitcher", "Not Pitcher"],
		"Age": [24, 28, 40, 22, 29, 33, 31, 26, 21, 36, 25, 31]}
df = pd.DataFrame(data)
# group by Team, get mean, min, and max value of Age for each value of Team.
grouped_single = df.groupby('Team').agg({'Age': ['mean', 'min', 'max']})

print(grouped_single)
```
Output:<br>
```
PS C:\Users\Dell> & C:/Users/Dell/AppData/Local/Programs/Python/Python311/python.exe "c:/Users/Dell/OneDrive/Desktop/Ineuron Big Data Bootcamp/Python Assignment/python pandas assignment/pandas_assignment.py"
               Age        
              mean min max
Team
Red Sox  29.333333  22  40
Yankees  28.333333  21  36
```
Q12. How do you pivot a Pandas DataFrame?<br>
Ans.<br>
```
import numpy as np
import pandas as pd
df = pd.DataFrame({'fff': ['one', 'one', 'one', 'two', 'two',
                           'two'],
                   'bbb': ['P', 'Q', 'R', 'P', 'Q', 'R'],
                   'baa': [2, 3, 4, 5, 6, 7],
                   'zzz': ['h', 'i', 'j', 'k', 'l', 'm']})
print(df.pivot(index='fff', columns='bbb', values='baa'))
```
Output:<br>
```
PS C:\Users\Dell> & C:/Users/Dell/AppData/Local/Programs/Python/Python311/python.exe "c:/Users/Dell/OneDrive/Desktop/Ineuron Big Data Bootcamp/Python Assignment/python pandas assignment/pandas_assignment.py"
bbb  P  Q  R
fff
one  2  3  4
two  5  6  7
```
Q13. How do you change the data type of a column in a Pandas DataFrame?<br>
Ans.<br>
```
import pandas as pd
dictionary={ 'Name':['Hardik','Narendra','Hardik'], 'Age':[25,52,78]}
df = pd.DataFrame(dictionary)
df = df.astype({'Age':float})
print(df['Age'].dtypes)

```
Output:<br>
```
PS C:\Users\Dell> & C:/Users/Dell/AppData/Local/Programs/Python/Python311/python.exe "c:/Users/Dell/OneDrive/Desktop/Ineuron Big Data Bootcamp/Python Assignment/python pandas assignment/pandas_assignment.py"
float64
```

Q14. How do you sort a Pandas DataFrame by a specific column?<br>
Ans.<br>
```
import pandas as pd
dictionary={ 'Name':['Hardik','Narendra','Hardik'], 'Age':[25,102,78]}
df = pd.DataFrame(dictionary)
print(df.sort_values('Age'))
```
Output:<br>
```
PS C:\Users\Dell> & C:/Users/Dell/AppData/Local/Programs/Python/Python311/python.exe "c:/Users/Dell/OneDrive/Desktop/Ineuron Big Data Bootcamp/Python Assignment/python pandas assignment/pandas_assignment.py"
       Name  Age
0    Hardik   25
2    Hardik   78
1  Narendra  102
```
Q15. How do you create a copy of a Pandas DataFrame?<br>
Ans.<br>
```
import pandas as pd
data = {
  "name": ["Hardik", "Jodha", "John"],
  "qualified": [True, False, False]
}

df = pd.DataFrame(data)
newdf = df.copy()

print(newdf)
```
Output:<br>
```
PS C:\Users\Dell> & C:/Users/Dell/AppData/Local/Programs/Python/Python311/python.exe "c:/Users/Dell/OneDrive/Desktop/Ineuron Big Data Bootcamp/Python Assignment/python pandas assignment/pandas_assignment.py"
     name  qualified
0  Hardik       True
1   Jodha      False
2    John      False
```

Q16. How do you filter rows of a Pandas DataFrame by multiple conditions?<br>
Ans.<br>
```
# import module
import pandas as pd
import numpy as np

# assign data
dataFrame = pd.DataFrame({'Name': [' RACHEL ', ' MONICA ', ' PHOEBE ',
								' ROSS ', 'CHANDLER', ' JOEY '],
						
						'Age': [30, 35, 37, 33, 34, 30],
						
						'Salary': [100000, 93000, 88000, 120000, 94000, 95000],
						
						'JOB': ['DESIGNER', 'CHEF', 'MASUS', 'PALENTOLOGY',
								'IT', 'ARTIST']})

# filter dataframe								
filtered_values = np.where((dataFrame['Salary']>=100000) & (dataFrame['Age']< 40) & (dataFrame['JOB'].str.startswith('D')))
print(filtered_values)
print(dataFrame.loc[filtered_values])

```
Output:<br>
```
PS C:\Users\Dell> & C:/Users/Dell/AppData/Local/Programs/Python/Python311/python.exe "c:/Users/Dell/OneDrive/Desktop/Ineuron Big Data Bootcamp/Python Assignment/python pandas assignment/pandas_assignment.py"
(array([0], dtype=int64),)
       Name  Age  Salary       JOB
0   RACHEL    30  100000  DESIGNER
```
Q17. How do you calculate the mean of a column in a Pandas DataFrame?<br>
Ans. we can calculate using df.mean(axis=1) function<br>

Q18. How do you calculate the standard deviation of a column in a Pandas DataFrame?<br>
Ans. we can use data_frame.std() function.<br>

Q19. How do you calculate the correlation between two columns in a Pandas DataFrame?<br>
Ans. we can calculate using .corr() function.<br>
syntax is:<br>
```
dataframe[‘first_column’].corr(dataframe[‘second_column’])
```
Code:<br>
```
# import pandas module
import pandas as pd

# create dataframe with 3 columns
data = pd.DataFrame({
	"column1": [12, 23, 45, 67],
	"column2": [67, 54, 32, 1],
	"column3": [34, 23, 56, 23]
}
)
# display dataframe
print(data)

# correlation between column 1 and column2
print(data['column1'].corr(data['column2']))

# correlation between column 2 and column3
print(data['column2'].corr(data['column3']))

# correlation between column 1 and column3
print(data['column1'].corr(data['column3']))
```
Output:<br>
```
 column1  column2  column3
0       12       67       34
1       23       54       23
2       45       32       56
3       67        1       23
-0.9970476685163736
0.07346999975265099
0.0
```
Q20. How do you select specific columns in a DataFrame using their labels?<br>
Ans.<br>
```
# import module
import pandas as pd
import numpy as np

# assign data
dataFrame = pd.DataFrame({'Name': [' RACHEL ', ' MONICA ', ' PHOEBE ',
								' ROSS ', 'CHANDLER', ' JOEY '],
						
						'Age': [30, 35, 37, 33, 34, 30],
						
						'Salary': [100000, 93000, 88000, 120000, 94000, 95000],
						
						'JOB': ['DESIGNER', 'CHEF', 'MASUS', 'PALENTOLOGY',
								'IT', 'ARTIST']})


print(dataFrame.loc[:,['Name','Salary']])

```
Output:<br>
```
PS C:\Users\Dell> & C:/Users/Dell/AppData/Local/Programs/Python/Python311/python.exe "c:/Users/Dell/OneDrive/Desktop/Ineuron Big Data Bootcamp/Python Assignment/python pandas assignment/pandas_assignment.py"
       Name  Salary
0   RACHEL   100000
1   MONICA    93000
2   PHOEBE    88000
3     ROSS   120000
4  CHANDLER   94000
5     JOEY    95000
```
Q21. How do you select specific rows in a DataFrame using their indexes?<br>
Ans. we can use "df.loc[start:stop:step]"<br>
```
# import module
import pandas as pd
import numpy as np

# assign data
dataFrame = pd.DataFrame({'Name': [' RACHEL ', ' MONICA ', ' PHOEBE ',
								' ROSS ', 'CHANDLER', ' JOEY '],
						
						'Age': [30, 35, 37, 33, 34, 30],
						
						'Salary': [100000, 93000, 88000, 120000, 94000, 95000],
						
						'JOB': ['DESIGNER', 'CHEF', 'MASUS', 'PALENTOLOGY',
								'IT', 'ARTIST']})
print(dataFrame.loc[1:5])
```
Output:<br>
```
PS C:\Users\Dell> & C:/Users/Dell/AppData/Local/Programs/Python/Python311/python.exe "c:/Users/Dell/OneDrive/Desktop/Ineuron Big Data Bootcamp/Python Assignment/python pandas assignment/pandas_assignment.py"
       Name  Age  Salary          JOB
1   MONICA    35   93000         CHEF
2   PHOEBE    37   88000        MASUS
3     ROSS    33  120000  PALENTOLOGY
4  CHANDLER   34   94000           IT
5     JOEY    30   95000       ARTIST
```
Q22. How do you sort a DataFrame by a specific column?<br>
Ans.<br>
```
import pandas as pd
import numpy as np
# assign data
dataFrame = pd.DataFrame({'Name': [' RACHEL ', ' MONICA ', ' PHOEBE ',
								' ROSS ', 'CHANDLER', ' JOEY '],
						'Age': [30, 35, 37, 33, 34, 30],
						'Salary': [100000, 93000, 88000, 120000, 94000, 95000],
						'JOB': ['DESIGNER', 'CHEF', 'MASUS', 'PALENTOLOGY',
								'IT', 'ARTIST']})
print(dataFrame.sort_values(by=['Age']))
```
Output:<br>
```
PS C:\Users\Dell> & C:/Users/Dell/AppData/Local/Programs/Python/Python311/python.exe "c:/Users/Dell/OneDrive/Desktop/Ineuron Big Data Bootcamp/Python Assignment/python pandas assignment/pandas_assignment.py"
       Name  Age  Salary          JOB
0   RACHEL    30  100000     DESIGNER
5     JOEY    30   95000       ARTIST
3     ROSS    33  120000  PALENTOLOGY
4  CHANDLER   34   94000           IT
1   MONICA    35   93000         CHEF
2   PHOEBE    37   88000        MASUS
```

Q23. How do you create a new column in a DataFrame based on the values of another column?<br>
Ans. we can use .assign() method and much more ways to do it.<br>
```
import pandas as pd
import numpy as np
# assign data
dataFrame = pd.DataFrame({'Name': [' RACHEL ', ' MONICA ', ' PHOEBE ',
								' ROSS ', 'CHANDLER', ' JOEY '],
						'Age': [30, 35, 37, 33, 34, 30],
						'Salary': [100000, 93000, 88000, 120000, 94000, 95000],
						'JOB': ['DESIGNER', 'CHEF', 'MASUS', 'PALENTOLOGY',
								'IT', 'ARTIST']})
df1=dataFrame.assign(CTC = lambda x: x.Salary - 4000)
print(df1)
```
Output:<br>
```
PS C:\Users\Dell> & C:/Users/Dell/AppData/Local/Programs/Python/Python311/python.exe "c:/Users/Dell/OneDrive/Desktop/Ineuron Big Data Bootcamp/Python Assignment/python pandas assignment/pandas_assignment.py"
       Name  Age  Salary          JOB     CTC
0   RACHEL    30  100000     DESIGNER   96000
1   MONICA    35   93000         CHEF   89000
2   PHOEBE    37   88000        MASUS   84000
3     ROSS    33  120000  PALENTOLOGY  116000
4  CHANDLER   34   94000           IT   90000
5     JOEY    30   95000       ARTIST   91000
```

Q24. How do you remove duplicates from a DataFrame?<br>
Ans. we can use drop_duplicates() function.<br>
```
import pandas as pd
import numpy as np
# assign data
dataFrame = pd.DataFrame({'Name': [' RACHEL ', ' ROSS ', ' PHOEBE ',
								' ROSS ', 'CHANDLER', ' ROSS ',],
						'Age': [30, 35, 37, 33, 34, 30],
						'Salary': [100000, 93000, 88000, 120000, 94000, 95000],
						'JOB': ['DESIGNER', 'CHEF', 'MASUS', 'PALENTOLOGY',
								'IT', 'ARTIST']})
dataFrame.drop_duplicates(subset = 'Name', inplace = True)
print(dataFrame)
```
Output:<br>
```
PS C:\Users\Dell> & C:/Users/Dell/AppData/Local/Programs/Python/Python311/python.exe "c:/Users/Dell/OneDrive/Desktop/Ineuron Big Data Bootcamp/Python Assignment/python pandas assignment/pandas_assignment.py"
       Name  Age  Salary       JOB
0   RACHEL    30  100000  DESIGNER
1     ROSS    35   93000      CHEF
2   PHOEBE    37   88000     MASUS
4  CHANDLER   34   94000        IT
```

Q25. What is the difference between .loc and .iloc in Pandas?<br>
Ans. The loc and iloc functions in Pandas are used to slice a data set. The function .loc is primarily used for label indexing, while .iloc is mainly used for integer indexing.<br>