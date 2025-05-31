# 🧠 Denoising Autoencoder on Grayscale Natural Images

This project implements a **denoising autoencoder** using PyTorch to clean noisy grayscale images (e.g., bikes) of size `64×64`. The model is trained to reconstruct clean images from Gaussian-corrupted inputs.

---

## 📂 Dataset

- A small custom dataset of grayscale natural images (e.g., bikes)
- Images are resized to `64x64`
- Zero-mean Gaussian noise with variable standard deviation is added

---

## 🏗️ Model Architecture

The autoencoder consists of:

### Encoder:
- 4 convolutional layers with ReLU activation and downsampling (stride=2)

### Decoder:
- 4 transposed convolution layers with ReLU activation
- Final layer uses Sigmoid to output pixel values in `[0,1]`

---

## 📈 Training Details

- Loss function: `Mean Squared Error (MSE)`
- Optimizer: `Adam`
- Batch size: `4`
- Number of epochs: `30`
- Framework: `PyTorch`
- Hardware: GPU (via Google Colab)

---

## 💡 Sample Results

Below is a visual example of the model's performance:


![image](https://github.com/user-attachments/assets/251c129e-d138-44ae-8d90-ddf9513d31ca)

![image](https://github.com/user-attachments/assets/4784cf3a-e79e-4624-8e6a-a1137bfece73)







---

## 🚀 How to Run

### ▶️ In Google Colab

1. Open the notebook in Google Colab
2. Upload your own dataset or use the included one
3. Run all cells to train and evaluate the model
4. View the denoising results and loss curves

---

## 🔧 Requirements

- `torch`
- `torchvision`
- `matplotlib`
- `PIL`
- `numpy`

You can install them using:

```bash
pip install torch torchvision matplotlib pillow numpy


