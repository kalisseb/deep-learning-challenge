# Deep Learning - Neural Networks


## Overview

In this analysis, I used Deep Learning Neural Networks to create a tool that will allow the nonprofit, Alphabet Soup, identify which of their funding applicants have the best chance of success. A CSV file containing 34,000+ organizations that previously received funding via Alphabet Soup was provided for this analysis.


## Results

### Data Processing
To process and clean the CSV file provided, the following steps were completed:

	1. Review of initial data.
 
	2. The "EIN" and "NAME" columns were dropped as they didn't provide the necessary information.
 
	3. The number of unique values in each column was identified. 
 
	4. Columns with more than 10 unique values were scaled back by grouping the unique values that appeared the least often into one group and labeled as "Other". The columns and the parameters of which values were grouped as "Other" are below.
 
		a. "Application_Type" - This column contained 17 unique values. Any values that occurred <500 times were grouped leaving 9 unique values, including "Other".
	
		b. "Classification" - Column originally had 71 unique values. Any values that occurred <100 times were grouped leaving 12 unique values, including "Other".

	5. Categorical Data like "Application_Type" and "Classification" were converted to numeric values using Pandas.get_dummies. This pivoted the previously listed unique values in one column and converted each value into a distinct one. Then those columns were populated with "True" or "False" depending on the original value of the original column.
