To calculate the variance for a sample
```np.var(msleep['sleep_total'], ddof=1) ```

Notice the ddof parameter means that we divide by N-1. Which is the proper way to estimate the variance of a sample. For the hole population ddof = 1 works best.

Standard deviation vs. mean absolute deviation
- Standard deviation squares distances, penalizing longer distances more than shorter ones.
- Mean absolute deviation penalizes each distance equally.
- One isn't better than the other, but SD is more common than MAD.

## Quantiles

```
np.quantile(msleep['sleep_total'], 0.5)
```

0.5 quantile is the median. 

For multiple values:

```
np.quantile(msleep['sleep_total'], [0, 0.25, 0.5, 0.75, 1])
```

you can also use linespace

```
np.quantile(msleep['sleep_total'], [0, 0.2, 0.4, 0.6, 0.8, 1])
```

this is useful is you want to give the start, end and number of bins instead of the actual values

```
np.quantile(msleep['sleep_total'], np.linspace(0, 1, 5))
```


Outlier: data point that is substantially different from the others  
How do we know what a substantial difference is? A data point is an outlier if:  
data < Q1 - 1.5 × IQR or  
data > Q3 + 1.5 × IQR  


# How to randomly sample

without replacement
```
df.sample(n) # where n is the number of smaples
```

with sampling
```
df.sample(n, replace = True)
```

if we want to be able to reproduce the output, we set a seed first

```
np.random.seed(10)
```
