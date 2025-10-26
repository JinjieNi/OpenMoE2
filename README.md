<div align="center">

<p align="center" width="100%">
<img src="resources/imgs/dense_vs_moe.png"  width="100%" height="100%">
</p>

<!-- TITLE -->
**OpenMoE 2: Sparse Diffusion Language Models**
===========================

<h4>The first-ever sparse diffusion large language model trained from scratch, focusing on architectural insights.</h4>

[![Static Badge](https://img.shields.io/badge/Blog-2025--10--02-darkcyan)](https://jinjieni.notion.site/OpenMoE-2-Sparse-Diffusion-Language-Models-277d8f03a8668065a4ecd23f23bd6aac?source=copy_link)
[![Twitter](https://img.shields.io/twitter/url/https/twitter.com/cloudposse.svg?style=social&label=tweet)](https://x.com/NiJinjie/status/1973747616082186349)


[Jinjie Ni](https://jinjieni.github.io/) and the team

<!-- †Correspondence to: Jinjie Ni \<jinjieni@nus.edu.sg\> -->
</div>

# News
[2025-10-27] We release the codebase and all training checkpoints. The codebase is highly optimized and is industry-level in terms scalability and efficiency.

[2025-10-03] The blog is out! Check it out [here](https://jinjieni.notion.site/OpenMoE-2-Sparse-Diffusion-Language-Models-277d8f03a8668065a4ecd23f23bd6aac?source=copy_link)!


<br>

# Code
The codebase is released [here](https://github.com/JinjieNi/MegaDLMs). It is a highly-optimized codebase for any-scale DLMs training backend with Megatron-LM.

> The full MoE implementation is not yet released. We plan to release it after the main training is done.



<br>

# Resources

We opensource all model checkpoints, training logs, and datasets mentioned in the paper. All of them can be downloaded at https://huggingface.co/collections/jinjieni/mdga.

The easiest way to download a folder is using this script (setup the variables properly):
```
python utils/hf_download_folder.py
```

Alternatively, you can also use `wget` to directly download individual files from the folder, e.g.:
```bash
wget https://huggingface.co/datasets/MDGA-1/openmoe2_logs/blob/main/dense_vs_moe/dense_100b_1e_1b7_difflm/tensorboard/events.out.tfevents.1755443508.0648415733
```

We link the related resources below:

- Parameter–Compute Trade-off
    - [[ckpt]()][[log]()] dense 1.7b
    - [[ckpt]()][[log]()] dense 8b
    - [[ckpt]()][[log]()] moe-8b1.7a-topk
    - [[ckpt]()][[log]()] moe-8b1.7a-ec
- Diffusion + MoE is a Double Win
    - [[ckpt]()][[log]()] AR dense 1b
    - [[ckpt]()][[log]()] DLM dense 1b
    - [[ckpt]()][[log]()] AR dense 8b
    - [[ckpt]()][[log]()] DLM dense 8b
    - [[ckpt]()][[log]()] AR MoE 8b1a
    - [[ckpt]()][[log]()] DLM MoE 8b1a
- Token-choice vs. Expert-choice
    - [[ckpt]()][[log]()] tc
    - [[ckpt]()][[log]()] ec
- Token-Wise Load-Balancing
    - [[ckpt]()][[log]()] with
    - [[ckpt]()][[log]()] without
- with and without shared experts
    - [[ckpt]()][[log]()] with
    - [[ckpt]()][[log]()] without
- scaling the expert granularities
    - [[ckpt]()][[log]()] 16
    - [[ckpt]()][[log]()] 64
    - [[ckpt]()][[log]()] 256
- scratch vs. upcycling
    - [[ckpt]()][[log]()] scratch
    - [[ckpt]()][[log]()] upcycling
- Skip the First 2 MoE Layers
    - [[ckpt]()][[log]()] skip
    - [[ckpt]()][[log]()] keep
- with and without scaling factors
    - [[ckpt]()][[log]()] tc with
    - [[ckpt]()][[log]()] tc without
    - [[ckpt]()][[log]()] ec with
    - [[ckpt]()][[log]()] ec without
- Batch vs. Sequence Level Expert Choice
    - [[ckpt]()][[log]()] batch
    - [[ckpt]()][[log]()] seq
- Softmax vs. Sigmoid
    - [[ckpt]()][[log]()] softmax
    - [[ckpt]()][[log]()] sigmoid

<br>


# Todo List

**This is an on-going project! We will tick the below todo list one-by-one.**

- [x]  Architectural Design Choices
- [ ]  Scaled-up Pre-training
- [ ]  Post-training
- [ ]  Routing & Other Analysis
- [ ]  Full Paper
- [ ]  Code & Checkpoint Open-sourcing


<br>

# Citation
```
@misc{ni2025openmoe2,
title={OpenMoE 2: Sparse Diffusion Language Models},
author={Ni, Jinjie and team},
year={2025},
howpublished={\url{https://jinjieni.notion.site/OpenMoE-2-Sparse-Diffusion-Language-Models-277d8f03a8668065a4ecd23f23bd6aac}},
note={Notion Blog},
}
```
