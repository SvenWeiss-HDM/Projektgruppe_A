### Peer review team

- Peer review by: **Group A**
- Names of team members that participated in this review: Alexander Benz, Lukas Zaiser, Sven Weiß

### Goal of the project

- Give answers to the following research questions:
    -  Does the longer average annual working hours increase labor productivity? (rephrase like :"is there a correlation between working hours and labor productivity?")
    -  What is the most related factor in improving labor productivity?

### Data

- Data has:
    - 9 features, one target variable
    - 66 observartions
<br>
<br>
- Remarks:
    - We feel that the quantity of observations will not suffice (at least 500 Obsevations required) to train the model properly
    - There is no data dictionary in the analysis (only in proposal)
    - Raw data seems to fit time series analysis better than regression (you need to clarify why you only chose year 2017)
    - Explain why you took GDP as productivity factor, as GDP and productivity has an obvious correlation

### Approach, tools and methods

- Describe the approaches, tools, and methods that will be used.
    - Continent was set as categorial (why not country?)
    - Dropped NaN values for the complete dataset and went from 66 to 47 observations. :(
    - Singular regression was done for first research question
    - Scatterplot of Average annual working hours per worker and productivity clearly displays a negative correlation
    - Linear Regression and KNN were used as models
    - Cross val score for all models looks really unstable
    - Relationships are not linear in all cases, some (esp. life statisfaction and productivity are definetely not, should use splines)
    - Difference between MSE and RMSE seem to be way off

### Lack of clarity

- Overall, it would be **very helpful** to have a short explanation for each code cell
- OLS and the regression model have nothing to do with each other --> explain what you do with statsmodels
- Is it sensible to check for statistically significant with 47 observations?

### Possible improvements

- Add the null hypothesises for your questions?
- Please explain why and how you use which model?
- Explain the outcomes and interpret what the results mean in the real world (e.g. working 0 hours results in 170 BIP.. not really)
- You check for multicolinearity - draw some conclutions
- Reflect on how good models are performing and give possible solutions

### Presentation

- Explain how you collected the data and why you took it
- Describe each feature and what it means, because this is really essential and hard to get (e.g. *Gini score*)
- Display the Pairplots with the regression lines and explain correlations

### Organization

- Rename variables to be better aligned (`gini_coefficient` is different than `Average annual working hours per worker`), maybe remove white spaces in variable names
  
### Further comments

- Elaborate a bit more on the motivation of this project
- Be carefull when using productivity, explain why the GDP matters as a productivty indicator to be set in relation with hours.
- Make sure that the values you compare are in fact comparable (GDP *per capita*, hours *per worker*)
- How is life satisfaction measured? Why did you choose life satisfaction? How can you be sure that the data is collected correctly?