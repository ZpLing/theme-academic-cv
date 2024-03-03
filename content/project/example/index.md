---
title: A Feature Base Approach to Analyzing Word Complexity 
summary: The Starting Point of My AI Journey.
tags:
  - Machine Learning
date: '2016-04-27T00:00:00Z'

# Optional external URL for project (replaces project detail page).
external_link: ''

image:
  caption: Photo by rawpixel on Unsplash
  focal_point: Smart

url_code: ''
url_pdf: 'https://github.com/ZpLing/MCM/blob/main/MCM%20Paper.pdf'
url_slides: ''
url_video: ''

# Slides (optional).
#   Associate this project with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides = "example-slides"` references `content/slides/example-slides.md`.
#   Otherwise, set `slides = ""`.


---

Wordle serves as a popular puzzle and continues to grow in popularity. Have been asked to do an analysis of the data provided, we modeled according to the tasks.Several models are established: Model Ⅰ:Interval Prediction Based on ARIMA Model; Model Ⅱ:Gradient Descent Optimization Model; Model Ⅲ:Associated Percentage Prediction Model; Model Ⅳ:Words Difficulty Classification Model. With varieties of visualization methods applied, most of our results are displayed in figures, making it intuitive to be shown. Model Ⅰ:As the daily number of reported results(from 7,Jan,2022 to 31,Dec,2023) is given, we firstly set out to build the ARIMA(p,d,q) model. Then, based on the verification of the unit root test and white noise test, the validation of using ARIMA model is fully proved. Next, the 250 previous data is used to predict the rest 109 data. we select the strongly predictive time series which matches the predicted known data best and determine d=1. With the introduction of ACF and PACF, the parameter p and q of ARIMA is identified 1 and 0. Finally, according to the ARIMA(1,1,0), The interval prediction of number of reported results is shown in Figure 9. Model Ⅱ: To simplify the problem, we split the words into letters and define the type and number of the letters as the attributes of the word, regardless of the sequence of the order. For each single word, its attribute is represented by a 1*26 vector. By combining all vectors of
sample words, we got a matrix. In this step, we can quanlify the attributes of the words, since the number of letters in one word is five. The results are shown in the Figure 10,which demonstrates that attributes of the word affect the percentage of scores in hard mode greatly. Model Ⅲ: This model is actually a supplement to Model Ⅰ . In the Model 1, the
predicted data only considers the factor of date and there is a necessity to consider the factor of a given word. And in this section, what we focus is the factor of word, as the factor of date has been discussed in Model 1. By collecting letters’ data and converting them into a matrix, we can finally quantify the features of the words. The result is displayed in Figure 12. Model Ⅳ: Based on the Model Ⅱ, we can score the difficulty of all letters through creating a “Grading System”. Meanwhile, we add up all the scores of letters in one word. Therefore, we are able to score each word and classify words by the difficulty. And we use
scatter diagram to plot the different classifications in different colors in order to clearly present the relationship between each sample.The result is given in Figure 13. In addition, we list and describe 2 interesting features of the data set : One is we find that the strong relativity of number in hard mode and reported results, which is displayed directly in Figure 15. The other is that the try of different words can show different amount of information and the result is visualized in Figure 17. Finally, as for the sensitivity analysis, we randomly choose 50% of the samples, use
them to create 2 matrix and calculate their personal relativity with the result shown in Figure. Afterwards, a letter of results has been written for Puzzle Editor of the New York Times.
