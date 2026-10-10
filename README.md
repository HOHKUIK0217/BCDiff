<div align="center">

# BCDiff

### Bidirectional Cross-Modal Diffusion with Text Intent Guidance for Remote Sensing Classification

Official project page and preview release.

<img src="assets/motivation.png" alt="Comparison between conventional multimodal feature fusion and BCDiff" width="620">

</div>

## Overview

BCDiff is a multimodal remote-sensing classification framework that combines text-intent-guided adaptive fusion with bidirectional conditional diffusion. It is designed to promote complementary interaction between heterogeneous modalities while preserving modality-specific information.

The main ideas are:

- a multimodal graph encoder for structured feature extraction;
- text-intent-guided adaptive fusion for semantic regulation;
- bidirectional conditional diffusion for cross-modal interaction and refinement.

## Framework

<div align="center">
  <img src="assets/bcdiff_framework.png" alt="Overview of the BCDiff framework" width="100%">
</div>

## Quantitative Results

The table reports **OA / AA / Kappa (%)** under the experimental protocol used in the paper.

| Method | Houston 2013 | Augsburg | Trento |
|:--|:--:|:--:|:--:|
| S2FL | 89.75 / 90.26 / 88.91 | 61.21 / 62.07 / 51.19 | 71.35 / 73.59 / 62.83 |
| CoSpace-l1 | 87.14 / 87.71 / 86.08 | 45.13 / 48.71 / 32.94 | 82.30 / 85.22 / 76.95 |
| CoSpace-l2 | 90.34 / 90.70 / 89.54 | 61.79 / 60.87 / 51.46 | 86.40 / 89.23 / 82.14 |
| EndNet | 92.38 / 92.33 / 91.75 | 69.32 / 64.26 / 59.95 | 90.75 / 91.47 / 87.72 |
| DSHFNet | 91.15 / 92.50 / 90.43 | 63.33 / 50.77 / 46.86 | 98.91 / 98.28 / 98.53 |
| TMCFN | 95.22 / 96.18 / 94.83 | 85.46 / 81.54 / 80.03 | 98.35 / 98.12 / 97.80 |
| MSFMamba | 95.90 / 96.58 / 95.57 | 88.89 / 79.62 / 84.51 | 98.16 / 97.93 / 97.54 |
| THSGR | 95.85 / 96.69 / 95.51 | 88.70 / 84.54 / 84.17 | 98.38 / 98.35 / 97.84 |
| **BCDiff (Ours)** | **97.31 / 97.75 / 97.09** | **91.13 / 85.53 / 87.61** | **99.18 / 98.85 / 98.91** |

## Qualitative Results

### Houston 2013

<div align="center">
  <img src="assets/houston_results.png" alt="Classification maps on the Houston 2013 dataset" width="100%">
</div>

### Augsburg

<div align="center">
  <img src="assets/augsburg_results.png" alt="Classification maps on the Augsburg dataset" width="100%">
</div>

### Trento

<div align="center">
  <img src="assets/trento_results.png" alt="Classification maps on the Trento dataset" width="100%">
</div>

## Per-Class Accuracy Distribution

<div align="center">
  <img src="assets/class_accuracy_boxplot.png" alt="Per-class accuracy distributions on three datasets" width="100%">
</div>

## Environment

Create the reference Conda environment with:

```bash
conda env create -f environment.yml
conda activate bcdiff
```

The environment file records the main software versions used by the project. CUDA and PyTorch builds may be adjusted to match the local hardware.

## Reference Configurations

Dataset-level reference configurations are provided for:

- [Houston 2013](configs/houston.yaml): HSI + LiDAR;
- [Augsburg](configs/augsburg.yaml): HSI + SAR;
- [Trento](configs/trento.yaml): HSI + LiDAR.

The paths in these files are placeholders and should be updated for the local dataset layout. The configurations expose dataset and common experimental settings only; method-specific implementation details are not included in this preview release.

## Release Status

This preview release provides the project overview, reference environment, dataset configurations, quantitative results, and experimental visualizations. Additional implementation details will be made available after publication.

## Citation

Citation information will be updated when the paper becomes publicly available.
