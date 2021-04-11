# IBM-Creative-Challenge-QCHack-2021
This repository represents work done in IBM creative challenge  in Quantum Coalition Hack 2021

## Idea
Based on brycefuller: 
Build a quantum circuit classifier that classifies the digits of mnist. (use the version of the dataset in qiskit that lets you reduce the number of features.) Start with just classifying {0,1 }with ~ 2-6 features. Start with a small # of data, maybe 20 of each class. 


Normally, a classifier will store it's prediction in the expectation value of the output state with some observable. <psi|Z|psi> for example. 

Instead train this classifier so that the output state looks like the digit you're trying to classify when you plot it with city_state.
In other words, if I pass in a data point which should be labeled 1, the circuit returns a state whose city_state plot looks like the digit 1.

## Implementaion details
- Build QUnatum classifier based on these [tutorilas](https://github.com/kareem1925/Ismailia-school-of-AI) provided by Kareem El Safety
- Version 1: use 6 features only from MNIST data set, for digits 0 and 1. Witjout discarding or minimizing this new dataset 
- Train classifier to predict output state looks like the digit
- Visualize
