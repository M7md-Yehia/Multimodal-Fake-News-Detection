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
We use the [FakeNewsNet](https://arxiv.org/abs/1809.01286) dataset as a base. Our cleaned and filtered data is available [here](https://drive.google.com/drive/folders/14LYqAASzauCwIpoa2nX-lr-qIKPZ1QY8?usp=sharing).  
For the latest version of FakeNewsNet, please check: https://github.com/KaiDMML/FakeNewsNet.

### Image Captioning Tool  
We utilize the [BLIP (Bootstrapping Language-Image Pre-training)](https://github.com/salesforce/BLIP) model for image captioning. This tool generates descriptive captions from images, which are then used in our multimodal analysis.

### Word Embedding  
For word embeddings, we use the pre-trained [GloVe 840B 300d vectors](https://github.com/stanfordnlp/GloVe).  
Due to the large size and processing time of the GloVe embeddings, we provide precomputed word maps and embedding results [here](https://drive.google.com/drive/folders/14LYqAASzauCwIpoa2nX-lr-qIKPZ1QY8?usp=sharing).  

---

## Image Captioning and Embedding Script

This script performs the following steps:

1. Mounts Google Drive to access project data.
2. Loads the filtered dataset CSV containing image metadata.
3. Extracts preprocessed images from a ZIP archive.
4. Uses the Salesforce BLIP model to generate captions for all images in the dataset.
5. Saves the captions with labels into a CSV file and copies it back to Google Drive.
6. Extracts GloVe embeddings and a precomputed word embedding file from ZIP archives.
7. Loads GloVe embeddings into memory.
8. Computes sentence-level embeddings for the generated captions by averaging GloVe word embeddings.
9. Saves the caption embeddings as a NumPy array.
10. Loads and cleans the caption CSV for further processing or merging.

**Requirements:**

- Python packages: `pandas`, `torch`, `transformers`, `Pillow`, `tqdm`, `numpy`
- Google Drive access for input/output files
- Pretrained models and embeddings as specified in the project

**Usage:**

Run this script in a Google Colab environment or any environment with access to the datasets and required libraries.

```bash
python image_captioning_and_embedding.py
