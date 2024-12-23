---
layout: post
title: 2022-2~2023-1 Capstone Project
subtitle: 
tags: [Bachelor's project]
author: Seokjun Kim
---

{: .box-note}
**Capstone project**

The final capstone project when I was an undergraduate. The final project was about EV (Elecrtic Vehicle), and BMS (Battery Management System), DTE (Distance To Empty)

Details of the BMS data of EV cannot be disclosed for security reasons (it is not my own data), but simple information and model results are disclosed later.

This project allowed me to gain advanced experience in Cassandra Database, Python, and server interworking.

The data we used are BMS data and telematics data. BMS data exists every 2 seconds, and every 1 minute for telematics data. This data was transmitted to raw data with noise or error, and preprocessing started to refine this data.

![rul_bms](https://withalliam.github.io/assets/img/rul_bms.png)

We initially tried to predict the SoH of electric vehicle batteries by using this data to predict the RUL (Remaining Useful Life), the life of the battery, but the initial data only existed about 10 electric vehicles and about 3 months of data. Therefore, it was virtually impossible to predict the SoH of the long term, and we changed the target to predict the DTE that could replace the SoH.

We created a model that predicts DTE based on the remaining SoCs using the core idea. To be precise, by putting the SoC that starts driving (StartSoC) and the SoC that are used (UseSoC) into the model to predict the mileage (in the cycle), the two features are set equally when predicting the mileage so that the remaining mileage in that SoC can be predicted. For example, if you want to predict the mileage when there are 50% of SoC left, you can put 50 each in StartSoC and UseSoC. 

![rul_model](https://withalliam.github.io/assets/img/rul_model.png)

We confirmed that the x-axis is the actual mileage, the y-axis is the predicted mileage, and that the predictions performed by the model performed more than twice the RMSE, MAPE criteria, and more than three times the R-squared criteria than the onboard predictions received through telematics data.

![rul_result](https://withalliam.github.io/assets/img/rul_result.png)

The link to the paper written in Korean is as follows.

[[Real-world BMS Signal-based Driving Range Prediction for Electric Vehicles](https://www.dbpia.co.kr/pdf/pdfView.do?nodeId=NODE11705610&googleIPSandBox=false&mark=0&minRead=5&ipRange=false&b2cLoginYN=false&icstClss=010000&isPDFSizeAllowed=true&accessgl=Y&language=ko_KR&hasTopBanner=true)]

