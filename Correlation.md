Three correlations to know about:
1. Pearson's (r)
2. Kendall's (tau)
3. Spearmen's (rho)


```
import seaborn as sns
sns.scatterplot(x="sleep_total", y="sleep_rem", data=msleep)
plt.show()

#add a trend line
sns.lmplot(x="sleep_total", y="sleep_rem", data=msleep, ci=Non)
plt.show()


#calculate correlation
msleep['sleep_total'].corr(msleep['sleep_rem'])

```
