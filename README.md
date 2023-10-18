<p align = "center">
  <img src = "images/gai.png" alt = "" width = "30%" height = "30%" />
</p>

# Utilise ChatGPT as a learning companion, not as a substitution!
I teach “Data Analysis with Python” for various under graduate students pursuing Bachelor of Technology, Bachelor of Commerce, Bachelor of Business Administration, etc.

Recently in a class, we were discussing calculating statistical values in datasets using Python as a programming language. One of the students asked a very relevant question “Sir, why should I not ask AI to directly get me the Skewness and Kurtosis values (meaning, why should I bother about programming)?”

Having worked with Generative Artificial Intelligence (GAI) like ChatGPT / Bard / Llama for some time now, I explained how GAI suffer from “hallucinations” — confidently giving wrong answers.

Let us see this with an example.

## Kurtosis Calculation
In statistics, Kurtosis is a measure of tail of a distribution. There are several types of Kurtosis; generally “Fisher’s Kurtosis” also known as “Sample Excessive Kurtosis” is used, which is calculated as:
<p align = "center">
  <img src = "images/kurt.png" alt = "" width = "50%" height = "50%" />
</p>
where:

```
“n” is the number of data points,
"Xi" is the individual data point,
"Xavg" is the mean, and
"s" is the standard deviation (population std with ddof=True).
```

For a dataset of [4,2,5,8,6] the values are:

```
"n" = 5
"Xavg" = 25 / 5 = 5
"s" (with ddof=True) = 2.2360797749979 
"(Sum of (Xi — Xavg))^4" = 164
```

So calculating Kurtosis it comes out to,

**K = 0.2** *_(Platykurtic)_*.

This is the same answer we get with “kurt()” function both in Python and Excel.
