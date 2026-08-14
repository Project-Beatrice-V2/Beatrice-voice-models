# 🎙️ Trump Neural Voice Model (Step 5000)

Pre-trained weights for the Donald Trump neural voice model, trained for the **[Project Beatrice V2](https://github.com/Project-Beatrice-V2)** real-time voice conversion engine.

## 📦 Model Files

- `beatrice_paraphernalia_data_00005000.toml`: Configuration manifest and hyperparameter definitions.
- `waveform_generator.bin`: Neural vocoder generator weights (7.9 MB).
- `phone_extractor.bin`: Phoneme feature extractor weights (7.2 MB).
- `pitch_estimator.bin`: Pitch and frequency estimator weights (3.5 MB).
- `embedding_setter.bin`: Speaker embedding setter weights (264 KB).
- `speaker_embeddings.bin`: Target speaker vector embeddings (234 KB).
- `noimage.png`: Target model display avatar.

## ⚡ How to Load in Beatrice Voice Changer

1. Open **Beatrice Voice Changer** on macOS (Metal/MPS) or Windows (CUDA/DirectML).
2. Under **Model / Target Voice**, select **Load Directory** or choose `beatrice_paraphernalia_data_00005000.toml`.
3. Set your microphone as input and virtual cable (BlackHole / VB-Cable) as output.
4. Begin real-time voice conversion!
