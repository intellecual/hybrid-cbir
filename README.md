# hybrid-cbir

Hybrid CBIR using VGG16, color autocorrelogram, and LBP features. Finds visually and semantically similar images from a dataset using deep learning plus classical vision. Includes visualization for quick comparison of query and top results.

![MIT License](https://img.shields.io/badge/license-MIT-green)
![Python](https://img.shields.io/badge/python-3.7%2B-blue)
![Deep Learning](https://img.shields.io/badge/deep%20learning-VGG16-blueviolet)
![CBIR](https://img.shields.io/badge/Image%20Retrieval-Hybrid-orange)

## Overview

This project implements a hybrid Content-Based Image Retrieval (CBIR) system. By combining deep features from a pre-trained VGG16 network with color autocorrelogram and Local Binary Pattern (LBP) descriptors, the system achieves higher precision in image similarity search than traditional or deep-only methods.

## Features

- Extracts high-level image semantics using VGG16.
- Captures perceptual color and texture via autocorrelogram and LBP.
- Hybrid feature fusion (with normalization and weighting).
- Searches large image datasets for the most relevant matches to a query image.
- Visualizes results side by side for easy comparison.

## Installation

Clone this repo:  git clone https://github.com/<your-username>/hybrid-cbir.git
cd hybrid-cbir

