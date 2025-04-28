# Image Encryption and Decryption Project

## Overview
This project demonstrates a basic image encryption and decryption technique for a college-level computer security course. It uses confusion (pixel shuffling) and diffusion (Caesar cipher on pixel values) to encrypt a grayscale image, then reverses the process to decrypt it. The project is implemented in Python using a Jupyter notebook and visualizes each step with Matplotlib.

### Objectives
- Understand fundamental concepts of image encryption: confusion and diffusion.
- Implement a Caesar cipher for diffusion on pixel values.
- Use pixel shuffling for the confusion step.
- Visualize the encryption and decryption process.

## Prerequisites
- Python 3.12 or higher
- Jupyter Notebook (or Jupyter Lab)
- Libraries: `numpy`, `Pillow`, `matplotlib`

## Setup Instructions
1. **Clone or Download the Project**
   ```
   git clone https://github.com/khaledkamr/image-encryption-decryption.git
   ```

2. **Install Dependencies**
   - Open a terminal and ensure you have Python installed.
   - Install the required libraries:
     ```
     pip install numpy pillow matplotlib
     ```
     If using Anaconda:
     ```
     conda install numpy pillow matplotlib
     ```

3. **Set Up Jupyter Notebook**
   - If not already installed, install Jupyter:
     ```
     pip install jupyter
     ```
   - Launch Jupyter Notebook:
     ```
     jupyter notebook
     ```

4. **Prepare the Input Image**
   - Save an image as `input_image.jpg` in the same directory as the notebook.
   - The code will convert it to grayscale for processing.
