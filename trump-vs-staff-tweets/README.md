# Trump vs Staff Tweets

This dataset provides recent tweets from the [@realDonaldTrump](https://twitter.com/realdonaldtrump) Twitter account, collected by David Robinson.  He provides an overview of his analysis below:

"My analysis concludes that the Android and iPhone tweets are clearly from different people, posting during different times of day and using hashtags, links, and retweets in distinct ways. What’s more, we can see that the Android tweets are angrier and more negative, while the iPhone tweets tend to be benign announcements and pictures."

Data source: [David Robinson](http://varianceexplained.org/r/trump-tweets/)

## Files 

The Rmd file below processes the tweets using [tidytext](https://cran.r-project.org/web/packages/tidytext/index.html) and then trains a binary classifier using the [h2o](https://cran.r-project.org/web/packages/h2o/index.html) R package.  The resulting model can then be used to determine the source of future Donald Trump tweets.

- [trump-vs-staff-tweets-binary-classification.Rmd](https://github.com/WiMLDS/election-data-hackathon/blob/master/trump-vs-staff-tweets/trump-vs-staff-tweets-binary-classification.Rmd)
- [trump-vs-staff-tweets-binary-classification.html](http://htmlpreview.github.io/?https://github.com/WiMLDS/election-data-hackathon/blob/master/trump-vs-staff-tweets/trump-vs-staff-tweets-binary-classification.html)


The script above downloads the data directly from the source as an RData file, but a CSV version of the data is provided here for convenience (and for non-R users):
 
trump_tweets.csv

	text
	favorited
	favoriteCount
	replyToSN
	created
	truncated
	replyToSID
	id
	replyToUID
	statusSource
	screenName
	retweetCount
	isRetweet
	retweeted
	longitude
	latitude 
