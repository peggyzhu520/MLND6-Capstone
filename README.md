# MLND6-Capstone
This is for Udacity MLDN capstone project
### Project Overview 
Overweight has become a common problem nowadays. It is estimated 40% of adults are overweighed (World Health Oraganisation, 2018). 
It will be interesting to quantify these factors that have impact to overweight. 
Hopefully the outcome of the analysis will help to bring up some solutions to prevent us from overweighting.

### Problem and Solution Statement
Whether one is overweight or not, is actually really straightforward to measure. Instead of predicting overweight, this project is trying
to predict whether one will increase their weight or not within a year, given the lifestyle they currently have. 
Inputs are personal demographic, dietary and laboratory data from Kaggle1 originally produced by CDC2.
I also want to explore what are the key contributors to weight increase? To be more specific, what are the factors that will help with 
reduce risk of weight gain? What are the factors that lead to weight gain?
Our solution is mainly focusing on using Logistic regression as benchmark model, and XGboost as challenger model.
Top variables from each model are then used as predictive factors to assess their impact to weight gain.

### Install

This project requires **Python 3.x** and the following Python libraries installed:

- [NumPy](http://www.numpy.org/)
- [Pandas](http://pandas.pydata.org)
- [matplotlib](http://matplotlib.org/)
- [scikit-learn](http://scikit-learn.org/stable/)
- [xgboost] (https://xgboost.readthedocs.io/en/latest/)
- [hyperopt] (https://github.com/hyperopt/hyperopt)

You will also need to have software installed to run and execute an [iPython Notebook](http://ipython.org/notebook.html)

We recommend students install [Anaconda](https://www.continuum.io/downloads), a pre-packaged Python distribution that contains all of the necessary libraries and software for this project. 

```bash
ipython notebook finding_donors.ipynb
```  
or
```bash
jupyter notebook finding_donors.ipynb
```

This will open the iPython Notebook software and project file in your browser.



### Data

The dataset I’m going to use is National Health and Nutrition Examination Survey (NHANES) dataset from 2013- 2014. It is available in 
Kaggle (https://www.kaggle.com/cdc/national-health-and-nutrition-examination-survey) and originally produced by CDC . 
My overall dataset will be aggregated from 5 datasets, including:
1.	Demographics dataset: it includes demographic feature like age, education etc. Most importantly, it also has sample weight  
2.	Examinations dataset, including Blood pressure, body measures etc.
3.	Dietary data, including dietary interview about total nutrient intakes
4.	Laboratory dataset, which includes information like Cholesterol – HDL, Insulin etc.
5.	Questionnaire dataset, including weight history, alcohol usage etc.
Final dataset has 9813 observations with 1816 features; out of which 1657 are 1 and 8156 are 0. With sample weight applied,
the weight gain rate is 20%. Hence it is an imbalanced dataset. I will split the dataset into training, validation and testing dataset by 60, 20, and 20 respectively, with stratifying the data using the target label. 
The dataset was carried out using machine-learning techniques for predicting different target as compared to our objective here, 
for example predicting sleep disorder , type 2 diabetics  . It gives us confidence that this dataset could be used for this research. 
