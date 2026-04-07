# Kaggle Titanic Competition with Random Forests 

## **Project Overview**

The goal of this project is to create a machine learning model that predicts which passengers survived the Titanic shipwreck. The data given to create this model were the characteristics of many of the passengers (name, gender, class, etc.). The random forest model that I created achieved an accuracy score of 78.22%.

## **Data Understanding**

The data used was provided on the competition page on Kaggle. The training data consisted of 891 passengers and 10 features. The test dataset contained 418 passengers with information on whether they survived or not included. 

Something that immediately stood out to me was the missing entries in the data, more specifically in the age and cabin columns. There were 687 entries missing for cabin and 177 entries missing for age. By examining these missing values, I saw that there was a positive correlation with having a non-NA entry and an increased chance of survival. To capture this information, I created a dummy variable column on whether a passenger had their age or cabin listed in the training data. To handle the missing values for the cabin, I ended up dropping the entire column, and for age, I replaced the NA values with the mean value of age in the dataset. 

In the training data I saw that 62% of the people in the dataset died and 38% survived. 

For the model that I created, the Cabin, Name, and Ticket columns were difficult to find a way to include in the model. I ultimately decided to drop these features for the model. 

## **Modeling and Evaluation** 

I used a random forest model to predict my results, and the final accuracy score from the test data was 78.22%. 

## **Conclusion**

The model performed decently, but there is definitely room for improvement. My model may have done better than a random guess of 50% accuracy, but I know that machine learning models are easily capable of reaching accuracy scores of 90-99%. The model can be improved with further feature engineering to try and incorporate some of the data I was unable to capture in my model. Also, different classification models could be tested to see if they perform better.
