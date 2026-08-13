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
pretty_name: Project Beatrice V2 Pre-Trained Neural Voice Models
widget:
- text: "Project Beatrice V2 Real-Time Voice Models"
---

# 🌿 Project Beatrice V2 — Pre-Trained Voice Models Hub

[![Website](https://img.shields.io/badge/Website-Visit_Official_Site-7C3AED?style=for-the-badge&logo=vercel&logoColor=white)](https://project-beatrice-v2.github.io/website/)
[![Hugging Face](https://img.shields.io/badge/HuggingFace-SatiricalGuru%2Fbeatrice--voice--models-FFD21E?style=for-the-badge&logo=huggingface&logoColor=black)](https://huggingface.co/SatiricalGuru/beatrice-voice-models)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=for-the-badge)](https://opensource.org/licenses/MIT)

Official community repository of pre-trained, high-fidelity neural voice model weights (`.pth` / `.bin`) for **[Project Beatrice V2](https://project-beatrice-v2.github.io/website/)** — the open-source real-time voice conversion ecosystem (<50ms latency).

---

## 🎙️ Available Voice Models

| Model Weight Name | Voice Style / Persona | Gender | Lang | Target Sample Rate | Download Link |
| :--- | :--- | :---: | :---: | :---: | :---: |
| `seraphina_v2.pth` | **Seraphina** (Expressive Podcast / VTuber) | Female | EN-US | 48kHz | [📥 Download (`seraphina_v2.pth`)](https://huggingface.co/SatiricalGuru/beatrice-voice-models/resolve/main/seraphina_v2.pth) |
| `eldritch_scholar.pth` | **Eldritch Scholar** (Deep Resonant RP Narration) | Male | EN-UK | 48kHz | [📥 Download (`eldritch_scholar.pth`)](https://huggingface.co/SatiricalGuru/beatrice-voice-models/resolve/main/eldritch_scholar.pth) |
| `harmony_vocal.pth` | **Harmony Vocal** (Acoustic Singing Voice) | Neutral | Multi | 48kHz | [📥 Download (`harmony_vocal.pth`)](https://huggingface.co/SatiricalGuru/beatrice-voice-models/resolve/main/harmony_vocal.pth) |

---

## ⚡ Quick Usage Guide

### 1. Download Model Weights
Click any download link above or clone this Hugging Face repository using `git-lfs`:

```bash
# Clone model repository via Git LFS
git lfs install
git clone https://huggingface.co/SatiricalGuru/beatrice-voice-models
```

### 2. Load into Beatrice Voice Changer
1. Launch **Project Beatrice Voice Changer** ([macOS Metal/MPS](https://github.com/Project-Beatrice-V2/Beatrice-voicechanger-macos) or [Windows CUDA](https://github.com/Project-Beatrice-V2/Beatrice-voicechanger-windows)).
2. Open the **Model Selector** dropdown and click **Load Local `.pth` Model**.
3. Select your downloaded model file (e.g. `seraphina_v2.pth`).
4. Select your **Microphone Input** and **Virtual Audio Cable Output** (BlackHole on macOS, VB-Cable on Windows).
5. Start live real-time voice conversion!

---

## 🛠️ Hardware & Latency Specifications

- **Latency Claim**: Sub-50ms glass-to-glass audio latency.
- **macOS Hardware**: Apple Silicon M1 / M2 / M3 / M4 Metal Performance Shaders (MPS).
- **Windows Hardware**: NVIDIA RTX CUDA 12+ or DirectML compatible GPUs.
- **Model Checkpoint Size**: ~40 MB per voice checkpoint.

---

## 📜 Public Repository Settings & License

This Hugging Face model repository is **publicly accessible** under the **MIT License**. You are free to download, mirror, fine-tune, or use these models in personal, streaming, and commercial applications.

🌐 **[Visit the Official Project Beatrice Website →](https://project-beatrice-v2.github.io/website/)**
