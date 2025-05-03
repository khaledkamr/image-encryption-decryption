# Image Encryption and Decryption

This project implements an image encryption and decryption system for RGB images using a combination of **confusion** (pixel shuffling) and **diffusion** (Caesar cipher) techniques. The script processes an RGB image by splitting it into its Red, Green, and Blue channels, encrypting each channel, decrypting them, and reconstructing the original image. The process is visualized by saving images of each step.

## Features

- **Input**: Accepts an RGB image (e.g., `input_image.jpg`).
- **Encryption**:
  - **Confusion**: Shuffles pixel positions in each channel using a reversible permutation with a fixed seed for reproducibility.
  - **Diffusion**: Applies a Caesar cipher to modify pixel values.
- **Decryption**:
  - Reverses the diffusion step using the inverse Caesar cipher.
  - Reverses the confusion step to restore original pixel positions.
- **Visualization**: Saves images of original, encrypted, decrypted channels, and the reconstructed image.
- **Output**: Generates PNG files in the `imgs/` directory for each stage of the process.

## Requirements

- Python 3.6 or higher
- Required Python packages:
  - `numpy`
  - `Pillow` (PIL)
  - `matplotlib`

You can install the dependencies using pip:

```bash
pip install numpy pillow matplotlib
```

## How to Run

1. **Prepare the Input Image**:
   - Place an RGB image named `input_image.jpg` in the `imgs/` directory. Ensure the image is in a supported format (e.g., JPEG, PNG).

2. **Run the Script**:
   - Execute the Python script from the command line:

     ```bash
     python image_encryption_decryption.py
     ```

3. **Check Outputs**:
   - After execution, check the `imgs/` directory for the generated PNG files:
     - `original_channels.png`
     - `encrypted_channels.png`
     - `decrypted_channels.png`
     - `reconstructed_image.png`

## Notes
- The project currently uses a `Caesar cipher` for the diffusion step, but you can modify the script to implement any other cipher algorithm for enhanced security or experimentation.
- The Caesar cipher shift value (`shift = 50`) and shuffling seeds (`seed = 42, 43, 44`) are hardcoded for simplicity. You can modify these in the script for different encryption strengths.
- The shuffling uses `numpy.random.shuffle` with a fixed seed to ensure the permutation is reversible and reproducible.
- Ensure the input image is in RGB format. If using a different image name or path, update the `image_path` variable in the script.