# SVM MNIST digit classification in python using scikit-learn

The project presents the well-known problem of [MNIST handwritten digit classification](https://en.wikipedia.org/wiki/MNIST_database).
For the purpose of this tutorial, I will use [Support Vector Machine (SVM)](https://en.wikipedia.org/wiki/Support_vector_machine)
the algorithm with raw pixel features.
The solution is written in python with use of [scikit-learn](http://scikit-learn.org/stable/) easy to use machine learning library.

![Sample MNIST digits visualization](/images/mnist_digits.png)

The table below shows some results in comparison with other models:

| Method                                     | Accuracy | Comments        |
| ------------------------------------------ | -------- | --------------- |
| Random forest                              | 0.937    |                 |
| Simple one-layer neural network            | 0.926    |                 |
| Simple 2 layer convolutional network       | 0.981    |                 |
| SVM RBF                                    | 0.9852   | C=5, gamma=0.05 |
| Linear SVM + Nystroem kernel approximation |          |                 |
| Linear SVM + Fourier kernel approximation  |          |                 |

## Project Setup

1. Install Python.
1. [Install pipenv](https://pipenv.readthedocs.io/en/latest/install/#pragmatic-installation-of-pipenv)
1. Git clone the repository
1. Install all necessary python packages executing this command in terminal

```
git clone https://github.com/ayushbhatt-07/MNIST-Digit-Classification-SVM.git
cd MNIST-Digit-Classification-SVM
pipenv install
```

## Solution

In this Project, I used two approaches to SVM learning.
First, uses classical SVM with RBF kernel. The drawback of this solution is rather long training on big datasets, although the accuracy with good parameters is high.
The second, use Linear SVM, which allows for training in O(n) time.
