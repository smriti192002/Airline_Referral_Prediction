# Project Title - Airline Passenger Referral Prediction 
`Predicting aircraft passenger referal and excavating the main influencing factors can help airlines improve their services and gain.`

![passenger-airplane-flying-above-clouds-view-window-plane-to-amazing-sky-beautiful-clouds-passenger-airplane-flying-112676322](https://user-images.githubusercontent.com/88886118/216586501-3a428d68-d693-4435-b185-8b5d38a8c2eb.jpeg)

---
## Contents <p id="contents"></p>
- <a href="#bquestions">Business Questions</a>
  - <a href="#business_impact">Business Impact</a>
- <a href="#methodology">Methodology</a>
  - <a href="#data_dictionary">Data Dictionary</a>
  - <a href="#data_cleaning">Data Cleaning</a>
  - <a href="#feature_engineering">Feature Engineering</a> 
- <a href="#data_exploration">Data Exploration</a>
- <a href="#machine_learning">Machine Learning Algorithms</a>
- <a href="#final_model_selection">Final Modeling Selection</a>

## 📝 Problem Statement <p id="bquestions"></p>

The goal of this project is to utilize passenger data from 2006 to 2019 to develop a model that can accurately predict the likelihood of a passenger recommending an airline to their friends. By understanding the factors that contribute to customer satisfaction and loyalty, we aim to identify opportunities for improving the customer experience and increasing word-of-mouth marketing for the airline. The data for this study includes responses from a variety of popular airlines, collected through scraping methods in the spring of 2019. This information will be used to train and evaluate the performance of our recommendation prediction model.

## 🤔 How it might be helpful for business? <p id="business_impact"></p>

Airline referral prediction helps businesses by providing a more efficient and targeted approach to customer acquisition. By identifying customers who are most likely to refer others to the airline, the airline can focus its marketing efforts on these customers, rather than blindly advertising to all customers. This can result in higher conversion rates, as the marketing message is tailored to the specific needs and interests of the target audience. Additionally, by improving customer loyalty and satisfaction, referral prediction can also help to reduce customer churn and increase repeat business, leading to increased revenue and profitability for the airline.

## 💻 Methodology <p id="methodology"></p>

![AIRLINE_PASNGR_REFF_649091ceef](https://user-images.githubusercontent.com/88886118/216589365-e5a9bef5-44b6-4dcd-aa01-4cb5fbfbb96a.png)

## 📝 DATA DICTIONARY <p id="data_dictionary"></p>
![Classification_Airline_Passenger_Referral_Prediction_8c4c72cc3f](https://user-images.githubusercontent.com/88886118/216590642-78e80a02-9448-4996-882f-59d5fc9d5804.png)

## 🧹 DATA CLEANING <p id="data_cleaning"></p>

Performing operations such as:

- Check the size and type of the data and converting it into respective type 
- Remove all rows with all null values in the data due to spacing issue in original excel
- Deleting Duplicates
- Dropping unneeded columns
- Text Cleaning in Reviews column 
- Analysis of Missing Values and treating them with mode and iterative imputation 

## ⚒️	FEATURE ENGENEERING <p id="feature_engineering"></p>

Important to increase the amount of information needed to better understand the phenomenon we are trying to model. Feature Engineering is also instrumental in obtaining more variables available for study during Data Analysis, which is the next step in this project.

## 🔎 EXPLORATORY DATA ANALYSIS <p id="data_exploration"></p>

Exploratory Data Analysis (EDA) is a method used to analyze and summarize datasets, in order to gain insights and understand the underlying structure of the data. It typically involves visualizing the data, computing basic statistics and identifying patterns, outliers, and relationships between variables.

### `Visualising count distribution for various features`
<p align="center">
<img src="https://user-images.githubusercontent.com/88886118/216743449-587bca80-8db5-4a66-b5a5-d8e02e6b2f0c.png">
</p> 


- Slightly more non recommending users are there as compare to recommending users
- Most of the users are giving either 1 or 4 rating to the seat comfort
- More users seems to be happy with service ratings and provide higher(5) ratings
- Lastly count of economy class in cabins are more and lesser in business class, first class and premium economy

<p align="center">
  <img src="https://user-images.githubusercontent.com/88886118/216746617-37a21e49-fe97-4e43-9c41-748dcbe0a01c.png">
</p>






- In all these distributions we can see more users to be providing 1 ratings
- Most of the users are either rating lowest or highest. Only few users are provinding mediocer rating(3)

### `Distributionof Overall in respect to recommend feature`
<p align="center">
 <img src="https://user-images.githubusercontent.com/88886118/216743764-0ad79a10-f982-45cf-85ac-36e0d96443b8.png" width="700" height="400"/>
</p>

- Overall seems to be very powerful variable there are nearly no recommendations with overall 1,2 and 3 rating and almost all the people are recommending who has 7,8,9 sand 10 rating

### `Checking the effect of layover on recommendation`

<p align="center">
<img src="https://user-images.githubusercontent.com/88886118/216778718-4f8df176-3dd2-4eed-b27e-489004a2474b.png" width="700" height="400"/>
</p>



- From the graph it seems like there is no serious effects of layover on recommendation to the flight as we can see both the flights with and without layover has higher no recommendation with very slight differences in count of each. We can see that for the flights having no information about layover has higher yes recommendation

### `Checking the effect of days difference between reviewed date and flown date on recommendation`

<p align="center">
<img src="https://user-images.githubusercontent.com/88886118/216778365-4ecd8282-a627-49fc-89c7-fa76fee54a4a.png">
</p>


- We have observed that when reviews are collected a sufficient number of days after a flight, the majority of users tend to recommend the flight. Conversely, when reviews are collected close to the date of the flight, more users are not recommending the flight. As a result, this may reflect on the airline reputation and it will be beneficial to keep this fact in mind while collecting and analyzing customer feedback to make more informed business decisions.

### `Rating Distribution Check`
<p align="center">
<img src="https://user-images.githubusercontent.com/88886118/216778488-65dc23f6-edad-43f4-b185-10430690e88c.png" width="1000"/>
</p>



- We can see that out of all the rating features. Out of all the user who is rating ground service most of them are rating 1 or can we said like out of different features ground service have most of 1 rated users
- Similarly cabin service is a star feature and nost of the people rated 5 to cabin service

### `We are check the relation of one feature with other rating feature`
 
 `Similarly we have done for other feature`

<p align="center">
<img src="https://user-images.githubusercontent.com/88886118/216778633-7b5c962d-561c-4581-97a5-e363979a6b26.png">
</p>

- Comparatively, couples and families who are travelling appear to be less satisfied with the services, as more than 45% of users have provided negative ratings for seat comfort. However, solo leisure users seem to be more satisfied with the seat comfort services.

- Approximately half of solo travelers have provided positive ratings for the cabin services, while feedback from couples and families indicates dissatisfaction with the cabin service provided

- Though there is no major difference in food and beverage ratings in different traveller type , still solo leisure seems to be happy with services

- An analysis of customer feedback on entertainment services does not reveal any significant insights as the ratings from all traveller type are not much different from each other

- feedback shows that solo travelers have given positive ratings with 42.42% satisfaction for ground services, while more than 50% of other traveler groups (business, couple leisure and family) have provided negative ratings for the same service

- over 50% of bussiness, couple ,and family travelers have given poor ratings (1 and 2) for value for money, while only 30% have given positive ratings.

## MACHINE LEARNING ALGORITHMS <p id="machine_learning"></p>

It is this project stage that involves the part that most data scientists like to work on, the use of machine learning algorithms. All the previous steps were designed to maximize the algorithms efficiency

## Machine Learning Modelling <p id="machine_learning_modelling"></p>

**Logistic Regression**

| Model Name	|Precision| recall	| accuracy |
| ----------- | ----------- |  ----------- |  ----------- |
| Logistic Regression |	0.96 |	0.95 |	0.95

**Decision Trees**

| Model Name	|Precision| recall	| accuracy |
| ----------- | ----------- |  ----------- |  ----------- |
| Decision Trees |	0.96 |	0.96 |	0.96

**Random Forest**

| Model Name	|Precision| recall	| accuracy |
| ----------- | ----------- |  ----------- |  ----------- |
| Random Forest |	0.96 |	0.96 |	0.96

**GradientBoost**

| Model Name	|Precision| recall	| accuracy |
| ----------- | ----------- |  ----------- |  ----------- |
| GradientBoost |	0.86 |	0.99|	0.91

**XtremeGradientBoost**

| Model Name	|Precision| recall	| accuracy |
| ----------- | ----------- |  ----------- |  ----------- |
| GradientBoost |	0.96 |	0.95|	0.95

## 📊 FINAL MODEL SELECTION <p id="final_model_selection"></p>

<p align="center">
<img src="https://user-images.githubusercontent.com/88886118/216779937-8b462480-4faf-47d7-811d-d85c06831dca.png">
</p>

`Conclusion on Predictive modelling`

We have observed that nearly all the models are giving up the same scores from logistic regression to xtreme gradient boost.Scores are similar because we have seen in our data analysis as well relation seems to straight forward and easy between recommended and other rating varables.

`Score metrics`

Now there are two major scores precision and recall they are coming out to be nearly same and equal. We can provide the importance to each depending on the case for which the model can be used :

Case 1: If the primary concern of an airline company in seeking a recommendation system is to reduce customer churn by identifying areas for improvement, then it is important to prioritize high precision for class 1 (indicating customers who are likely to churn). This means that the recommendation system should accurately identify customers who are at risk of leaving, so that the company can take appropriate actions to retain them.

case 2: If airline company is using this to somewhere to attract customer and trying to show the happy customers then recall is important.

We can consider case 1 here and considering all the models are nearly same only and if timing of execution is not a concern then we can go for gradient boost or else we can pick up Loogistic regression or Decision Tree.


