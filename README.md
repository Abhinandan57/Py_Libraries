🔑 This repository contains the codes of important Python libraries for Data Science. The codes will be the part of my learning. 

The libraries are:  
🏷 NumPy  
🏷 Pandas  
🏷 SciPy  
🏷 Matplotlib  
🏷 Seaborn  
🏷 Plotly  
🏷 Scikit-Learn  
🏷 Bokeh  
🏷 Statsmodel  

# NumPy

- __NumPy (Numerical Python) is the foundational package for mathematical computing in Python.__
- It supports fast and efficient multidimensional arrays (ndarray).
- Executes element-wise computations and mathematical calculations.
- Performs linear algebraic operations, Fourier transforms and random number generation.
- It has tools for reading/writing array based datasets to disk.
- It has efficient way of storing and manipulating data.
- Numpy is a Python library, that supports a data container called Arrays. Arrays are like Lists but they can do something that Lists can't. They easily allow you to perform mathematical operations over the entire dataset.


# Pandas

- NumPy is great when it comes to mathematical computing. But it is still a low level tool when it comes to data munging. This is where Pandas prove useful as it uses NumPy and adds several more functionalities on top of it.
- Pandas is built on top of NumPy. Thus it is fast and efficient when it comes to data wrangling.
- Pandas includes features like intrinsic data alignment and offers data operation functions such as merge, groupby, join methods and so on, that makes it efficient for data wrangling and manipulation. It also offers functions for handling missing data values and is a great data standardization tool.

## Pandas Data structures:  
- Data structures are the basic building blocks that helps data scientists wrangle and analyze data. The 4 main libraries of Pandas data structure are:  
__(1) Series:__ One-dimensional array-like structure used to represent a dataset and can be visualized as a single row dataset. Supports multiple data types such as integer, string and float.  
__(2) DataFrame:__ Two-dimensional labeled array and can be visualized as a typical spreadsheet structure or a SQL database table with rows and columns. It also supports multiple data types such as integer, string, float etc and can be formed in many ways. A Series can be an input to a Data Frame. Another Data Frame can also be an input to it.  
__(3) Panel:__ Three-dimensional labeled array and supports multiple data types. It is mainly used to represent and wrangle three-dimensional datasets and can be visualized as x,y and z axis. Items -> axis 0, Major axis -> rows, Minor axis -> columns  
__(4) Panel 4D:__ Four-dimensional array and not very widely used. It is in experimental phase. 
- Series and DataFrame are the two main data structures which Data Scientists use to tackle real world problems.

### Series:

- Series is a one-dimensional array-like object containing data and labels(or index).
- __Data Types:__ Integer, String, Python Object, Floating Point
- Series can be created in multiple ways with the help of data elements which, if defined properly, act as data input to create a series. Therefore, __data input__ can be an ndarray, dict, scalar, list.
- An ndarray can be used as an input to create Pandas series. The use of ndarry is recommended wherever the dataset is number-centric and requires complex numerical computing.
- A Pandas series can also be created using dictionary and it is very efficient when it comes to indexing or reindexing a dataset for data wrangling purposes. dict works in a key-value fashion, so use it whenever the dataset is structured as key-value pair.
- Scalar data is another way to create Series. It is a stand-alone quantity and works with both vector and scalar datasets that can be used accordingly.
- List is another basic Python data structure which can act as an input to create Pandas series. List can hold a range of values of multiple data types. So if a dataset appears as a list, use list as input to create series.  
__Steps to create a series:__  
- Import Pandas as it is the main library: __import pandas as pd__
- When dealing with ndarray or other NumPy functions, import NumPy: __import numpy as np__
- Apply the syntax and pass the data elements as arguments
__Syntax to create series:__ S = pd.Series(data, index = [index])

### DataFrame:

- Data frame is a way to store data in rectangular grids that can easily be overviewed. Each row of these grids corresponds to measurements or values of an instance, while each column is a vector containing data for a specific variable. DataFrame is a two-dimensional labeled data structure with columns of potentially different data types.
- __Data Types:__ Integer, String, Python Object, Floating point
- __Data Inputs:__ ndarray, dict, list, Series, DataFrame


# SciPy

- __Scientific Python (SciPy) is an extension of NumPy for scientific and advanced mathematical algorithms and functions.__
- SciPy builds on NumPy and therefore if you import SciPy, there is no need to import NumPy.
- SciPy comes in useful to deal with the task of multiple domains of Scientific Domain such as Statistics, Spatial Data, Image Science, Mathematical Equations, Platform Integration, Signal Processing, Optimization. It's a Python library which has built-in packages such as Mathematics Integration, Linear algebra, Statistics, Language Integration, Multidimensional image processing.

__Characteristics of SciPy:__  
- It has a huge collection of built in mathematical libraries and functions to support complex scientific computations.
- High level commands for data manipulation and visualization.
- Efficient and fast data processing. Since it is built on top of NumPy, the data processing is extremely fast and efficient.
- Integrates well with multiple systems and environments.
- Large collection of sub-packages for different scientific domanins.
- Its developer friendly libraries and functions, simplifies scientific application development.


# Seaborn

__1. Numerical Data Ploting__
- relplot()
- scatterplot()
- lineplot()  

__2. Categorical Data Ploting__
- catplot()
- boxplot()
- stripplot()
- swarmplot()  

__3. Visualizing Distribution of the Data__
- distplot()
- kdeplot()
- jointplot()
- rugplot()  

__4. Linear Regression and Relationship__
- regplot()
- implot()  

__5. Controlling Ploted Figure Aesthetics__
- figure styling
- axes styling
- color palettes

## Univariate Analysis
- Univariate analysis is the simplest form of analysis where we explore a single variable.
- We perform Univariate analysis of Numerical and categorical variables differently because plotting uses different plots.

### Categorical Data:
__1. CountPlot__  
- Countplot is basically a count of frequency plot in form of a bar graph.
- It plots the count of each category in a separate bar.
- When we use the pandas’ value counts function on any column, it is the same visual form of the value counts function.

__2. Pie Chart__  
- The pie chart is also the same as the countplot, only gives you additional information about the percentage presence of each category in data means which category is getting how much weightage in data.

### Numerical Data
__1. Histogram__  
- A histogram is a value distribution plot of numerical columns.
- It basically creates bins in various ranges in values and plots it where we can visualize how values are distributed.
- We can have a look where more values lie like in positive, negative, or at the center(mean).

__2. Distplot__  
- Distplot is also known as the second Histogram because it is a slight improvement version of the Histogram.
- Distplot gives us a KDE(Kernel Density Estimation) over histogram which explains PDF(Probability Density Function) which means what is the probability of each value occurring in this column.

__3. Boxplot__  
- A box plot (or box-and-whisker plot) shows the distribution of quantitative data in a way that facilitates comparisons between variables or across levels of a categorical variable.
- The box shows the quartiles of the dataset while the whiskers extend to show the rest of the distribution, except for points that are determined to be “outliers” using a method that is a function of the inter-quartile range.

## Bivariate/ Multivariate Analysis
- Bivariate Analysis is used when we have to explore the relationship between 2 different variables and we have to do this because, in the end, our main task is to explore the relationship between variables to build a powerful model.
- When we analyze more than 2 variables together then it is known as Multivariate Analysis.

### Numerical and Numerical
__Scatter Plot__  
- To plot the relationship between two numerical variables scatter plot is a simple plot to do.

### Numerical and Categorical
__1. Bar Plot__  
- Bar plot is a simple plot which we can use to plot categorical variable on the x-axis and numerical variable on y-axis and explore the relationship between both variables.
- The blacktip on top of each bar shows the confidence Interval.

__2. Boxplot__  
- We can draw a separate boxplot for both the variable.

__3. Distplot__  
- Distplot explains the PDF function using kernel density estimation.

### Categorical and Categorical
__1. Heatmap__  
- It basically shows that how much presence of one category concerning another category present in the dataset.

__2. Cluster map__  
- We can also use a cluster map to understand the relationship between two categorical variables.
- A cluster map basically plots a dendrogram that shows the categories of similar behavior together.


# Plotly

Plotly is a library that allows you to create interactive plots that you can use in dashboards or websites.


# Scikit-Learn

- Scikit is a powerful and modern machine learning Python library. It a tool for fully and semi-automated data analysis and information extraction.
- It has efficient tools to identify and organize problems such as whether data fits supervised or unsupervised learning model.
- It contains many free and open datasets.
- It has a rich set of built-in libraries for learning and predicting.
- It provides model support for every problem type.
- It also has built-in functions such as pickle for Model persistence.
- It is supported by a huge open source community and vendor base.

__Scikit-Learn - Problem Solution Approach:__  
(1) __Model Selection:__ Choosing the model and machine algorithm based on the dataset type.  
(2) __Estimator Object:__ Using the __Estimator__ Object, which represents the model in Scikit-learn, by importing the class and instantiating it.  
(3) __Model Training:__ Fitting the data into the model to train and test it.  
(4) __Predictions:__ Using the __predict__ method to forcast the response of unseen or new dataset.  
(5) __Model Tuning:__ Tunning the model through multiple iterations and result observations .  
(6) __Accuracy:__ Striving for accuracy using built-in methods that supports the predictive model.
