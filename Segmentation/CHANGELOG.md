# Segmentation Changelog

This file documents all notable changes to the segmentation methods and related tools used in the segmentation of music sheets into systems of the **VisionScores** dataset.


## [Unreleased]
### Planned
- Addition of a script for executing the full segmentation pipeline on complete sheet images.


## [v0.3.0]
### Added
- Evaluation metrics for segmentation performance:
  - Intersection over Union (IoU)
  - F1-score
  - Precision
  - Recall


## [v0.2.0]
### Added
- Construction of a **synthetic segmentation dataset**, using systems extracted from the Franz Liszt scenario (v0.1.0 of the main dataset). Randomized combinations of systems were used to generate artificial sheet music and corresponding segmentation maps.
- Implementation and training of a **U-Net** segmentation model on the synthetic dataset with a three-layer configuration (8, 16, 32 channels).
- Design and implementation of **CutNet**, an extension of U-Net incorporating an adaptive subtraction mechanism to restore segmentation-relevant profiles.
- Profile-based postprocessing for both U-Net and CutNet to extract system boundaries using the same logic as the threshold-based approach.


## [v0.1.0]
### Added
- Implementation of the developed **threshold-based segmentation method**.
  - This method operates by computing the row-wise sum of pixel intensities in a score image.
  - Gaussian filtering is applied to smooth the profile and identify minima corresponding to inter-system whitespace.
  - Selection of segmentation points is made using a threshold.
- Applied to system extraction in the Franz Liszt scenario.

