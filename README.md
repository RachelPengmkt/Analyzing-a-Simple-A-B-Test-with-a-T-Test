# Analyzing-a-Simple-A-B-Test-with-a-T-Test
I includeed two methods of t tests that compare conversion rate and click through rate of control and experiment group

### * What do the raw data look like?
	 - Raw data file was downloaded from AdWords and it has data of conversions, clicks and impressions of each ad group for both control and experiment group
	 - That means, before doing any analysis, we either need to aggregate data for perforamnce metrics first (method 1) or convert data to aother format (method 2)
### * What is the difference of the two methods?
	 - Method 1 first aggregates data for each performance metric (conversions, clicks and impressions), and then calculates mean, standard deviation, t statistics and p value using match equations.
	 - Method 2 converts raw data of performance metrics (conversions, clicks and impressions) to either 0 (didn't click or didn't convert) or 1 (clicked, converted or impression served) first, and then call scipy.stats.ttest_ind. to calculate t statistics, p value and uses numpy to calcualte standard deviation.
     - Note that after data conversion, data under column "Impressions" should be all 1 (meaning inpression was served)
### * Which method do I like better?
     - I like method 2 better as it's quicker and easier. LOL. We don't have to calculate metrics using match equations
     - But method 1 can enhance our understanding of t test
### * What are the input and output of this Python code?	
	- Input: a csv file downloaded from AdWords that containins data of conversions, clicks and impressions for control and experiment group
	- Output: 
		- mean
		- t statistics
		- p value
		- standard deviation
		- histogram graph of each metric