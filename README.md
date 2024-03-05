# Pandas

# Data Analysis:-
                Data analysis is a process of inspecting, cleansing, transforming, and modelling data with the goal of discovering useful information, informing conclusions, 
                and supporting decision-making.

# What is Pandas?
                ➤ The name "pandas" has a reference to both "panel data", and "python data analysis" and was created by wes mckinney in 2008.
                ➤ Pandas is a python library used for working with data sets.
                ➤ It has functions for analyzing, cleaning, exploring, and manipulating data.
                ➤ Read and write data structures and different formats: csv, XML, JSON,ZIP etc.

# Pandas Data Structures:
                Three Data Structures:
                            1. Series: One-Dimensional labeled arrays pd.Series(data)
                            2. DataFrames: Two-Dimensional data structure with columns, much like a table.
                            3. Panel: A panel is a 3D container of data.

# Series: 
        It is defined as a one-dimensional array that is capable of storing various data types.


'''Example: 1'''


import pandas as pd
a = pd.Series()
print(a)



'''Example: 2'''

import pandas as pd
x = [1,2,3,4,5]
var = pd.Series(x)
print(var)
print(type(var))
print(var[2])


Output:-
0    1
1    2
2    3
3    4
4    5
dtype: int64
<class 'pandas.core.series.Series'>
3


# Indexing:

import pandas as pd
x = [1,2,3,4,5]
var = pd.Series(x,index = ['i','ii','iii','iv','v'])
print(var)


Output:-
i      1
ii     2
iii    3
iv     4
v      5
dtype: int64



# dtype (float):

import pandas as pd
x = [1,2,3,4,5]
var = pd.Series(x,index = ['i','ii','iii','iv','v'],dtype = "float")
print(var)


Output:
i      1.0
ii     2.0
iii    3.0
iv     4.0
v      5.0
dtype: float64


# Series from a dictionary:

'''Example: 1'''

import pandas as pd

Testmatch = {"day1": 420, "day2": 380, "day3": 390}

var = pd.Series(Testmatch)

print(var)


Output:-
day1    420
day2    380
day3    390
dtype: int64


'''Example: 2'''


import pandas as pd
dic = {"Name":['Python','C','C++','Java'],"Rating":[10,4,6,8],"Rank":[1,4,3,2]}
var = pd.Series(dic)
print(var)


Output:
Name      [Python, C, C++, Java]
Rating             [10, 4, 6, 8]
Rank                [1, 4, 3, 2]
dtype: object
