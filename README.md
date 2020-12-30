# pointy

Point estimates are usually evaluated in a framework like https://arxiv.org/abs/0912.0902

However, this library tries to evaluate the value of point estimates, and transformations, "downstream". The idea is that a point estimate is merely a step on the road towards a distributional (quantile) estimate that might be evaluated by (say) continuous ranked probability score (CRPS). So a point estimate is not trying to minimize RMSE or some other metric, but rather minimize (in a vague sense) the remaining work required to produce a good distributional estimate. 

Suppose ys is a time series of observations and xs a vector of point estimates. We let zs = ys-xs denote the residual. We compare two such vectors of point estimates by the CRPS score of the empirical distribution of zs, after a burn-in period. 

Note that xs can be viewed as a sequence of transformations: f_i : y -> y - xs[i]

More generally, if f_i( ) is a sequence of monotone transformations then we can infer the CRPS of a running estimate of the distribution (that is, f_i composed with the empirical distribution.  

It's just an idea. 


