# Changelog

All notable changes to the **VisionScores** dataset will be documented in this file.

This changelog follows [Semantic Versioning](https://semver.org/) and the [Keep a Changelog](https://keepachangelog.com/en/1.0.0/) guidelines.


## [Unreleased]
### Planned
- Inclusion of additional composers and composition types.
- Improved metadata validation and system ordering.
- Updates to segmentation outputs for better system completeness.


## [v1.0.0] – 2025-06
### Added
- First official release of the **VisionScores** dataset.
- 24,810 grayscale `.jpg` system-segmented images at 128 × 512 resolution:
  - 10,810 samples from various compositions by Franz Liszt.
  - 14,000 samples from Sonatinas by various composers.
- Metadata per sample, including: piece title, composer, key (if available), IMSLP page reference, PDF page number system index.
- Segmentation methods used: CutNet & U-Net for Sonatinas, threshold-based method for Franz Liszt.

### Known Issues
- Metadata **key** field is incomplete or missing in some entries.
- **System index** does not always reflect the true sequential order due to discarded or invalid samples.
- A small subset of samples exhibits **imprecise segmentation**, typically near system boundaries.


## [v0.2.0] – (Internal Build – Sonatinas Construction)
### Added
- Download and filtering of 366 Sonatina PDF files, resulting in 3,927 valid page images.
- 20,490 segmented system candidates generated using threshold-based, U-Net, and CutNet methods.
- 14,000 validated samples selected for release.
- All samples normalized to 128 × 512 resolution.

### Known Issues
- Metadata field "key" missing for some samples.
- System index is relative to segmented samples, not original sheet order.


## [v0.1.0] – (Internal Build – Franz Liszt Construction)
### Added
- Download and filtering of 356 Franz Liszt PDF files, resulting in 4,013 valid page images.
- 21,348 segmented system candidates generated using threshold-based method.
- 10,810 validated samples selected for release.
- All samples normalized to 128 × 512 resolution.

### Known Issues
- Metadata field "key" missing for some samples.
- System index is relative to segmented samples, not original sheet order.

