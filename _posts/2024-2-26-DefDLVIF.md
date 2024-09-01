---
title: "Context-aware Learning-Based Autofocus Metric for Deformable Motion in Interventional CBCT"
permalink: "/researchPosts/DLVIF/"
layout: post
categories: media
---

Extending The Concept of Learning-Based Autofocus Metric to Deformable Motion in Interventional CBCT by Utilizing Context-Aware Architecture

## [2024] Deformable Motion Compensation in Interventional Cone-Beam CT with a Context-Aware Learned Autofocus Metric

[Huang H, Liu Y, Siewerdsen JH, et al. Deformable motion compensation in interventional cone-beam CT with a context-aware learned autofocus metric. *Med Phys*. 2024; 51: 4158–4180. ](https://doi.org/10.1002/mp.17125.)

Interventional Cone-Beam CT (CBCT) offers 3D visualization of soft-tissue and vascular anatomy, enabling 3D guidance of abdominal interventions. However, its long acquisition time makes CBCT susceptible to patient motion. Image-based autofocus offers a suitable platform for compensation of deformable motion in CBCT, but it relies on handcrafted motion metrics based on first-order image properties and that lack awareness of the underlying anatomy. This work proposes a data-driven approach to motion quantification via a learned, context-aware, deformable metric, $\mathbf{VI⁢F_{D⁢L}}$, that quantifies the amount of motion degradation as well as the realism of the structural anatomical content in the image.

<p align='center'>
  <img src="/researchPosts/DefDLVIF/images/clinicalCase.png" alt="Rigid Motion Compensation on Cadaver Head" title="LDSDE Results" style="zoom:100%;">
</p>


## [2023] Multi-stage Adaptive Spline Autofocus (MASA) with a learned metric for deformable motion compensation in interventional cone-beam CT

[H. Huang, J. H. Siewerdsen, A. Lu, Y. Hu, W. Zbijewski, M. Unberath, C. R. Weiss, and A. Sisniega, “Multi-stage Adaptive Spline Autofocus (MASA) with a learned metric for deformable motion compensation in interventional cone-beam CT”, Proc. SPIE 12463, Medical Imaging 2023: Physics of Medical Imaging, 1246314 (7 April 2023)](https://doi.org/10.1117/12.2654361)

Cone-beam CT (CBCT) is widespread in abdominal interventional imaging, but its long acquisition time makes it susceptible to patient motion. Image-based autofocus has shown success in CBCT deformable motion compensation, via deep autofocus metrics and multi-region optimization, but it is challenged by the large parameter dimensionality required to capture intricate motion trajectories. This work leverages the differentiable nature of deep autofocus metrics to build a novel optimization strategy, Multi-Stage Adaptive Spine Autofocus (MASA), for compensation of complex deformable motion in abdominal CBCT. MASA poses the autofocus problem as a multi-stage adaptive sampling strategy of the motion trajectory, sampled with Hermite spline basis with variable amplitude and knot temporal positioning. The adaptive method permits simultaneous optimization of the sampling phase, local temporal sampling density, and time-dependent amplitude of the motion trajectory. The optimization is performed in a multi-stage schedule with increasing number of knots that progressively accommodates complex trajectories in late stages, preconditioned by coarser components from early stages, and with minimal increase in dimensionality. MASA was evaluated in controlled simulation experiments with two types of motion trajectories: i) combinations of slow drifts with sudden jerk (sigmoid) motion; and ii) combinations of periodic motion sources of varying frequency into multi-frequency trajectories. Further validation was obtained in clinical data from liver CBCT featuring motion of contrast-enhanced vessels, and soft-tissue structures. The adaptive sampling strategy provided successful motion compensation in sigmoid trajectories, compared to fixed sampling strategies (mean SSIM increase of 0.026 compared to 0.011). Inspection of the estimated motion showed the capability of MASA to automatically allocate larger sampling density to parts of the scan timeline featuring sudden motion, effectively accommodating complex motion without increasing the problem dimension. Experiments on multifrequency trajectories with 3-stage MASA (5, 10, and 15 knots) yielded a twofold SSIM increase compared to single-stage autofocus with 15 knots (0.076 vs 0.040, respectively). Application of MASA to clinical datasets resulted in simultaneous improvement on the delineation of both contrast-enhanced vessels and soft-tissue structures in the liver. A new autofocus framework, MASA, was developed including a novel multi-stage technique for adaptive temporal sampling of the motion trajectory in combination with fully differentiable deep autofocus metrics. This novel adaptive sampling approach is a crucial step for application of deformable motion compensation to complex temporal motion trajectories.

<p align='center'>
  <img src="/researchPosts/DefDLVIF/images/autofocus.png" alt="Rigid Motion Compensation on Cadaver Head" title="LDSDE Results" style="zoom:100%;">
</p>

## [2022] Context-Aware, Reference-Free Local Motion Metric for CBCT Deformable Motion Compensation

[H. Huang, J.H. Siewerdsen, W. Zbijewski, C. R. Weiss, M. Unberath, A. Sisniega, “Context-Aware, Reference-Free Local Motion Metric for CBCT Deformable Motion Compensation,” in Proceedings of 7th International Conference on Image Formation in X-Ray Computed Tomography](https://doi.org/10.1117/12.2646857) 

Deformable motion is one of the main challenges to image quality in interventional cone beam CT (CBCT). Autofocus methods have been successfully applied for deformable motion compensation in CBCT, using multi-region joint optimization approaches that leverage the moderately smooth spatial variation motion of the deformable motion field with a local neighborhood. However, conventional autofocus metrics enforce images featuring sharp image-appearance, but do not guarantee the preservation of anatomical structures. Our previous work (DL-VIF) showed that deep convolutional neural networks (CNNs) can reproduce metrics of structural similarity (visual information fidelity - VIF), removing the need for a matched motion-free reference, and providing quantification of motion degradation and structural integrity. Application of DL-VIF within local neighborhoods is challenged by the large variability of local image content across a CBCT volume and requires global context information for successful evaluation of motion effects. In this work, we propose a novel deep autofocus metric, based on a context-aware, multi-resolution, deep CNN design. In addition to the inclusion of contextual information, the resulting metric generates a voxel-wise distribution of reference-free VIF values. The new metric, denoted CADL-VIF, was trained on simulated CBCT abdomen scans with deformable motion at random locations and with amplitude up to 30 mm. The CADL-VIF achieved good correlation with the ground truth VIF map across all test cases with R2 = 0.843 and slope = 0.941. When integrated into a multi-ROI deformable motion compensation method, CADL-VIF consistently reduced motion artifacts, yielding an average increase in SSIM of 0.129 in regions with severe motion and 0.113 in regions with mild motion. This work demonstrated the capability of CADL-VIF to recognize anatomical structures and penalize unrealistic images, which is a key step in developing reliable autofocus for complex deformable motion compensation in CBCT.

<p align='center'>
  <img src="/researchPosts/DefDLVIF/images/network.png" alt="Rigid Motion Compensation on Cadaver Head" title="LDSDE Results" style="zoom:100%;">
</p>


