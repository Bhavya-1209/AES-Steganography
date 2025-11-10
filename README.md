# 🔐 AES-Based Image Steganography using Python

This project demonstrates **secure data hiding** using **AES encryption** combined with **image steganography**.  
It encrypts a secret message using the **AES (CBC mode)** algorithm and embeds the encrypted data into an image using **pixel manipulation**.

---

## 🧠 Overview

Steganography is the practice of concealing secret information within a non-secret medium—in this case, an image.  
To enhance security, this project combines **cryptography (AES encryption)** with **steganography**.  
Even if someone detects the hidden data, it remains **encrypted** and unreadable without the correct key.

---

## ⚙️ Features

- ✅ AES-128 encryption using SHA-256 derived key  
- ✅ CBC (Cipher Block Chaining) mode for secure block encryption  
- ✅ Simple pixel-based embedding of encrypted data  
- ✅ Key-based verification for secure decryption  
- ✅ Works with standard image formats like `.jpg` or `.png`

---

## 📂 Project Structure
```bash
AES_Steganography/
│
├── AES_Stegonography_final.ipynb   # Main Python script
├── stego.jpg                       # Input cover image
├── encrypted_img.jpg               # Output stego image
└── README.md                       # Documentation
```


---

## 💡 How It Works

### 🔸 Step 1: AES Encryption
- The user enters a **key** and **message**.
- The key is hashed with **SHA-256** and truncated to 128 bits for AES.
- The message is encrypted using AES in **CBC mode**.

### 🔸 Step 2: Data Embedding
- Each encrypted byte is XORed with key bytes and stored into the image pixels.
- The result is a modified (stego) image that visually looks the same as the original.

### 🔸 Step 3: Data Extraction & Decryption
- The hidden bytes are retrieved from the stego image.
- Using the same key, the original message is decrypted and displayed.

---

## 🧪 Example Output
```bash
Image size: 256 256
Enter Key to encrypt & hide: 458
Enter Text to hide: This is a top secret message.

Encrypted message length (in bytes): 48
success

Enter 1 to extract data from Image: 1
enter key to extract text: 458
Decrypted message: This is a top secret message.

```
---
## 🔐 Security Notes

AES (CBC mode) ensures confidentiality of data.

The key must be the same during both encryption and decryption.

The project is designed for educational and research use — not for production or large-scale deployment.

Image quality remains largely unaffected since data is hidden subtly in pixel values.

---

