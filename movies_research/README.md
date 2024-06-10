
## Movies

You need to study the Russian film distribution market and identify current trends. Pay attention to the films that have received government support.

## Used libraries:

matplotlib, numpy, pandas, plotly, seaborn, sklearn, tqdm

## Conclusion:

1. Uploaded both data files. Then I combined them, saving all the lines from the mrkf_movies file.
2. I checked the data type in the dataframe and changed some of them. In the show_start_date column, I changed the data type from object to datetime64. Changed the data type in the rating column, while bringing the rating to the same scale.
3. I studied the gaps in the dataframe. I filled in what I could.
4. Studied the duplicates. I concluded that there are a lot of repetitions in the title column. I believe this is due to the premiere of films in several countries. Since show_start_date is different. There are also many duplicates in the show_start_date column. I can assume that this may be the date of the film's appearance in the database or publication on a streaming service
5. Studied the categorical data. There were implicit duplicates in the type column. Removed spaces before words. I also changed the data entry in the production_country column. Brought it to a comma-separated entry.
6. I used histograms to check quantitative values. I found many values equal to zero. Mostly in columns related to the budget. I decided not to delete anything at this stage
7. Added new columns with the name of the main director, the main genre and the year of the premiere. I calculated how much of the total budget is state support
8. We see a clear increase in the release of films from 2010 to 2015. Further, the number of films increases and decreases again without any one-sided dynamics. Of the entire dataframe, information about the film's rental is available in 42 % of cases
9. The distribution of film fees by year looks rather strange. There is a feeling that I have missed something, or there are errors in the data. Since the statistics here start from 2014.
10. By average and median value, 2017 is the most profitable year. In absolute terms, a little more was collected in 2018.
11. Determined that the highest-grossing films have a rating of 16+, the lowest fees are in the 0+ category
12. There is a weak relationship between the film's fees and the budget. There was no good correlation of the rating with other parameters. The rating has the highest correlation coefficient (0.15) with the amount of fees
13. The average rating of films with state support is slightly higher than 6.
14. To characterize the payback of films, I took the ratio of fees to the budget. On average, this proportion is 0.76. Only 22% of films with state support pay off.
