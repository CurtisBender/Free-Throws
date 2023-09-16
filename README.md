# Are Consecutive Free Throws Dependent Events?

# Purpose
The goal of this project was to determine if the first free throw shot affects the probability of making the second free throw shot, and if it does, how does it affect it?

If a player makes the first free throw, does it lead to overconfidence and result in a lower probability of making the second free throw? Or does making the first free throw indicate that the player is in the 'zone' and has a higher probability of making the second free throw?

# Tools
This project was completed using the pandas, NumPy, and SciPy libraries in Python.

# Sources
The dataset was comprised of information for over 600 thousand NBA free throw shots from 2006 to 2016. The dataset was obtained from Kaggle:

Mantey, S. (2017). NBA Free Throws. Kaggle. https://www.kaggle.com/datasets/sebastianmantey/nba-free-throws 


The test statistic used to calculate the p-value for each player was obtained from NIST:

7.3.3. How can we determine whether two processes produce the same proportion of defectives?. National Institute of Standards and Technology. 
(n.d.). https://www.itl.nist.gov/div898/handbook/prc/section3/prc33.htm 

# Process
I started this project by downloading the dataset and importing the csv as a dataframe in Python. As a result of an error by the NBA or the Kaggle member that scraped the data, there were instances of free throw 1 of 2 appearing twice or not having free throw 2 of 2. As a result, some data cleaning was required. From there, I reconfigured the dataframe to allow me to perform statistical analysis. 

A sample size of at least 30 free throws in both the missed first and made first groups was considered large enough. For each player with a large enough sample of free throws, I calculated the p-value with the null hypothesis that consecutive free throws are independent events. Here is a rigorous sample calculation for the p-value of [LeBron James](https://github.com/CurtisBender/Free-Throws/blob/main/P-Value%20Calculation%20Example.pdf).

# Results
```
Total Players                500
Statistically Significant     40
Better to Make 1st            36
Better to Miss 1st             4
```

Of the sample of 500 players that had a large enough sample size, only 40 had statistically significant differences at the 0.05 level. Of those 40 players, 36 had a higher probability of making the second free throw if they made the first free throw, and 4 had a higher probability of making the second free throw if they missed the first free throw.

In conclusion, for most players, there is not a statistically significant difference in the probability of making the second free throw after making or missing the first free throw. Of the few players that do have a statistically significant difference, most players had a higher probability of making the second free throw if they made the first free throw. This supports the idea that making the first shot indicates that the player is in the 'zone'.
