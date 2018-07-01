# Analyzing-a-Simple-A-B-Test-with-a-T-Test
I includeed two methods of t tests that compare conversion rate and click through rate of control and experiment group

### * What do the raw data look like?
	 - Raw data file were downloaded from AdWords and include data of conversions, clicks and impressions in each ad group for both control group and experiment group
	 - That means, before doing any analysis, we either need to aggregate data for each metrics first (method 1) or convert data to aother format (method 2) first
### * What is the difference of the two methods?
	 - Method 1 aggregate data for each metric (conversions, clicks and impressions) first, and then calculate mean, standard deviation, t statistics and p value using equations.
	 - Method 2 convert raw data of conversions, clicks and impressions to either 0 (didn't click or didn't convert) or 1 (clicked or converted) first, and then call scipy.stats.ttest_ind. to calculate t statistics, p value and use np to calcualte standard deviation
     - Note that after converting data, data under column "Impressions" should be all 1 (meanuing inpression was served)
### * Which method do I like better?
     - I like method 2 better as it's quicker and easier. LOL. You don't have to calculate each metric using equations
     - But method 1 can enhance you understanding of t test
### * What are the input and output of this Python code?	
	- Input: a csv file downloaded from AdWords that containins data of conversions, clicks and impressions for control and experiment group
	- Output: 
		- mean
		- t statistics
		- p value
		- standard deviation
		- histogram graph of each metric