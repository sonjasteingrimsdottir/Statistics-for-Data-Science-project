# Statistics for Data Science 🌌

### Problem Statement
In an effort to find life in the universe, a space mission discovers a small remote planet with inhabitants. Our task is to estimate the total population of the planet, denoted as **Nmax**. Since we cannot survey every inhabitant, we sample 100 inhabitants and record their assigned numbers, which range from 1 to **Nmax**. 

Using this data, we apply statistical methods to estimate **Nmax** through two approaches:
1. **Sample maximum (x(N)):** The largest observed number in the sample.
2. **Twice the mean (2 * x̄):** Two times the average number in the sample.

Additionally, we analyze the variability of these estimators using the **Bootstrap** method.

---

### Table of Contents
- [Tech Stack](#tech-stack)
- [Project Overview](#project-overview)
- [Bootstrap Method](#bootstrap-method)
- [Steps of Analysis](#steps-of-analysis)

---

### Tech Stack
- **R Studio**
- **R Libraries:** readxl, ggplot2, dplyr, boot
- **Excel:** For data input

---

### Project Overview
The project explores two main estimators of the total population **Nmax**: the sample maximum and twice the sample mean. We used **inhabitants.xlsx**, which contains a random sample of 100 inhabitants’ numbers. 

We estimate **Nmax** and analyze the reliability of these estimators through the **Bootstrap method**, which allows us to approximate the distribution of both estimators and assess their variability.

---

### Bootstrap Method
The **Bootstrap** is a powerful simulation technique used to estimate the variability of statistics, especially when the underlying distribution is unknown. For our analysis:
1. We sample 100 observations **with replacement** from the original data.
2. We compute both the maximum (x(N)) and twice the mean (2 * x̄) for each bootstrap sample.
3. We repeat this process 200 times to approximate the distribution and compute confidence intervals for each estimator.

---

### Steps of Analysis
1. Create 200 bootstrap samples from the data in `inhabitants.xlsx`.
2. Compute the maximum (x(N)) and twice the mean (2 * x̄) for each sample.
3. Calculate the average and standard deviation of both estimators across the 200 bootstrap samples.
4. Construct 95% confidence intervals for both estimators by taking the 2.5% and 97.5% percentiles.
5. Visualize the distributions of both estimators using histograms.
6. Critically analyze the performance of both estimators using concepts such as bias and mean squared error (MSE).
7. Discuss the pros and cons of each method in terms of accuracy and variability.


