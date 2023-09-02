# Are Consecutive Free Throws Independent Events?

# Purpose
The goal of this project was to determine if the first free throw shot affects the probability of making the second free throw shot, and if it does, how does it affect it?

If a player makes the first free throw, does it lead to overconfidence and result in a lower probability of making the second free throw? Or does making the first free throw indicate that the player is in the 'zone' and has a higher probability of making the second free throw?

# Tools
This projects was completed using the pandas library, NumPy package, and SciPy stats module in Python. 

# Sources
The dataset was comprised of information for over 600 thousand NBA free throw shots from 2006 to 2016. The dataset was obtained from Kaggle:

Mantey, S. (2017). NBA Free Throws. Kaggle. https://www.kaggle.com/datasets/sebastianmantey/nba-free-throws 


The test statistic used to calculate the p-value for each player was obtained from NIST:

7.3.3. how can we determine whether two processes produce the same proportion of defectives?. National Institute of Standards and Technology. 
(n.d.). https://www.itl.nist.gov/div898/handbook/prc/section3/prc33.htm 

# Process
I started this project by downloading the dataset and imporing the csv as a dataframe in Python. From there, I cleaned the data and reconfigured it to allow me to perform statistiacal analysis. 

For each player with a large enough sample of free throws, I calculated the p-value with the null hypothesis that consecutive free throws are independent events.

# Results
![image](https://github.com/CurtisBender/Free-Throws/assets/143849290/33ac5abe-53f6-4a29-bee0-1e8ab043f95f | width=100)

Of the sample of 500 players that had a large enough sample size, only 40 had statistically significant differences at the 0.05 level. Of those 40 players, 36 players had a higher probability of making the second free throw if them made the first free throw, and 4 had a higher probability of making the second free throw if they missed the first free throw.

In conclusion, for most players there is not a statistically significant difference in the probability of making the second free throw after making or missing the first free throw. Of the few players that do have a statistically significant difference, most players had a higher probability of making the second free throw if they made the first free throw. This supports the idea that making the first shot indicates that the player is in the 'zone'.
