Part 1
------

The topic of this project: In this project the author will investigate the exponential distribution in R and compare it with the Central Limit Theorem. The exponential distribution can be simulated in R with rexp(n, lambda) where lambda is the rate parameter. The mean of exponential distribution is 1/lambda and the standard deviation is also 1/lambda. Set lambda = 0.2 for all of the simulations. The author will investigate the distribution of averages of 40 exponentials with a thousand simulations.

The histogram of the random expponentail is shown below:

``` r
set.seed(1234)
hist(rexp(1000))
```

![](Assignment_files/figure-markdown_github/unnamed-chunk-1-1.png)

The distribution of the average and standard deviation of the 40 exponentials with lambda 0.2 is:

``` r
set.seed(1234)
exmn=NULL
exsd=NULL
for(i in 1:1000){exmn <- c(exmn,mean(rexp(40,.2)))}
for(i in 1:1000){exsd <- c(exsd,sd(rexp(40,.2)))}
par(mfrow=c(1,2))
hist(exmn)
hist(exsd)
```

![](Assignment_files/figure-markdown_github/unnamed-chunk-2-1.png)

You can also embed plots, for example:

![](Assignment_files/figure-markdown_github/pressure-1.png)

Note that the `echo = FALSE` parameter was added to the code chunk to prevent printing of the R code that generated the plot.
