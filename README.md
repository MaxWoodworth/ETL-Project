#Prologue
I chose to do this project alone as I go to Wisconsin with my father, uncles, great uncles, and cousins every year the weekend before Thanksgiving to go deer hunting. Very unproductive outing for us all but it was nice to see family members that I only see once a year especially this year when nothing seems normal.

# ETL-Project Report
My objective for this project was originally to take historical data on the "spread" (the amount a NFL team is favored to win by) and see if there was a correlation with the most points favored in a season to the winner of the Super Bowl that same year. Unfortunately my available data did not tell me which team was projected to win, just the number the unidentified team was expected to win by. Therefore I shifted gears and looked at the historical total points in games since 1979 to see if there was a correlation with the total points scored in the Super Bowl.

#Extraction
The data was retrieved from two users Kaggle. I used the "spreadspoke_scores.csv from kaggle.com/tobycrabtree/nfl-scores-and-betting-data?select=spreadspoke_scores.csv and the superbowl.csv from https://www.kaggle.com/timoboz/superbowl-history-1967-2020 . Other than the hiccup early on these were both very useful csv's because they had a ton of data and from over two decades worth.

#Transformation
After I had the two files extracted I first began cleaning the data. I created plenty of dataframes until I had the data I wanted and could use to work together. I then added a column to both dataframes to add the points scored by both teams to obtain total scores from each game listed. I chose to make an additional dataframe based off the .describe function to recieve the mean of total score of all games played since 1979. Once I had this figure I created a bar chart of all the Super Bowls by total points since 1979 and added a mean line. This was a challenge for me becasue I couldnt recall any time we added a line that was not specifically the mean of the data being inputed. The mean line was actually the figure from the opposite dataframe to give perspective on the relationship between the average total score of all games and those of just the super bowl. There was certainly a correlation and with the occasional outlier. 

#Load
I chose to load all of the data to my local PGAdmin using to.sql and showed that the data was also pullable. I also chose to not combine the tables because the way I chose to use the data did not really make this possible. This is because I used many games from each year for the mean figure on the first dataframe but only one game per year for the Super Bowl dataframe. 

Outliers
There were instances where I had to delete a few years data prior to 1979 because the data was incomplete and it would have sqewed my findings. Another outlier could be weather as this was something there was limited data given but with the alloted time I chose to omit.

#Next Steps
Moving forward I would like to finish what I started and find which teams were favored in each year and see if my original hypothesis was correct. As for the total scores I would like to add information on the weather as I stated above as well as extending this to the projected over under odds that vegas sets.
