# Handwritten Digit Classification using ANN

## Dataset

- 60,000 Gray scale images of dimensions 28x28 pixels

## Implementation

1. ANN class:

   - args:
     - Input size
     - Number of classes
     - Number of hidden layers
     - Number of neurons in each hidden layers
   - methods:

     - `forward()`: Perform forward pass

       - I/P: Tensors of dataset images
       - O/P: Logits of classes

     - `describeANN()`: Print args and architecture of neural network

     - `train()`: Train neural network with defined params

       - I/P: Train loader, Test loader, Number of epochs, Optimizer (name), Loss function (name), Learning rate
       - O/P: Stores all evaluation metrics (Accuracy, Precision, Recall, F1-score)

     - `print_metrics()`: Print all evaluation metrics

2. Train and Test:
   - Splitted dataset into 55000 - 5000 for training and validation
   - Trained neural network for different nuber of hidden layers and different number of neurons in each layers
   - Generated and plotted results

## Results

- Training params:
  - Optimizer: SGD
  - Loss function: Cross Entropy
  - Learning rate: 1e-2
  - Epochs: 10

1. ANN with 3 hidden layers [512,256,128]:

| Metric    | Value (Last epoch) |
| --------- | ------------------ |
| Accuracy  | 0.94               |
| Precision | 0.94               |
| Recall    | 0.94               |
| F1-Score  | 0.94               |

2. ANN with 4 hidden layers [512,256,128,64]:

| Metric    | Value |
| --------- | ----- |
| Accuracy  | 0.94  |
| Precision | 0.94  |
| Recall    | 0.94  |
| F1-Score  | 0.94  |

3. ANN with 5 hidden layers [512,256,128,64,32]:

| Metric    | Value |
| --------- | ----- |
| Accuracy  | 0.94  |
| Precision | 0.93  |
| Recall    | 0.93  |
| F1-Score  | 0.94  |
