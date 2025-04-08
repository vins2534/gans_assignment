# GAN Variants Performance Comparison

This repository presents a comparative study of three prominent Generative Adversarial Network (GAN) variants — **LSGAN**, **WGAN**, and **WGAN-GP** — based on their performance in generating high-quality synthetic images.

## Overview

GANs are powerful generative models that learn to produce realistic data through adversarial training. Different variants aim to improve stability, convergence, and output quality. This project evaluates the visual performance and quantitative metrics of:

- **Least Squares GAN (LSGAN)**
- **Wasserstein GAN (WGAN)**
- **Wasserstein GAN with Gradient Penalty (WGAN-GP)**

## Evaluation Metrics

Two primary metrics are used to evaluate GAN performance:

- **Fréchet Inception Distance (FID ↓)**: Lower FID indicates that the generated images are closer to real ones in distribution.
- **Inception Score (IS ↑)**: Higher IS implies better image quality and diversity.

Additionally, **visual inspection** of the generated images helps assess mode collapse, blurriness, and overall realism.

## Results Summary

| Model      | FID ↓   | IS ↑   | Visual Quality |
|------------|---------|--------|----------------|
| **LSGAN**  | 48.13   | 2.02   | ✅ Best         |
| **WGAN**   | 133.26  | 1.72   | ❌ Blurry       |
| **WGAN-GP**| 414.35  | 1.00   | ❌ Collapsed    |

## Conclusion

- **LSGAN** outperformed others in both quantitative and qualitative evaluations, demonstrating stable training and sharp image generation.
- **WGAN** showed moderate performance but suffered from blurriness.
- **WGAN-GP**, despite its theoretical improvements, experienced training instability in this setup, leading to mode collapse.

This analysis highlights the importance of empirical evaluation when choosing the right GAN variant for a task, as performance can vary widely based on architecture, data, and training configurations.

