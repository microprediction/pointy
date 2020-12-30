# pointy

Point estimates are usually evaluated in a framework like https://arxiv.org/abs/0912.0902

However, this library tries to evaluate the value of point estimates, and transformations, "downstream". The idea is that a point estimate is merely a step on the road towards a distributional estimate that might be evaluated by (say) continuous ranked probability score. So a point estimate is not trying to minimize RMSE or some other metric, but rather minimize (in a vague sense) close this brings us towards a good distributional estimate. It is better, therefore, to think of point estimates as mere anchor points or as translations of distributions - a translation applied at each and every data point. 



