# Outside Trader

## Hyun Ki Kim, Jessica Jee Yoon Song, Weiwei Zheng



### Index of Files
* code - codes for webscraping, data cleaning and modeling (read detailed comments in each .py file)
  *  web_scraping.py - different functions to scrap and save different data
  *  data_combining.py - cleans raw data and make a total data frame for analyze  
  *  modeling.py - import different methods to calculate predictions from the data/dataframe/comined_dataframe.json for each model  
  *  method - files for running different methods on data/dataframe/combined_dataframe.json, files are imported from modeling.py  
  *  backtesting.py - functions for calculating and drawing balance from the data/dataframe/combined_dataframe.json, and getting all search time of Tree model
                
* data - raw data files and clean/modified data files 
  *  balance_report - balance sample file (result) for February 27
  *  dataframe - dataframes for February (without prediction), March (without prediction) and a combined dataframe (with prediction)
  *  discussion - discussion raw data from February 14 to March 7 (trading days only)
  *  market - market index raw data from February 14 to March 7
  *  model - prediction results for each best model made from each machine learning method
  *  price - price raw data from Feburary 14 to March 7
  *  ranking - ranking table raw data from Feburary 8
  *  searching_time - the time when stocks in Tree (best model) portfolio appeared in search ranking table
  *  company_info.json - company data for each stock
  *  krx_code.json - maps company names to stock code
  
* presentation - proposal and final presentation slides

* Django - codes to run Django app and show results of different models

### Django

We have created a Django app to display the results of models we've implemented with graphs 
and tables. 

To go on to the website:
 * Run Django with "source myvenv/bin/activate"
 * Run the app locally with "python3 manage.py runserver"
 * Open the server "http://127.0.0.1:8000/" on the website

To load data: 
 * To populate the data we've scraped from the web and results of models, we've written a file "load_data.py"
   - from the shell
   "python3 load_data.py"
   
   - with Django activated state (Please run Django with "source myvenv/bin/activate")
   "python3 manage.py makemigrations main"
   "python3 manage.py migrate"
 
 
 To check up on data in Django:
  * To write queries and explore models we've implemented
  
    - with Django activated state (Please run Django with "source myvenv/bin/activate")
    "python3 manage.py shell"
    
    i.e. from main.models import MODEL_NAME

### Package to install
* apscheduler
* scikit-learn
* graphviz
    
### Students' Responsibiliy 
* Hyun Ki Kim - data_combining, backtesting
* Jessica Jee Yoon Song - Django
* Weiwei Zheng - web_scraping, modeling

### References

http://excelsior-cjh.tistory.com/entry/5-Pandas를-이용한-Naver금융에서-주식데이터-가져오기

https://github.com/JWarmenhoven/ISLR-python
