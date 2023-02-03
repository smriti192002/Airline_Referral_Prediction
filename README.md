# Project Title - Airline Passenger Referral Prediction 
Predicting aircraft passenger referal and excavating the main influencing factors can help airlines improve their services and gain.

![passenger-airplane-flying-above-clouds-view-window-plane-to-amazing-sky-beautiful-clouds-passenger-airplane-flying-112676322](https://user-images.githubusercontent.com/88886118/216586501-3a428d68-d693-4435-b185-8b5d38a8c2eb.jpeg)

---
## Contents <p id="contents"></p>
- <a href="#bquestions">Business Questions</a>
  - <a href="#business_impact">Business Impact</a>
- <a href="#methodology">Methodology</a>
  - <a href="#data_dictionary">Data Dictionary</a>
  - <a href="#data_collect">Data Collect</a>
  - <a href="#data_cleaning">Data Cleaning</a>
    - <a href="#data_description">Data Description</a>
- <a href="#data_exploration">Data Exploration</a>

## 📝 Problem Statement <p id="bquestions"></p>

The goal of this project is to utilize passenger data from 2006 to 2019 to develop a model that can accurately predict the likelihood of a passenger recommending an airline to their friends. By understanding the factors that contribute to customer satisfaction and loyalty, we aim to identify opportunities for improving the customer experience and increasing word-of-mouth marketing for the airline. The data for this study includes responses from a variety of popular airlines, collected through scraping methods in the spring of 2019. This information will be used to train and evaluate the performance of our recommendation prediction model.

## 🤔 How it might be helpful for business? <p id="business_impact"></p>

Airline referral prediction helps businesses by providing a more efficient and targeted approach to customer acquisition. By identifying customers who are most likely to refer others to the airline, the airline can focus its marketing efforts on these customers, rather than blindly advertising to all customers. This can result in higher conversion rates, as the marketing message is tailored to the specific needs and interests of the target audience. Additionally, by improving customer loyalty and satisfaction, referral prediction can also help to reduce customer churn and increase repeat business, leading to increased revenue and profitability for the airline.

## 💻 Methodology <p id="methodology"></p>

![AIRLINE_PASNGR_REFF_649091ceef](https://user-images.githubusercontent.com/88886118/216589365-e5a9bef5-44b6-4dcd-aa01-4cb5fbfbb96a.png)

## 📝 DATA DICTIONARY <p id="data_dictionary"></p>
![Classification_Airline_Passenger_Referral_Prediction_8c4c72cc3f](https://user-images.githubusercontent.com/88886118/216590642-78e80a02-9448-4996-882f-59d5fc9d5804.png)

## 🧹DATA CLEANING <p id="data_cleaning"></p>
Performing operations such as:

- Check the size and type of the data and converting it into respective type 
- Remove all rows with all null values in the data due to spacing issue in original excel
- Deleting Duplicates
- Dropping unneeded columns
- Text Cleaning in Reviews column 
- Analysis of Missing Values and treating them with mode and iterative imputation 

## FEATURE ENGENEERING

Important to increase the amount of information needed to better understand the phenomenon we are trying to model. Feature Engineering is also instrumental in obtaining more variables available for study during Data Analysis, which is the next step in this project.

## EXPLORATORY DATA ANALYSIS <p id="data_exploration"></p>

Visualising count distribution for various features

<p align="center">
  <img src="https://user-images.githubusercontent.com/88886118/216599991-64653b72-7a51-4966-9371-c92be39578d7.png">
</p> 

- Slightly more non recommending users are there as compare to recommending users
- Most of the users are giving either 1 or 4 rating to the seat comfort
- More users seems to be happy with service ratings and provide higher(5) ratings
- Lastly count of economy class in cabins are more and lesser in business class, first class and premium economy

<p align="center">
  <img src="https://user-images.githubusercontent.com/88886118/216605056-b50e5d35-ad7c-44df-b976-966cc370e380.png">
</p>

- In all these distributions we can see more users to be providing 1 ratings
- Most of the users are either rating lowest or highest. Only few users are provinding mediocer rating(3)

<p align="center">
 <img src="https://user-images.githubusercontent.com/88886118/216608386-a9b8464a-f1e4-448b-8322-bfbd36feb53b.png">
</p>

- Overall seems to be very powerful variable there are nearly no recommendations with overall 1,2 and 3 rating and almost all the people are recommending who has 7,8,9 sand 10 rating

<p align="center">
<img src="https://user-images.githubusercontent.com/88886118/216608807-8325047e-fb4b-45c0-a258-46d5c2ed85c8.png">
</p>

- From the graph it seems like there is no serious effects of layover on recommendation to the flight as we can see both the flights with and without layover has higher no recommendation with very slight differences in count of each. We can see that for the flights having no information about layover has higher yes recommendation
