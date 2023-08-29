---
title: "Rising: High-Performance Data Loading and Augmentation for 2D & 3D Images"
excerpt: "Rising is a high-performance data loading and augmentation library for 2D and 3D data completely written in PyTorch. Our goal is to provide a seamless integration into the PyTorch Ecosystem without sacrificing usability or features. All transformations are directly implemented in PyTorch which allows gradient propagation and direct execution on GPUs. The provided dataloading module allows for various types of transformations (CPU vs GPU, per sample vs batched) to maximise the resuability of all implemented components."
collection: projects
code: 'https://github.com/PhoenixDL/rising'
---

<img src='/images/rising_logo.svg'>
<br/>

`Rising` consists of two primiary components: `rising.transforms` and `rising.loading`. More information on both components can be found below:

### `rising.transforms`
This module implements many transformations which can be used during training for preprocessing and augmentation. All of them are implemented directly in PyTorch such that gradients can be propagated through the transformations and (optionally) it can be applied on the GPU. Finally, all transforms are implemented for 2D (natural images) and 3D (volumetric) data. Affine transformations can be directly chained behind each other and `rising` will automatically move the resampling operations backwards to reduce resampling artifacts during augmentation and improve the efficiancy of the pipeline. Additional support of grid based augmentations (e.g. `Random Elastic Augmentation`) into the automatic resampling are planned for the future.

### `rising.loading`
The `Dataloader` of `rising` handles all of transformations and applies them efficiently to the data either on CPU or GPU. On CPU the user can easily switch between transformations which can only be performed per sample and transformations which can be applied per batch. In contrast to the native PyTorch datasets the user doesn't need to integrate their augmentation into their dataset. Hence, the only purpose of the dataset is to provide an interface to access individual data samples. The provided `DataLoader` is a direct subclass of the PyTorch's dataloader and handles the batch assembly and applies the augmentations/transformations to the data.

The flow chart below visualizes the default augmentation pipeline found in many other frameworks. The transformations are applied to individual samples which are loaded and augmented inside of multiple background workers from the CPU. This approach is already efficient and might only be slightly slower than batched execution of the transformations (if applied on the CPU). GPU augmentations can be used to perform many operations in parallel and profit heavily from vectorization.

<div align="center">
    <img src='/images/dataloading_default.svg' alt=''>
</div>

`rising` lets the user decide from case to case where augmentations should be applied during this pipeline. This can heavily dependent on the specific tasks and the underlying hardware. Running augmentations on the GPU is only efficient if they can be executed in a batched fashion to maximize the parallelization GPUs can provide. As a consequence, `rising` implements all its transformations in a batched fashion and the `Dataloader` can execute them efficiently on the CPU and GPU. Optionally, the `Dataloader` can still be used to apply transformations on a per sample fashion, e.g. when transforms from other frameworks should be integrated.

<div align="center">
    <img src='/images/dataloading_rising.svg' alt=''>
</div>

Because the `rising` augmentation pipeline is a superset of the currently used methods, external frameworks can be directly integrated into `rising`.
