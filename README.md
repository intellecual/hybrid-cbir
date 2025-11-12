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
Install dependencies using pip:

bash
python -m pip install -r requirements.txt
If you don’t have a requirements.txt, install dependencies manually:

bash
python -m pip install tensorflow keras opencv-python scikit-image scikit-learn scipy matplotlib numpy
Place your .jpg or .png images in the images/ folder (or update the code with your image folder path).

## Usage
Set your query image and dataset path in cbir_hybrid.py.

Run the script:

text
python cbir_hybrid.py
To visualize query and top results, use the matplotlib code provided.

## Example
Query and result image display:

python
import matplotlib.pyplot as plt
import matplotlib.image as mpimg
files = [
    "images/1.jpg",
    "images/11.jpg",
    "images/17.jpg",
    "images/5.jpg",
    "images/12.jpg",
]
titles = ['Query', '1st', '2nd', '3rd', '4th']
plt.figure(figsize=(18, 4))
for idx, f in enumerate(files):
    plt.subplot(1, 5, idx+1)
    plt.imshow(mpimg.imread(f))
    plt.title(titles[idx])
    plt.axis('off')
plt.tight_layout(); plt.show()
## File Structure
cbir_hybrid.py - Main script implementing feature extraction, indexing, and retrieval

requirements.txt - Python dependencies

images/ - Place your image dataset here

README.md - Project documentation

## License
This project is released under the MIT License.
Feel free to contribute or adapt for your academic or personal use!

