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


## Submission
Submit a zip file on Canvas. The directory and contents of the files to be submitted are as follows:

```
your name/workspace/lab1/
  ├── answers.yaml
  ├── 1_pytorch_dnn.ipynb
  ├── 2_first_principles.ipynb
  ├── 3_hardware.ipynb
```
 
