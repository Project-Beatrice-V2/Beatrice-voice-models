<div align="center">

<img src="docs/media/app-icon.png" alt="Beatrice app icon" width="128" />

# Beatrice Voice Models

**Ready-made voices for the Beatrice voice changer.**<br/>
Download a ZIP, choose **Upload Custom Model**, and talk in a new voice, live and on your own computer.

[![Download trump.zip](https://img.shields.io/badge/Download-trump.zip-000000?style=for-the-badge&logo=github&logoColor=white&labelColor=000000)](https://github.com/Project-Beatrice-V2/Beatrice-voice-models/raw/main/downloads/trump.zip)
[![Website](https://img.shields.io/badge/Website-project--beatrice.vercel.app-7c8cff?style=for-the-badge&labelColor=000000)](https://project-beatrice.vercel.app)
[![Hugging Face mirror](https://img.shields.io/badge/Hugging%20Face-mirror-000000?style=for-the-badge&logo=huggingface&logoColor=FFD21E&labelColor=000000)](https://huggingface.co/SatiricalGuru/beatrice-voice-models)
[![Stars across all Beatrice repos](https://img.shields.io/endpoint?url=https%3A%2F%2Fproject-beatrice.vercel.app%2Fapi%2Fstars%3Fformat%3Dshields&style=for-the-badge)](https://github.com/Project-Beatrice-V2)

![Models](https://img.shields.io/badge/models-1-a887dc?style=flat-square&labelColor=000000)
![Format](https://img.shields.io/badge/format-2.0.0--rc.0-a887dc?style=flat-square&labelColor=000000)
![Latency](https://img.shields.io/badge/latency-~10%20ms-3dffa8?style=flat-square&labelColor=000000)
![License](https://img.shields.io/badge/license-MIT-a1a1aa?style=flat-square&labelColor=000000)

[Models](#-models) · [Website](https://project-beatrice.vercel.app) · [Beatrice for Mac](https://github.com/satiricalguru/Beatrice-voicechanger-mac) · [Beatrice for Windows](https://github.com/satiricalguru/Beatrice-voicechanger-windows) · [Train your own](https://github.com/Project-Beatrice-V2/Beatrice-colab) · [Report a problem](https://github.com/Project-Beatrice-V2/Beatrice-voice-models/issues/new)

</div>

---

## ✨ Why use these

- 📦 **One file per voice.** Each model has a ready ZIP for **Upload Custom Model**, so there's nothing to unpack or rename.
- 🎙️ **Real-time and on-device.** The Beatrice voice changer converts your voice live with about 10 ms of latency, and your audio never leaves your computer.
- ✅ **Checked before it's listed.** Every model here loads in the Beatrice 2.0.0-rc.0 engine that the voice changer uses.
- 🗃️ **Plain files too.** The raw model files are in `voice_models/<name>/` if you'd rather use them yourself.

## 🎭 Models

| Model | Voice | Training steps | Size | Download | Avatar · sample |
|:--|:--|:--:|:--:|:--|:--|
| [`trump`](voice_models/trump) | Donald Trump impression | 5,000 | 19.6 MB (18.1 MB ZIP) | [trump.zip](https://github.com/Project-Beatrice-V2/Beatrice-voice-models/raw/main/downloads/trump.zip) | Placeholder avatar, no sample yet |

<sub>The model's manifest marks it as **personal use only** and an early checkpoint, so it hasn't been compared with longer training. Please read [Responsible use](#-responsible-use) before using it.</sub>

## 🚀 Use a model in Beatrice

1. Install Beatrice for [Mac](https://github.com/satiricalguru/Beatrice-voicechanger-mac/releases/latest) or [Windows](https://github.com/satiricalguru/Beatrice-voicechanger-windows/releases/latest).
2. Download the model's ZIP, for example [trump.zip](https://github.com/Project-Beatrice-V2/Beatrice-voice-models/raw/main/downloads/trump.zip). Don't unzip it.
3. In Beatrice, open the model menu and choose **Upload Custom Model**.
4. Pick the ZIP, type a name (for example *Donald Trump*), choose a category and click **Import**. Beatrice looks up a portrait for the name and switches to the new voice.
5. Press the power button so it says **LIVE**, and talk. In Discord, Zoom or OBS, choose Beatrice's virtual microphone (**BlackHole 2ch** on Mac).

> [!NOTE]
> Upload Custom Model uses the `.bin` files from the ZIP and writes its own `model.toml` from the name you type, so the name and category are yours to choose.

<details>
<summary><b>Using the raw files instead</b></summary>
<br/>

`voice_models/trump/` is a standard Beatrice 2.0.0-rc.0 *paraphernalia* folder, the format that the official [Beatrice VST](https://prj-beatrice.com) and [VCClient](https://github.com/w-okada/voice-changer) read. To get it with Git:

```bash
git clone https://github.com/Project-Beatrice-V2/Beatrice-voice-models.git
```

| File | What it is | Size |
|:--|:--|--:|
| `beatrice_paraphernalia_data_00005000.toml` | Model manifest (name, voice, average pitch) | 568 B |
| `phone_extractor.bin` | Speech content features | 7.2 MB |
| `pitch_estimator.bin` | Pitch tracking | 3.5 MB |
| `waveform_generator.bin` | Generates the target voice | 7.9 MB |
| `embedding_setter.bin` | Speaker embedding setup | 264 KB |
| `speaker_embeddings.bin` | The target speaker (1 voice) | 234 KB |
| `noimage.png` | Placeholder portrait from the trainer | 389 KB |

SHA-256 hashes are in [`voice_models/trump/README.md`](voice_models/trump/README.md). They match the [Hugging Face mirror](https://huggingface.co/SatiricalGuru/beatrice-voice-models).
</details>

## 🧠 Train your own

| | |
|:--|:--|
| ☁️ [Colab & Kaggle notebooks](https://github.com/Project-Beatrice-V2/Beatrice-colab) | Train for free on a cloud GPU. [Open in Colab](https://colab.research.google.com/github/Project-Beatrice-V2/Beatrice-colab/blob/main/BeatriceV2_Trainer_Notebook_Colab.ipynb) |
| 🍎 [Trainer for Mac](https://github.com/Project-Beatrice-V2/Beatrice-trainer-macos) · 🪟 [Windows](https://github.com/Project-Beatrice-V2/Beatrice-trainer-windows) | Train on your own computer |
| 📂 [Dataset Web UI](https://github.com/Project-Beatrice-V2/Beatrice-dataset-webui-macos) | Prepare recordings for training |

The notebooks export `beatrice_paraphernalia_<voice>_<step>.zip`, which imports in Beatrice the same way as the ZIPs here.

## 🤝 Contribute a model

1. **Train it** with the Beatrice trainer 2.0.0-rc.0, using the notebooks or the Mac and Windows trainers above.
2. **Add the folder** `voice_models/<name>/` with the five `.bin` files, the `beatrice_paraphernalia_*.toml` and, if you like, a square PNG portrait you have the rights to.
3. **Add the ZIP** `downloads/<name>.zip`, containing exactly **one** model folder. Beatrice collects the `.bin` files from anywhere in the ZIP and keeps the last copy of each, so two models in one ZIP get mixed up. If a ZIP is over 20 MB, attach it to a [GitHub release](https://github.com/Project-Beatrice-V2/Beatrice-voice-models/releases) instead of committing it.
4. **Check it imports**: Upload Custom Model, go LIVE and talk.
5. **Add a row** to the [Models](#-models) table with the training steps, size, the dataset you used and its licence.
6. **Open a pull request.** Only share voices you have the right to share: your own, a speaker who agreed, or a dataset whose licence allows it. No private individuals.

> [!WARNING]
> Commit the real model files, not Git LFS pointers. Each `.bin` should be hundreds of KB to several MB. A tiny text file starting with `version https://git-lfs` won't load.

## 🧭 Responsible use

- The `trump` model imitates a real, living public figure. It isn't affiliated with or endorsed by him. Its manifest says *personal/private use only, not for public redistribution*.
- Use voice models for clearly labelled fun, parody or experiments. Don't use them to impersonate someone, deceive or defraud people, harass anyone, spread political misinformation or for commercial work.
- Laws on voice and likeness differ by country, and many platforms require you to disclose synthetic voices. Following them is up to you.

## 🌐 The Beatrice family

| | |
|:--|:--|
| 🍎 [Beatrice for Mac](https://github.com/satiricalguru/Beatrice-voicechanger-mac) | The real-time voice changer for Apple Silicon Macs |
| 🪟 [Beatrice for Windows](https://github.com/satiricalguru/Beatrice-voicechanger-windows) | The same app for Windows 10 and 11 |
| 🌍 [Website](https://project-beatrice.vercel.app) | Downloads, guides and voice samples |
| 🧠 [Trainer for Mac](https://github.com/Project-Beatrice-V2/Beatrice-trainer-macos) · [Colab](https://github.com/Project-Beatrice-V2/Beatrice-colab) | Train your own voice model |
| 📂 [Dataset Web UI](https://github.com/Project-Beatrice-V2/Beatrice-dataset-webui-macos) | Prepare recordings for training |

## 🙏 Credits

- **Beatrice engine and trainer** by [Project Beatrice](https://prj-beatrice.com) ([beatrice-vst](https://github.com/prj-beatrice/beatrice-vst), [beatrice-trainer](https://huggingface.co/fierce-cats/beatrice-trainer))
- Models trained and shared by the [Project Beatrice V2](https://github.com/Project-Beatrice-V2) community

## 📜 License

The repository's code and documentation are **MIT** licensed, © 2026 Project Beatrice V2 Contributors & SatiricalGuru (see [LICENSE](LICENSE)). The licence covers these files only: it gives no rights to anyone's voice or likeness, and each model's own terms (such as the `trump` manifest's personal-use note) still apply.

<div align="center">
<br/>

**Made a voice others would enjoy? Open a pull request, and ⭐ star the repo.**

<a href="#beatrice-voice-models">Back to top ↑</a>

</div>
