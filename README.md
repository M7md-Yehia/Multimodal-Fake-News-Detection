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
