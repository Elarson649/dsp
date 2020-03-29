[Think Stats Chapter 3 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2004.html#toc31) (actual vs. biased)

resp = nsfg.ReadFemResp()

num_child=resp['numkdhh']

num_child.value_counts()

hist_unbiased = thinkstats2.Hist(num_child)

print(hist_unbiased)

pmf_unbiased = thinkstats2.Pmf(hist_unbiased, label='actual')

pmf_unbiased.Print()

biased_pmf = BiasPmf(pmf_unbiased, label='observed')

thinkplot.PrePlot(2)

thinkplot.Pmfs([pmf_unbiased, biased_pmf])

thinkplot.Config(xlabel='Number of Children', ylabel='PMF')

print('Unbiased Mean is {:.3f} children per family'.format(pmf_unbiased.Mean()))

print('Biased Mean is {:.3f} children per family'.format(biased_pmf.Mean()))


Unbiased Mean is 1.024 children per family

Biased Mean is 2.404 children per family
