# Project 5: Data Collection, SQL, and Statistical Analysis of Taxi Services

## Introduction to the project:
The goal for this task is to understand passenger preferences and the impact of external factors on rides for a new ride-sharing company.
This will be achieved by analyzing a database comprised of competitor data and test a hypothesis about the impact of weather on ride frequency.

## Outline summary:
* Write a code to parse the data on weather in Chicago in November 2017 from the website: https://code.s3.yandex.net/data-analyst-eng/chicago_weather_2017.html
* Exploratory data analysis:
  * Found number of rides for each taxi company and grouped them as "other" besides the two most popular companies.
* Test the hypothesis that the duration of rides from the the Loop to O'Hare International Airport changes on rainy Saturdays:
  * Retrieved the identifiers of the O'Hare and Loop neighborhoods from the neighborhoods table.
  * For each hour, retrieve the weather condition records from the weather_records table. 
   * Used the CASE operator to break all hours into two groups: "Bad" if the description field contains the words "rain" or "storm," and "Good" for others.
   * Named the resulting field weather_conditions. The final table includes two fields: date and hour (ts) and weather_conditions.
  * Retrieve from the trips table all the rides that started in the Loop (neighborhood_id: 50) and ended at O'Hare (neighborhood_id: 63) on a Saturday.
   * Got the weather conditions for each ride Using the method from the previous task. 
   * Also retrieved the duration of each ride, ignoring rides for which data on weather conditions is not available.
* Exploratory data analysis (Python): 
  * Identified the top 10 neighborhoods in terms of drop-offs.
  * Made graphs: taxi companies and number of rides, top 10 neighborhoods by number of dropoffs.
  * Drew conclusions based on each graph and explain the results.
* Test the hypothesis: "The average duration of rides from the Loop to O'Hare International Airport changes on rainy Saturdays."
