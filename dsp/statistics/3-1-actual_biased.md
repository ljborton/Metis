[Think Stats Chapter 3 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2004.html#toc31) (actual vs. biased)

>> 
```
import thinkstats2
import thinkplot

def BiasPmf(pmf, label):
    new_pmf = pmf.Copy(label=label)

    for x, p in pmf.Items():
        new_pmf.Mult(x, x)
        
    new_pmf.Normalize()
    return new_pmf

df = nsfg.ReadFemResp()

numkdhh=df['numkdhh']
pmf = thinkstats2.Pmf(numkdhh, label='actual')
thinkplot.Pmf(pmf)
thinkplot.Config(xlabel='Number of Kids per Household', ylabel='Pmf')
```

![Q2-1](https://github.com/ljborton/dsp/blob/master/img/ljb_q2_image1.png)

```
biased_pmf = BiasPmf(pmf, label='observed')
thinkplot.Pmf(biased_pmf)
thinkplot.Config(xlabel='Number of Kids per Household', ylabel='Pmf')
```
![Q2-2](https://github.com/ljborton/dsp/blob/master/img/ljb_q2_image2.png)

```thinkplot.PrePlot(2)
thinkplot.Pmfs([pmf, biased_pmf])
thinkplot.Config(xlabel='Number of Kids per Household', ylabel='PMF')
```

![Q2-2](https://github.com/ljborton/dsp/blob/master/img/ljb_q2_image3.png)

```print('mean', pmf.Mean())
print('biased_mean', biased_pmf.Mean())
```
mean 1.024205155043831
biased_mean 2.403679100664282
