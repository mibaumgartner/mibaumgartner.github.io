---
title: "Taming Detection Transformers for Medical Object Detection"
collection: publications
permalink: /publication/2023_TaimingDETR
date: 2023-06-27
venue: 'BVM Workshop 2023'
paperurl: 'https://link.springer.com/chapter/10.1007/978-3-658-41657-7_39'
pdf: 'https://arxiv.org/pdf/2306.15472.pdf'
citation: 'Ickler, Marc K. and Baumgartner, Michael, et al. "Taming Detection Transformers for Medical Object Detection." BVM Workshop. Wiesbaden: Springer Fachmedien Wiesbaden, 2023.'
---

The accurate detection of suspicious regions in medical images is an error-prone and time-consuming process required by many routinely performed diagnostic procedures. To support clinicians during this difficult task, several automated solutions were proposed relying on complex methods with many hyperparameters. In this study, we investigate the feasibility of DEtection TRansformer (DETR) models for volumetric medical object detection. In contrast to previous works, these models directly predict a set of objects without relying on the design of anchors or manual heuristics such as non-maximum-suppression to detect objects. We show by conducting extensive experiments with three models, namely DETR, Conditional DETR, and DINO DETR on four data sets (CADA, RibFrac, KiTS19, and LIDC) that these set prediction models can perform on par with or even better than currently existing methods. DINO DETR, the best-performing model in our experiments demonstrates this by outperforming a strong anchor-based one-stage detector, Retina U-Net, on three out of four data sets.

Publication was presented as an oral presentation during BVM 2023 and has ranked third for the best paper award.
{: .notice--success}

<div align="center">
    <img src='/images/detr_architecture.svg' alt=''>
</div>
