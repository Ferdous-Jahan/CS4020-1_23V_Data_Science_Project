# Project Overview

This is our final project for CS4020-1 23V Data Science course. We'll try to predict the match result of football matches in the English Premier League based on training machine learning model with 21-22,22-23 season data of premier league teams.  

**Project Steps**
 
* Data collection by scraping from two data sources mentioned below.
* Data cleaning using pandas.
* Make predictions about about match result using scikit-learn.
* Measure error and improve our predictions.


## Group Members

[Ferdous Jahan](ferdousjahan2@gmail.com)

[Nabila Tabassum](nabilatabassum147@gmail.com)
## Code

You can find the code for this project [here](https://github.com/Ferdous-Jahan/CS4020-1_23V_Data_Science_Project).

File overview:

* `scraping_player_list.ipynb` - a Jupyter notebook that scrapes data for first team players of each match from [EPL official site](https://www.premierleague.com)
* `match_stats_scrapping.ipynb` - a Jupyter notebook that scrapes match stats data from [fbref](https://fbref.com/en/)
* `merge_player_list_&_stats_per_match.ipynb` - a Jupyter notebook that merges data frames of previous two scrapped datasets.
* `match_prediction.ipynb` - a Jupyter notebook that pre process dataset for training ML model, then trains ML model and then make predictions.

# Local Setup

## Installation

To follow this project, please install the following locally:

* Anaconda3
* Python 3.8+
* Python packages
    * BeautifulSoup (built in Anaconda)
    * requests
    * pandas (built in Anaconda)
    * scikit-learn (built in Anaconda)

## Code Running guide

* First open `scraping_player_list.ipynb` in Jupyter notebook. Run the code in first block with `for match_number in range(66342,66722):` in line 8 and comment out the next line. this will download dataset consisting first team players for each match of 2021-22 season [set the csv file name to 'player_list_per_match_2021-2022.csv']. Then run the code of first block again with `for match_number in range(74911,75189):` in line 9 and comment out line 8. This will download dataset consisting first team players for each match of 2022-23 season [set the csv file name to 'player_list_per_match_2022-2023.csv']. Then run the code in second block which will save a csv file merging the two datasets of those seasons.

* Then open `match_stats_scraping.ipynb` in Jupyter notebook. Run the cells one by one. This will result in a csv file consisting match stats data of 2021-22 & 2022-23 seasons.

* Then open `merge_player_list_&_stats_per_match.ipynb` in Jupyter notebook. Run the cells one by one. This will result in a csv file consisting merged data of players and match stats data of 2021-22 & 2022-23 seasons.

* Then open `match_result_prediction.ipynb` in Jupyter notebook. Run the cells one by one. Data categorization, Model training, Prediction scores and results are there.
