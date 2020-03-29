[Think Stats Chapter 4 Exercise 2](http://greenteapress.com/thinkstats2/html/thinkstats2005.html#toc41) (a random distribution)

random_numbers=np.random.random(1000)

random_pmf = thinkstats2.Pmf(random_numbers)

thinkplot.pmf(random_pmf)

thinkplot.Config(xlabel='Random Number Between 0-1', ylabel='PMF')

#Each random number is unique, so each value has a probability of 0.001 (1/1000)

random_cdf = thinkstats2.Cdf(random_pmf)

thinkplot.Cdf(random_cdf)

thinkplot.Config(xlabel='Random Number Between 0-1', ylabel='CDF')

#Yes, the distribution is uniform!
