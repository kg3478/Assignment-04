# Learning Probability Density Functions using data

## Objective

The objective of this assignment is to learn the probability density function (PDF) of transformed NO₂ data using a Generative Adversarial Network (GAN).

---

## Dataset

The dataset used contains air quality measurements. From this dataset, only the NO₂ (Nitrogen Dioxide) values were considered.
Missing values were removed before further processing.

---

## Transformation

The original NO₂ values were normalized and then transformed using the following equation:

z = x + a·sin(bx)

where:
r = 102303431
a = 2.0
b = 0.6

This transformation introduces non-linearity in the data.

---

## GAN Architecture

Two neural networks were used:

**Generator**

* Takes random noise as input
* Produces synthetic data samples

**Discriminator**

* Takes real and generated samples as input
* Predicts whether the sample is real or fake

Both networks were implemented using simple fully connected layers.

---

## Training Process

* Binary Cross Entropy loss was used
* Adam optimizer was applied
* The model was trained for 300 epochs
* In each step, the discriminator and generator were trained alternately

---

## PDF Estimation

After training, synthetic samples were generated using the generator.
Kernel Density Estimation (KDE) was applied to estimate the probability density function of the generated data.

---

## Observations

* The GAN was able to learn the general shape of the distribution
* Some variations were observed due to randomness in training
* The estimated PDF closely follows the generated data distribution

<img width="744" height="451" alt="Screenshot 2026-03-25 at 12 40 47 PM" src="https://github.com/user-attachments/assets/b21fba2b-346b-4db9-aae6-1695b6f49715" />

---

---
