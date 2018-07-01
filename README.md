# Analyzing-a-Simple-A-B-Test-with-a-T-Test
I includeed two ways of t tests that compare conversion rate and click through rate of two groups

### * What do the raw data look like?
	 - Raw data were downloaded from AdWordsa and include conversion, click and impression data for two groups of ads in each ad groups.
	 - That means, before doing any analysis, we either need to aggregate data for each metrics first (method 1) or convert data to aother format (method 2) first
### * What is the difference of the two methods?
	 - Method 1 aggregate metrics (conversions, clicks and impressions) first and then calculate mean, standard deviation, t statistics and p value using equations.
	 - Method 2 convert raw data of conversions, clicks and impressions to 0 (didn't click or didn't convert) and 1 (clicked or converted) first, and then call scipy.stats.ttest_ind. to calculate t statistics, p value and use np to calcualte standard deviation
     - Note that After converting data, data udner column "Impressions" should be all 1 (meanuing inpression served)
### * Which method do I like better?
     - I like method 2 better as it's quicker and easier. LOL. You don't have to calculate each metric using equations
     - But method 1 can potentially enhance you understanding of t test
### * What are the input and output of this Python code?	
	- Input: a csv file downloaded from AdWords that containins data of conversions, clicks and impressions for each group of ad
	- Output: 
		- t statistics
		- p value
		- standard deviation
		- histogram graph of each metric