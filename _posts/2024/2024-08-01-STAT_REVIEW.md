---
title: "Statistics & Probability Lecture Reivew "
layout: single
classes: wide
categories: lectureReview
read_time: True
typora-root-url: ../
tag: [dataScience,statistics,probability,lectureReview]
toc: true 
---

# -(editing)

<Statistics & Probability Review>

- Introduction of Statistics (2023) Whole Lecture Review



**Group Study** Aug 3rd, 2024

## **Chapter 1-3. <Mathematics & Probability Review, Basic Concepts>**



Data

- Categorical: Nominal, Ordinal, Ranked
- Quantitative: Discrete(pre-determined increments), Continuous(sliding scale)



Describing Categorical Distribution

- Which chart or graph do we need to use for the explanation
- frequencies on variables-



- Categorical 
  - Bar Chart
  - Absolute frequency & relative frequency on proportion



- Continuous
  - Histogram: for discrete and continuous as well
    - Binwidth or the length of the intervals: Use Sturges’ formula
    - Workflow



- Distribution
  - Center: mean, median, mode, trimmed mean
    - Mean: Sensitive to outliers
    - Median: the middle value of the ordered data (50th Percentile or Q2)
    - K%Trimmed Mean: Removing the highest & lowest k% of observations (Both removed)
      - 0%: sample mean, 50%: median
      - Compromise of Mean & Median / Not too sensitive to outliers
    - Mode: the most frequent value
      - Unimodal, Bimodal, Multimodal
      - symmetric & unimodal = mean, median, and mode are about to be the same
         \* Unimodal & Asymmetric: In general, the median is between mean and mode 
  - Dispersion(Spread): quantiles, IQR, variance, standard deviation, CV
    - Quantile: Kth percentile k/100 sample quantile
    - Qualtiles = 0.25, 0.50, 0.75 percentile range
    - IQR: Interquartile Range: the difference between 0.75 and 0.25 (having median)
      - Middle 50% of the observations
    - This can be visualized in 
      - Boxplot (minimum, Q1, Q2, Q3, and maximum)
      - Modified Boxplot
        - Whisker will be extended only within the Standard Span area 
        - Outliers will be set beyond the span separately
        - Standard Span: 1.5*(Q3-Q1)
    - Variance: The average squared deviation of observations from the mean
    - Standard Deviation: The positive square root of the variance
      - Size of the “typical” deviation from the mean, measured in the same units as observations
    - Coefficient of Variation: the ratio of the standard deviation to the mean
      - Dispersion that does not depend on units
      - Beneficial for comparing dispersion across different scenarios
      - The higher the CV, the higher the dispersion



- Skewness: a measure of the asymmetry of a distribution
  - Left skewed: Negative / Right skewed: Positive value



- Normality: z-scores, Empirical Rule
  - Z-score: standardizes the data by measuring how far a data point is from the mean in terms of standard deviation units
    - Z-score of 0: The data point is exactly at the mean.
    - Positive Z-score: The data point is above the mean.
    - Negative Z-score: The data point is below the mean.
    - Magnitude of the Z-score: Indicates the number of standard deviations the data point is from the mean. For example, a Z-score of +2 means the data point is two standard deviations above the mean.
    - Z-scores are helpful in various statistical analyses, such as identifying outliers, comparing scores from different distributions, and standardizing data for further study.
  - Empirical Rule:
    - Suitable for bell-shaped, symmetric, unimodal
    - One standard deviation: 68% / two standard deviations: 95% / 3 standard deviations of the mean: 99.7%
  - Chebyshev’s Inequality
    - The data is not symmetric & unimodal
    -  At least 1-(1/k)^2 of observations in a data set lie within k standard deviations of the mean.



- Z score is helpful for
  1. **Normalization**: By dividing by the standard deviation, Z-scores standardize data to a common scale with a mean of 0 and a standard deviation of 1. This allows for comparison across different distributions regardless of the original scale or units of the data.
  2. **Relative Position**: It provides a relative measure of the position of a data point within a distribution. Instead of just knowing the absolute difference from the mean, the Z-score tells us how significant that difference is in the context of the data's variability.
  3. **Comparability**: When data from different sources or distributions are standardized, their Z-scores can be directly compared. This is especially useful in fields like finance, education, and psychology, where scores from different tests or measurements must be compared.
  4. **Probability and Statistical Inference**: Z-scores are used in probability and inferential statistics to determine the likelihood of a score occurring within a normal distribution and to calculate probabilities. They are fundamental in standard normal distribution (a normal distribution with a mean of 0 and a standard deviation of 1).
  5. **Outlier Detection**: Z-scores help in identifying outliers. Data points with Z-scores beyond a certain threshold (e.g., greater than 2 or 3 in absolute value) are considered outliers, as they differ significantly from the mean.





- Quantile Plots
  - If we want to see if the data follows a normal distribution
  - quantile-quantile (Q-Q) plots
  - the sample quantiles (y) vs theoretical quantiles (x) 
  - Interpretation: left skewed/ right skewed





Transformation of Data

- Linear Transformation
  - change units, such as F to C
  - merely change the overall shape of the data
  - Check the skewness by using transformation



- Log Transformation: Reduce skewness
  - Right skewed: Reducing larger values in proportion to smaller one



- Box-Cox Power Transformation
  - lambda is necessary / The peak of the graph / to estimate optimal parameter lambda (over 95%) for a good fit





Two Variables

- Case CQ: Categorical and Quantitative 
  - e.g., Group A/ Group B / Height // mean, median, SD, etc., for each category/group
  - numerical statistics of each group
  - histogram or side-by-side boxplots



- Case CC: Conditional Distributions 
  - e.g., smokers, non-smokers
  - two-way table / cross-tabulation of two categorical variables
  - useful to calculate conditional distributions



- Case QQ: Quantitative and Quantitative
  - e.g., a relationship between weight & height
  - Two-way scatter Plot
    - Direction: positive, negative or neither
    - Form: linear, non-linear, or no
    - Strength: Strong, weak, or none (sparsity)
    - Outliers: if one unusual point is not on the line, it’s not an outlier
    - Correlation: the degree of linearly associated or related
      - Pearson’s Correlation Coefficient (Sample Correlation Coefficient)
      - how strong of a correlation is
        - r = cov(x,y) / var(x)*var(y)
      - Correlation vs. Covariance
        - both correlation and covariance measure the relationship between variables
        - Positive values = positive (linear) relationship
        - Negative values = negative (linear) relationship
        - Covariance: direction / not standardized
        - Correlation: direction & strength / standardized -1 and 1
        - Can be sensitive to outliers
      - It does not imply causation
        - not specifying the cause-and-effect relationship







10th Aug, 2024



## **Chapter 4. \<Probability and Combinatorics\>**

Probability

- the mathematics of random occurrences
- Events
  - Sample space: all possible outcomes that can be observed in a given situation
  - Event: which probability can be applied
    - possible outcomes / observed values
  - Intersection / Union / Complement
  - Null events = that can never occur
- Operations on Events: De Morgan’s Laws
  - $(A \bigcup B)^c$ = $A^c \bigcap B^c $$
  - $(A \bigcap B)^c $= $A^c \bigcup B^c$
- $Pr(A)$ = # of times A occurs / total # of trials



Mutual Exclusivity and Exhaustiveness

- When the probabilities of mutually exclusive events sum to 1, the events are exhaustive (i.e., no other possible outcomes)
- Addition Rule: Mutually Exclusive Events
  - $Pr$($A \bigcup B$) = $Pr(A)$ + $Pr(B)$
  - $Pr(A \bigcup B)$ = $Pr(A) + Pr(B) - Pr(A \bigcap B)$
- Conditional Probability
  - The probability that event A will occur, given that we already know the outcome of Event B
  - $Pr(A \vert B)$ = probability of A given B
  - $Pr(B \vert A) \neq 1- Pr(A \vert B)$
  - $Pr(B \vert A) \neq  1- Pr(B \vert A^c)$
  - $Pr(B \vert A) = 1 - Pr(B^c \vert A)$
- Multiplicative Rule
  - $Pr(A \bigcap B) = Pr(A)\cdot Pr(B\vert A) = Pr(B) \cdot Pr(A\vertB)$



Independence

- The outcome of one event has no effect on the outcome of another event
- $Pr(A \vert B) = Pr(A)$, $Pr(B \vert A) = Pr(B)$
   $\Rightarrow$ $Pr(A \vert B) = Pr(A \bigcap B) / Pr(B) = Pr(A) \cdot Pr(B) / Pr(B) = P(A) $



Mutual Independence

- Suppose we have n events, N. These n events are mutually independent iff, for every subset of events M subset N
   $ \Rightarrow Pr(A_1 \bigcap {A_2} \bigcap A3) = Pr(A_1) \cdot Pr(A_2) \cdot Pr(A_3)$
- If all but the last equality hold, $A_1$, $A_2$, $A_3$ are pairwise independent, but not mutually independent 
- Mutual Exclusivity and Independence are not the same thing
  (Independence 독립변수: 각 사건의 확률에 영향을 주지 않는다 / its probability is unaffected
   Mutual Exclusivity 상호배타적: 공유하는 원소가 없음 / no mutual elements)



Law of Total Probability

- mutually exclusive and exhaustive events
- $Pr(E)$ = $Pr(E \bigcap A_1) + Pr(E \bigcap A_2) + … + Pr(E \bigcap A_n) $
        $= Pr(E \vert A1) \cdot Pr(A1) + Pr(E \vert A2) \cdot Pr(A2) + \dots + Pr(E \vert A_n) \cdot Pr(A_n)$



Bayes’ Theorem

$Pr(A \vert B)   = Pr(B \vert A) \cdot Pr(A) / Pr(B) = Pr(B \vert A) \cdot Pr(A) / Pr(B \vert A) \cdot Pr(A) + Pr(B \vert A^c) \cdot Pr(A^c)$

Posterior =  Likelihood * Prior / Prior



![Pasted Graphic.jpg](blob:file:///ea97178c-6f40-4c05-9b3f-1df09adcfb60)





Diagnostic Tests (Probability of)

- Sensitivity(True Positive): a positive test given that actually has the disease
  - $Pr(T+ \vert D_1)$
- False negative probability: a negative test given that actually has the disease
  - $Pr(T- \vert D_1) = 1$ - Sensitivity
- Specificity(True Negative): a negative test given that does not have the disease
  - $Pr(T- \vert D_2)$
- False positive probability: a positive test given that does not have the disease
  - $Pr(T+ \vert D_2)$ = 1 - Specificity





Positive Predictive Value (PPV)

- The probability that a person has a positive test with actual disease
  - $Pr(D_1  T+)
     = Pr(D_1 \bigcap T+) / Pr (T+)
     = Pr(T+ \vert D_1) \cdot Pr(D_1) / Pr(T+ \vert D_1) \cdot Pr(D_1) + Pr(T+ \vert D_2) \cdot Pr(D_2)$ 



Negative Predictive Value (NPV)

- The probability that a person with a negative test with no disease
  - $ Pr(D_2 \vert T-)$ (by using Bayes’ Rule, sensitivity, and specificity)
    $ = Pr(D_2 \bigcap T-) / Pr (T-)$
    $ = Pr (T- \vert D_2) \cdot Pr(D_2) / Pr(T- \vert D_2) \cdot Pr(D_2) + Pr(T- \vert D_1) \cdot Pr(D_1)$







## **Chapter 5. \<Distribution I\>**



Random Variables

- Random Variable: A variable that can take on different values based on chance.
  - Discrete random variable: has distinct outcomes within a finite or countably infinite sample space
    - Example: Coin flip 
  - Continuous random variable: has any value outcomes in an interval within uncountable sample space
    - Examples: Time required to run a mile



Probability Distribution

- A list of all possible values for a random variable, along with their probabilities.
  - Discrete: Probability Mass Function (PMF)
  - Continuous: Probability Dense Function (PDF)
- Discrete PMF:  $0 \geq p_x(s) = Pr (X= x) \geq 1$
  $ S_x$(sample space) consists of all $x$ for which $p_x(x) > 0$ (all achivebable outcomes)
- Continuous PDF: $Pr(a \geq X \geq b) = \int_{a}^{b} fx(x)dx$
   = Area under f between a and b



Normalization

- (must) probability distributions sum / integrate to 1 
- **Normalization: Scalar adjustment in order to ensure that $Pr(S_x) = 1$**
  - Normalization constant: 1/denominator



Cumulative Distribution Functions (CDFs)

- The cumulative distribution function(CDF) of a random variable X is
   $F_X(x) = Pr(X \leq x)$ for all $x$ is $(- \infty, \infty)$



Expected Value $E(X)$

- A theoretical average of a infinitely large sample
  - $X$ is a discrete variable :
    $\mu_X = E(X) = \sum_{X \in S_X} \cdot Pr(X=x)$
  - $X$ is a continous random variable:
    $\mu_X = E(X) = \int^{\infty}_{\infty} x \cdot f_X(x)dx$
  - If $c$ is constant, then
    $E(c) = c$



Variance $var(X)$

- Measures the tendency of $X$ to deviate from $E(X)$
- $var(X) = E\bigg(\big(X-E(X) \big)^{2} \bigg)  $
  $ = E(X^2) - E(X)^2$
- $\sigma^2 =  \sigma^2_{X} = var(X)$ 
  Standard deviation: $\Rightarrow \sigma = \sigma_X = \sqrt{var(X)}$
  - $X$ is a discrete variable with mean $\mu_X$:
    $\sigma^2_{X} = \sum_{S_X}(x- \mu_X)^2Pr(X=x)$
  - $X$ is a continous random variable with mean $\mu_X$:
    $\sigma^2_X = \int^{\infty}_{-\infty} (x-\mu_X)^2f_X(x)dx$



<br>

<br>

