# Final-Poject-BMI
This repository contains R functions for various tasks in data analysis and manipulation.

## Functions

### logLikBernoulli

```r
logLikBernoulli <- function(data) {
  # Compute the maximum likelihood estimate of the success probability for a Bernoulli trial
}
```

### survCurv

```r
survCurv <- function(status, time) {
  # Compute and plot a survival curve based on the status and time data.
}
```

### unscale

```r
unscale <- function(x) {
  # Reverse the centering and scaling applied to the vector x.
}
```

### pcApprox

```r
pcApprox <- function(x, npc) {
  # Return an approximation to the data x based on npc principal components.
  # The approximation is rescaled and centered to match the original data.
}
```

### standardizeNames

```r
standardizeNames <- function(data) {
  # Standardize variable names in the input data to small camel case.
}
```

### minimumN

```r
minimumN <- function(x1, x2 = NULL) {
  # Compute the minimum sample size needed for a t-test of the null hypotheses.
  # If x2 is provided, it's used for a two-sample t-test; otherwise, a one-sample t-test is performed.
}
```

### downloadRedcapReport

```r
downloadRedcapReport <- function(redcapTokenName, redcapUrl, redcapReportId) {
  # Download a Redcap report using the Redcap API.
}
```

## Usage

```r
# Example usage of logLikBernoulli
data <- c(1, 0, 0, 0, 1, 1, 1)
logLikBernoulli(data)

# Example usage of survCurv
data <- read.csv("https://jlucasmckay.bmi.emory.edu/global/bmi510/Labs-Materials/survival.csv")
survCurv(data$status, data$time)

# Example usage of unscale
scaled_vector <- scale(c(1, 2, 3, 4, 5))
unscale(scaled_vector)

# Example usage of pcApprox
data <- matrix(rnorm(100), ncol = 10)
npc <- 2
pcApprox(data, npc)

# Example usage of standardizeNames
data <- tibble::tibble(
  This_Is_A_Test = 1,
  Another_Test = 2
)
standardizeNames(data)

# Example usage of minimumN
x1 <- rnorm(20)
minimumN(x1)
x2 <- rnorm(30)
minimumN(x1, x2)

# Example usage of downloadRedcapReport
# downloadRedcapReport("redcapToken", "https://redcap.emory.edu/api/", "46524")
```

For more detailed information and usage instructions, please refer to the documentation of each function.
