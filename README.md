# IBM-Creative-Challenge-QCHack-2021
This repository represents work done in IBM creative challenge  in Quantum Coalition Hack 2021

## Idea
Based on brycefuller: 
Build a quantum circuit classifier that classifies the digits of mnist. (use the version of the dataset in qiskit that lets you reduce the number of features.) Start with just classifying {0,1 }with ~ 2-6 features. Start with a small # of data, maybe 20 of each class. 


Normally, a classifier will store it's prediction in the expectation value of the output state with some observable. <psi|Z|psi> for example. 

Instead train this classifier so that the output state looks like the digit you're trying to classify when you plot it with city_state.
In other words, if I pass in a data point which should be labeled 1, the circuit returns a state whose city_state plot looks like the digit 1.

## Implementaion details
- Build Qunatum classifier based on these [tutorials](https://github.com/kareem1925/Ismailia-school-of-AI) provided by Kareem El Safety
- Version 1: use 6 features only from MNIST data set, for digits 0 and 1. Witjout discarding or minimizing this new dataset  (Done, Notebook name: ML-prediction state qiskit.ipynb)
	- we interuppted kernel at middle of training as loss was so small, so we didn't need to continue training and training time was large.

- Version 2: use 12 features only from MNIST data set, for digits 0 and 1. Witjout discarding or minimizing this new dataset (Done, Notebook name: ML-prediction state qiskit v2.ipynb )

- Version 3: use 6 features only from MNIST data set, for digits 0, 1, 2, and 3. Witjout discarding or minimizing this new dataset (Done, Notebook name: ML-prediction state qiskit v3.ipynb)
	- unfortunately we couldn't complete training therefore training loss is still high, beacuse it was trained locally as there was problem on IBM Quantum experience and training took alot of time.
	- we visualized correct predictions in  testing.
	- we had a bug, which was due to that some batch contains only 3 or less classes, since circuit predict up to 4 classes log loss calculation fired exception.
	- we know that it's a bug we did were we made weight dimenssion for 4 tesnsor, while it should be 5 (to add bias). but when we use 4 tensor for weight it converges fasters.



- Train classifier to predict output state looks like the digit
- Visualize

## Visualize
1. predicted output state for 0
![Alt text](images/prediction_state_vector_0.png?raw=true "Title")

2. predicted output state for 1
![Alt text](images/prediction_state_vector_1.png?raw=true "Title")

3. predicted output state for 2
![Alt text](images/prediction_state_vector_2.png?raw=true "Title")

4. predicted output state for 3
![Alt text](images/prediction_state_vector_3.png?raw=true "Title")