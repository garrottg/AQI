# AQI
This project was completed as part of the requirements for the Linear Regression class. The goal was to understand what gasses had an effect on the air quality of India. 
Multicollinearity was check pairwise and beyond pairwise, meaning there maybe more than two variables that are correletated. We found that PM2.5 and PM10 as well as NOx
and NO are highly correleted, having a correcation higher than 80%. We did two seperate model, one dropping PM2.5 and NOx and the second dropping PM10 and NO. To check
beyond pairwise we looked at the variance inflation factor. We allowed for a VIF of less than 10 to be acceptable. For the model containg PM10 and NO we had no high VIF
values. Backward Variable selection was done in R, and NO2 and Benzene we found to not be significant. The residual plot was investigated to see if the model satisfies 
the Gauss Markov Assumtion of constant variance. In the current state is was found that it does not satisfy the constant variance assumption. To try and remedy this a
box-cox transformation was applied. Hoever, since the residual plot formed more of a double bow than a v, a box-cox transformation does not work. Influential and 
leverage points were also analyzed. The influential points were measured using DDFITS. The goal was to see what the percent change in our coefficients would be. The 
model had an R^2 adjusted of 85%. 

The same process was done, but now dropping PM10 and NO, and substituting PM2.5 and NOx. From backward variable selection we found to drop SO2 and Toluene. The final
model had an R^2 Adjusted of 85% as well. 

To decided which model to pick, I looked at the initial pairwise correlation matrixtow see if PM10 and NO or PM2.5 and NOx were more correlated with AQI. It was found
that PM2.5 and NOx were slightly more correlated with AQI, so they were used in the final model.

However, since neither model satisifed the Gauss Markov Assumption of constant variance than neither model is very good. the appropriate transformation needs to be found 
so that the resifual plot will yeild a constant variance shape.
