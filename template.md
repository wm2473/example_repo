Simple document
================

``` r
library(tidyverse)
```

    ## ── Attaching packages ─────────────────────────────────────── tidyverse 1.3.2 ──
    ## ✔ ggplot2 3.3.6      ✔ purrr   0.3.4 
    ## ✔ tibble  3.1.8      ✔ dplyr   1.0.10
    ## ✔ tidyr   1.2.0      ✔ stringr 1.4.1 
    ## ✔ readr   2.1.2      ✔ forcats 0.5.2 
    ## ── Conflicts ────────────────────────────────────────── tidyverse_conflicts() ──
    ## ✖ dplyr::filter() masks stats::filter()
    ## ✖ dplyr::lag()    masks stats::lag()

I’m an R Markdown document!

# Section 1

Here’s a **code chunk** that samples from a *normal distribution*:

``` r
samp = rnorm(1000)
length(samp)
```

    ## [1] 1000

# Section 2

I can take the mean of the sample, too! The mean is -0.0547935.

If roundup the mean: round(mean(samp),#round up num) ex: round up 2:
round(mean(samp),2)

# Section 3

This is going to make a plot! First I gengerate a dataframe, then use ”
ggplot” to make a scatterplot. control, alt, I–\> echo= FALSE message =
FALSE ![](template_files/figure-gfm/chunk_scatterplot-1.png)<!-- -->

``` r
ggplot(plot_df, aes(x=x, y =y)) + geom_point()
```

![](template_files/figure-gfm/chunk_histogram-1.png)<!-- -->

Quick solution on the website

``` r
la_df=
   tibble(
    norm= rnorm(n=500, mean = 1),
    logical = norm > 0,
    abs_norm = abs(norm),
    round(median(norm),2)
  )

ggplot(la_df, aes(x= abs_norm)) + geom_histogram()
```

    ## `stat_bin()` using `bins = 30`. Pick better value with `binwidth`.

![](template_files/figure-gfm/unnamed-chunk-3-1.png)<!-- --> Tables
————————————————————

| First Header | Second Header |
|--------------|---------------|
| Content Cell | Content Cell  |
| Content Cell | Content Cell  |
