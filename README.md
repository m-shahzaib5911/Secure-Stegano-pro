# 🔐 Secure-Stegano-Pro

**Secure-Stegano-Pro** is an advanced steganography application that allows you to securely hide and extract encrypted data within images using **AES-256-GCM encryption** and **LSB-based (Least Significant Bit)** embedding.

> 🧩 This repository provides the **compiled application only**.  
> The **source code is private** and not included for intellectual property and security reasons.

---

## 🚀 Features

- AES-256-GCM encryption with password-based key derivation (PBKDF2)
- Multi-threaded image encoding and decoding
- Secure data embedding using LSB technique
- Clean and responsive GUI for easy use
- Supports multiple image formats (`.png`, `.bmp`)
- Error handling, file integrity checks, and progress tracking

---

## 🖥️ Installation

1. Go to the **[Releases](../../releases)** section of this repository.
2. Download the latest version for your operating system:
   - **Windows:** `SecureSteganoPro_v1.1_Setup.exe`
   - **Linux / macOS:** (coming soon)
3. Run the installer and follow the on-screen instructions.

> ⚠️ Windows SmartScreen or antivirus tools may flag unknown executables.  
> You can verify the integrity of your download using the SHA256 checksum provided below.

---

## 🧾 File Integrity Verification

Each release includes a file named `checksums.txt` with SHA-256 hashes.

To verify your file:
```bash
CertUtil -hashfile SecureSteganoPro_vX.X_Setup.exe SHA256

---

Compare the hash output with the one listed in checksums.txt.


