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


# Named Indexes:

import pandas as pd

data = {"calories": [420, 380, 390],"duration": [50, 40, 45]}

df = pd.DataFrame(data, index = ["day1", "day2", "day3"])

print(df) 



Output:-
         calories  duration
day1       420        50
day2       380        40
day3       390        45



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


'''Example: 3'''

import pandas as pd
dic = {"Name":['Python','C','C++','Java'],"Rating":[10,4,6,8],"Rank":[1,4,3,2]}
var = pd.Series(dic)
print(var)
s = pd.Series(10,index = [1,2,3,4,5])
print(s)


Output:-
Name      [Python, C, C++, Java]
Rating             [10, 4, 6, 8]
Rank                [1, 4, 3, 2]
dtype: object
1    10
2    10
3    10
4    10
5    10
dtype: int64



'''Example: 4'''

import pandas as pd

data = {"calories": [420, 380, 390],"duration": [50, 40, 45]}

var = pd.DataFrame(data)

print(var)



Output:-
      calories  duration
0       420        50
1       380        40
2       390        45


# ADD s1+s2

import pandas as pd
s1 = pd.Series(10,index = [1,2,3,4,5])
s2 = pd.Series(10,index = [1,2,3])
print(s1+s2)


Output:-
1    20.0
2    20.0
3    20.0
4     NaN
5     NaN
dtype: float64




# DataFrames in Pandas:
                   A Pandas DataFrame is a 2-dimensional data structure, like a 2 dimensional array, or a table with rows and columns.




'''Example: 1'''

import pandas as pd
l = [1,2,3,4,5]
var = pd.DataFrame(l)
print(var)
print(type(var))


Output:-
   0
0  1
1  2
2  3
3  4
4  5
<class 'pandas.core.frame.DataFrame'>



'''Example: 2'''

import pandas as pd
d = {"Name":["Shivanshi","Radha","Shivansh"],"TM":[1000,2000,3000]}
var = pd.DataFrame(d)
print(var)


Output:-
      Name    TM
0  Shivanshi  1000
1      Radha  2000
2   Shivansh  3000







Indexing:- 

import pandas as pd
d = {"Name":["Shivanshi","Radha","Shivansh"],"TM":[1000,2000,3000]}
var = pd.DataFrame(d,index = ['a','b','c'])
print(var)


Output:-
        Name    TM
a  Shivanshi  1000
b      Radha  2000
c   Shivansh  3000




'''Example: 3'''

import pandas as pd
d = {"Name":["Shivanshi","Radha","Shivansh"],"TM":[1000,2000,3000]}
var = pd.DataFrame(d,index = ['a','b','c'])
#print(var)
print(var["Name"])


Output:-
a    Shivanshi
b        Radha
c     Shivansh
Name: Name, dtype: object


'''Example: 4'''

import pandas as pd
list = [[1,2,3,4,5],[11,12,13,14,15],[11,22,33,44,55]]
var = pd.DataFrame(list)
print(var)


Output:-
    0   1   2   3   4
0   1   2   3   4   5
1  11  12  13  14  15
2  11  22  33  44  55






'''Example: 5'''


import pandas as pd
sr = {"s":pd.Series([1,2,3,4]),"r":pd.Series([5,6,7,8])}
var = pd.DataFrame(sr)
print(var)


Output:-
   s  r
0  1  5
1  2  6
2  3  7
3  4  8





# Arithmetic Operators in Python Pandas:-
