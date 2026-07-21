# StemFX — Demo Page

Audio examples and figures for:

> **StemFX: Learning Mixing Style Representations via Autoregressive FX Chain Prediction on Source-Separated Stems**
> Yuan-Chiao Cheng, Jui-Te Wu, Brian Chen, Yen-Tung Yeh, Yu-Hua Chen, Yi-Hsuan Yang
> *Proc. of the 27th Int. Society for Music Information Retrieval Conf. (ISMIR), Abu Dhabi, UAE, 2026.*

**[▶ Open the demo page](https://barry-mir.github.io/stemfx-demo/)**

[Paper (arXiv)](https://arxiv.org/abs/2607.15634) · [Code](https://github.com/barry-mir/stemfx) · [MultiAFx Toolkit](https://github.com/barry-mir/multiafx)

## What's here

The page presents supplementary material for the paper:

- **System overview and retrieval figures** from the paper.
- **Paired style transfer** — same content, different mix. For each example: target, FX-normalized input, StemFX (ours), StemFX forced, and the two ITO baselines. Each method's predicted per-stem FX chain is inspectable inline.
- **Unpaired style transfer** — cross-song transfer on MUSDB18, shown in both directions.

Headphones recommended; all audio is loudness-normalized to −23 LUFS.

## Contents

```
index.html            demo page (self-contained, no build step)
audio/                paired/ and unpaired/ examples + predicted FX chain JSON
figures/              system overview and retrieval figures
```

## Running locally

Static site — serve the directory with any HTTP server (the FX-chain panels fetch JSON, so opening `index.html` via `file://` will not load them):

```sh
python3 -m http.server 8000
# then open http://localhost:8000/
```

## Citation

```bibtex
@inproceedings{cheng2026stemfx,
  title     = {{StemFX}: Learning Mixing Style Representations via Autoregressive
               {FX} Chain Prediction on Source-Separated Stems},
  author    = {Cheng, Yuan-Chiao and Wu, Jui-Te and Chen, Brian and
               Yeh, Yen-Tung and Chen, Yu-Hua and Yang, Yi-Hsuan},
  booktitle = {Proceedings of the 27th International Society for Music
               Information Retrieval Conference (ISMIR)},
  address   = {Abu Dhabi, UAE},
  year      = {2026},
  eprint    = {2607.15634},
  archivePrefix = {arXiv},
  primaryClass  = {eess.AS}
}
```

## License

The paper is © 2026 the authors, licensed under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/).
Audio examples are derived from [MUSDB18](https://sigsep.github.io/datasets/musdb.html) and are provided for research demonstration purposes only.
