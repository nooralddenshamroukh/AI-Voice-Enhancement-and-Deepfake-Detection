# 🎙️ AI Voice Enhancement & Deepfake Detection

## 📌 Overview
This repository contains our **graduation project** (Hashemite University, 2025), which integrates three major modules for modern speech processing:

1. **Noise Cancellation** – Enhances audio quality by removing background noise while preserving human speech.
2. **AI Voice Converter (Deepfake Voice)** – Transforms a speaker’s voice into another target speaker using AI-based models (WavLM, RMVPE, HiFi-GAN).
3. **AI Voice Detection** – Identifies whether an audio sample is a **real human voice** or an **AI-generated deepfake**.

These modules address key challenges in voice communication: clarity, privacy, creativity, and security.

---

## 📂 Project Structure
AI-Voice-Enhancement-and-Deepfake-Detection/
│
├── Noise_Cancellation/ # Code and outputs for noise cancellation
├── Voice_Converter/ # Code and outputs for AI-based voice conversion
├── Voice_Detection/ # Code and outputs for AI voice detection
│
├── README.md # This file
├── Presentation.pptx # Project presentation slides
└── Report.pdf # Full project documentation

---

## 🚀 Features

### 🔹 Noise Cancellation
- Based on **Demucs**, **Whisper**, and DSP techniques (bandpass filtering, silence detection).
- Runs on **Google Colab** with GPU acceleration.
- Outputs clean, enhanced human speech from noisy recordings.

### 🔹 AI Voice Converter
- Preprocessing: silence removal, segmentation, normalization.
- **Feature extraction** with:
  - **WavLM** → captures semantic & acoustic voice features.
  - **RMVPE** → extracts pitch (F0).
- **HiFi-GAN Vocoder** for natural-sounding speech synthesis.
- Converts source speech into the target speaker’s voice.

### 🔹 AI Voice Detection
- Converts input audio into **Mel Spectrograms**.
- **3-layer CNN classifier** with batch normalization & dropout.
- Detects whether a voice is **Real (Human)** or **Fake (AI-generated)**.
- Provides prediction + confidence scores.

---

## 🛠️ Tech Stack
- **Python 3.10**
- **PyTorch**
- **Librosa, Soundfile, TorchAudio**
- **WavLM (Microsoft)**
- **RMVPE (Pitch Estimation)**
- **HiFi-GAN (Speech Vocoder)**
- **Demucs (Vocal Separation)**
- **Whisper (Speech Recognition)**
- **Google Colab** (GPU acceleration)

---

## 📊 Evaluation
- **Noise Reduction** → Improved **SNR** & clarity.
- **Voice Conversion** → Produces natural, human-like converted voices.
- **Voice Detection** → CNN model achieves strong performance on detecting synthetic voices.

Metrics used:
- PESQ (Perceptual Evaluation of Speech Quality)  
- MOS (Mean Opinion Score)  
- F1 Score for detection models  

---

## ⚖️ License & Attribution
This repository contains **educational and research work**.  

- Some components rely on **external pre-trained models and libraries** (e.g., **WavLM**, **RMVPE**, **HiFi-GAN**, **Demucs**, **Whisper**) which are **developed and owned by their original authors**.  
- These models are **not created by us** and are included here **only for academic demonstration purposes**.  
- Redistribution or commercial use of those models is **not permitted** — please refer to their original licenses.  

If you use or extend this project, please **cite both our work and the original authors** of the referenced models.

---

## 📌 Contributors
- Noor Aldden Shamroukh (1932591)  
- Osamah Muneer Radwan (2034078)  
- Abdel Rahman Zaid Khamees (2145800)  
- Toleen Osama Abu Ali (2034553)  

**Advisor:** Dr. Enshirah Ibrahim Abdel H. Altarawneh  
**Institution:** Hashemite University – Computer Engineering Department (2024–2025)

---

## 📜 How to Run
Each module (`Noise_Cancellation`, `Voice_Converter`, `Voice_Detection`) contains its own **README** with usage instructions.  
Most experiments are designed to run on **Google Colab** with GPU acceleration.  

---

## 📽️ Project Materials
- 📑 [GPT2_documentation.pdf](./GPT2_documentation.pdf) – Full documentation  
- 📊 [GPT2_Presentation (FINAL).pptx](./GPT2_Presentation (FINAL).pptx) – Project slides
