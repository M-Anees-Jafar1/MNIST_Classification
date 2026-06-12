# 🎯 MNIST Handwritten Digit Classification (PyTorch CNN)

In this project, I built a custom **Convolutional Neural Network (CNN)** using **PyTorch** to classify handwritten digits (from 0 to 9). I also included a real-world image testing pipeline so we can upload our own handwritten numbers and see the model predict them live.

## 🚀 Main Features
- **Custom CNN Model:** Designed the neural network layers (`Conv2d`, `MaxPool2d`, `Linear`) manually using PyTorch.
- **Real Image Testing:** Used OpenCV to process custom user images by automatically resizing them to $28 \times 28$ pixels, converting them to grayscale, and inverting colors.
- **Model Save/Load:** Implemented a save pipeline using `.pth` files so we don't have to train the model from scratch every time.
- **High Accuracy:** Achieved **97%+ Accuracy** on completely unseen testing data.

---

## 📁 Project Structure
- `MNIST_Classification.ipynb` -> A single, self-contained notebook containing data loaders, model architecture, training loop, and the prediction pipeline.
- `README.md` -> Project documentation and guide.

---

## 🏗️ Model Architecture (Data Flow)

The model processes the input image through the following steps:

1. **Input:** Grayscale Image tensor ($28 \times 28$ pixels).
2. **Conv Layer 1:** Extracts basic features like edges and lines from the digit.
3. **Pooling:** Reduces the image size to make calculations faster.
4. **Conv Layer 2:** Extracts deeper patterns and shapes.
5. **Flatten:** Reshapes the 2D image matrix into a 1D vector (straight line).
6. **Fully Connected Layers:** Makes the final decision on which digit (0-9) is present in the image.

---

## ⚙️ Hyperparameters & Settings
- **Dataset:** MNIST (60,000 training images, 10,000 testing images)
- **Loss Function:** `CrossEntropyLoss` (Standard for multi-class classification)
- **Optimizer:** Adam Optimizer (`lr=0.001` for stable training)
- **Epochs:** 3 Rounds
- **Batch Size:** 64

---

## 🏃 How to Run & Replicate

1. Clone or download this repository.
2. Open the `.ipynb` notebook file in Google Colab.
3. Run the cells sequentially:
   - First, the MNIST dataset will download.
   - Next, the model will train for 3 epochs and save the weights.
   - Finally, use the prediction cell to upload your own local `.jpg` or `.png` handwritten image to test the model.

---

## 🧠 Key Takeaways & Learnings
- Learned how to manage **Tensor Dimensions** and track shape changes across neural network layers.
- Mastered the core steps of a PyTorch training loop: `zero_grad()`, `backward()`, and `optimizer.step()`.
- Learned how to bridge the gap between clean training datasets and noisy, real-world user images using computer vision preprocessing.

---
💡 *Built as part of my practical portfolio for Deep Learning and Computer Vision.*
