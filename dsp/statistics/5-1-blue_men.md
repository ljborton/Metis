[Think Stats Chapter 5 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2006.html#toc50) (blue men)

>> 
```
import scipy.stats

low=(5*12+10)*2.54
high=(6*12+1)*2.54
mu=178
sigma=7.7
```
```
lowperc=scipy.stats.norm.cdf(low, loc=mu, scale=sigma)
highperc=scipy.stats.norm.cdf(high, loc=mu, scale=sigma)
diffperc = highperc-lowperc
print('lowperc',lowperc,'highperc',highperc,'diffperc', diffperc)
```
lowperc 0.48963902786483265 highperc 0.8323858654963072 diffperc 0.34274683763147457      
A little over 34% of the US male population is between 5'10" and 6'1".
