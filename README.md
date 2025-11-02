# Secure-Stegano-pro
Secure Stegano Pro is an advanced desktop utility that successfully merges Least Significant Bit (LSB) Steganography with robust data security measures. Developed using Python and the PyQt5 framework, this tool provides users with a comprehensive solution for concealing files, folders, and text within ordinary image files.

The core objective of this application is to ensure that hidden data is not only concealed (via LSB manipulation) but is also unreadable should the steganographic image fall into unauthorized hands (via strong encryption).

# 🛡️ Core Technology and Security
LSB Hiding: Data is sequentially embedded into the Least Significant Bit (LSB) of the Red, Green, and Blue colour channels for every pixel of the carrier image. This method results in no perceptibly visible change to the image.

Military-Grade Encryption: Before embedding, every payload (text, file, or compressed folder archive) is encrypted using the user-provided password and the AES-256 GCM (Galois/Counter Mode) algorithm. The GCM mode ensures both confidentiality and integrity of the data.

Multithreaded Performance: Time-consuming operations, such as data embedding and extraction, are executed within dedicated worker threads to ensure the Graphical User Interface (GUI) remains responsive and smooth during processing.

Data Integrity: The encrypted payload includes necessary headers (salt, nonce, tag) and a unique End Marker to ensure the application can correctly locate the data boundary and verify that the data has not been tampered with upon extraction.

# ✨ Key Features
🔒 High Security: Implements AES-256 GCM encryption for maximum data protection before LSB embedding.

📝 Versatile Payload: Hide text, individual files, entire folders (auto-zipped), or video files within a standard image.

⚙️ Multithreaded Operations: Encoding and decoding processes run in separate worker threads to keep the GUI responsive.

📂 Standalone Crypto Tools: Includes a dedicated utility panel for encrypting and decrypting standalone text and files using the same strong AES standard, independent of steganography.

🧹 Data Eradication: A feature to remove steganographic data by clearing the LSB of every RGB channel in the carrier image.

🔄 Image Management: Functions for loading, saving, copying/pasting images, and an Update/Overwrite function to commit changes.
