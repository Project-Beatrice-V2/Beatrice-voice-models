<div align="center">

<img src="assets/beatrice-logo.png" alt="Project Beatrice V2 Logo" width="160" />

# Project Beatrice V2 — Neural Voice Models

**Official repository of pre-trained, high-fidelity neural voice models for the Beatrice real-time voice conversion engine.**

[![Website](https://img.shields.io/badge/Website-Project_Beatrice_V2-7C3AED?style=for-the-badge&logo=vercel&logoColor=white)](https://project-beatrice-v2.github.io/website/)
[![Hugging Face Hub](https://img.shields.io/badge/HuggingFace-SatiricalGuru%2Fbeatrice--voice--models-FFD21E?style=for-the-badge&logo=huggingface&logoColor=black)](https://huggingface.co/SatiricalGuru/beatrice-voice-models)
[![GitHub Org](https://img.shields.io/badge/GitHub-Project--Beatrice--V2-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/Project-Beatrice-V2)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=for-the-badge)](LICENSE)
[![Latency](https://img.shields.io/badge/Latency-%3C50ms_Real--Time-22C55E?style=for-the-badge)](https://github.com/Project-Beatrice-V2/Beatrice-voicechanger-macos)

</div>

---

## 📂 Repository Structure

```
beatrice-voice-models/
├── assets/
│   └── beatrice-logo.png              # Official Project Beatrice V2 Logo
├── voice_models/
│   └── trump/                         # Trump Neural Voice Model (Step 5000)
│       ├── beatrice_paraphernalia_data_00005000.toml  # Model Manifest & Checkpoint Config
│       ├── waveform_generator.bin     # Neural Vocoder Waveform Generator (7.9 MB)
│       ├── phone_extractor.bin        # Phoneme Feature Extractor (7.2 MB)
│       ├── pitch_estimator.bin        # Pitch & Frequency Estimator (3.5 MB)
│       ├── embedding_setter.bin       # Speaker Embedding Setter (264 KB)
│       ├── speaker_embeddings.bin     # Target Speaker Vector Embeddings (234 KB)
│       ├── noimage.png                # Model Avatar Icon (388 KB)
│       └── README.md                  # Model-Specific Documentation
├── LICENSE                            # MIT Open-Source License
└── README.md                          # Repository Documentation & Usage Guide
```

---

## 🎙️ Available Voice Models (`voice_models/`)

### 1. Donald Trump Neural Voice (`voice_models/trump/`)

High-fidelity neural voice model trained on clean speech recordings, fully convergent at **5,000 steps** for ultra-low latency real-time voice conversion.

| File Name | Description | Size | Direct Download |
| :--- | :--- | :---: | :---: |
| `beatrice_paraphernalia_data_00005000.toml` | Model Configuration & Checkpoint Manifest | 568 B | [📥 Download Config](https://raw.githubusercontent.com/Project-Beatrice-V2/beatrice-voice-models/main/voice_models/trump/beatrice_paraphernalia_data_00005000.toml) |
| `waveform_generator.bin` | Neural Vocoder Waveform Generator Weights | 7.9 MB | [📥 Download Vocoder](https://raw.githubusercontent.com/Project-Beatrice-V2/beatrice-voice-models/main/voice_models/trump/waveform_generator.bin) |
| `phone_extractor.bin` | Phoneme Feature Extractor Weights | 7.2 MB | [📥 Download Extractor](https://raw.githubusercontent.com/Project-Beatrice-V2/beatrice-voice-models/main/voice_models/trump/phone_extractor.bin) |
| `pitch_estimator.bin` | Pitch & Frequency Estimator Weights | 3.5 MB | [📥 Download Pitch Model](https://raw.githubusercontent.com/Project-Beatrice-V2/beatrice-voice-models/main/voice_models/trump/pitch_estimator.bin) |
| `embedding_setter.bin` | Speaker Embedding Setter Weights | 264 KB | [📥 Download Embedding Setter](https://raw.githubusercontent.com/Project-Beatrice-V2/beatrice-voice-models/main/voice_models/trump/embedding_setter.bin) |
| `speaker_embeddings.bin` | Target Speaker Vector Embeddings | 234 KB | [📥 Download Speaker Vector](https://raw.githubusercontent.com/Project-Beatrice-V2/beatrice-voice-models/main/voice_models/trump/speaker_embeddings.bin) |

---

## ⚡ How to Load Voice Models into Beatrice Voice Changer

### Method 1: Clone the Entire Models Repository
```bash
git clone https://github.com/Project-Beatrice-V2/beatrice-voice-models.git
```

### Method 2: Load into Beatrice Voice Changer App
1. Open **Beatrice Voice Changer** on [macOS (Metal/MPS)](https://github.com/Project-Beatrice-V2/Beatrice-voicechanger-macos) or [Windows (CUDA)](https://github.com/Project-Beatrice-V2/Beatrice-voicechanger-windows).
2. Under **Model / Target Voice**, click **Load Directory** or select the manifest file:
   ```
   voice_models/trump/beatrice_paraphernalia_data_00005000.toml
   ```
3. Set your **Microphone Input** and **Virtual Audio Output** (`BlackHole 2ch` on macOS, `VB-Audio Virtual Cable` on Windows).
4. In Discord, OBS Studio, or game settings, select the virtual driver as your microphone to start streaming with transformed speech!

---

## 🛠️ Performance & Technical Specifications

- **Latency**: Glass-to-glass real-time inference latency `<50ms`.
- **Audio Sample Rate**: Native 48kHz high-fidelity output.
- **Hardware Acceleration**:
  - **macOS**: Apple Silicon Metal Performance Shaders (`MPS`).
  - **Windows**: NVIDIA `CUDA` & DirectX 12 `DirectML`.
- **Model Package Size**: ~19.5 MB total footprint per voice model.
- **Hugging Face Mirror**: [SatiricalGuru/beatrice-voice-models](https://huggingface.co/SatiricalGuru/beatrice-voice-models)

---

## 📜 License

This project is licensed under the [MIT License](LICENSE) — free for both personal and commercial use.

---

<div align="center">
  <sub>Maintained by the <strong>Project Beatrice V2</strong> Open-Source Community.</sub>
</div>
