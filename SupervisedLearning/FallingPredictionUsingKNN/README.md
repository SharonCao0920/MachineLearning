# Falling Prediction using KNN
[Google Slides](https://docs.google.com/presentation/d/1z5GFLShOoHuqnHfVUDxjvl3xSzjspt1Gtjoe5K3-0mk/edit?usp=sharing)

## About the Project

### Description
This project is to predicet the fall using KNN algorithm with data collected from two sensors. 
Data sent from Gyroscope senso and Accelerometer sensor can be used to categorize any motion.

* 3 numbers from Accelerometer sensor
* 3 numbers from Gyroscope sensor

### Main algorithm used: KNN
Basic Assumption:

* All instances correspond to points in the n-dimensional space where n represents the number of features in any instance.
* The nearest neighbors of an instance are defined in terms of the Euclidean distance.

## Data

<img width="527" alt="Screenshot_20230206_062101" src="https://user-images.githubusercontent.com/54694766/217131496-b023b90e-eef3-4766-8ce0-9521579ddc6a.png">


## Determine the Value of K
n = 8

K = sqrt(8) = 2.828427 = 3

## Mannually Calcualte the Prediction

Euclidean Distance = SQRT((Apred - Ax)^2+(Apred - Ay)^2+(Apred - Az)^2+(Gpred - Gx)^2+(Gpred - Gy)^2+(Gpred - Gz)^2)

<img width="662" alt="Screenshot_20230206_062232" src="https://user-images.githubusercontent.com/54694766/217131703-ab9ac675-b5fd-4ad4-89ce-e9e56ee4b7b0.png">


## Pythong Program to Predict
## [Full Code](https://github.com/SharonCao0920/MachineLearning/blob/main/SupervisedLearning/FallingPredictionUsingKNN/CS550_Week3_HW1_KNN.ipynb)
### KNN Oringial code

```
import math
def euclidean_distance(row1, row2):
	distance = 0.0
	for i in range(len(row1)-1):
		distance += (row1[i] - row2[i])**2
	return math.sqrt(distance)
   
def get_neighbors(train, test_row, k_neighbors):
  distances = list()
  for train_row in train:
    dist = euclidean_distance(test_row, train_row)
    distances.append((train_row, dist))
  distances.sort(key=lambda tup: tup[1])
  print("List of calsulated distance from predict data:")
  for i in range(len(distances)):
    print(distances[i])
  neighbors = list()
  for i in range(k_neighbors):
    neighbors.append(distances[i][0])
  return neighbors

def predict_classification(train, test_row, num_neighbors):
  neighbors = get_neighbors(train, test_row, num_neighbors)
  print("\nNeighbors selected are: ")
  for i in range(len(neighbors)):
    print(neighbors[i])
  
  output_values = [row[-1] for row in neighbors]
  prediction = max(set(output_values), key=output_values.count)
  return prediction
```

```
prediction = predict_classification(dataset[1:], dataset[0], 3)
```

### KNN iwht python sklearn
```
x_train, x_test, y_train, y_test = sklearn.model_selection.train_test_split(X,Y, test_size=0.1)

model = KNeighborsClassifier(n_neighbors=3)
model.fit(x_train, y_train)

model.score(x_test, y_test)

print("Predicted result is ", model.predict([(7, 6, 5, 5, 6, 7)]))

```

## Compare the Result
All results predicted for faling(+).
