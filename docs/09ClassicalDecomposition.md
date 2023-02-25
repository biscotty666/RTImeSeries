Classical Decomposition: Additive and Multiplicative
================

- <a href="#additive-decomposition"
  id="toc-additive-decomposition">Additive Decomposition</a>
- <a href="#multiplicative-decomposition"
  id="toc-multiplicative-decomposition">Multiplicative Decomposition</a>

[Scott Burk’s
Video](https://www.youtube.com/watch?v=vHoxz8ArxMQ&list=PLX-TyAzMwGs-I3i5uiCin37VFMSy4c50F&index=9)

``` r
library(fpp2)
```

    ## Registered S3 method overwritten by 'quantmod':
    ##   method            from
    ##   as.zoo.data.frame zoo

    ## ── Attaching packages ────────────────────────────────────────────── fpp2 2.5 ──

    ## ✔ ggplot2   3.4.1     ✔ fma       2.5  
    ## ✔ forecast  8.20      ✔ expsmooth 2.3

    ## 

# Additive Decomposition

- Estimate Trend: $T_t$
- Calculate the De-trended Series: $y_t-T_t$
- Estimate Seasonal Components: $S_t$
- Remainder: $R_t=y_t-T_t-S_t$

``` r
elecequip %>% 
  decompose(type = "additive") %>%
    autoplot() +
    xlab("Year") +
    ggtitle("Classical Additive Decomposition of Electrical Equipment Index")
```

![](09ClassicalDecomposition_files/figure-gfm/unnamed-chunk-2-1.png)<!-- -->

# Multiplicative Decomposition

- Estimate Trend: $T_t$
- Calculate the De-trended Series: $\frac{y_t}{T_t}$
- Estimate Seasonal Components: $S_t$
- Remainder: $R_t=\frac{y_t}{T_t \times S_t}$

``` r
elecequip %>% 
  decompose(type = "multiplicative") %>%
    autoplot() +
    xlab("Year") +
    ggtitle("Classical Multiplicative Decomposition of Electrical Equipment Index")
```

![](09ClassicalDecomposition_files/figure-gfm/unnamed-chunk-3-1.png)<!-- -->
