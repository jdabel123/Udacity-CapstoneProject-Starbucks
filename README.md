# Udacity Capstone Project

## Starbucks

Final project for Udacity's Data Scientist Nanodegree.

## Installation

In order to run the Jupyter notebook you will need to have python 3 installed and the following dependencies:

- [pandas](https://pandas.pydata.org/)
- [Sklearn](https://scikit-learn.org/stable/)
- [Numpy](https://numpy.org/)
- [Matplotlib](https://matplotlib.org/)
- [Seaborn](https://seaborn.pydata.org/)

## Project Motivation

Using similated data obtained from Starbucks that mimics how customer are influenced by promotional offers. The aim of this project is to conduct an exploratory analysis to see which demographics of Starbucks customers responded to which offers and to create a predictive model to predict whether the combination of user and offer type will result in a successful offer.


## File Descriptions

The analysis and predictive models are available in the Jupyter Notebook.

The datasets are a simplified version of the real Starbucks app because the data only contains information regarding one product whereas Starbucks has a whole line of products.

The data given to us was stored in 3 json files:

- `portfolio.json` - containing offer ids and data regarding the offer: duration, difficutlty and type.
- `Profile.json`  data containing demographic information for each customer.
- `transcript.json` - data containing every record for transaction, offers recieved, offers reviewed and offers completed.

Here are the schemas for each file:

`Portfolio.json`

- offer_id (string) - offer id
- offer type (string) - the type of offer: Informational, Discount, BOGO.
- difficulty (int) - minimum required to spend to complete an offer.
- reward (int) - the reward is given for completing the offer.
- duration (int) - time for the offer to be open in days.
- channels (list of strings)

`Profile.json`

- age (int) - age of the user
- become_member_on (int) - integer referring to the date the customer created an account.
- gender (string) - gender of the customer (Male, Female, Other)
- id (str) - customer id
- income (float) - customers income

`Transcript.json`

- event (string) - record description (transaction, offer received, offer completed, offer viewed)
- person (string) - customer_id
- time (int) - time in hours since the start of the test. 
- value (dictionary containing strings) - contains either offer id, amount or reward depending on the event.

## Results

The main findings of this project can be found in my medium post about the project [here](https://johnabel1997.medium.com/starbucks-capstone-challenge-350575a03f9a).

Essentally i used Logistic Regression, Support Vector Machines, Linear Discriminant Analysis and a AdaBoost Classifier to predict whether an offer would be successful.

The SVM model was the most accurate with an accuracy of 78%, a f1 score of 0.79 and auc score of 0.78.


## Licensing, Authors and Acknowlegements

I would like to thank Starbucks for supplying the datasets and Udacity.






