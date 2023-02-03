# CapstoneProjectMaanikGupta

Problem Statement:
Hotels are facing a massive amount of cancellations on booking every year.
By looking through multiple datasets I've found that this is around 30% of
bookings cancelled. This is significant enough of a number that I feel
confident that I could create a model that accurately predicts who would likely
cancel.

Procedure:
First I had to clean up my dataset, creating a dummy dataset that got rid of
categorical variables and turned them into binaries.
Then I had to create a testing and training set with that being 75/25 respectively
From their I was able to fit a Random Forest classifier. That came to be about
91% accurate.
I also tried a bagging classifier that was only about 89% accurate.
I tried to modify the parameters of the dataset before messing with the
hyperparameters but found that it didn't help. I first tried to get rid of any
outliers, but none of the datapoints were even 1 standard deviation away from
the mean in their importance. So I decided to instead get rid of all columns
that were less important than the average. This made the model less accurate.
Finally I used a GridSearchCV to try and make a more accurate model.
Regardless of how I modified the hyperparameters I was unsuccessful.