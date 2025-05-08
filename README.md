# 😄 Facial Expression Generation Using GAN and Autoencoder

![Python](https://img.shields.io/badge/Python-3.8%2B-blue?style=for-the-badge&logo=python)
![TensorFlow](https://img.shields.io/badge/TensorFlow-2.x-orange?style=for-the-badge&logo=tensorflow)
![Accuracy](https://img.shields.io/badge/ACCURACY-90%25%2B-brightgreen?style=for-the-badge&logo=google)
![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge&logo=opensourceinitiative)


This project leverages deep learning to generate facial expressions from labeled data using an **autoencoder architecture** trained on the **CelebA** dataset. The model learns facial features (e.g., "Smiling") and can reconstruct or generate faces conditioned on these attributes.

## 🔍 Overview

Facial expression generation is a complex area in computer vision. This notebook uses the CelebA dataset, focusing on labeled facial attributes to generate or classify expressions using an autoencoder structure.

## 📁 Project Structure

```
Facial_Expression_Generation_Labeled.ipynb
README.md
```

## 🚀 Features

- 📂 Loads and filters CelebA facial attribute dataset
- 🧠 Trains a custom encoder-decoder (autoencoder) network
- 🎨 Generates expressions based on labeled features (e.g., "Smiling")
- 📊 Tracks and visualizes accuracy, loss, and outputs
- 🧪 Evaluates generation quality and classification accuracy

## 🧰 Technologies Used

- Python 3.x
- PyTorch
- torchvision
- Google Colab
- Matplotlib, Pandas
- PIL, NumPy

## 📊 Dataset

**CelebA** — a large-scale face dataset with 202,599 celebrity images, each annotated with 40 attribute labels (e.g., *Smiling*, *Male*, *Eyeglasses*).

This project focuses on the "Smiling" label to:
- Train the encoder to learn a latent representation of smiling vs non-smiling faces
- Use the decoder to generate corresponding facial images

## 🧪 Model Evaluation

The training process monitors:

- **Reconstruction Loss** (MSE or BCE): Measures how well the decoder recreates the input.
- **Attribute Accuracy**: A simple classifier is sometimes used on the latent representation to test if attributes like "Smiling" are preserved.
- **Loss & Accuracy Visualization**: The notebook includes plots to visualize training dynamics.

## ⚙️ How to Use

1. Clone the repo or download the notebook.
2. Upload the CelebA dataset and attribute file (`img_align_celeba.zip` and `list_attr_celeba.txt`) to your Google Drive.
3. Run the notebook on **Google Colab** (recommended).
4. All required packages will be installed at runtime.

## 📈 Output Examples

The notebook generates:

- Reconstructed face images side-by-side with originals
  ![image](https://github.com/user-attachments/assets/ea4a7ad2-90b4-4695-ac61-728390d96656)

- Images with changed expression attributes
- Loss and accuracy graphs per epoch
 ![image](https://github.com/user-attachments/assets/64045dc5-35a6-492e-a41d-b7ac5a317222)
-Confusion Matrix
![image](https://github.com/user-attachments/assets/3f677031-08d7-4636-84a1-5d501215d05f)
-Hyperparamater Tuning
![image](https://github.com/user-attachments/assets/2f701c82-709b-4f23-ad3a-72ec85ae1458)




## 📌 Notes

- The model uses a **custom `CelebAZipDataset` class** to read images from a ZIP file without extracting.
- Ensure you have enough runtime memory in Colab (recommended: GPU backend).
- The model can be extended to other labels like “Happy,” “Sad,” or “Surprised” by changing attribute filters.

## ✅ Future Work

- Extend to full expression classification (multi-label)
- Use a Conditional GAN for sharper results
- Evaluate with metrics like FID or IS scores
- Add a web demo using Streamlit or Gradio

## 👨‍💻 Author
Sanya Shresta Jathanna
 
