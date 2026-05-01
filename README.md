# 🔢 MNIST Digit Predictor

A browser-based web app that recognizes handwritten digits (0–9) using four deep learning models — running **directly in the browser**, no server or backend required.

🌐 **Live Demo:** [mnist-predictor-with-model-selection.netlify.app](https://mnist-predictor-with-model-selection.netlify.app/)

---

## ✨ Features

- ✏️ **Draw mode** — Draw digits directly on the canvas using mouse or touch
- 📁 **Upload mode** — Upload any handwritten digit image
- 🤖 **4 trained models** — Compare predictions from two models side by side
- 📊 **Probability bars** — See confidence scores for all 10 digits (0–9)
- ⚡ **No backend needed** — Everything runs in the browser via ONNX Runtime Web

---

## 🧠 Models

| Model | Architecture | Test Accuracy |
|-------|-------------|---------------|
| **MyCNN** | Custom CNN | ~99.2% |
| **LeNet** | Classic LeNet-5 | ~98.8% |
| **ResNet** | ResNet-18 (modified) | ~99.3% |
| **MobileNet** | MobileNetV2 (modified) | ~99.1% |

All models were trained on the [MNIST dataset](https://www.kaggle.com/competitions/mnist-dataset-number-classification) — 60,000 training images of handwritten digits.

---

## 🗂️ Project Structuremnist-predictor/
├── index.html            # Complete web app (HTML + CSS + JS in one file)

├── mycnn_final.onnx      # Custom CNN model weights

├── lenet_final.onnx      # LeNet-5 model weights

├── resnet_final.onnx     # ResNet-18 model weights

├── mobilenet_final.onnx  # MobileNetV2 model weights

└── README.md

---

## 🚀 Run Locally

```bash
git clone https://github.com/AMANOT-ULLAH/mnist-predictor-with-live-model-selection.git
cd mnist-predictor-with-live-model-selection
python3 -m http.server 8080
```

Open in browser: `http://localhost:8080`

> ⚠️ You must use a local server. Opening `index.html` directly will not load the ONNX models due to browser security restrictions.

---

## 🛠️ Tech Stack

| Layer | Technology |
|-------|-----------|
| Frontend | HTML, CSS, Vanilla JavaScript |
| ML Inference | ONNX Runtime Web |
| Model Training | PyTorch (Google Colab) |
| Deployment | Netlify (static hosting) |

---

## 📓 Training

Models were trained in Google Colab using PyTorch on the MNIST dataset, then exported to `.onnx` format for browser-based inference using `torch.onnx.export`.

Training notebook: `MNIST_basic_basic_play.ipynb`

---

## 👤 Author

**AMANOT-ULLAH**
GitHub: [github.com/AMANOT-ULLAH](https://github.com/AMANOT-ULLAH)

---

## 📄 License

MIT License — Copyright (c) 2026 AMANOT-ULLAH

Free to use and modify. Please keep the author credit if you reuse this code.
