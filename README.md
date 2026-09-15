# CS5720 – Home Assignment 1
**Course:** CS5720 Neural Networks and Deep Learning, Fall 2026
**University:** University of Central Missouri
**Student Name:** Anuradha Kurupathi
**Student ID:** 700781806

---

##  Overview
This repository contains my solutions for Home Assignment 1, covering short-answer conceptual questions (Part I) and four hands-on TensorFlow/Keras programming tasks (Part II). All code was written and executed in Google Colab.

---

##  Repository Contents
- `CS5720_ASSIGNMENT1_Anu.ipynb` — Colab notebook with all 4 programming tasks
- `README.md` — this file
- (Optional) `answers.md` or PDF — written responses to Part I short-answer questions

---

##  Part I – Short Answer Questions
Conceptual questions covering:
- Traditional programming vs. machine learning, and the AI → ML → Deep Learning relationship
- Roles of input/hidden/output layers, weights, biases, and activation functions
- Perceptrons, and why they solve AND/OR but fail at XOR
- Activation functions (Sigmoid, Tanh, ReLU), the vanishing-gradient problem, and the forward/backward training cycle

*(Full written answers are included in the assignment submission.)*

---

##  Part II – Programming Tasks

### Task 1: Tensor Reshaping & Broadcasting
- Created a random tensor of shape **(4, 6)**
- Found its rank and shape using `tf.rank()` and `.shape`
- Reshaped it to **(2, 3, 4)** and transposed it to **(3, 2, 4)**
- Broadcast a smaller **(1, 4)** tensor and added it to the transposed tensor
- **Output:** Printed rank/shape before and after reshaping, and the final broadcasted shape

### Task 2: Loss Functions & Hyperparameter Tuning
- Defined `y_true` and `y_pred` for a 3-class classification example
- Computed **Mean Squared Error (MSE)** and **Categorical Cross-Entropy (CCE)** losses
- Slightly modified the predictions and recomputed both losses to observe the change
- Plotted a bar chart comparing MSE vs. CCE for original and modified predictions using Matplotlib

### Task 3: Train MNIST with Adam vs. SGD
- Loaded and normalized the **MNIST** handwritten-digit dataset
- Built a simple neural network (Flatten → Dense(128, ReLU) → Dense(10, Softmax))
- Trained two identical models for 5 epochs — one with the **Adam** optimizer, one with **SGD**
- Plotted validation accuracy curves for both optimizers to compare performance

### Task 4: Train & Log to TensorBoard
- Trained the same MNIST model for 5 epochs with a `TensorBoard` callback
- Logs were saved to `logs/fit/<timestamp>/`
- Launched TensorBoard inside Colab (`%tensorboard --logdir logs/fit`) to visualize training vs. validation accuracy and loss

**Reflection questions:**
- *Patterns observed:* Training accuracy increased steadily each epoch; validation accuracy rose more slowly and leveled off.
- *Detecting overfitting in TensorBoard:* A widening gap between training and validation curves — training loss keeps falling while validation loss flattens or rises — signals overfitting.
- *Effect of more epochs:* Training accuracy tends to keep climbing, but validation accuracy can plateau or drop once the model starts overfitting to the training data.

---

##  How to Run
1. Open the `.ipynb` file in [Google Colab](https://colab.research.google.com).
2. Run all cells in order (**Runtime → Run all**).
3. Task 3 and Task 4 take a few minutes since they train on the real MNIST dataset.

---
