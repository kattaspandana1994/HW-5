Overview
This repository contains my solutions for Home Assignment 5, covering Generative Adversarial Networks (GANs), AI ethics and harm, data poisoning, legal/ethical implications of GenAI, and bias/fairness tools. The assignment includes both theoretical explanations and practical programming tasks.

Table of Contents
1. GAN Architecture
2. Ethics and AI Harm
3. Programming Task: Basic GAN Implementation
4. Programming Task: Data Poisoning Simulation
5. Legal and Ethical Implications of GenAI
6. Bias & Fairness Tools
How to Run
References
1. GAN Architecture
This section explains the adversarial process in GAN training, the goals of the generator and discriminator, and how they improve through competition.
A diagram is included in the report to illustrate the data flow and objectives of each component.

2. Ethics and AI Harm
I discuss representational harm in generative AI, using the example of biased image generation. Two mitigation strategies are proposed:

Curating diverse and representative training data
Regular bias auditing and post-processing
3. Programming Task: Basic GAN Implementation
A simple GAN is implemented using PyTorch to generate handwritten digits from the MNIST dataset.
Features:

Custom Generator and Discriminator architectures
Training loop with alternating updates
Sample images saved at epochs 0, 50, and 100
Loss plots for both generator and discriminator
Files:

gan_mnist.py (main code)
gan_epoch_0.png, gan_epoch_50.png, gan_epoch_100.png (generated samples)
gan_losses.png (loss plot)
4. Programming Task: Data Poisoning Simulation
A data poisoning attack is simulated on a sentiment classifier using a small movie review dataset.

The attack targets reviews mentioning "UC Berkeley" by flipping their sentiment labels.
The impact is analyzed using accuracy, confusion matrix, and predictions on new phrases.
Files:

data_poisoning.py (main code)
poisoning_results.png (visualization of label flipping and predictions)
5. Legal and Ethical Implications of GenAI
This section discusses the risks of AI memorizing private data and generating copyrighted material.
I argue that generative AI models should be restricted from certain data during training to protect privacy, respect intellectual property, and maintain public trust.

6. Bias & Fairness Tools
I review the False Negative Rate (FNR) Parity metric from the Aequitas Bias Audit Tool, explaining what it measures, why it matters, and how a model might fail this metric.
An example is provided to illustrate fairness auditing.

How to Run
Clone this repository.
Install dependencies:
pip install torch torchvision matplotlib numpy scikit-learn seaborn
To run the GAN example:
python gan_mnist.py
Generated images and loss plots will be saved in the working directory.
To run the data poisoning simulation:
python data_poisoning.py
The script will output analysis and save a visualization.
Student Info
Name: [Your Name]
Student ID: [Your ID]
Email: [Your Email]
References
Goodfellow, I. et al. (2014). Generative Adversarial Nets.
Aequitas Bias Audit Tool: https://github.com/dssg/aequitas
PyTorch Documentation: https://pytorch.org/docs/stable/index.html
Scikit-learn Documentation: https://scikit-learn.org/stable/
