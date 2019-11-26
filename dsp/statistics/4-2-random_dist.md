[Think Stats Chapter 4 Exercise 2](http://greenteapress.com/thinkstats2/html/thinkstats2005.html#toc41) (a random distribution)

>> 
```import random
import numpy as np 
```
```
rdm = np.random.random(1000)
    
pmf = thinkstats2.Pmf(rdm, label='1000 random numbers')
thinkplot.Pmf(pmf)
thinkplot.Show(xlabel='Random Number', ylabel='PMF')
```
![Q3-1](https://github.com/ljborton/dsp/blob/master/img/ljb_q3_image1.png)

```
cdf = thinkstats2.Cdf(rdm, label='1000 Random Numbers')
thinkplot.Cdf(cdf)
thinkplot.Show(xlabel='Random Number', ylabel='CDF')
```
![Q3-2](https://github.com/ljborton/dsp/blob/master/img/ljb_q3_image2.png)
