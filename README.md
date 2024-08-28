# CycleGAN with Self-Attention Mechanism for MRI to CT Image Translation
This project implements a CycleGAN model enhanced with a Self-Attention mechanism to translate MRI images to CT images. The CycleGAN architecture allows for unpaired image-to-image translation, enabling the generation of CT images from MRI scans without requiring paired training data.

## Table of Contents
Introduction
Requirements
Usage
Training
Model Architecture
Results
Acknowledgments

## Introduction
Magnetic Resonance Imaging (MRI) and Computed Tomography (CT) are two widely used medical imaging modalities. Translating MRI images to CT images can help in providing complementary information for diagnosis. This project explores the use of CycleGANs with an integrated Self-Attention mechanism to improve the quality of image translation from MRI to CT.

## Requirements
Python 3.8+
TensorFlow 2.10+
NumPy
Pandas
PIL (Pillow)
Matplotlib
scikit-learn
glob2

## Usage
1. Prepare the dataset
Place your MRI images in CT_MRI/Dataset Split/images/trainA/ and CT_MRI/Dataset Split/images/testA/.
Place your CT images in CT_MRI/Dataset Split/images/trainB/ and CT_MRI/Dataset Split/images/testB/.
2. Preprocess the data
The preprocessing and data loading are automatically handled by the train.py script.
3. Train the model
4. Monitor the training process
   Use TensorBoard to visualize training metrics:
   tensorboard --logdir=logs/
5. Generate CT images from MRI

## Model Architecture
CycleGAN: The CycleGAN consists of two generator networks (MRI to CT and CT to MRI) and two discriminator networks. The U-Net generators are enhanced with self-attention mechanisms to capture long-range dependencies in images.
Self-Attention: The self-attention layers allow the model to focus on relevant parts of the image, improving the quality of translation especially for medical images where fine details are crucial.

## Results
The results are saved in the logs/ directory and can be visualized using TensorBoard.
Generated images, loss curves, and other metrics are logged during training.

## Acknowledgments
This project is inspired by the original CycleGAN paper and various self-attention mechanisms applied in the context of image-to-image translation.
The project also builds upon open-source implementations of GANs and medical image processing.
