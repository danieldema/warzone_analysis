# Initial Analysis

On April 3rd 2025, Activision launched a major update for their online game 'Call of Duty: Warzone' in which they re-introduced the game's original map 'Verdansk' which was previously removed in December 2021, as well as several old gameplay mechanics.

In this project, I analyzed and compared the community's perception of the game for the month prior to and the month after the release of this update. I used the library steamreviews to gather review data of the game on Steam, and then used pandas to clean the data and separate it into a dataset based on reviews posted between March 3rd and April 3rd, and reviews posted between April 3rd and May 3rd.

I used NLTK's sentiment analysis tool VADER to calculate polarity scores of both datasets, which quantifies the sentiment expressed through the reviews. For both datasets, I found that polarity score is negatively correlated with recommendation status. This suggests that a large number of recommendations use negative language in their review, or a large number of non-recommendations use positive language in their review. One possible explanation is the use of sarcasm, which VADER fails to detect. Another possible explanation is reviews that use positive language but do not recommend the game due to technical issues (bugs). This warrants further investigation.

I calculated the proportions of recommendations in both time ranges. Between March 3rd and April 3rd, 29.7% of reviews recommend the game and 70.3% of reviews recommend the game (88 versus 208). Between April 3rd and May 3rd, 25.8% of reviews recommend the game and 74.2% of reviews recommend the game (201 versus 577). Note that between the two time periods there was a 228% increase in recommendations and a 277% increase in non-recommendations.

I calculated the proportions of polarity scores in both time ranges. Between March 3rd and April 3rd, 33.8% of reviews had positive polarity score, 41.6% had negative polarity score, and 24.7% had polarity score 0. Between April 3rd and May 3rd, 31.7% of reviews had positive polarity score, 44.6% had negative polarity score, and 23.7% had polarity score 0. This indicates an increase in the use of negative language in reviews following the update.

# Followup Analysis
