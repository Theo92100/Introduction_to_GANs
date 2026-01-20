# Generative Models Part 1: An Introduction to GANs

This repository contains the PyTorch implementation accompanying the PDF note **"Generative Models Part 1: An Introduction to GANs."**

It provides a minimal, self-contained walkthrough of training Generative Adversarial Networks (GANs) on MNIST, specifically designed to demonstrate the link between optimization stability and the mathematical objective functions (Jensen-Shannon vs. Wasserstein).

## 📄 Content Overview

The notebook (`minimal_gan_mnist_adam_sgd_wgangp.ipynb`) implements three specific training scenarios.

1. **Vanilla GAN (Adam):** Implementation of the standard Min-Max game using the non-saturating generator loss.


2. **Mode Collapse (SGD):** A demonstration of how optimization instability (using plain SGD) can cause the generator to collapse to a single mode (producing only one digit, e.g., "1"), despite a valid architecture.


3. **WGAN-GP:** Implementation of the **Wasserstein GAN** using **Gradient Penalty**. This replaces the discriminator with a 1-Lipschitz "critic" to solve the vanishing gradient problem caused by support mismatch.



## 🛠️ Usage

### Option 1: Google Colab (Recommended)

Click the badge above to run the notebook directly in your browser with free GPU acceleration.

### Option 2: Local Installation

1. Clone the repo:
```bash
git clone https://github.com/Theo92100/Introduction_to_GANs.git
cd Introduction_to_GANs

```


2. Install dependencies:
```bash
pip install torch torchvision matplotlib numpy jupyter

```


3. Run the notebook:
```bash
jupyter notebook minimal_gan_mnist_adam_sgd_wgangp.ipynb

```



## 📊 Results & Visualization

The notebook automatically generates  grids of samples at regular intervals to visualize the "digit manifold" learning process.

| Vanilla GAN (Adam) | Mode Collapse (SGD) | WGAN-GP |
| --- | --- | --- |
| *Diverse digits* | *Collapsed to single digit* | *Stable training* |
|  |  |  |

<img width="482" height="242" alt="epoch 2 wgan (1)" src="https://github.com/user-attachments/assets/20df30b6-5c7d-460b-bbd5-2958dd38bb6f" />


## 📚 References

This work is inspired from the MVA Generative Models lecture by Arthur Leclaire and Bruno Galerne.

* 
**GAN:** Goodfellow et al., *Generative Adversarial Nets*, 2014.


* 
**WGAN:** Arjovsky et al., *Wasserstein GAN*, 2017.


* 
**WGAN-GP:** Gulrajani et al., *Improved Training of Wasserstein GANs*, 2017.



## 📬 Contact

If you found this useful or you have any questions, feel free to reach out or follow the discussion on [LinkedIn](https://www.linkedin.com/in/th%C3%A9o-niemann-8b3b16226/).
