# Super-Resolution (NTIRE18)

## Introduction

This project was completed as part of our Semester 6 coursework. We have been tasked with completing one of the challenges in the 2nd NTIRE competition. This specific challenge is centered around the restoration of rich details in low-resolution images. The challenge revolves around single image super-resolution, aiming to recover high-frequency details lost in low-resolution images by referencing paired low-resolution and high-resolution images. 

This problem is complex due to the multitude of potential high-resolution counterparts for each low-resolution image, escalating with the magnification factor. To tackle this challenge, we researched relevant papers and opted to implement the "Photo-Realistic Single Image Super-Resolution Using a Generative Adversarial Network" (SRGAN) paper. This paper introduced SRGAN as the solution, and we have implemented the SRGAN model for our approach.

## Project Overview

### Objectives
- Recover high-frequency details lost in low-resolution images.
- Develop a robust framework for 4x upscaling factor single image super-resolution.

### Solution Approach
Our implementation follows the SRGAN architecture, which uses a combination of:
1. **Generator Network**: Responsible for generating high-resolution images from low-resolution inputs.
2. **Discriminator Network**: Distinguishes between the generated images and ground-truth high-resolution images.
3. **Perceptual Loss Function**: Combines adversarial and content loss to ensure perceptual similarity between generated and real images.

## Dataset

The DIV2K dataset was used for training and evaluation. This dataset provides paired low-resolution and high-resolution images, which are essential for supervised learning in single image super-resolution tasks.

## Training Details

- **Hardware**: NVIDIA GeForce RTX 3060 Laptop GPU (6GB).
- **Software**: Python 3.11.5, PyTorch, CUDA 11.8.
- **Training Configuration**:
  - Pre-training: 2000 epochs
  - Fine-tuning: 1000 epochs
- **Loss Function**:
  - Perceptual loss: Combines adversarial and VGG feature-based content loss.

## Results

The trained model demonstrated promising results in restoring high-frequency details in low-resolution images. However, there remains a performance gap compared to state-of-the-art models like ESRGAN and RankSRGAN. 

### Visual Examples
Generated outputs and comparisons can be found in the `Results/` directory.

## References
- [Photo-Realistic Single Image Super-Resolution Using a Generative Adversarial Network](https://openaccess.thecvf.com/content_cvpr_2017/papers/Ledig_Photo-Realistic_Single_Image_CVPR_2017_paper.pdf)
- [DIV2K Dataset](https://data.vision.ee.ethz.ch/cvl/DIV2K/)
- NTIRE Challenge papers and resources

## Acknowledgments
This project was completed as part of our Semester 6 coursework. It is a replication of the original NTIRE challenge, allowing us to gain hands-on experience with state-of-the-art techniques in image super-resolution.

We extend our gratitude to the NTIRE competition organizers for providing an inspiring problem and dataset, and to the authors of the SRGAN paper for their foundational work in this domain.


