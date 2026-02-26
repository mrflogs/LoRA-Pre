<div align="center">

# Taming Momentum: Rethinking Optimizer States Through Low-Rank Approximation

**ICLR 2026 Oral** 🎉

[![Paper](https://img.shields.io/badge/Paper-OpenReview-b31b1b)](https://openreview.net/forum?id=9Q0dNBYeEY)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](https://github.com/mrflogs/LoRA-Pre/blob/main/LICENSE)
<!-- [![arXiv](https://img.shields.io/badge/arXiv-xxxx.xxxxx-b31b1b)](https://arxiv.org/abs/xxxx.xxxxx) -->

[Zhengbo Wang](https://zhengbo.wang/)<sup>1,2</sup>,&nbsp;
[Jian Liang](https://liangjian.xyz/)<sup>2,3†</sup>,&nbsp;
[Ran He](https://people.ucas.ac.cn/~heran)<sup>2,3</sup>,&nbsp;
[Zilei Wang](https://faculty.ustc.edu.cn/zlwang)<sup>1</sup>,&nbsp;
[Tieniu Tan](https://www.nju.edu.cn/en/info/2292/4261.htm)<sup>4</sup>

<sup>1</sup> University of Science and Technology of China &nbsp;&nbsp;
<sup>2</sup> CRIPAC & MAIS, Institute of Automation, CAS <br>
<sup>3</sup> University of Chinese Academy of Sciences &nbsp;&nbsp;
<sup>4</sup> Nanjing University

<sup>†</sup> Corresponding author

</div>

## 📰 News

- 🔥 **[2026/01]** LoRA-Pre is accepted as an **Oral** at ICLR 2026!
- 📦 **[2026/xx]** Code release — *coming soon!*

## 💡 TL;DR

We reframe the exponential moving average (EMA) in Adam/Muon as training an online linear regressor, and introduce **LoRA-Pre** — a low-rank optimizer that compresses momentum into a compact low-rank subspace. LoRA-Pre achieves state-of-the-art pre-training performance from 60M to 1B parameters with remarkable rank efficiency (1/8 the rank of baselines), and delivers strong fine-tuning gains (**+3.14** on Llama-3.1-8B, **+6.17** on Llama-2-7B over standard LoRA).

## ✨ Highlights

- 📐 **Novel perspective** — We reveal an equivalence between EMA momenta and online linear regression, enabling principled low-rank compression of optimizer states.
- 🚀 **Extreme rank efficiency** — LoRA-Pre matches or beats baselines with only **1/8 the rank**.
- 📈 **Pre-training** — State-of-the-art results across Llama 60M → 1B on C4.
- 🎯 **Fine-tuning** — Consistent improvements over LoRA, GaLore, and other efficient baselines on Llama-2-7B and Llama-3.1-8B.
- 💾 **Memory efficient** — Significantly reduced optimizer memory footprint via low-rank momentum decomposition.

## 📋 Abstract

Modern optimizers like Adam and Muon are central to training large language models, but their reliance on first- and second-order momenta introduces significant memory overhead, which constrains scalability and computational efficiency. In this work, we reframe the exponential moving average (EMA) used in these momenta as the training of a linear regressor via online gradient flow. Building on this equivalence, we introduce LoRA-Pre, a novel low-rank optimizer designed for efficient pre-training. Specifically, LoRA-Pre reduces the optimizer's memory footprint by decomposing the full momentum matrix into a compact low-rank subspace within the online linear learner, thereby maintaining optimization performance while improving memory efficiency. We empirically validate LoRA-Pre's efficacy by pre-training models from the Llama architecture family, scaling from 60M to 1B parameters. LoRA-Pre achieves the highest performance across all model sizes. Notably, LoRA-Pre demonstrates remarkable rank efficiency, achieving comparable or superior results using only 1/8 the rank of baseline methods. Beyond pre-training, we evaluate LoRA-Pre's effectiveness in fine-tuning scenarios. With the same rank, LoRA-Pre consistently outperforms all efficient fine-tuning baselines.

## 🛠️ Code

We are actively preparing the codebase for public release. Code and training scripts will be available as soon as possible.

**Stay tuned** — ⭐ star and 👀 watch this repo to get notified!

<!-- 
## Installation

```bash
pip install -e .
```

## Quick Start

### Pre-training

```bash
# Coming soon
```

### Fine-tuning

```bash
# Coming soon
```
-->

## 📝 Citation

If you find this work useful, please consider citing:

```bibtex
@inproceedings{wang2026taming,
  title={Taming Momentum: Rethinking Optimizer States Through Low-Rank Approximation},
  author={Zhengbo Wang and Jian Liang and Ran He and Zilei Wang and Tieniu Tan},
  booktitle={The Fourteenth International Conference on Learning Representations (ICLR)},
  year={2026},
}
```

## 📬 Contact

If you have any questions, feel free to contact 📫zhengbowang@mail.ustc.edu.cn.
