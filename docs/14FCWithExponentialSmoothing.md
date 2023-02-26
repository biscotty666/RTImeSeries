Forecasting with Exponential Smoothing
================

[Scott Burk’s
Video](https://www.youtube.com/watch?v=aquvCL3_6pI&list=PLX-TyAzMwGs-I3i5uiCin37VFMSy4c50F&index=14)

$$\hat{y}_{T+1/T}= \alpha y_T+ \alpha(1- \alpha)y_{T-1}+ \alpha (1- \alpha )^2y_{T-2}+...$$

- $0 <=\alpha<=1$ is the smoothing parameter
  - Larger $\alpha$ gives more weight on $y_T$ and quicker dampening,
    smaller is closer to equal weight
- Weighted Averages of Past Observations
- Weights decay exponentially
- Simple Exponential Smoothing (SES)
  - Applicable when no clear trend or seasonal pattern exists
- Some variations
  - Naive method
  - Average method
  - Weighted Average method
