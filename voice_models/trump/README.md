# trump

A Donald Trump impression for the [Beatrice voice changer](https://project-beatrice.vercel.app), trained for **5,000 steps** with the Beatrice trainer 2.0.0-rc.0. It has one voice, with an average pitch of 50.875 (MIDI note number).

**Import it:** download [trump.zip](https://github.com/Project-Beatrice-V2/Beatrice-voice-models/raw/main/downloads/trump.zip). In Beatrice, open the model menu, choose **Upload Custom Model**, pick the ZIP, name it, choose a category and click **Import**.

## Files

| File | Bytes | SHA-256 |
|:--|--:|:--|
| `beatrice_paraphernalia_data_00005000.toml` | 568 | |
| `phone_extractor.bin` | 7,244,608 | `6802d2b5fb6d36c7bdac5589f0a3b0911a2f1967307ff6e98ce16cb7fe3915b7` |
| `pitch_estimator.bin` | 3,499,136 | `fcb47ba5250362b8c37d0ce64dee8ba074d4c43d14c524eb3e48688c282d01dc` |
| `waveform_generator.bin` | 7,921,664 | `90f58e06ad7e82ff9866380ea545667408652cfc29ce193501fa9eaf3aa197c7` |
| `embedding_setter.bin` | 264,192 | `0856f6e13924b1c307ebf82d13c543dab8123658e0e69def336216385c865211` |
| `speaker_embeddings.bin` | 234,496 | `e7d689f10fef265343306481428d7b59b785a1efcb6d5008b96e20096fd5ca68` |
| `noimage.png` | 388,874 | Placeholder portrait from the trainer |

`downloads/trump.zip` holds these files in one `beatrice_paraphernalia_trump_00005000/` folder. Its SHA-256 is `adcc07b036e8b3119c599483f78c3b46d58d55cc0106a100c53858c58adbb4bb`.

## Notes

- The manifest marks the model as **personal/private use only** and an early checkpoint that hasn't been compared with longer training (10k+ steps).
- The training dataset isn't recorded with the model.
- It imitates a real public figure and isn't affiliated with or endorsed by him. See [Responsible use](../../README.md#-responsible-use).
