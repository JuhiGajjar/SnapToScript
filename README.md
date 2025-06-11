# 🖼️ SnapToScript

## 📌 Introduction  
This project demonstrates an **Image Caption Generator** that combines **Computer Vision** and **Natural Language Processing** to interpret images and generate human-like captions.  
It has impactful applications in:
- Assistive technologies for the visually impaired  
- Medical image analysis  
- Geospatial mapping and exploration

---

## 🎯 Use Cases

- **🔊 Assistive Technology**: Converts image captions into speech to help the visually impaired understand their surroundings.
- **📈 Marketing**: Automatically generate image captions for advertising, reducing manual effort.
- **🩺 Medical Imaging**: Supports medical professionals in identifying abnormalities in diagnostic scans.
- **🌍 Geospatial Analysis**: Generates insights from satellite and aerial images.
- **🤖 Robotics**: Helps robots detect and describe objects for better interaction with their environment.

---

## 📂 Dataset

- **Source**: [Flickr8k Dataset on Kaggle](https://www.kaggle.com/datasets/adityajn105/flickr8k)  
- **Details**:
  - ~1,500 images  
  - Each image has 5 different captions written by humans  
  - Captions are linked to images using image IDs  

---

## 🚀 Steps to Execute
1. Caption Cleaning
- Remove punctuation, numbers, and single-character words for clean inpu

2. Special Tokens
- Use <start> and <end> markers to indicate the start and end of each 
caption.

3. Feature Extraction
- Use a pre-trained VGG16 CNN model to extract 4096 features per image.

4. Grouping
- Group similar images using extracted features for better modeling.

5. Merging & Tokenization

 - Merge the first caption with its image

 - Convert text to numerical tokens

6. Data Splitting
Create training, validation, and testing datasets.

7. Model Building (LSTM)
- Build an LSTM-based neural network with multiple layers to learn capti
generation from image features and word sequences.

8. Evaluation
- Generate captions for unseen images and evaluate using BLEU scores — 
higher score indicates closer resemblance to real captions.

---

## ⚙️ Installation

Install the required libraries:

```bash
pip install tensorflow
pip install keras
pip install nltk
pip install h5py
