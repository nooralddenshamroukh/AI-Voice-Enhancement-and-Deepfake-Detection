
---

## 🔹 `Voice_Detection/README.md`

```markdown
# 🕵️ AI Voice Detection

## 📌 Overview
This module detects whether a voice sample is **real (human)** or **fake (AI-generated deepfake)**.  
It uses **Convolutional Neural Networks (CNNs)** trained on Mel Spectrograms.

---

## 🚀 Features
- Converts audio → **Mel Spectrogram**.
- **3-layer CNN** with BatchNorm & Dropout.
- Supports variable-length inputs (adaptive pooling).
- Outputs prediction + confidence score.

---

## ⚙️ Tools & Libraries
- Python 3.10
- PyTorch
- Librosa
- TorchAudio
- Matplotlib (for spectrograms)

---

## 📂 Project Structure
Voice_Detection/
│
├── utils.py # Data preparation
├── model.py # CNN model definition
├── train.py # Training script
├── predict.py # Inference script
├── data/ # Training dataset (not included)
├── checkpoints/ # Saved models
└── examples/ # Example audio files

---

## ▶️ How to Run
### Training
```bash
python train.py --data data/ --epochs 20 --save checkpoints/

Inference
python predict.py --input examples/test.wav --model checkpoints/best_model.pth

Output:
Prediction: Fake (AI-generated)
Confidence: 92%

📊 Evaluation

Training Data: Real vs Fake (AI-generated) voices

Metrics: Accuracy, F1-Score

Achieved strong performance on benchmark datasets.

⚖️ License Note

The detection model is implemented by our team, but it builds on CNN architectures widely used in research.
Datasets and benchmarks used belong to their original authors and are not redistributed here.
