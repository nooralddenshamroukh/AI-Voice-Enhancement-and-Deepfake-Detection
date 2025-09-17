⚖️ License Note

This project uses Demucs and Whisper, created by their original authors.
They are included here only for academic purposes. Redistribution or commercial use must follow their original licenses.
---

## 🔹 `Voice_Converter/README.md`

```markdown
# 🎙️ AI Voice Converter (Deepfake Voice)

## 📌 Overview
This module converts a speaker’s voice into another **target speaker’s voice** using AI models.  
It is based on **WavLM, RMVPE, and HiFi-GAN**.

---

## 🚀 Features
- Preprocessing: silence trimming, normalization, chunking (6s clips).
- **WavLM** → extracts speech content & features.
- **RMVPE** → extracts pitch (F0).
- **HiFi-GAN Vocoder** → generates natural speech in target voice.
- Runs in **Google Colab** for easy testing.

---

## ⚙️ Tools & Libraries
- Python 3.10
- [WavLM (Microsoft)](https://huggingface.co/microsoft/wavlm-base)
- [RMVPE](https://github.com/DreamVoice/rmvpe)
- [HiFi-GAN](https://github.com/jik876/hifi-gan)
- Librosa, SoundFile, TorchAudio
- FAISS (for similarity search)

---

## 📂 Project Structure
Voice_Converter/
│
├── prepare_data_svc.py # Data preprocessing
├── train_svc.py # Model training
├── inference_svc.py # Voice conversion (inference)
├── config_svc.py # Centralized configuration
├── models/ # Pretrained weights (not included)
├── input/ # Source audio
├── output/ # Converted audio
└── voice_converter_colab.ipynb # Google Colab demo

---

## ▶️ How to Run
1. Place your input audio in `input/`.
2. Run inference:
   ```bash
   python inference_svc.py --input input/source.wav --output output/converted.wav
3. Converted audio will be available in output/.
Colab Option:
Open voice_converter_colab.ipynb → upload audio → run all cells → download converted file.

📊 Example

Input: noor_voice.wav

Target: Trained model (e.g., speaker X)

Output: noor_as_speakerX.wav
