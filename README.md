# Number-plate-detection
License Plate Recognition using Python, OpenCV, and Tesseract OCR

This project implements an automatic license plate recognition (ALPR) system using Python, OpenCV, and Tesseract OCR. It detects the license plate region from an image, processes it for clarity, and extracts the alphanumeric text using Optical Character Recognition (OCR).

📋 Table of Contents

Overview

Features

Tech Stack

Installation

How It Works

Usage

Output

Future Improvements

License

🧠 Overview

License Plate Recognition (LPR) is widely used in traffic monitoring, toll systems, and security applications.
This project demonstrates a simple, efficient approach to detect and recognize license plates from vehicle images using image processing and OCR techniques.

✨ Features

✅ Automatic detection of license plate region
✅ Image preprocessing with Gaussian blur and Canny edge detection
✅ Contour-based plate localization
✅ Text extraction using Tesseract OCR
✅ Works on real-world vehicle images

🛠️ Tech Stack

Language: Python 🐍

Libraries:

OpenCV (for image processing)

pytesseract (for OCR)

matplotlib (for visualization)

numpy

⚙️ Installation

Clone this repository

git clone https://github.com/<your-username>/license-plate-recognition.git
cd license-plate-recognition


Install dependencies

pip install opencv-python pytesseract matplotlib numpy


Install Tesseract OCR

Windows:
Download from Tesseract OCR for Windows

Linux:

sudo apt install tesseract-ocr


macOS:

brew install tesseract


Set Tesseract executable path (in your Python script)

pytesseract.pytesseract.tesseract_cmd = r"C:\Program Files\Tesseract-OCR\tesseract.exe"

🔍 How It Works

Image Loading:
The input image is read and displayed using Matplotlib.

Preprocessing:

Convert to grayscale

Apply Gaussian blur to reduce noise

Detect edges using the Canny algorithm

License Plate Detection:

Find and sort contours by area

Identify rectangular contours (possible license plates)

Draw bounding boxes around detected plates

Text Extraction (OCR):

Apply adaptive thresholding and morphological operations

Use Tesseract OCR with a whitelist of alphanumeric characters

Print the recognized license plate number

▶️ Usage

Place your test image in the project folder (e.g., car.jpg).

Run the script:

python license_plate_recognition.py


The detected plate and extracted text will be displayed on the screen.

🖼️ Output Example
Step	Preview
Original Image	

Detected License Plate	

OCR Result	MH12AB1234
🚀 Future Improvements

Support for multiple plates in one image

Real-time license plate detection from live camera feed

Integration with vehicle database for validation

Better OCR accuracy using deep learning models
