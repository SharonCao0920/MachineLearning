# **A Neural Network Primer XOR Gate Design**

[Goolge Slides](https://docs.google.com/presentation/d/1nHJwsJU7U8JmaJuQXD-s7nK-Owf1rLdAr4iTP1U02ns/edit?usp=sharing)

## **Introduction**

### Perceptron

The basic building block for a Neural network.

<img width="398" alt="Screenshot 2023-03-31 205327" src="https://user-images.githubusercontent.com/54694766/229266472-c6e19859-b85a-4ed5-8ab0-fa3565c78f40.png">

### Sigmoid Neuron

A sigmoid neuron is a slightly more sophisticated model than the perceptron.

<img width="435" alt="Screenshot 2023-03-31 205346" src="https://user-images.githubusercontent.com/54694766/229266474-28c4b983-0397-417b-965f-7e01c99ad78d.png">

## **Design**

* NAND Gate
* OR Gate
* AND Gate

<img width="343" alt="Screenshot 2023-03-31 205726" src="https://user-images.githubusercontent.com/54694766/229266513-bb46742b-a391-4406-8107-25013d5fe24f.png">

**1. Forward process**

Calculate the output Z for the given input (X,Y).

**2. Backward process**

* If the output Z is too low, increase the weights by 0.5 which had inputs that were "1".
* If the output Z is too high, decrease the weights by 0.5 which had inputs that were "1".

**3. Using step activation function**

Z := ( W0 * C + W1 * X + W2 * Y >= T ) 
     where T := 1.0

if ( W0 * C + W1 * X + W2 * Y >= T ) 
then output is 1
else output = 0


## **Implementation**

* NAND Gate

<img width="75" alt="Screenshot 2023-03-31 211031" src="https://user-images.githubusercontent.com/54694766/229266522-dc86f78b-68c3-401a-a21f-8bccecf70312.png">

<img width="360" alt="Screenshot 2023-03-31 211056" src="https://user-images.githubusercontent.com/54694766/229266533-e189d884-a3bf-449f-bacb-d42c8f9d3135.png">

<img width="378" alt="Screenshot 2023-03-31 211126" src="https://user-images.githubusercontent.com/54694766/229266542-76c965de-9ac5-48d1-940d-1a2a9cdb518c.png">

<img width="376" alt="Screenshot 2023-03-31 211154" src="https://user-images.githubusercontent.com/54694766/229266547-3e0da309-7d85-4d84-9bcb-85a738bd3542.png">

<img width="376" alt="Screenshot 2023-03-31 211240" src="https://user-images.githubusercontent.com/54694766/229266548-75c70e0a-a512-41c8-83cb-870efdb617bc.png">

<img width="377" alt="Screenshot 2023-03-31 211315" src="https://user-images.githubusercontent.com/54694766/229266549-976204a7-1287-4a39-82e2-99c14603fa06.png">

<img width="342" alt="Screenshot 2023-03-31 211331" src="https://user-images.githubusercontent.com/54694766/229266550-da82d9d5-6476-49c6-bf1e-d2307441b697.png">

* OR Gate

<img width="60" alt="Screenshot 2023-03-31 211616" src="https://user-images.githubusercontent.com/54694766/229266552-72ed8849-a813-44f8-b7c2-0eeeaf51d52b.png">

<img width="334" alt="Screenshot 2023-03-31 211635" src="https://user-images.githubusercontent.com/54694766/229266558-be7ffdf5-d6c9-461c-9c29-0e3909b9ef94.png">

<img width="207" alt="Screenshot 2023-03-31 211700" src="https://user-images.githubusercontent.com/54694766/229266559-baa1ec67-4ce9-4f2a-b47c-6758d8a12c4b.png">


* AND Gate

<img width="85" alt="Screenshot 2023-03-31 215047" src="https://user-images.githubusercontent.com/54694766/229266565-9f3d4b00-81a6-44b7-bd43-33637681fc61.png">

<img width="391" alt="Screenshot 2023-03-31 215120" src="https://user-images.githubusercontent.com/54694766/229266567-57f38e1f-8b4a-4cfc-986c-dedefe2dbf53.png">


## **Test**

<img width="527" alt="Screenshot 2023-03-31 213757" src="https://user-images.githubusercontent.com/54694766/229266575-ba9146b1-d7a5-472b-887c-73c051cc4b1f.png">


## **Conclusion**

<img width="388" alt="image" src="https://user-images.githubusercontent.com/54694766/229266592-76def2c4-fa13-4e15-a717-c2bdb61a679c.png">


## **Enhancement**

Current design is based on very simple calculation, and the steps are not set by any algorithms. To achieve more accurate and efficient design, we should take this into consideration.


## **References**

https://towardsdatascience.com/what-constitutes-a-neural-network-af6439f0cdd7 
https://hc.labnet.sfbu.edu/~henry/sfbu/course/machine_learning/neural_network/slide/ann.html 
https://hc.labnet.sfbu.edu/~henry/sfbu/course/machine_learning/deep_learning/slide/exercise_deep_learning.html#xor 

