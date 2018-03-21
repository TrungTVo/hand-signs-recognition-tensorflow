# Hand signs recognition with Tensorflow
We'll train Convolutional Network model to recognize hand sign images.

<img width="992" alt="dataset" src="https://user-images.githubusercontent.com/20756728/37721962-425f95b0-2d01-11e8-9602-c1580973fc40.png">

# Install dependencies
Assume all basic Python packages (Numpy, Matplotlib, etc) are already installed and configured properly.

Install TensorFlow from its official website: https://www.tensorflow.org/install/

# Model architecture

| Layers          | Info                                        |
|:---------------:|:-------------------------------------------:|
| convolution 1   | 4x4x3 size, 8 filters, stride 1, padding 0  |
| ReLU 1          | same size as output of convolution 1        |
| pooling 1       | filter size 2, stride 2, padding 0          |
| convolution 2   | 2x2x8 size, 16 filters, stride 1, padding 0 |
| ReLU 2          | same size as output of convolution 2        |
| pooling 2       | filter size 2, stride 2, padding 0          |
| flatten         | size 16x16x16                               |
| dropout         | p = 0.5 (can be modified to get good result)|
| fully connected | output size = 6 (number of classes)         |

# TensorFlow computational graph
![graph1](https://user-images.githubusercontent.com/20756728/37725320-1a59696c-2d09-11e8-8b9f-5ee6532ae749.png)
![graph2](https://user-images.githubusercontent.com/20756728/37725325-1c18a13c-2d09-11e8-9e11-b7053eb7efe7.png)

# Results

![dropout_result](https://user-images.githubusercontent.com/20756728/37725508-82779a14-2d09-11e8-824f-aac3a9262748.png)
![confusion_matrix](https://user-images.githubusercontent.com/20756728/37725438-56251ce8-2d09-11e8-8ad4-7ed2a9bbb4ed.png)
