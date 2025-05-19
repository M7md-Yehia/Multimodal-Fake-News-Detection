"# Multimodal-Fake-News-Detection" 
Detect fake news by analyzing both text and images using deep learning techniques combining NLP and computer vision.


## Image Download Script

**`download_images.py`**

- Reads dataset CSV with image URLs and labels.
- Downloads images into separate folders by label.
- Verifies images are not corrupted.
- Logs success and failures, drops failed rows from dataset.
- Outputs cleaned dataset CSV without failed images.

**Usage:**

```bash
python scripts/download_images.py
```

## Resources

### Dataset  
We use the [FakeNewsNet](https://arxiv.org/abs/1809.01286) dataset as a base. Our cleaned and filtered data is available [here](https://drive.google.com/drive/folders/1gSx4S9i6Haul4TQRkoNQtj3sRHVwGFQ3?usp=sharing).  
For the latest version of FakeNewsNet, please check: https://github.com/KaiDMML/FakeNewsNet.

### Image Captioning Tool  
We utilize the [BLIP (Bootstrapping Language-Image Pre-training)](https://github.com/salesforce/BLIP) model for image captioning. This tool generates descriptive captions from images, which are then used in our multimodal analysis.

### Word Embedding  
For word embeddings, we use the pre-trained [GloVe 840B 300d vectors](https://github.com/stanfordnlp/GloVe).  
To efficiently compute sentence embeddings, we employ the [Smooth Inverse Frequency (SIF)](https://github.com/PrincetonML/SIF) method.  
Due to the large size and processing time of the GloVe embeddings, we provide precomputed word maps and embedding results [here](https://drive.google.com/drive/folders/1yJSwmx7kpmEHvJ5OTt5mdF9FtFxs4Mqd?usp=sharing).  
Please refer to the **embedding** branch for modified code related to embedding computations.

---
