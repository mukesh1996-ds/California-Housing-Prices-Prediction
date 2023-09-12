# California Housing Prices Prediction

### Work Flow:

1. Looking at the big picture
2. Get the data
3. Discover and Visualize the data to gain insights
4. Pipeline building 
5. Prepare dataset for Machine Learning algorithms 
6. Select a model and train it
7. Fine-tune the model


### Task:

* The first task you are asked to perform is to build a model of housing prices in California using the California census data. This data has metrics such as the population, median income, median housing price, and so on for each block group in California.

* Block groups are the smallest geographical unit for which the US Census Bureau publishes sample data (a block
group typically has a population of 600 to 3,000 people).

### Pipelines:

A sequence of data processing components is called a data pipeline. Pipelines are very common in Machine Learning systems, since there is a lot of data to manipulate and many data transformations to apply.

### Initial Understanding:

It is clearly a typical supervised learning task since you are given labeled training examples (each instance comes with the expected output, i.e., the district’s median housing price). Moreover, it is also a typical regression task, since you are asked to predict a value. More specifically, this is a multiple regression problem since the system will use multiple features to make a prediction (it will use the district’s population, the median income, etc.). It is also a univariate regression problem since we are only trying to predict a single value for each district.

If we were trying to predict multiple values per district, it would be a multivariate regression problem. Finally, there is no continuous flow of data coming in the system, there is no particular need to adjust to changing data rapidly, and the data is small enough to fit in memory, so plain batch learning should do just fine.

### Deciding Performance Measure:

* A typical performance measure for regression problems is the Root Mean Square Error (RMSE). It gives an idea of how much error the system typically makes in its predictions, with a higher weight for large errors.

![RMSE](https://github.com/mukesh1996-ds/California-Housing-Prices-Prediction/blob/main/Images/1%20(RMSE).png)

* Even though the RMSE is generally the preferred performance measure for regression tasks, in some contexts you may prefer to use another function. For example, suppose that there are many outlier districts. In that case, you may consider using the Mean Absolute Error (also called the Average Absolute Deviation

![MAE](https://github.com/mukesh1996-ds/California-Housing-Prices-Prediction/blob/main/Images/2%20(MAE).png)

