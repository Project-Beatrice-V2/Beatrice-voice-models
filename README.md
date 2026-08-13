---
language:
- en
license: mit
tags:
- voice-conversion
- beatrice-v2
- real-time-voice-changer
- audio
- pytorch
- metal
- cuda
pretty_name: Trump Beatrice V2 Voice Model
widget:
- text: "Project Beatrice V2 Real-Time Voice Model"
---

# 🌿 Project Beatrice V2 — Trump Voice Model

[![Website](https://img.shields.io/badge/Website-Visit_Official_Site-7C3AED?style=for-the-badge&logo=vercel&logoColor=white)](https://project-beatrice-v2.github.io/website/)
[![Hugging Face Hub](https://img.shields.io/badge/HuggingFace-SatiricalGuru%2Fbeatrice--voice--models-FFD21E?style=for-the-badge&logo=huggingface&logoColor=black)](https://huggingface.co/SatiricalGuru/beatrice-voice-models)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=for-the-badge)](https://opensource.org/licenses/MIT)

Pre-trained **Trump Voice Model** weights for **[Project Beatrice V2](https://project-beatrice-v2.github.io/website/)** — the open-source real-time neural voice conversion engine (<50ms latency).

---

## 🎙️ Model Files & Downloads (`trump/`)

| File Name | Description | Size | Download Link |
| :--- | :--- | :---: | :---: |
| `beatrice_paraphernalia_data_00005000.toml` | Model Configuration & Checkpoint Manifest (Step 5000) | 568 B | [📥 Download Config](https://huggingface.co/SatiricalGuru/beatrice-voice-models/resolve/main/trump/beatrice_paraphernalia_data_00005000.toml) |
| `waveform_generator.bin` | Neural Vocoder Waveform Generator Weights | 7.9 MB | [📥 Download Vocoder](https://huggingface.co/SatiricalGuru/beatrice-voice-models/resolve/main/trump/waveform_generator.bin) |
| `phone_extractor.bin` | Phoneme Feature Extractor Weights | 7.2 MB | [📥 Download Extractor](https://huggingface.co/SatiricalGuru/beatrice-voice-models/resolve/main/trump/phone_extractor.bin) |
| `pitch_estimator.bin` | Pitch & Frequency Estimator Weights | 3.5 MB | [📥 Download Pitch Model](https://huggingface.co/SatiricalGuru/beatrice-voice-models/resolve/main/trump/pitch_estimator.bin) |
| `embedding_setter.bin` | Speaker Embedding Setter Weights | 264 KB | [📥 Download Embedding Setter](https://huggingface.co/SatiricalGuru/beatrice-voice-models/resolve/main/trump/embedding_setter.bin) |
| `speaker_embeddings.bin` | Target Speaker Vector Embeddings | 234 KB | [📥 Download Speaker Vector](https://huggingface.co/SatiricalGuru/beatrice-voice-models/resolve/main/trump/speaker_embeddings.bin) |

---

## ⚡ How to Load this Model in Beatrice Voice Changer

### 1. Download Model Folder
Clone or download the `trump/` folder directly:

```bash
git lfs install
git clone https://huggingface.co/SatiricalGuru/beatrice-voice-models
```

### 2. Load into Beatrice Voice Changer Client
1. Open **Beatrice Voice Changer** ([macOS Metal/MPS](https://github.com/Project-Beatrice-V2/Beatrice-voicechanger-macos) or [Windows CUDA](https://github.com/Project-Beatrice-V2/Beatrice-voicechanger-windows)).
2. Under **Model / Target Voice**, select **Load Directory / TOML** and point to the `trump/` directory (or select `beatrice_paraphernalia_data_00005000.toml`).
3. Map your **Microphone Input** and **Virtual Audio Output** (BlackHole on macOS, VB-Cable on Windows).
4. Start live real-time voice conversion!

---

## 🛠️ Performance & Requirements

- **Latency**: Sub-50ms glass-to-glass real-time inference.
- **Hardware Acceleration**: Apple Silicon MPS (macOS) / NVIDIA CUDA & DirectML (Windows).
- **Total Model Package**: ~19 MB complete model footprint.

🌐 **[Visit the Official Project Beatrice Website →](https://project-beatrice-v2.github.io/website/)**
