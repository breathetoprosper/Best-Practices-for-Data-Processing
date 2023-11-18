#Best Practices for Pre-Processing Data for Machine Learning Models .by Diogo Marques 2023

Before jumping directly to coding, you need to first ask: 
1. What is the specific outcome of what you are doing? What is it that you want to know?

->The more specific you are in your questions and what is it that you are trying to achieve, it will be most useful to you so you can successfully complete the project.

Then this is required:

2. Data needs to be subject to transformation so you can be able to use statistical methods on it.
    #Step 1 - deciding if it is linear or not How?
            Scatter Plots:
                Begin by creating scatter plots of the variables of interest. Assess the shape of the relationship between the variables. If the points form a straight line, it suggests a linear relationship. If the relationship is more complex, it may be non-linear.
            Residual Analysis
                Fit a linear regression model to the data and examine the residuals (differences between observed and predicted values). A random scattering of residuals around zero supports a linear relationship, while patterns in residuals might indicate non-linearity.
            Correlation Coefficient:
                Calculate the correlation coefficient between the variables. A high absolute value suggests a strong linear relationship. However, low correlation doesn't necessarily rule out non-linear relationships.
            Polynomial Regression:
                Fit polynomial regression models of different degrees (e.g., quadratic, cubic) and assess the goodness of fit. Higher-degree polynomials can capture non-linear patterns.
            Q-Q Plots and Histograms:
                Create Q-Q plots and histogra 2, ms to examine the distribution of the variables. Deviations from normality may suggest non-linear transformations.
            Domain Knowledge:
                Consider domain knowledge. If there are known non-linearities in the underlying processes, it might guide your choice of transformations.
            Local Regression (LOESS):
                Apply local regression (LOESS) to visualize trends in the data. LOESS can reveal non-linear patterns without assuming a specific functional form.
            Nonlinear Regression:
                Fit non-linear regression models and compare their fit to linear models. Assess whether a more complex non-linear model significantly improves the fit.
            Interaction Terms:
                In regression analysis, include interaction terms between variables to capture potential non-linear interactions.

            Iterative Analysis:
                Perform an iterative analysis, trying different transformations and models to see which approach provides the best fit and aligns with the nature of the data.
     
    #Step 2: After knowing this we decide on the linear or non-linear method to apply the transformation, depending which one the dataset is:
     1. linear
        either one of these:
        1. Log transformation
        2. Square Root Transformation
        3. Box-Cox Transformation
    2. non-linear
        1. log transformation
        2. square Root Transformation
        3. Box-Cox Transformation
        4. Exponential Transformation
        5. Power Transformation
        6. Arcsine Transformation
        7. Inverse Transformation
        

3. After being transformed:
    Visualize the transformed data to confirm desired effects, ensuring improved linearity or normality

4. Scale it
    1. standardization (Z-score normalization)
    2. Min-Max scaling (rescaling to a specific range)
    3. robust scaling (medians and interquartile ranges)
    4. max-abs scaling (scaling by the maximum absolute value)
   
   
5a. Finally, if you are training a Machine Leaning model, this is where the model implementation kicks in.

5b. If the purpose of the work is data analytics, you can now conduct the multivariate test and draw conclusions.

Conclusion: This serves as a framework to help send the data first through a "box" so you can then use it for what you want.

Happy coding!.