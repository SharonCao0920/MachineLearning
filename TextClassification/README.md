# Project: Who is the real author of Hamlet?
[Google Slide](https://hc.labnet.sfbu.edu/~henry/sfbu/course/mllib/naive_bayes/slide/exercise_naive_bayes.html)

## Introduction

### Description

This project is to use the text classifier to determine who is the real author of Hamlet (the given text).

<img width="494" alt="Screenshot 2023-03-04 145800" src="https://user-images.githubusercontent.com/54694766/223354909-bab9286d-252f-4f79-a1f3-0c53294295fb.png">

### Text Classification: Definition

<img width="308" alt="Screenshot 2023-03-06 223653" src="https://user-images.githubusercontent.com/54694766/223355185-e3c8dff0-c08b-4d18-b277-699f3df94b8c.png">

### Text Classification: Application 

* Assigning subject categories, topics, or genres
* Spam detection
* Authorship identification
* Age/gender identification
* The identification of the language used in a document
* Sentiment analysis (positive or negative movie review)

### Text Classification: Bayes’ Rule 

<img width="270" alt="Screenshot 2023-03-06 223902" src="https://user-images.githubusercontent.com/54694766/223355452-9e708599-ff44-44aa-91af-1b4301b5a2f2.png">


## Design

### Example

**Data**

<img width="87" alt="Screenshot 2023-03-06 224245" src="https://user-images.githubusercontent.com/54694766/223355599-0ffd1a32-7df6-4aa3-91d7-b57ae227c6e0.png">

<img width="182" alt="Screenshot 2023-03-06 224314" src="https://user-images.githubusercontent.com/54694766/223355638-011673da-ec8c-4235-9336-7157614d5aa2.png">

<img width="270" alt="Screenshot 2023-03-06 223955" src="https://user-images.githubusercontent.com/54694766/223355667-0b8f0c38-7633-436f-ba2f-1af62e29ea5c.png">

**Training**

<img width="292" alt="Screenshot 2023-03-06 224448" src="https://user-images.githubusercontent.com/54694766/223355860-94f92f25-b1ac-4c24-89e5-ba8ebfe8f81f.png">

<img width="426" alt="Screenshot 2023-03-06 224533" src="https://user-images.githubusercontent.com/54694766/223355909-e310ed83-632a-4da5-a044-fe647afd0bce.png">

<img width="487" alt="Screenshot 2023-03-06 224630" src="https://user-images.githubusercontent.com/54694766/223355989-72a36e64-a0c9-46f6-8078-4c3d25876922.png">

**Test**

<img width="415" alt="Screenshot 2023-03-06 224950" src="https://user-images.githubusercontent.com/54694766/223356127-de1fda03-15cd-4d48-b1e6-e0c106ed82aa.png">

<img width="415" alt="Screenshot 2023-03-06 225000" src="https://user-images.githubusercontent.com/54694766/223356152-2425c5bc-b364-4a66-a218-d4c97a46c906.png">

**Conclusion**

<img width="212" alt="Screenshot 2023-03-06 225039" src="https://user-images.githubusercontent.com/54694766/223356213-60ecba7c-4d66-4976-9697-10e1c08b4f12.png">

## Implementation - Training

**Prior**

* P(C) = Nc / N 
= Number of class C / Total number of classes = 3/7

* P(W) = Nw / N 
= Number of class W / Total number of classes = 2/7

* P(F) = Nf / N 
= Number of class F / Total number of classes = 2/7

**Conditional Probabilities:**

<img width="487" alt="Screenshot 2023-03-06 225925" src="https://user-images.githubusercontent.com/54694766/223356749-466a1612-d032-4c79-91d1-eee814a24a77.png">

<img width="474" alt="Screenshot 2023-03-06 230044" src="https://user-images.githubusercontent.com/54694766/223356754-95ebf38c-7d7b-4afc-ba34-8bbd963b70df.png">

<img width="476" alt="Screenshot 2023-03-06 230209" src="https://user-images.githubusercontent.com/54694766/223356755-667a1cd4-9f77-4975-abc1-d056bc1dfa79.png">

<img width="480" alt="Screenshot 2023-03-06 230252" src="https://user-images.githubusercontent.com/54694766/223356743-17c435ec-fe8b-41df-b6c0-592e3fdd06bf.png">

<img width="474" alt="Screenshot 2023-03-06 230318" src="https://user-images.githubusercontent.com/54694766/223356748-d1d41bde-889a-4d98-9abf-f297efe30a04.png">

## Test

All Claculated data:

<img width="617" alt="Screenshot 2023-03-06 232203" src="https://user-images.githubusercontent.com/54694766/223357598-df537eeb-7db7-4ba3-8ab8-41c8450eb457.png">

<img width="462" alt="Screenshot 2023-03-06 232235" src="https://user-images.githubusercontent.com/54694766/223356816-6ea2a6a0-9eaf-4266-9b24-38e6f19207df.png">


## Conclusion

<img width="364" alt="Screenshot 2023-03-06 232304" src="https://user-images.githubusercontent.com/54694766/223356845-f7f208bc-6656-452e-a1f6-18eee4b9e4e4.png">

## Enhancement

More implementations in the future under consideration:

* Convert the project to programs
* Training and testing with more complex data

##References

https://hc.labnet.sfbu.edu/~henry/sfbu/course/mllib/naive_bayes/slide/text_classifier.html 
https://hc.labnet.sfbu.edu/~henry/sfbu/course/mllib/naive_bayes/slide/text_classification_2_naive_bayes.html 
