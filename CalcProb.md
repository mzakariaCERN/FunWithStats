# Calculate the Probability from a continuous distribution 

Calculate the Probability in a Continuous Distribution assuming the period is between 0 and 30


Import uniform from scipy.stats  
```
from scipy.stats import uniform  
```
Calculate probability of waiting 10-20 mins  
```
prob_between_10_and_20 = uniform.cdf(20, 0, 30) - uniform.cdf(10, 0, 30)  
print(prob_between_10_and_20)
```
