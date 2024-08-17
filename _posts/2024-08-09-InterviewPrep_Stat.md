---
title: "(editing) Data Science Interview Prep - Statistics"
layout: single
classes: wide
categories: interviewPrep
typora-root-url: ../
tag: [interviewPrep,dataScience,statistics,interviewGoogle]
toc: true 
---

# Interview Questions & Answers

### Statistics

---

Questions from: 

<font size= 4pt>
  <I>
    <b>Medium "Google Data Scientist Interview Questions Step by Step" by John. H </b> <br> (https://medium.com/@bigtechinterviews/google-data-scientist-interview-questions-step-by-step-answers-2024-edition-094506cbde21) <Br>
    
<b>GitHub "Data Science Interview Questions & Answers" by Yossef Hosni</b>
    <br> (https://github.com/youssefHosni/Data-Science-Interview-Questions-Answers/blob/main/Statistics%20Interview%20Questions%20%26%20Answers%20for%20Data%20Scientists.md)
    </I>
    </font>



---

<br><br>



Explain the significance of the **p-value** in hypothesis testing.

- When conducting hypothesis testing, the p-value is critical as it assesses <u>the likelihood of obtaining observed results</u> or more extreme ones, <u>given that the null hypothesis is true</u>. If the p-value falls below a predetermined threshold, typically 0.05, it signifies a statistically significant difference and **leads to the rejection of the null hypothesis**. Essentially, the p-value is instrumental in determining the significance of the results derived from a data set.<br><br>



How would you use **linear regression** to predict future trends?

- Linear regression is a foundational tool in predictive modeling. It enables the prediction of a dependent variable based on one or more independent variables. Establishing the best-fit linear relationship between the variables provides a formula for predicting future values. This method is widely used in forecasting, where past data is analyzed to predict future occurrences.<br><Br>



What is **Bayes’ Theorem,** and how is it applied in data science?

- Bayes’ Theorem updates <u>the probabilities for hypotheses</u> <u>as more evidence or information becomes available.</u> It’s a vital component in a data scientist's predictive modeling and risk assessment toolkit. By incorporating prior knowledge, data scientists can refine their predictions and analyses, making Bayes’ Theorem critical for decision-making processes in data science.<br><br>



How can the **Central Limit Theore**m be used in data analysis?

- The Central Limit Theorem (CLT) is a crucial principle in statistics. It states that when we have a large enough number of *<u>independent</u>*, <u>*identically distributed random variables*</u>, the sampling distribution of the sample mean (or sum) will be approximately <u>*normally distributed*</u>, regardless of the original distribution of the variables. This significant theorem enables us to conclude population parameters using sample statistics, even when the population distribution is abnormal.
- Application examples
  - Confidence Intervals:
    - **Example**: Estimating the average height of adult women in a city. By taking a sufficiently large random sample, the sample mean can be used to construct a confidence interval for the population mean, assuming the sampling distribution is approximately normal.
  - Hypothesis Testing
    - **Example**: Testing whether a new drug reduces blood pressure. The mean blood pressure reduction in a sample of patients can be tested against a known value (e.g., no reduction) using the normal distribution properties provided by the CLT.

<br><br>



Briefly explain the **A/B testing** and its application. What are some common pitfalls encountered in A/B testing?

- **A/B Testing** (split testing) compares <u>two versions</u> of a webpage, app, or other user experience <u>to determine which one performs better.</u> By conducting an A/B test, we can statistically infer whether changes made to a product lead <u>to improvements or declines</u> in user behavior.



