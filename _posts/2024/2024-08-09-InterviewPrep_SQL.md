---
title: "(editing) Data Science Interview Prep - SQL "
layout: single
classes: wide
categories: interview_Prep
read_time: True
typora-root-url: ../
tag: [interviewPrep,dataScience,statistics,interviewGoogle]
toc: true 
---

# Interview Questions & Answers

### SQL

---

Questions from: 

<I><b>[Medium "Google Data Scientist Interview Questions Step by Step" by John. H](https://medium.com/@bigtechinterviews/google-data-scientist-interview-questions-step-by-step-answers-2024-edition-094506cbde21) </b></I>

<I><b>[GitHub "Data Science Interview Questions & Answers" by Yossef Hosni](https://github.com/youssefHosni/Data-Science-Interview-Questions-Answers/blob/main/Statistics%20Interview%20Questions%20%26%20Answers%20for%20Data%20Scientists.md)</b></I>

---





How would you calculate the **median** in SQL?

- There are many ways to calculate the median in SQL, but one approach is to use a combination of the <u>COUNT and RANK</u> functions. First, count the total number of values in the column using COUNT, then rank each value using RANK (with an ORDER BY clause). Finally, select the value with a rank equal to half of the total count.

How would you **handle missing value**s in a dataset using SQL?

- One approach to handling missing values is to use the <u>CASE</u> statement. This allows you to set specific conditions <u>for replacing missing values with another value, such as zero or the average of the column’s non-missing values.</u>

What’s the **difference** between using a **UNION** and a UNION ALL in SQL?

- The main difference between using a UNION and a UNION ALL in SQL is that <u>UNION automatically removes duplicate records from the results, whereas UNION ALL includes all duplicates.</u> <br>

  By default, UNION performs a distinct operation on the results, which can be helpful when you want to ensure that all returned rows are unique. On the other hand, UNION ALL does not perform any duplicate removal, making it faster in cases where you know the datasets do not overlap or when duplicate records are needed in the result set.

<img src="/blog/images/2024-08-05-InterviewPrep_SQL/image-20240805131700584.png">