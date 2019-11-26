[Think Stats Chapter 2 Exercise 4](http://greenteapress.com/thinkstats2/html/thinkstats2003.html#toc24) (Cohen's d)

>> 
```!python nsfg.py      
import nsfg
import math

def CohenEffectSize(group1,group2):
        diff = group1.mean() - group2.mean()
        var1 = group1.var()
        var2 = group2.var()
        n1,n2 = len(group1), len(group2)
        
        pooled_var = (n1*var1 + n2*var2)/(n1+n2)
        d =diff/math.sqrt(pooled_var)
        return d
```
```
preg=nsfg.ReadFemPreg()
live=preg[preg.outcome==1]    
firsts=live[live.birthord==1]    
others = live[live.birthord!=1]

mean1 = firsts.totalwgt_lb.mean() 
mean2 = others.totalwgt_lb.mean()
diff = mean1-mean2
print('mean1',mean1,'mean2', mean2, 'diff', diff)
```
mean1 7.201094430437772 mean2 7.325855614973262 diff -0.12476118453549034   
First born babies are about 0.12 lbs lighter than other babies.

```
CohenEffectSize(firsts.totalwgt_lb,others.totalwgt_lb)
```
-0.088672927072602   

The difference in means between first born babies and all others is -.09 standard deviations.  This is three times larger than 0.03, the difference in means for pregnancy length.

      
