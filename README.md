# AstroRestore-UNet

# AstroRestore: Deep Convolutional Signal Recovery for Galactic Imagery

## 🌌 Overview
In observational astronomy, images are often degraded by atmospheric turbulence (blur) and sensor limitations (Poisson noise). **AstroRestore** is a Deep Learning-based solution designed to recover high-fidelity structural details from low-Signal-to-Noise Ratio (SNR) galactic observations.

Using a **U-Net architecture with skip-connections**, this model learns to invert the effects of Point Spread Function (PSF) blurring and photon-counting noise.

## 🚀 Key Features
* **Physics-Informed Data Augmentation:** Custom pipeline to simulate realistic telescope artifacts (Gaussian blur and Poisson distribution).
* **U-Net Architecture:** Implemented with 200k+ parameters, optimized for $512 \times 512$ resolution with minimal memory footprint.
* **Signal Reconstruction:** Successfully reduced Mean Squared Error (MSE) from 0.0626 to 0.0017 over 15 epochs.
* **Memory Optimization:** Designed for accessibility on edge-computing or standard GPU environments (Colab/TensorFlow).

## 🛠️ Technical Stack
* **Language:** Python
* **Framework:** TensorFlow / Keras
* **Architecture:** U-Net (Encoder-Decoder with Skip Connections)
* **Image Processing:** NumPy, SciPy, Matplotlib

## 📊 Results
The model effectively restores diffuse galactic structures and sharpens spiral arm boundaries that are typically lost in raw telescopic data.

| Input (Noisy/Blurred) | AI Reconstructed (Cleaned) | Ground Truth (Reference) |
| :---: | :---: | :---: |
| *[Insert Image 1]* | *[Insert Image 2]* | *[Insert Image 3]* |

## 📖 Future Scope
* Implementation of **Perceptual Loss (VGG)** to better preserve high-frequency stellar details.
* Testing on multi-wavelength data (X-ray vs. Infrared).
