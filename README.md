# Initial Analysis

On April 3rd 2025, Activision launched a major update for their online game 'Call of Duty: Warzone' in which they re-introduced the game's original map 'Verdansk' which was previously removed in December 2021, as well as several old gameplay mechanics.

In this project, I analyzed and compared the community's perception of the game for the month prior to and the month after the release of this update. I used the library steamreviews to gather review data of the game on Steam, and then used pandas to clean the data and separate it into a dataset based on reviews posted between March 3rd and April 3rd, and reviews posted between April 3rd and May 3rd.

I used NLTK's sentiment analysis tool VADER to calculate polarity scores of both datasets, which quantifies the sentiment expressed through the reviews. For both datasets, I found that polarity score is negatively correlated with recommendation status. This suggests that a large number of recommendations use negative language in their review, or a large number of non-recommendations use positive language in their review. One possible explanation is the use of sarcasm, which VADER fails to detect. Another possible explanation is reviews that use positive language but do not recommend the game due to technical issues (bugs). This warrants further investigation.

I calculated the proportions of recommendations in both time ranges. Between March 3rd and April 3rd, 29.7% of reviews recommend the game and 70.3% of reviews do not recommend the game (88 versus 208). Between April 3rd and May 3rd, 25.8% of reviews recommend the game and 74.2% of reviews do not recommend the game (201 versus 577). Note that between the two time periods there was a 228% increase in recommendations and a 277% increase in non-recommendations.

I calculated the proportions of polarity scores in both time ranges. Between March 3rd and April 3rd, 33.8% of reviews had positive polarity score, 41.6% had negative polarity score, and 24.7% had polarity score 0. Between April 3rd and May 3rd, 31.7% of reviews had positive polarity score, 44.6% had negative polarity score, and 23.7% had polarity score 0. This indicates an increase in the use of negative language in reviews following the update.

# Followup Analysis

On December 6th 2023, Activison launched the map 'Urzikstan'. I used similar techniques as above to compare the reviews posted between November 6th 2023 and December 6th 2023 to those posted between December 6th 2023 to January 6th 2024. 

Between November 6th and December 6th, 35.2% of reviews recommend the game and 64.8% do not recommend the game (90 versus 166). Between December 6th and January 6th, 23% of reviews recommend the game and 77% do not recommend the game (183 versus 611). Between the time periods, we see a 203% increase in recommendations and a 368% increase in non-recommendations.

Between November 6th and December 6th, 32.8% of reviews had positive polarity score, 37.5% had negative polarity score, and 29.7% had zero polarity score. Between December 6th and January 6th, 29.6% of reviews had positive polarity score, 44.2% had negative polarity score, and 26.2% had polarity score zero.

Comparing to our results for 'Verdansk', we see that this map has a smaller increase in recommendations, a larger increase in non-recommendations, and a larger increase in the prevalence of negative language used in reviews.

On November 16th 2022, Activision launched the map 'Al Mazrah'. I used similar techniques as above to assess reviews posted between November 16th 2022 and December 16th 2022. This is also the first month for which 'Warzone' was available on Steam, so this consists of the game's first batch of Steam reviews.

Of these reviews, 33.6% recommend the game, while 66.4% do not recommend the game (1987 versus 3918). Moreover, 38.6% of reviews had positive polarity score, 39.3% had negative polarity score, and 22% had polarity score zero. The higher proportion of recommendations and higher proportion of positive language in reviews compared to the months following the other two maps is possibly due to this being the game's first month on Steam.

# Comments

Warzone, with its original rendition of the map 'Verdansk', was launched on March 20th 2020. Subsequent map releases include the launch of the maps 'Caldera' on December 8th 2021, 'Al Mazrah' on November 16th 2022, and 'Urzikstan' on December 6th 2023. It was my hope to compare the reception of the game prior to and after each of these launches to that of the 'Verdansk' relaunch. However in the process of gathering data, I learned that Warzone was only released on Steam on November 16th 2022, which is why the followup analysis only accounts for reception of the game prior to and after the release of 'Urzikstan' and after the release of 'Al Mazrah'. It would be interesting to see analogous results for the launches of 'Al Mazrah' and 'Caldera', though at this time I am unaware of an alternative reliable source of reviews.
