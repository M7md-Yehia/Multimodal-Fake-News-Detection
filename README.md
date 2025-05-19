Got it! Here's an updated version of your README with a more concise and **English** version, without detailing each file’s functionality:

---

# Multimodal Fake News Detection

This project detects fake news by analyzing both text and images using deep learning techniques, combining Natural Language Processing (NLP) and computer vision.

## Scripts

### 1. **`download_images.py`**

This script downloads images from URLs in the dataset, checks for corruption, and saves the cleaned data in a new CSV file.


### 2. **`image_captioning_and_embedding.py`**

Generates captions for images using the BLIP model, extracts GloVe word embeddings, and computes sentence-level embeddings for the captions. Results are saved as CSV and NumPy files.


### 3. **`train_early_fusion_bert.py`**

Trains a multimodal classifier using BERT embeddings for both text and image captions, evaluates the model, and plots the training/validation metrics.


---

## Resources

### Dataset

We use the [FakeNewsNet dataset](https://arxiv.org/abs/1809.01286) as a base. Cleaned and filtered data is available [here](https://drive.google.com/drive/folders/14LYqAASzauCwIpoa2nX-lr-qIKPZ1QY8?usp=sharing).
For the latest version of FakeNewsNet, visit: [FakeNewsNet GitHub](https://github.com/KaiDMML/FakeNewsNet).

### Image Captioning Tool

The project uses the [BLIP model](https://github.com/salesforce/BLIP) for generating captions from images.

### Word Embedding

For word embeddings, we use pre-trained [GloVe 840B 300d vectors](https://github.com/stanfordnlp/GloVe). Precomputed word maps and embedding results are available [here](https://drive.google.com/drive/folders/14LYqAASzauCwIpoa2nX-lr-qIKPZ1QY8?usp=sharing).

