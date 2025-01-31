# Due date: Feb 7, 2025 at 11:59 P.M.

# Lab 1: Neural Network Profiling and Inference

In this problem set, we will cover the basics of running neural network
inference in [PyTorch](https://pytorch.org/). PyTorch is a very popular neural
network framework maintained by Facebook, and it is used by a multitude of
researchers worldwide. Our goal will be to prototype networks for two classic
tasks: the MNIST digit recognition task and the ImageNet object classification
task. We will go through basic network inspection, inference and training in
these questions. Since the eventual goal of this course is to design hardware
for neural network inference, an important focus of this problem set will be to
develop a quantitative understanding of the computation involved in these tasks
and how these computations will be realized in hardware.

# Doing the lab

The lab is broken into 3 different python notebooks. All 3 must be completed to receive credit. The third notebook uses Timeloop, an open source analytic hardware model infrastructure originally developed by NVIDIA. If you want to learn more about how Timeloop works, it is highly recommended to read the paper:

```
A. Parashar et al., "Timeloop: A Systematic Approach to DNN Accelerator Evaluation," 2019 IEEE International Symposium on Performance Analysis of Systems and Software (ISPASS), Madison, WI, USA, 2019
```

Also more resources can be found at the homepage on timeloop.csail.mit.edu

The lab is setup to use regression tests to check your answers automatically. In order to use this system the code uses a special "answer()" function that you will use to indicate a graded answer. In some cases, all you will do is fill in a value into the answer directly. In other cases, obtaining the answer requires writing new code of your own that indirectly supports or finds the answer. 

If you are expected to write the answer then the value will be "FILL ME". In some cases the answer is multiple choice and the options are indicted by the "required_types" field (i.e., 'Accuracy Increase', 'Accuracy Decrease', 'No Change'). In this case, your answer must exactly match one of these options to receive credit. In other cases the required_type will be more general like "str" for string, indicating that you should provide a custom answer of that type that we will grade by hand. In some cases, the answer is itself a reference into code you wrote and you should not change the answer directly, but only the indicated functions. In this case, the line will be marked with a comment "Do Not Change This Line". Changing these lines will probably result in losing points.

Running the python notebook will cause the creation of a file "answers.yaml" that must be submitted along with your code changes (see below). If you are curious, the source code for "answer()" and related functions can be found in "loaders.py". If you have not used YAML before then it is highly recommended to do an online tutorial to learn the format. This another very useful tool that will serve you in many different circumstances and programming languages.


## Submission
Submit a zip file on Canvas. The directory and contents of the files to be submitted are as follows:

```
your name/workspace/lab1/
  ├── answers.yaml
  ├── 1_pytorch_dnn.ipynb
  ├── 2_first_principles.ipynb
  ├── 3_hardware.ipynb
```
 
