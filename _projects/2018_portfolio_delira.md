---
title: "Delira - A Backend Agnostic High Level Deep Learning Library"
excerpt: "Lightweight framework for fast prototyping and training of deep neural networks with PyTorch and TensorFlow. `delira` is designed to work as a backend agnostic high level deep learning library which allwos the user to compare various models written in different backends without rewriting them."
collection: projects
code: 'https://github.com/delira-dev/delira'
---

<img src='/images/delira.svg'>
<br>

`delira` is designed to work as a backend agnostic high level deep learning library. The user can choose among several computation backends. It allows the user to compare various models written for different backends without rewriting them.

For this case, `delira` couples the entire training and prediction logic in backend-agnostic modules to achieve identical behavior for training in all backends.

`delira` is designed in a very modular way so that almost everything is easily exchangeable or customizable.

A (non-comprehensive) list of the features included in `delira`:

- Dataset loading
- Dataset sampling
- Augmentation (multi-threaded) including 3D images with any number of channels (based on batchgenerators)
- A generic trainer class that implements the training process for all backends
- Training monitoring using Visdom or Tensorboard
- Model save and load functions
- Already impelemented Datasets
- Many operations and utilities for medical imaging
