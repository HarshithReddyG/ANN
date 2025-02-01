1. Project Overview
The project aims to implement a feedforward neural network that learns from provided training data, performs forward propagation, and backpropagation for error minimization. The network is constructed with layers of neurons, activation functions, and a custom optimization algorithm.

2. Features
Custom-built implementation of Sigmoid and Softmax activation functions.
A forward propagation process that passes input data through the network layers.
Backpropagation for calculating gradients and updating weights.
The network is trained on a cat vs. non-cat dataset, with custom preprocessing and dataset loading steps.

3. Architecture
The neural network architecture is designed with the following components:

Input layer: Takes in data from CSV files and normalizes it.
Hidden layers: Uses sigmoid activation functions to process data.
Output layer: Utilizes softmax for classification into multiple categories (e.g., cat vs. non-cat).
4. Mathematical Explanation​
The sigmoid function transforms the input into a range between 0 and 1. It is widely used for binary classification tasks.
 
The softmax function converts the raw output scores into probabilities by normalizing the exponentials of the raw scores.

Backpropagation:
The weights are adjusted by calculating the derivative of the loss function with respect to the weights and updating them using gradient descent.

5. Code Explanation
Loading Data:
The datasets are loaded using np.loadtxt() with CSV files containing training and test data. The data is normalized by dividing by 255.0.

Activation Functions:
The sigmoid() and softmax() functions are defined manually to handle activation and output layer processing.

Training Loop:
The training loop performs forward propagation to predict outputs, computes the loss, and uses backpropagation to update the weights based on the error.

6. Usage
Install necessary packages:
pip install numpy matplotlib

Prepare the dataset files in the dataset/ directory (cat_train_x.csv, cat_train_y.csv, cat_test_x.csv, cat_test_y.csv).

Run the script to train the network:
python ann.py
The script will output the loss curve and final accuracy on the test set.

7. Conclusion
This ANN implementation demonstrates the core components of a neural network, from forward propagation to error backpropagation, all implemented from scratch. It is a great learning tool for understanding the mathematical foundations of neural networks.
