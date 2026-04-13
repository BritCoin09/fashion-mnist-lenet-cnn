# Fashion MNIST Classification with a LeNet‑Style Convolutional Neural Network

This project builds and trains a convolutional neural network (CNN) to classify images from the Fashion‑MNIST dataset. The model is based on a modernized version of the classic **LeNet‑5** architecture, using **ReLU activations** and the **Adam optimizer** for improved training stability and performance.

The goal of the project was to achieve at least **87% accuracy** on the test set.  
The final model reached **88.63%**, exceeding the requirement.

---

## 📦 Dataset

**Fashion‑MNIST** contains 70,000 grayscale images (28×28) across 10 clothing categories:

- T‑shirt/top  
- Trouser  
- Pullover  
- Dress  
- Coat  
- Sandal  
- Shirt  
- Sneaker  
- Bag  
- Ankle boot  

Images were normalized to `[0, 1]` and reshaped to `(28, 28, 1)` for CNN compatibility.

---

## 🧠 Model Architecture

This project uses a lightweight CNN inspired by **LeNet‑5**, adapted for Fashion‑MNIST:

- **Conv2D (6 filters, 5×5, ReLU, same padding)**  
- **AvgPool2D**
- **Conv2D (16 filters, 5×5, ReLU)**
- **AvgPool2D**
- **Flatten**
- **Dense (120 units, ReLU)**
- **Dense (84 units, ReLU)**
- **Dense (10 units, softmax)**

Optimizer: **Adam**  
Loss: **Sparse Categorical Crossentropy**  
Metrics: **Accuracy**

This architecture is intentionally simple and efficient, making it ideal for small grayscale images.

---

## 🏋️ Training Setup

- **Epochs:** up to 15  
- **Batch size:** 128  
- **Validation split:** 20%  
- **EarlyStopping:**  
  - `monitor='val_loss'`  
  - `patience=3`  
  - `restore_best_weights=True`

Early stopping ensured the model did not overfit and restored the best-performing weights.

---

## 📈 Results

| Metric | Score |
|--------|--------|
| **Best Validation Accuracy** | 0.8892 |
| **Final Test Accuracy** | **0.8863** |

The model demonstrated stable learning and strong generalization.

---

## 📝 Conclusion

This project shows that a compact LeNet‑style CNN can achieve high accuracy on Fashion‑MNIST with minimal tuning. The model exceeded the required performance threshold and remained stable throughout training.

**Future improvements could include:**

- Adding dropout for regularization  
- Trying data augmentation  
- Experimenting with deeper architectures (e.g., small ResNet or VGG variants)

---

## 📁 Files in This Repository

- [**fashion_mnist_lenet.ipynb**](https://github.com/BritCoin09/fashion-mnist-lenet-cnn/blob/main/fashion_mnist_lenet.ipynb) — full notebook with preprocessing, model creation, training, and evaluation

- [**README.md**](https://github.com/BritCoin09/fashion-mnist-lenet-cnn/blob/main/README.md)
 — project overview and documentation  

---

## 🚀 How to Run

1. Open the notebook in Google Colab or Jupyter Notebook  
2. Install TensorFlow if needed  
3. Run all cells — the notebook handles data loading, training, and evaluation automatically

---

## 💡 Author

Project completed by **Britny Chambers** as part of a computer vision module.  
