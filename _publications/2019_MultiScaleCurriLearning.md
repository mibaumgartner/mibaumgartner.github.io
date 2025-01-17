---
title: "Multi Scale Curriculum CNN for Context-Aware Breast MRI Malignancy Classification"
collection: publications
permalink: /publication/2019_MultiScaleCurriLearning
date: 2019-10-10
venue: 'Medical Image Computing and Computer Assisted Intervention–MICCAI 2019'
paperurl: 'https://link.springer.com/chapter/10.1007/978-3-030-32251-9_54'
pdf: 'https://arxiv.org/pdf/1906.06058.pdf'
code: 'https://github.com/haarburger/multi-scale-curriculum'
citation: 'Haarburger, Christoph, et al. "Multi scale curriculum CNN for context-aware breast MRI malignancy classification." Medical Image Computing and Computer Assisted Intervention–MICCAI 2019: 22nd International Conference, Shenzhen, China, October 13–17, 2019, Proceedings, Part IV 22. Springer International Publishing, 2019.'
---
Classification of malignancy for breast cancer and other cancer types is usually tackled as an object detection problem: Individual lesions are first localized and then classified with respect to malignancy. However, the drawback of this approach is that abstract features incorporating several lesions and areas that are not labelled as a lesion but contain global medically relevant information are thus disregarded: especially for dynamic contrast-enhanced breast MRI, criteria such as background parenchymal enhancement and location within the breast are important for diagnosis and cannot be captured by object detection approaches properly.

In this work, we propose a 3D CNN and a multi scale curriculum learning strategy to classify malignancy globally based on an MRI of the whole breast. Thus, the global context of the whole breast rather than individual lesions is taken into account. Our proposed approach does not rely on lesion segmentations, which renders the annotation of training data much more effective than in current object detection approaches.

Achieving an AUROC of 0.89, we compare the performance of our approach to Mask R-CNN and Retina U-Net as well as a radiologist. Our performance is on par with approaches that, in contrast to our method, rely on pixelwise segmentations of lesions.
