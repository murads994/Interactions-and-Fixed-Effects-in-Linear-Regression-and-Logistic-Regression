# Interactions in Regression, Fixed Effects in Regression and Logistic Regression

In this project, we will be exploring the effects of interaction in Linear Regression and Logistic Regression. We will be going over how to interpret the coefficients of the interaction terms, and will also be looking at how they effect the model performance for both Logistic and Linear Regression.

## Interaction effects in Linear Regression. 
First, we will start by fitting a Linear Regression model on the "sales.csv" dataset, to predict the total_sales for a new area using given sales from three areas. We will also include the interaction terms between different areas in our model, to see if synergy between them affect the sales in new area. We will be comparing the full interactionless model, with a model with interactions with respect to their $R^{2}$ values, and the significance of  coefficinets of interaction terms. We will also be giving insights on how to interpret the coefficients of interaction terms in Linear Regression. 

Generally, for a linear regression model with interaction:

$$Y = \beta_{0} + \beta_{1} \* X_{1} + \beta_{2} \* X_{2} + \beta_{3} \* X_{1} \* X_{2}$$

The coefficient of the interaction term $\beta_{3}$ is the increase in effectiveness of $X_{1}$ for a 1 unit change in $X_{2}$, and vice-versa. However, interpertrations might vary slightly based on types of variables interacting with each other(continuous, categorical, etc.)

## Interpreting Coefficients and Interaction Effects in Logistic Regression 
Next, we will be fitting a full Logistic Regression model on the "customer.csv" dataset, to predict whether the customer will purchase the product. We will also be fitting alternative Logistic regression models trimmed over different features, and comparing them to the full model with respect to their in-sample $R^{2}$"(pseudo). We will also be interpreting the coefficents of the best performing model. (For example, what effect does a positive or negative coefficient have on the model and so on)

In general in Logistic Regression,

$$ \frac{p}{1-p}=exp[ \beta_{0} + \beta_{1} \* X_{1} + ...+\beta_{p} \* X_{p}] $$

$e^{\beta_{p}}$ is the odds multiplier for the unit increase in $X_{p}$. In other words, 1 unit increase in  $X_{p}$ will multiply the odds of variable of interest by $e^{\beta_{p}}$.

When the coefficient is positive, that means the odds are going to be multiplied by a number that is bigger than 1, which means the odds of dependent variable will be increased.

In contrast, When the coefficient is negative, that means the odds are going to be multiplied by a number that is less than 1, which means the odds of dependent variable will be decreased.

In this project, we will also briefly discuss why the accuracy might not be a good metric to judge the performance of the model in our case, although it is commonly used metric. We will also suggest what other metrics we can use to to judge the predictive performance of a Logistic Regression model

## Interaction Plots
Last but not the least, we will be creating interaction plots between different variables in the "customer.csv" dataset, and commenting on how we can assess if there is interaction between variables looking the interaction plots. 
