# 🖼️ Image Steganography using Edge Detection and AES Encryption

This project implements an **edge detection-based image steganography** technique in Python using Jupyter Notebook.  
It securely hides secret text within a cover image using **AES-256 encryption** and **gradient-based edge detection** to ensure both data confidentiality and image quality.

---

## 📘 Overview

Steganography is the practice of concealing information inside non-secret media to protect its existence.  
This project enhances traditional **LSB (Least Significant Bit)** steganography by focusing on **edges** in the image — areas where minor pixel changes are less visually noticeable — and by encrypting the hidden data before embedding.

---

## ⚙️ Key Features

-  **AES-256 Encryption** of secret text before embedding  
-  **Gradient-based edge detection** to identify suitable embedding regions  
-  **High-quality stego image** with minimal perceptual distortion  
-  **Robust retrieval and decryption** process for extracting hidden text  
-  Implemented entirely in **Python (Jupyter Notebook)**

---

## 🧩 Methodology

1. **Edge Detection:**  
   The gradient method is applied to identify strong edges in the cover image.

2. **Encryption:**  
   The secret text is encrypted using **AES-256**, ensuring that even if extracted, it remains unreadable.

3. **Embedding:**  
   The encrypted binary stream is embedded in the **least significant bits (LSBs)** of detected edge pixels, allowing more bits to be hidden without affecting image quality.

4. **Extraction & Decryption:**  
   The stego image is processed to extract the hidden binary data, which is then decrypted using the same 256-bit key to retrieve the original message.

---
## 🖼️ Example Output

| Original Image | Stego Image (After Embedding Secret Text) |
|----------------|--------------------------------------------|
| ![Original Image](original_image.jpg) | ![Stego Image](stego_image_aes.png) |

The visual difference between the two images is nearly imperceptible, demonstrating that the secret data is hidden securely within the cover image without noticeable degradation in image quality.

## 🧠 Technologies Used

- **Python**
- **NumPy**
- **OpenCV**
- **Matplotlib**
- **Pillow (PIL)**
- **Cryptography (AES-256)**
- **Jupyter Notebook**

---

## 🚀 How to Run

1. Clone this repository:
   ```bash
   git clone https://github.com/Prajwal-0101/Image-Steganography.git

2. Install dependencies:
   ```bash
   Make sure you have Python 3.8+ installed, then run:
   pip install -r requirements.txt

3. Open the Jupyter Notebook:
   ```bash
   jupyter notebook image_steganography.ipynb

4. Run all cells:
   - Follow the step-by-step implementation inside the notebook.  
   - You can modify the input cover image and secret text to test your own examples.
