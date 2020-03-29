[Think Stats Chapter 2 Exercise 4](http://greenteapress.com/thinkstats2/html/thinkstats2003.html#toc24) (Cohen's d)

first_wgt=firsts['totalwgt_lb']

other_wgt=others['totalwgt_lb']

mean_diff=first_wgt.mean()-other_wgt.mean()

n1=len(first_wgt)

n2=len(other_wgt)

pooled_var=(n1*first_wgt.var()+n2*other_wgt.var())/(n1+n2)

weight_eff_size=mean_diff/(np.sqrt(pooled_var))

print('The birth weight effect size is {:+.3f} standard deviations'.format(weight_eff_size))


The birth weight effect size is -0.089 standard deviations

