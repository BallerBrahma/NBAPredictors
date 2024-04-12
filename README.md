# NBAPredictors

- Utilized elements of web scraping and machine learning to predict the outcome of NBA games.
- Incorporated several different libraries to assist with web scraping: os, Beautiful Soup, Playwright, time, and pandas
- Incorporated several different libraries to assist with machine learning: pandas, Scikit-learn (Model Selection, Feature Selection, and Linear Model)

- Project Overview:
- get_data:
    - Determined amount of seasons to utilize to predict future outcomes
    - Used library 'os' to join the paths of files with certain directories
    - Created a function to derive html from https://basketball-reference.com
      - HTML with 'a' tags
      - Ensured that webscraping was not occurring too quickly to avoid being banned
    - Created a function to go through each month of each NBA season and retrieve its HTML
    - Created a function that derived all the scores from each month on the NBA schedule for each season
    - Utilized these functions to get over 18,000 games across 9 NBA seasons and consolidate each game's HTML in a directory
- parse_data:
    - Cleaned data by creating a function to delete all files that don't end with ".html"
    - Created a function to consolidate all the games into a table with several columns with both basic and advanced statistics for each game
    - Created a function that writes all the games into a .csv file to help with readability for machine learning
- predict:
    - Cleaned data by deleting columns that would not help with the predictions
    - Added new columns with values that represented which team won the game
    - Removed all values that contained "null"
    - Used the Scikit-learn library to create a model using its methods such as RidgeClassifier, TimeSeriesSplit, MinMaxScalar, and SequentialFeatureSelector
    - Created a method to select specific columns to train and test the model
      
-  Overall, created a predictor model that predicted future NBA games at a higher percentage than utilizing whether a game is at home (A high percentage indicator for NBA games)


