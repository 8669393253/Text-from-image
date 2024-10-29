# Text-from-image
# OCR Text Extraction Script

This Python script utilizes OpenCV, Tesseract OCR, and the `python-docx` library to extract text from a selected region of an image and save it into a Word document. It provides a simple interface to visually select the text area you want to extract.

## Table of Contents

- [Features](#features)
- [Requirements](#requirements)
- [Installation](#installation)
- [Usage](#usage)
- [Code Overview](#code-overview)
- [Error Handling](#error-handling)
- [License](#license)
- [Acknowledgments](#acknowledgments)

## Features

- Load an image and display it in a window.
- Allow users to select a region of the image using mouse events.
- Extract text from the selected region using Tesseract OCR.
- Save the extracted text into a Word document.

## Requirements

Make sure you have the following installed:

- Python 3.x
- OpenCV
- NumPy
- Pillow (PIL)
- Tesseract OCR
- python-docx

You can install the required Python packages using pip:
pip install opencv-python numpy Pillow pytesseract python-docx


### Tesseract OCR
Tesseract OCR needs to be installed separately. Follow the installation instructions for your operating system:

**Windows**: Download the installer from [Tesseract at UB Mannheim](https://github.com/UB-Mannheim/tesseract/wiki).
**macOS**: Install using Homebrew:
  brew install tesseract

**Linux**: Install using your package manager, for example:
  sudo apt-get install tesseract-ocr


After installation, make sure to set the correct path to the Tesseract executable in the script if necessary.

## Installation

1. Clone the repository or download the script file.
   git clone <repository-url>
   cd <repository-directory>


2. Ensure all dependencies are installed as mentioned above.

3. Update the script with your image path and Word document path if needed.

## Usage

1. Run the script:
   python ocr_text_extraction.py


2. An image window will open displaying your selected image. Use your mouse to click and drag over the area you want to extract text from.

3. Release the mouse button to finalize your selection. The script will extract the text from the selected region and display it in the console.

4. The extracted text will be saved in a Word document at the specified path.

## Code Overview

**Image Loading**: The script uses OpenCV to load the image from a specified path.
**Mouse Callback**: It sets up a callback function to handle mouse events, allowing users to select the desired region.
**Text Extraction**: After selection, it uses Tesseract OCR to extract text from the selected image region.
**Word Document Creation**: The extracted text is saved into a Word document using the `python-docx` library.

## Error Handling

The script includes basic error handling. If the image fails to load or if the Tesseract OCR is not found, appropriate error messages will be displayed in the console. Consider enhancing error handling for a more robust user experience.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- [OpenCV](https://opencv.org/)
- [Tesseract OCR](https://github.com/tesseract-ocr/tesseract)
- [python-docx](https://python-docx.readthedocs.io/en/latest/)
