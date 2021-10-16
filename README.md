# we_rate_dogs_analysis

Wrangled and analyzed the Twitter archive of We Rate Dogs through August 1, 2017.

wrangle_act.ipynb contains the data wrangling and the initial analysis.

act_report.pdf contains a more focused and refined analysis.

wrangle_report.pdf is an overview of the data wrangling steps I performed.

## Overview of project

There were three data sources: a file with dog names and their status (a dog or a puppy or etc) that was given to me by Udacity; a file with detailed info about the same tweets (how many times the tweets were favorited or retweeted, etc) that I got by querying Twitter with an api; and a file with predictions about the breeds of the dogs in the tweets that I downloaded programatically from Udacity (they'd created this file using machine learning).

I found and corrected two tidiness issues and eight quality issues in the data set.

For the analysis, I first compared favorited_count to retweet_count and found they correlated very well, except at the highest numbers of favorites and retweets. I chose retweet_count as my main metric for measuring a tweet's popularity in this project. I then compared tweets with the dog status of "puppy" versus those of "dog". I found "puppy" averaged less retweets and favorites than "dog", but I concluded that this might be related to the fact that there are many more total tweets labeled "puppy" than "dog". Finally, I compared the number of times dogs of various breeds were retweeted. Factoring in total number of times a given breed is tweeted, how many total favorites and retweets tweets about the breed receive, and the average number of favorites and retweets the tweets receive; I concluded that golden retriever was the most popular dog in the dataset. But then I further concluded that I probably did not know enough to say anything definite about the popularity of the dogs tweeted. 

After the project had already been completed, I discovered the Pearson test and found that favorite and retweet counts had a score of .93

I'd thought I could get an even higher score by throwing out the top 25% of retweets or favorites (because the scatterplot points seem to spread out more at higher values), but when I removed the highest values, the pearson scores actually went down a little.






