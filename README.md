# Secure-Stegano-pro
Secure Stegano Pro is an advanced desktop utility that successfully merges Least Significant Bit (LSB) Steganography with robust data security measures. Developed using Python and the PyQt5 framework, this tool provides users with a comprehensive solution for concealing files, folders, and text within ordinary image files.

The core objective of this application is to ensure that hidden data is not only concealed (via LSB manipulation) but is also unreadable should the steganographic image fall into unauthorized hands (via strong encryption).

# 🛡️ Core Technology and Security
## LSB Hiding
Data is sequentially embedded into the Least Significant Bit (LSB) of the Red, Green, and Blue colour channels for every pixel of the carrier image. This method results in no perceptibly visible change to the image.

## Military-Grade Encryption
Before embedding, every payload (text, file, or compressed folder archive) is encrypted using the user-provided password and the AES-256 GCM (Galois/Counter Mode) algorithm. The GCM mode ensures both confidentiality and integrity of the data.

## Multithreaded Performance 
Time-consuming operations, such as data embedding and extraction, are executed within dedicated worker threads to ensure the Graphical User Interface (GUI) remains responsive and smooth during processing.

## Data Integrity
The encrypted payload includes necessary headers (salt, nonce, tag) and a unique End Marker to ensure the application can correctly locate the data boundary and verify that the data has not been tampered with upon extraction.

## ✨ Key Features

### 🧩 Steganography
- Hide **Text**, **Files**, **Folders**, and **Videos** inside images.
- Extract hidden data using a password.
- Clear hidden information (erase steganographic data from image pixels).
- Real-time **image preview** panel with scaling and updates.

### 🔐 Encryption Tools
- AES-256-GCM encryption/decryption for **Text** and **Files**.
- Uses **PBKDF2** key derivation with 100,000 iterations.
- Encrypt/decrypt directly inside the app.

### ⚙️ Utility Features
- Built-in **file explorer** to navigate directories.
- **Copy/Paste** via system clipboard (text or image).
- **Progress bar** for visual feedback.
- Temporary files cleaned automatically.
- Responsive, modern PyQt5 interface.

---

## 🧭 Button Functionality Guide

| **Category** | **Button** | **Icon** | **Functionality** |
|---------------|-------------|-----------|-------------------|
| 🗂 **File Operations** | 🆕 **New** | | Clears all data and resets the app. |
| | 📁 **Open** | | Opens and loads an image into the preview panel. |
| | 💾 **Save** | | Saves the current (possibly modified) image. |
| | 🧹 **Clear** | | Clears all text, image, and progress data. |

| **Clipboard Tools** | 📋 **Copy** | | Copies current text or image to clipboard. |
| | 📌 **Paste** | | Pastes text or image from clipboard. |
| | ❌ **Clear** | | Clears clipboard content. |

| 🔒 **Data Hiding** | 🔒 **Hide Text** | | Hides entered text inside the loaded image. |
| | 📁 **Hide Files** | | Select and hide one or more files (auto-zipped). |
| | 🗂️ **Hide Folder** | | Hides a complete folder by compressing it. |
| | 🎥 **Hide Video** | | Hides a video file inside an image. |

| 📤 **Data Extraction** | 📝 **Extract Text** | | Extracts hidden text from the image. |
| | 📂 **Extract File** | | Extracts a hidden file and restores it. |
| | 📁 **Extract Folder** | | Extracts and restores a hidden folder archive. |
| | 🎬 **Extract Video** | | Extracts a hidden video file. |

| 🔐 **Encryption Tools** | 🔐 **Encrypt Text** | | Encrypts text using AES-256-GCM. |
| | 🔓 **Decrypt Text** | | Decrypts encrypted text back to plain text. |
| | 📁 **Encrypt File** | | Encrypts a selected file to `.enc` format. |
| | 📂 **Decrypt File** | | Decrypts an `.enc` file to its original. |

| 🧰 **Preview & Maintenance** | 🔄 **Update** | | Refreshes preview and overwrites the original image if needed. |
| | 🚪 **Exit** | | Closes the app safely, cleaning temporary data. |
| | 🧹 **Erase Hidden Data** | | Clears hidden steganographic data from image pixels (LSB cleaning). |

---

## 🧠 How It Works

1. **Load an image** (`.png`, `.jpg`, `.jpeg`, `.bmp`).
2. Choose to **Hide Text**, **File**, **Folder**, or **Video**.
3. Enter a strong **password** (used for AES-256 encryption).
4. The app embeds the encrypted data securely inside the image.
5. To recover, open the same image and choose **Extract** with the same password.

---

## 🧩 Tech Stack

- **Python 3.9+**
- **PyQt5** — GUI framework  
- **Pillow (PIL)** — Image handling  
- **PyCryptodome** — AES encryption/decryption  
- **zipfile** — Folder compression and extraction

## 🔐 Security Details

AES-256-GCM Encryption ensures both confidentiality and integrity.

Passwords are stretched using PBKDF2 (100,000 iterations) with a random 32-byte salt.

Embedded data is stored in Least Significant Bits (LSBs) of image pixels.

The Erase Hidden Data feature can sanitize images to remove hidden traces.

## 🧹 Cleanup & Temporary Files

Temporary directories and files are automatically managed and deleted on exit.

Each hidden or extracted file is stored safely in a system temp directory before cleanup.

## 💡 Tips

Prefer .png images for hiding larger data (lossless format).

Use strong passwords (8+ characters, mixed symbols/numbers).

Avoid hiding files larger than the image capacity (app shows a warning).
<img width="1366" height="725" alt="image" src="https://github.com/user-attachments/assets/1eef9a5e-3fb9-4be1-85f6-6869789910e9" />
