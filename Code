# a. Graph the data in a scatterplot to determine if there is a possible linear relationship.
datatable = read.csv('Price_vs_Age.csv')
plot(datatable$Age, datatable$Price)

# b. Compute and interpret the linear correlation coefficient, r.
cor(datatable$Age, datatable$Price)
cor.test(datatable$Age, datatable$Price)

# c. Determine the regression equation for the data.
fit_model = lm(Price ~ Age, data = datatable)
print(fit_model)

# d. Graph the regression equation and the data points. 
plot(datatable$Age, datatable$Price)
abline(fit_model)

# e. Identify potential influential observations.
par(mfrow = c(2, 2))
plot(fit_model)

# f. At the 5% significance level, do the data provide sufficient evidence to conclude that the
# slope of the population regression line is not 0 and, hence, that age is useful as a predictor of sales price for Toyata Alphard?
summary(fit_model)

# g. Obtain the residuals and create a residual plot. Decide whether it is reasonable to consider
# that the assumption for regression analysis are met by the variables in questions.
par(mfrow = c(2, 2))
plot(fit_model)

# h. Compute and interpret the coefficient of determination, r^2.
summary(fit_model)

# i. Find the predicted sales price of Jack Smith's 4-year-old Toyata Alphard.
newdata = data.frame(Age = 4)
predict(fit_model, newdata)

# j. Determine a 95% prediction interval for the sales price of Jack Smith's 4-year-old Toyata Alphard.
predict(fit_model, newdata, interval = "predict", level = 0.99)
