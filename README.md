# Learning Diffusion Models
<p align="center">
  <img src="images/header.png" alt="Diffusion Model Spiral Example" width="500"/>
</p>


A collection of notebooks implemented from scratch to learn step-by-step major concepts of diffusion models. In this project I opted for simple implementations, derived from first princples. Starting from the basics with an unconditional DDPM to reconstruct spiral-shaped data, I go through image generation, classifier-free guidance, flow matching, latent diffusion and gradient-based optimization.
I built this over time as an excuse to learn diffusion from the basics, hopefully it will be helpful to you as well!


## Notebooks

### 1. Diffusion Basics
Introduction to the fundamental concepts of diffusion models using a simple 2D spiral dataset. Learn how neural networks can reverse the forward diffusion process to generate data from noise.

### 2. Generating Images
Apply diffusion models to real image data using the MNIST dataset. Implement a U-Net architecture for image denoising and extend to conditional generation.

### 3. Classifier-Free Guidance
Explore how to improve conditional generation by training models that can operate in both conditional and unconditional modes, allowing for stronger adherence to conditions during inference.

### 4. Flow Matching
Learn about an alternative to traditional diffusion models that uses continuous normalizing flows (CNFs) to define smooth, deterministic trajectories from noise to data. This approach learns velocity fields instead of noise predictions.

### 5. Latent Diffusion
Discover how to work in compressed latent spaces using Variational Autoencoders (VAEs), enabling more efficient generation of high-resolution images. This is the approach used by models like Stable Diffusion.

### 6. Gradient-Based Optimization
Implement gradient-based steering mechanisms that can guide generation toward specific properties or constraints at inference time without retraining the model.

### 7. Diffusion Energy-Based Modelling
Learn how the concept of energy can be applied to diffusion models by tweaking a simple architecture and how to score and filter generated samples by quality.


## Next steps
It would be interesting to explore more advanced concepts like Diffusion Transformers, Optimal Transport and Multi-Objective Optimization.

## Requirements

- Python >= 3.12
- PyTorch >= 2.9.1
- torchvision >= 0.24.1
- numpy >= 2.3.5
- matplotlib >= 3.10.7
- ipywidgets >= 8.1.8

## Setup

This project uses `uv` for dependency management. To set up the environment:

```bash
# Install dependencies
uv sync

# Activate the environment
source .venv/bin/activate  # On macOS/Linux
# or
.venv\Scripts\activate  # On Windows
```

Alternatively, if you're using pip:

```bash
pip install torch torchvision numpy matplotlib ipywidgets
```

## Dataset

The notebooks use the MNIST dataset for image generation tasks. The dataset will be automatically downloaded when you run the notebooks that require it.

## License

Feel free to use and modify the code. 

## Acknowledgments

- Visualization in the Flow Matching notebook by Alec Helbling ([Diffusion Explorer](https://github.com/helblazer811/Diffusion-Explorer))
