# SYDE 212: Probability and Statistics

We when start looking at our data, we start with a graphical summary.
## Graphical Representations
### Histogram

**Guide to # of bins**

* $\approx \sqrt n$
* $2^1, 2^2, 2^3, ... 2^i$
* Using a histogram will end up losing all of the information afterwards.

### Stem-Leaf Plots
![](http://www.webquest.hawaii.edu/kahihi/mathdictionary/images/stem_leaf_graph1.gif)

### Box Plot
Based on 5 data points. Breaks up the data into quarters.

* Minimum Value (10000)
* Q1
  * First quartile. Take median of median.
* Median
  * For odd n: $\frac {(n+1)^\text{nth}} 2$ largest value
  * For even: take middle number between centers
* Q3
  * Third quartile. Take median of top 50%.
* Maximum Value (33000)

## Measures of Variability
* The (sample) variance of a set of $n$ numbers, denoted by $s^2$ is
$$s^2 = \frac {\sum(x_i - \overline{x})^2} {n-1}$$
* The standard deviation, denoted by $s$, is the (positive) square root of the variance
$$s = \sqrt {\frac {\sum(x_i - \overline{x})^2} {n-1}}$$