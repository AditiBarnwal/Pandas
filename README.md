# Pandas

1. Fast and efficient for manipulating and analyzing data.
2. Data from different file objects can be loaded.
3. Easy handling of missing data (represented as NaN) in floating point as well as non-floating point data
4. Size mutability: columns can be inserted and deleted from DataFrame and higher dimensional objects
5. Data set merging and joining.
6. Flexible reshaping and pivoting of data sets
7. Provides time-series functionality.
8. Powerful group by functionality for performing split-apply-combine operations on data sets.

💭 Why Pandas is used for Data Science?

***This is because pandas are used in conjunction with other libraries that are used for data science. It is built on the top of the NumPy library which means that a lot of structures of NumPy are used or replicated in Pandas. The data produced by Pandas are often used as input for plotting functions of Matplotlib, statistical analysis in SciPy, and machine learning algorithms in Scikit-learn.***

# Introduction
Pandas has two data structures for manipulating data, They are: 
- `Series`
- `DataFrame`

Series: 1D Array capable of holding data of any type(integer, string, float, python objects, etc.).The axis labels are collectively called indexes.Pandas Series is nothing but a column in an excel sheet.Pandas Series can be created from the lists, dictionary, and from a scalar value etc.

Binary operation methods on series:

FUNCTION	DESCRIPTION
- add()	Method is used to add series or list like objects with same length to the caller series
- sub()	Method is used to subtract series or list like objects with same length from the caller series
- mul()	Method is used to multiply series or list like objects with same length with the caller series
- div()	Method is used to divide series or list like objects with same length by the caller series
- sum()	Returns the sum of the values for the requested axis
- prod()	Returns the product of the values for the requested axis
- mean()	Returns the mean of the values for the requested axis
- pow()	Method is used to put each element of passed series as exponential power of caller series and returned the results
- abs()	Method is used to get the absolute numeric value of each element in Series/DataFrame
- cov()	Method is used to find covariance of two series
 
Pandas series method:

FUNCTION	DESCRIPTION
- Series()	A pandas Series can be created with the Series() constructor method. This constructor method accepts a variety of inputs
- combine_first()	Method is used to combine two series into one
- count()	Returns number of non-NA/null observations in the Series
- size()	Returns the number of elements in the underlying data
- name()	Method allows to give a name to a Series object, i.e. to the column
- is_unique()	Method returns boolean if values in the object are unique
- idxmax()	Method to extract the index positions of the highest values in a Series
- idxmin()	Method to extract the index positions of the lowest values in a Series
- sort_values()	Method is called on a Series to sort the values in ascending or descending order
- sort_index()	Method is called on a pandas Series to sort it by the index instead of its values
- head()	Method is used to return a specified number of rows from the beginning of a Series. The method returns a brand new Series
- tail()	Method is used to return a specified number of rows from the end of a Series. The method returns a brand new Series
- le()	Used to compare every element of Caller series with passed series.It returns True for every element which is Less than or Equal to the element in passed series
- ne()	Used to compare every element of Caller series with passed series. It returns True for every element which is Not Equal to the element in passed series
- ge()	Used to compare every element of Caller series with passed series. It returns True for every element which is Greater than or Equal to the element in passed series
- eq()	Used to compare every element of Caller series with passed series. It returns True for every element which is Equal to the element in passed series
- gt()	Used to compare two series and return Boolean value for every respective element
- lt()	Used to compare two series and return Boolean value for every respective element
- clip()	Used to clip value below and above to passed Least and Max value
- clip_lower()	Used to clip values below a passed least value
- clip_upper()	Used to clip values above a passed maximum value
- astype()	Method is used to change data type of a series
- tolist()	Method is used to convert a series to list
- get()	Method is called on a Series to extract values from a Series. This is alternative syntax to the traditional bracket syntax
- unique()	Pandas unique() is used to see the unique values in a particular column
- nunique()	Pandas nunique() is used to get a count of unique values
- value_counts()	Method to count the number of the times each unique value occurs in a Series
- factorize()	Method helps to get the numeric representation of an array by identifying distinct values
- map()	Method to tie together the values from one object to another
- between()	Pandas between() method is used on series to check which values lie between first and second argument
- apply()	Method is called and feeded a Python function as an argument to use the function on every Series value. This method is helpful for executing custom operations that are not included in pandas or numpy

DataFrame: 2D size-mutable, heterogeneous tabular data structure with labeled axes (rows and columns).2D data structure, i.e., data is aligned in a tabular fashion in rows and columns.3Components of Dataframe: data, rows, and columns.

Syntax:     `pandas.DataFrame(data, index, columns)`
where,

 - data: It is a dataset from which dataframe is to be created. It can be list, dictionary, scalar value, series, ndarrays, etc.
 - index: optional, index starts from 0 and ends at the last data value(n-1). It defines the row label explicitly.
 - columns: provide column names in the dataframe. If the column name is not defined by default, it will take a value from 0 to n-1.

DataFrame Methods:

FUNCTION	DESCRIPTION
index()	Method returns index (row labels) of the DataFrame

insert()	Method inserts a column into a DataFrame

add()	Method returns addition of dataframe and other, element-wise (binary operator add)

sub()	Method returns subtraction of dataframe and other, element-wise (binary operator sub)

mul()	Method returns multiplication of dataframe and other, element-wise (binary operator mul)

div()	Method returns floating division of dataframe and other, element-wise (binary operator truediv)

unique()	Method extracts the unique values in the dataframe

nunique()	Method returns count of the unique values in the dataframe

value_counts()	Method counts the number of times each unique value occurs within the Series

columns()	Method returns the column labels of the DataFrame

axes()	Method returns a list representing the axes of the DataFrame

isnull()	Method creates a Boolean Series for extracting rows with null values

notnull()	Method creates a Boolean Series for extracting rows with non-null values

between()	Method extracts rows where a column value falls in between a predefined range

isin()	Method extracts rows from a DataFrame where a column value exists in a predefined collection

dtypes()	Method returns a Series with the data type of each column. The result’s index is the original DataFrame’s columns

astype()	Method converts the data types in a Series

values()	Method returns a Numpy representation of the DataFrame i.e. only the values in the DataFrame will be returned, the axes labels will be removed

sort_values()- Set1, Set2	Method sorts a data frame in Ascending or Descending order of passed Column

sort_index()	Method sorts the values in a DataFrame based on their index positions or labels instead of their values but sometimes a data frame is made out of two or 
more data frames and hence later index can be changed using this method

loc[]	Method retrieves rows based on index label

iloc[]	Method retrieves rows based on index position

ix[]	Method retrieves DataFrame rows based on either index label or index position. This method combines the best features of the .loc[] and .iloc[] methods

rename()	Method is called on a DataFrame to change the names of the index labels or column names

columns()	Method is an alternative attribute to change the coloumn name

drop()	Method is used to delete rows or columns from a DataFrame

pop()	Method is used to delete rows or columns from a DataFrame

sample()	Method pulls out a random sample of rows or columns from a DataFrame

nsmallest()	Method pulls out the rows with the smallest values in a column

nlargest()	Method pulls out the rows with the largest values in a column

shape()	Method returns a tuple representing the dimensionality of the DataFrame

ndim()	Method returns an ‘int’ representing the number of axes / array dimensions.
Returns 1 if Series, otherwise returns 2 if DataFrame

dropna()	Method allows the user to analyze and drop Rows/Columns with Null values in different ways

fillna()	Method manages and let the user replace NaN values with some value of their own

rank()	Values in a Series can be ranked in order with this method

query()	Method is an alternate string-based syntax for extracting a subset from a DataFrame

copy()	Method creates an independent copy of a pandas object

duplicated()	Method creates a Boolean Series and uses it to extract rows that have duplicate values

drop_duplicates()	Method is an alternative option to identifying duplicate rows and removing them through filtering

set_index()	Method sets the DataFrame index (row labels) using one or more existing columns

reset_index()	Method resets index of a Data Frame. This method sets a list of integer ranging from 0 to length of data as index

where()	Method is used to check a Data Frame for one or more condition and return the result accordingly. By default, the rows not satisfying the condition are filled with NaN value 
[Click here to see example](https://www.geeksforgeeks.org/python-pandas-dataframe/) 

# Creating Objects
# Viewing Data

Pandas head() method is used to return top n rows of a data frame or series.

Syntax: `Dataframe.head(n=5)`

Pandas tail() method is used to return bottom n (5 by default) rows of a data frame or series.

Syntax: `Dataframe.tail(n=5)`

`Parameters:-n: integer value, number of rows to be returned`

Pandas describe() is used to view some basic statistical details like percentile, mean, std etc. of a data frame or a series of numeric values. When this method is applied to a series of string, it returns a different output which is shown in the examples below.

Syntax: `DataFrame.describe(percentiles=None, include=None, exclude=None)`

     Parameters:
           - percentile: list like data type of numbers between 0-1 to return the respective percentile
           - include: List of data types to be included while describing dataframe. Default is None
           - exclude: List of data types to be Excluded while describing dataframe. Default is None

Data structure can be converted to NumPy ndarray with the help of the DataFrame.to_numpy() method. In this article we will see how to convert dataframe to numpy array.

Syntax of Pandas DataFrame.to_numpy()
Syntax: `Dataframe.to_numpy(dtype = None, copy = False) `

         Parameters: 

              - dtype: Data type which we are passing like str. 
              - copy: [bool, default False] Ensures that the returned value is a not a view on another array.
Returns: numpy.ndarray 

Pandas Series.as_matrix() function is used to convert the given series or dataframe object to Numpy-array representation.

Syntax: `Series.as_matrix(columns=None)`

        Parameter :
          - columns : If None, return all columns, otherwise, returns specified columns.

# Selection
### How to select multiple columns in a pandas dataframe
Problem related to Columns:
 
1.How to get column names in Pandas dataframe
2.How to rename columns in Pandas DataFrame
3.How to drop one or multiple columns in Pandas Dataframe
4.Get unique values from a column in Pandas DataFrame
5.How to lowercase column names in Pandas dataframe
6.Apply uppercase to a column in Pandas dataframe
7.Capitalize first letter of a column in Pandas dataframe
8.Get n-largest values from a particular column in Pandas DataFrame
9.Get n-smallest values from a particular column in Pandas DataFrame
10.Convert a column to row name/index in Pandas

Problem related to Rows:

1.Apply function to every row in a Pandas DataFrame
2.How to get rows names in Pandas dataframe
### Dealing with Rows and Columns in Pandas DataFrame
### How to select multiple columns in a pandas dataframe
### Python | Pandas Extracting rows using .loc[]
### Python | Extracting rows using Pandas .iloc[]
### Indexing and Selecting Data with Pandas
### Boolean Indexing in Pandas
### Label and Integer based slicing technique using DataFrame.ix[ ]

# Manipulating Data

# Grouping Data
 In real data science projects, you’ll be dealing with large amounts of data and trying things over and over, so for efficiency, we use Groupby concept. Groupby concept is really important because it’s ability to aggregate data efficiently, both in performance and the amount code is magnificent. Groupby mainly refers to a process involving one or more of the following steps they are: 
 🔆 Splitting : It is a process in which we split data into group by applying some conditions on datasets.
 🔆 Applying : It is a process in which we apply a function to each group independently
 🔆 Combining : It is a process in which we combine different datasets after applying groupby and results into a data structure

Grouping Rows in pandas

Combining multiple columns in Pandas groupby with dictionary

# Merging, Joining and Concatenating

-Python | Pandas Merging, Joining, and Concatenating
-Concatenate Strings
-Append rows to Dataframe
-Concatenate two or more series
-Append a single or a collection of indices
-Combine two series into one
-Add a row at top in pandas DataFrame
-Join all elements in list present in a series
-Join two text columns into a single column in Pandas

# Working with Date and Time

- Timestamp using Pandas
- Current Time using Pandas
- Convert timestamp to ISO Format
- Get datetime object using Pandas
- Replace the member values of the given Timestamp
- Convert string Date time into Python Date time object using Pandas
- Get a fixed frequency DatetimeIndex using Pandas
# Working With Text Data

💢 Pandas.apply()

**Pandas.apply allow the users to pass a function and apply it on every single value of the Pandas series. It comes as a huge improvement for the pandas library as this function helps to segregate data according to the conditions required due to which it is efficiently used in data science and machine learning.**
Syntax:   `s.apply(func, convert_dtype=True, args=())`
Parameters:

-func: .apply takes a function and applies it to all values of pandas series.
-convert_dtype: Convert dtype as per the function’s operation.
-args=(): Additional arguments to pass to function instead of series.
-Return Type: Pandas Series after applied function/operation.

▪ Apply function to every row in a Pandas DataFrame
▪ Apply a function on each element of the series
▪ Aggregation data across one or more column
▪ Mean of the values for the requested axis
▪ Mean of the underlying data in the Series
▪ Mean absolute deviation of the values for the requested axis
▪ Mean absolute deviation of the values for the Series
▪ Unbiased standard error of the mean
▪ Find the Series containing counts of unique values
▪ Find the Series containing counts of unique values using Index.value_counts()

# Working with CSV and Excel files
# Operations
# Visualization

**Data Visualization is the presentation of data in graphical format. It helps people understand the significance of data by summarizing and presenting a huge amount of data in a simple and easy-to-understand format and helps communicate information clearly and effectively.**

Using built-in data visualization feature in pandas by plotting different types of charts.

Plot Types –
There are several plot types built-in to pandas, most of them statistical plots by nature:

`df.plot.area` `df.plot.barh` `df.plot.density` `df.plot.hist` `df.plot.line``df.plot.scatter` `df.plot.bar` `df.plot.box` `df.plot.hexbin` `df.plot.kde` `df.plot.pie`

You can also just call df.plot(kind='hist') or replace that kind argument with any of the key terms shown in the list above (e.g. ‘box’, ‘barh’, etc.).

#### Box plot visualization with Pandas and Seaborn

***Box Plot is the visual representation of the depicting groups of numerical data through their quartiles. Boxplot is also used for detect the outlier in data set. It captures the summary of the data efficiently with a simple box and whiskers and allows us to compare easily across groups. Boxplot summarizes a sample data using 25th, 50th and 75th percentiles. These percentiles are also known as the lower quartile, median and upper quartile.***

A box plot consist of 5 things.

- Minimum
- First Quartile or 25%
- Median (Second Quartile) or 50%
- Third Quartile or 75%
- Maximum

Draw the boxplot using seaborn library:

Syntax :
`seaborn.boxplot(x=None, y=None, hue=None, data=None, order=None, hue_order=None, orient=None, color=None, palette=None, saturation=0.75, width=0.8, dodge=True, fliersize=5, linewidth=None, whis=1.5, notch=False, ax=None, **kwargs)`

Parameters:
-x = feature of dataset
-y = feature of dataset
-hue = feature of dataset
-data = dataframe or full dataset
-color = color name

# Projects
