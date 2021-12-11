# Project Details

In this project, it is discussed that how big is the role of marketing in banking sector. Direct marketing plays a very crucial role in promoting any business which will result in understanding about the customers and their choice. Identifying the trusted customers is a challenge for financial institutions. It can be achieved by analyzing the past records of customers like personal details, loan details. The dataset also provides the important information about the previously conducted campaigns. Based on this data, it is analyzed and come up with good patterns which will be useful for the respective bank. All bank marketing campaigns involve huge data which was collected during the campaigns. It is impossible to come to a proper decision when it is worked upon such huge datasets. So, it definitely needs a model to make this process easy. Data mining models aid in generating the best results for these campaigns. The proposed model taking 5 random models such as LR, DT, RF, XGB, MLF and try to compare the accuracies generated by each model for the dataset. Among which, it is taken the top three classifiers with acceptable accuracy, as the initial estimators and the result is passed to the LR which can tell whether the customer will subscribe to bank offers or not, with 92% accuracy. It is better than the existing models. In addition to this, it is also necessary to show the hidden patterns for effective marketing strategies.

Keywords: Direct Marketing, Logistic Regression (LR), Decision Tree (DT), Random Forest (RF), XG-Booster (XGB), Multi Level Perceptron (MLP).

Direct Marketing -
With the startling rise over the last few decades of media and technology which increases the amount of information which we have at our fingertips (cell phones, television, Internet, etc), humans are now more connected than ever before. One result of this is that marketing campaigns are growing ever more pervasive in our daily lives. Marketing refers to activities undertaken by a company to promote the buying or selling of a product or service. Marketing includes advertising, selling, and delivering products to consumers or other businesses. Mass Marketing is a technique in which single communication message will be sent to all customers through different kinds of media such as television, radio or advertising firm etc, which aims at offering the information to various people, without having any guaranty that the customers read or seen the intended offer. This technique does not benefit the Organizations in profitable range. To avoid this problem, experts come up with a solution. It is Direct Marketing. 
Response rate of customer is high in direct marketing when compared to mass-marketing. By examining the importance of marketing in banking sector, identifying the customers who are more likely to respond to new product offers is an important issue in direct marketing. So, just going with the direct marketing is also not a better choice. Putting this in mind and in the attempt of increasing the response rate from the customers even more, I chose to do this project. In banks, there will be huge data that records all the information related to customers including personal and loan details. This data can be used to create clear relationship, interesting patterns and connection with the customers in order to target them individually for various products or banking offers. Here I'm analyzing the marketing data of a Portuguese banking institution which is based on phone calls.After understanding about the dataset, we have done data preprocessing. The data cleaning methods include replacing missing values and converting Categorical variables to Binary variables using dummy variables. We have imputed missing values using median. 

As it is a classification problem, we have applied classifiers – Logistic Regression, Decision tree, Random forest, XG-Boost Classifier, MLP Classifier. In addition to these, we have created a new model – Stacking Classifier which is a combination of Logistic Regression, Random forest, XG-Boost classifiers. We have also created a Web application which will be helpful for banks to know the right customers.
![image](https://user-images.githubusercontent.com/95888723/145663037-e332f18b-dc17-4ecc-9307-0b28b30632fc.png)

PROPOSED WORK - 
At first, I took a dataset related to the project and load into the model. Then, the model divides the entire data into training data and testing data, where the training data share, here it is 70% will be given to the stacking classifier, which combines the features of the selected three classifiers, such as logistic regression which is model-1, RF classifier which is model-2 and XG-B classifier which is model-3 working as first level of estimators. The three predicted results of the three models will be given as input features for the final estimator which I have chosen here is the Logistic Regression. The final prediction resulted from this estimator will be treated as the final result.
![image](https://user-images.githubusercontent.com/95888723/145663099-521db47c-ff74-4fe0-a773-cb0e6bc40ef9.png)

Working Methodology - 
1.	Understanding the dataset
2.	Data Visualization 
3.	Data preprocessing/cleaning
4.	Evaluate ML Algorithms - Building models
5.	Performance comparison and choosing the best model
6.	Developing a web app
7.	Deploying the web app in Heroku

Performance Comparision - 
After evaluating the algorithms, all performance metrics are compared. (Accuracy, AUC, F1-score, Precision, Recall scores) of all the applied algorithms on my dataset are given below.
![image](https://user-images.githubusercontent.com/95888723/145663336-93419cea-b8f3-444d-a73a-a8966ee53d65.png)

Developing Web Application - Creating Model using Pickle Library
I have converted the resultant model which is in the form of a python object into a character stream using pickling. (pickle library) and saved the file as model.pkl and taken two instances from dataset to check accuracy.

Process for Web Application -
First, I have installed flask library locally and downloaded all the required libraries.
It will automatically create “env” folder with all installed libraries.
Next, created templates folder which will contain index.html file – to write front end code. I have written all the required code with text fields and button.
Then, I have created app.py file which manages the input entered by user and it works like backend.
Then, verified the webpage with few test cases.

RESULTS - 
The best out of sample model performance was obtained for the Stacking Classifier (Logistic Regression + Random Forest + XGBoost Classifier) with nearly 92% accuracy. The importance of the features (in terms of how greatly they affected the coefficients) was also plotted. This provides valuable insight towards understanding which features contribute the most toward the models’ performance. From the feature importance plot, it can be inferred that Europe’s Libor rate, age of the applicant, employment variation rate, campaign, consumer confidence index, consumer price index, mode of contact (= telephone), and number of employees are some of the most important features in predicting the outcome.
