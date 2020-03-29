[Think Stats Chapter 5 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2006.html#toc50) (blue men)

import scipy.stats

mu = 178

sigma = 7.7

dist = scipy.stats.norm(loc=mu, scale=sigma)

type(dist)

dist.mean(), dist.std()

dist.cdf(mu-sigma)

minimum_height_in=5*12+10

maximum_height_in=6*12+1

minimum_height_cm=minimum_height_in*2.54

maximum_height_cm=maximum_height_in*2.54

#take the difference in the CDF for people between the maximum and minimum height to get the % of population that
#qualifies for blue man group

percent_qualifying=dist.cdf(maximum_height_cm)-dist.cdf(minimum_height_cm)

print('{:0.2F} percent of U.S. males are between 5ft 10 in and 6 ft 1 in'.format(percent_qualifying))

0.34 percent of U.S. males are between 5ft 10 in and 6 ft 1 in
