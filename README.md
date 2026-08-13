---
license: other
tags:
  - beatrice
  - voice-conversion
---

# Beatrice Voice Models (Private)

Personal collection of Beatrice v2 voice conversion checkpoints.** Voices are trained on real
individuals' audio; treat accordingly.

## Structure

Each voice lives in its own folder, containing the Beatrice model files
(`.bin`) and manifest (`.toml`) for that voice:

```
beatrice-voice-models/
├── trump/
│   ├── beatrice_paraphernalia_data_00005000.toml
│   ├── phone_extractor.bin
│   ├── pitch_estimator.bin
│   ├── speaker_embeddings.bin
│   ├── embedding_setter.bin
│   ├── waveform_generator.bin
│   ├── noimage.png
│   └── README.md
└── <next-voice>/
    └── ...
```

## Voices in this repo

| Folder | Checkpoint | Notes |
|---|---|---|
| `trump/` | step 5000 | Early-stage, see folder README |

## Adding a new voice

1. Create a new top-level folder named after the voice.
2. Drop in the Beatrice model files + `.toml` manifest for that voice.
3. Add a short `README.md` inside the folder (checkpoint step, pitch, notes).
4. Add a row to the table above.
5. Upload with: `hf upload SatiricalGuru/beatrice-voice-models <folder> <folder>`
