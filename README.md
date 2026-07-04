# Image Encryption Tool

## Project Overview

The Image Encryption Tool is a Python-based desktop application that encrypts and decrypts images using pixel manipulation techniques. It provides a simple graphical user interface (GUI) built with Tkinter, allowing users to securely transform images using a user-defined encryption key.

The project demonstrates the basic concepts of image encryption by combining two techniques:
- Pixel Value Manipulation
- Pixel Swapping

The same key is required to decrypt the image and restore the original image.

---

## Features

- Graphical User Interface (GUI)
- Select images using a file browser
- User-defined encryption key
- Encrypt images using pixel manipulation
- Decrypt encrypted images
- Automatic saving of encrypted and decrypted images
- Error handling for invalid inputs

---

## Technologies Used

- Python 3.x
- Tkinter (GUI)
- Pillow (PIL) for image processing
- OS module for file handling

---

## Encryption Technique

### 1. Pixel Value Manipulation

Each pixel contains three color values:

- Red (R)
- Green (G)
- Blue (B)

Each RGB value is modified using the formula:

Encryption:

R = (R + Key) % 256

G = (G + Key) % 256

B = (B + Key) % 256

Decryption:

R = (R - Key) % 256

G = (G - Key) % 256

B = (B - Key) % 256

The modulo operator ensures that all RGB values remain within the valid range of 0–255.

---

### 2. Pixel Swapping

After modifying the RGB values, every pair of neighboring pixels is swapped.

Example:

Original:

A B C D E F

Encrypted:

B A D C F E

During decryption, the pixels are swapped back before reversing the RGB transformation.

---

## Project Structure

```
Image_Encryption_Tool/
│
├── gui.py
├── README.md
├── sample.png (optional)
├── encrypted.png (generated)
└── decrypted.png (generated)
```

---

## Installation

### Step 1

Install Python 3.

### Step 2

Install Pillow.

```
pip install pillow
```

---

## Running the Project

Run the following command:

```
python gui.py
```

---

## How to Use

1. Launch the application.
2. Click **Select Image**.
3. Choose an image.
4. Enter an encryption key.
5. Click **Encrypt**.
6. The encrypted image is saved as **encrypted.png**.
7. To decrypt, select the encrypted image.
8. Enter the same encryption key.
9. Click **Decrypt**.
10. The original image is restored as **decrypted.png**.

---

## Input

- PNG
- JPG
- JPEG
- BMP

---

## Output

- encrypted.png
- decrypted.png

---

## Advantages

- Easy to understand
- User-friendly GUI
- Demonstrates image processing concepts
- Demonstrates basic cryptography concepts
- Suitable for academic projects and beginners

---

## Limitations

- This is a basic educational encryption algorithm.
- It is not intended for securing sensitive or confidential images.
- The encryption can be broken if the key and algorithm are known.

---

## Future Improvements

- Stronger encryption algorithms (AES)
- Password protection
- Randomized pixel permutation
- Drag-and-drop image support
- Preview window
- Support for batch encryption
- Save As functionality
- Progress bar during encryption

---

## Learning Outcomes

This project demonstrates:

- Python Programming
- Image Processing
- Pixel Manipulation
- Modular Arithmetic
- Cryptography Basics
- GUI Development using Tkinter
- File Handling
- Error Handling

---

## Author

**Name:** ATHIRA PILLAI

---

## License

This project is developed for educational purposes only.
