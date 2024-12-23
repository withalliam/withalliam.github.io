---
layout: post
title: 2022-2 Individual Project
subtitle: 
tags: [Bachelor's project]
author: Seokjun Kim
---

{: .box-note}
**Capstone project**

When I was undergraduate, I majored in computer science with mathematical statistics, and this post is a graduation study conducted by major in mathematical statistics.
I was looking for research that I could do with data from open source, and I could find data from MLB (Major League Baseball), one of my favorite sports.
The open-source data link is as follows.

[[Sean Lahman Baseball Dataset Open-source Link](http://seanlahman.com/)]

Sabermetrics, or the increasing use of data-driven baseball analysis, originated from Bill James' statistical study of baseball. Starting as a security guard at a factory, he rose to become a consultant for the Boston Red Sox, demonstrating his significant influence. The concept gained wider recognition and practical application, notably depicted in the movie Moneyball, where William Beane, the general manager of the Oakland Athletics, led the team to a 20-game winning streak in 2002.

One well-known metric in sabermetrics is the **Pythagorean Expectation**, which predicts a team's winning percentage **based on runs scored and runs allowed**. Its name comes from its mathematical resemblance to the Pythagorean theorem. The formula is derived from the Weibull distribution, and a proof for this derivation is provided below.

![weibull](https://withalliam.github.io/assets/img/weibull.png)

![weibull_proof](https://withalliam.github.io/assets/img/weibull_proof.png)

The format of the data is as follows, and information for machine learning also can be found below.

![baseball_data1](https://withalliam.github.io/assets/img/baseball_data.png)

![baseball_data2](https://withalliam.github.io/assets/img/baseball_data2.png)

Using the data above, preprocess the model features below. Code is also provided.

![baseball_model](https://withalliam.github.io/assets/img/baseball_model.png)

[[Code](https://github.com/withalliam/withalliam.github.io/blob/master/assets/code/baseball_winrate_prediction.ipynb)]

The model prediction results are as follows. A red line means a 5% error, and a red X mark means a point outside that range. Acc(5%) means how many predictions were successful within that point. In all metrics, using the features I preprocessed myself, you can see that the model predicted with various features of the team for the season showed the best results.

![baseball_result](https://withalliam.github.io/assets/img/baseball_result.png)

![baseball_result2](https://withalliam.github.io/assets/img/baseball_result2.png)

![baseball_result3](https://withalliam.github.io/assets/img/baseball_result3.png)

Finally, SHAP results from models excluding the features related to scores (runs, runs allowed, earned runs, ERA) that are key to predicting win rates, and features directly related to victory (save, shutout).

When these features are included, the importance of the features is so high that it is difficult to see the importance of other features.

![baseball_shap](https://withalliam.github.io/assets/img/baseball_shap.png)

The link to the paper written in Korean is as follows.

[[Comparison of Major League Baseball Winning Percentage Prediction Models and Pythagorean Expectation Using Machine Learning and Analysis of the Factors for Increasing or Decreasing Winning Percentage Using SHAP](https://www.dbpia.co.kr/pdf/pdfView.do?nodeId=NODE11183828&googleIPSandBox=false&mark=0&minRead=5&ipRange=false&b2cLoginYN=false&icstClss=010000&isPDFSizeAllowed=true&accessgl=Y&language=ko_KR&hasTopBanner=true)]