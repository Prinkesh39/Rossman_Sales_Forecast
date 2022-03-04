# Rossman_Sales_Forecast

Sales Forecasting for Rossman Stores

Installation and Library Used

1. Pandas
2. Numpy
3. Matplotlib
4. Seaborn
5. SKlearn

These libraries can be installed using simple pip command or conda (if you are using Jupyter).

Project Motivation: This project is a part of my learning for the concepts of Data Wrangling and Machine Learning Implementation.

This project consists of following files:

1. Python File consists of the working of the wmodel
2. README

Tha dataset is provided by the KAGGLE as a part of the competition, the link for which is https://www.kaggle.com/c/rossmann-store-sales/data

Brief Description of data:

Files

    train.csv - historical data including Sales
    test.csv - historical data excluding Sales
    sample_submission.csv - a sample submission file in the correct format
    store.csv - supplemental information about the stores

Data fields

Most of the fields are self-explanatory. The following are descriptions for those that aren't.

    Id - an Id that represents a (Store, Date) duple within the test set
    Store - a unique Id for each store
    Sales - the turnover for any given day (this is what you are predicting)
    Customers - the number of customers on a given day
    Open - an indicator for whether the store was open: 0 = closed, 1 = open
    StateHoliday - indicates a state holiday. Normally all stores, with few exceptions, are closed on state holidays. Note that all schools are closed on public holidays and weekends. a = public holiday, b = Easter holiday, c = Christmas, 0 = None
    SchoolHoliday - indicates if the (Store, Date) was affected by the closure of public schools
    StoreType - differentiates between 4 different store models: a, b, c, d
    Assortment - describes an assortment level: a = basic, b = extra, c = extended
    CompetitionDistance - distance in meters to the nearest competitor store
    CompetitionOpenSince[Month/Year] - gives the approximate year and month of the time the nearest competitor was opened
    Promo - indicates whether a store is running a promo on that day
    Promo2 - Promo2 is a continuing and consecutive promotion for some stores: 0 = store is not participating, 1 = store is participating
    Promo2Since[Year/Week] - describes the year and calendar week when the store started participating in Promo2
    PromoInterval - describes the consecutive intervals Promo2 is started, naming the months the promotion is started anew. E.g. "Feb,May,Aug,Nov" means each round starts in February, May, August, November of any given year for that store
    
Summary: In this project, we will analyze data for sales in the stores of Rossman Stores. Sales depends on various factors like holidays, promotional offers etc.  We'll use supervised learning techniques to predict the sales for the id of the stores given in the test dataset.

We find that XGBoost Classifier for supervised learning is the best model. Upon further tuning of Hyper parameters using GridSearch CV, we improved our model to some extent.


