# Use Overfitting To Evaluate Different Models 

## Google Slide
[Machine Learning Model Selection Overfitting](https://docs.google.com/presentation/d/1oRTwh54K7QsZ-z5fYvRjTz21NDB7mZ_mxdL08l1C-_g/edit?usp=sharing)

## Introduction
### Overfitting and Underfitting



### Linear and Non-Linear Regression



### Mean Square Error (MSE)


## Design
* ### **Data**
  50% for training phase, 25% for validation phase and 25% for testing phase.


* ### **Get Models -- Training Phase**
  Using data for training set, get two models:
  *Linear Regression: 
      y = a + b * x
  *Non-Learner Regression: 
      y = a + b * x^2


* ### **Select Models -- Validation Phase**
  Using the two models get in training phase and calculate MSE and compare Models and select. 


* ### **Predict -- Testing Pase**
  Get the y values for data in Testing phase using the model selected previously.


## Implementation
[Detailed Steps]()

Model 1:	y = 0.238803 + 0.918775x
Model 2: 	y = 1.349341 + 0.151809 x^2

## Test
***Codes are uploaded**


## Enhancement Ideas
Plot all in one graph!


## Conclusion
With the evaluation using overfitting concept, Linear Regression model is slightly better than the Non-Linear Regression model.
The less sensitive the model act when adding new data, the better. 


## References
https://www.geeksforgeeks.org/underfitting-and-overfitting-in-machine-learning/ 

https://www.investopedia.com/terms/n/nonlinear-regression.asp#:~:text=Linear%20regression%20relates%20two%20variables%20with%20a%20straight%20line%3B%20nonlinear,the%20variables%20using%20a%20curve. 
