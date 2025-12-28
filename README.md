<div align="center">

<p align="center" width="100%">
<img src="resources/imgs/dense_vs_moe.png"  width="100%" height="100%">
</p>

<!-- TITLE -->
**OpenMoE 2: Sparse Diffusion Language Models**
===========================

[Jinjie Ni](https://jinjieni.github.io/) and the team

---

<h4>The first-ever sparse diffusion large language model trained from scratch, focusing on architectural insights.</h4>

[![Static Badge](https://img.shields.io/badge/Blog-2025--10--02-darkcyan)](https://jinjieni.notion.site/OpenMoE-2-Sparse-Diffusion-Language-Models-277d8f03a8668065a4ecd23f23bd6aac?source=copy_link)
[![Static Badge](https://img.shields.io/badge/Infra-training--backend-darkblue)](https://github.com/JinjieNi/MegaDLMs)
[![Static Badge](https://img.shields.io/badge/Resources-ckpts--logs-green)](#resources)
[![Twitter](https://img.shields.io/twitter/url/https/twitter.com/cloudposse.svg?style=social&label=tweet)](https://x.com/NiJinjie/status/1973747616082186349)




</div>

# News
[2025-10-27] We release the codebase, all training checkpoints, and logs. The codebase is highly optimized and is industry-level in terms scalability and efficiency.

[2025-10-03] The blog is out! Check it out [here](https://jinjieni.notion.site/OpenMoE-2-Sparse-Diffusion-Language-Models-277d8f03a8668065a4ecd23f23bd6aac?source=copy_link)!


<br>

# Code
The codebase is released [here](https://github.com/JinjieNi/MegaDLMs). It is a highly-optimized codebase for any-scale DLMs training backend with Megatron-LM.

> The full MoE implementation is not yet released. We plan to release it after the main training is done.



<br>

# Resources

We opensource all model checkpoints and training logs mentioned in the paper. All of them can be downloaded at https://huggingface.co/collections/jinjieni/mdga.

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
    - [[ckpt](https://huggingface.co/datasets/MDGA-3/openmoe2_ckpts/tree/main/arch_exps/1.7b_dense)][[log](https://huggingface.co/datasets/MDGA-1/openmoe2_logs/tree/main/dense_vs_moe/dense_100b_1e_1b7_difflm)] dense 1.7b
    - [[ckpt](https://huggingface.co/datasets/MDGA-3/openmoe2_ckpts/tree/main/arch_exps/8b_dense)][[log](https://huggingface.co/datasets/MDGA-1/openmoe2_logs/tree/main/dense_vs_moe/dense_100b_1e_8b_difflm)] dense 8b
    - [[ckpt](https://huggingface.co/datasets/MDGA-3/openmoe2_ckpts/tree/main/arch_exps/tc)][[log](https://huggingface.co/datasets/MDGA-1/openmoe2_logs/tree/main/dense_vs_moe/moetopk_100b_1e_8b1b7a_difflm)] moe-8b1.7a-tc
    - [[ckpt](https://huggingface.co/datasets/MDGA-3/openmoe2_ckpts/tree/main/arch_exps/ec)][[log](https://huggingface.co/datasets/MDGA-1/openmoe2_logs/tree/main/dense_vs_moe/moeec_100b_1e_8b1b7a_difflm)] moe-8b1.7a-ec
- Diffusion + MoE is a Double Win
    - [[ckpt](https://huggingface.co/datasets/MDGA-1/super_data_learners_ckpts/tree/main/1b_96e_ar)][[log](https://huggingface.co/datasets/MDGA-1/super_data_learners_logs/tree/main/vary_sparsity/1b_96e_ar_1b1a)] AR dense 1b
    - [[ckpt](https://huggingface.co/datasets/MDGA-1/super_data_learners_ckpts/tree/main/1b_96e_dlm)][[log](https://huggingface.co/datasets/MDGA-1/super_data_learners_logs/tree/main/vary_sparsity/1b_96e_difflm_1b1a)] DLM dense 1b
    - [[ckpt](https://huggingface.co/datasets/MDGA-1/super_data_learners_ckpts/tree/main/1b_96e_ar_8b)][[log](https://huggingface.co/datasets/MDGA-1/super_data_learners_logs/tree/main/vary_sparsity/1b_96e_ar_8b8a)] AR dense 8b
    - [[ckpt](https://huggingface.co/datasets/MDGA-1/super_data_learners_ckpts/tree/main/1b_96e_dlm_8b)][[log](https://huggingface.co/datasets/MDGA-1/super_data_learners_logs/tree/main/vary_sparsity/1b_96e_difflm_8b8a)] DLM dense 8b
    - [[ckpt](https://huggingface.co/datasets/MDGA-2/openmoe2_ckpts/tree/main/arch_exps/8b1a_1b96e_tc_ar)][[log](https://huggingface.co/datasets/MDGA-1/super_data_learners_logs/tree/main/vary_sparsity/1b_96e_ar_8b1a)] AR MoE 8b1a
    - [[ckpt](https://huggingface.co/datasets/MDGA-2/openmoe2_ckpts/tree/main/arch_exps/8b1a_1b96e_tc_dlm)][[log](https://huggingface.co/datasets/MDGA-1/super_data_learners_logs/tree/main/vary_sparsity/1b_96e_difflm_8b1a)] DLM MoE 8b1a
- Token-choice vs. Expert-choice
    - [[ckpt](https://huggingface.co/datasets/MDGA-3/openmoe2_ckpts/tree/main/arch_exps/tc)][[log](https://huggingface.co/datasets/MDGA-1/openmoe2_logs/tree/main/ec_vs_tc/moetopk_100b_1e_8b1b7a_difflm)] tc
    - [[ckpt](https://huggingface.co/datasets/MDGA-3/openmoe2_ckpts/tree/main/arch_exps/ec)][[log](https://huggingface.co/datasets/MDGA-1/openmoe2_logs/tree/main/ec_vs_tc/moeec_100b_1e_8b1b7a_difflm)] ec
- Token-Wise Load-Balancing
    - [[ckpt](https://huggingface.co/datasets/MDGA-3/openmoe2_ckpts/tree/main/arch_exps/ec_lbl)][[log](https://huggingface.co/datasets/MDGA-1/openmoe2_logs/tree/main/expert_choice_ll/moeec_100b_1e_8b1b7a_difflm_yes)] with
    - [[ckpt](https://huggingface.co/datasets/MDGA-3/openmoe2_ckpts/tree/main/arch_exps/ec)][[log](https://huggingface.co/datasets/MDGA-1/openmoe2_logs/tree/main/expert_choice_ll/moeec_100b_1e_8b1b7a_difflm_no)] without
- with and without shared experts
    - [[ckpt](https://huggingface.co/datasets/MDGA-3/openmoe2_ckpts/tree/main/arch_exps/ec)][[log](https://huggingface.co/datasets/MDGA-1/openmoe2_logs/tree/main/shared_experts/moeec_100b_1e_8b1b7a_difflm_yes)] with
    - [[ckpt](https://huggingface.co/datasets/MDGA-3/openmoe2_ckpts/tree/main/arch_exps/ec_noshared)][[log](https://huggingface.co/datasets/MDGA-1/openmoe2_logs/tree/main/shared_experts/moeec_100b_1e_8b1b7a_difflm_no)] without
- scaling the expert granularities
    - [[ckpt](https://huggingface.co/datasets/MDGA-3/openmoe2_ckpts/tree/main/arch_exps/ec_16e)][[log](https://huggingface.co/datasets/MDGA-1/openmoe2_logs/tree/main/expert_granularity/moeec_100b_1e_8b1b7a_difflm_16)] 16
    - [[ckpt](https://huggingface.co/datasets/MDGA-3/openmoe2_ckpts/tree/main/arch_exps/ec)][[log](https://huggingface.co/datasets/MDGA-1/openmoe2_logs/tree/main/expert_granularity/moeec_100b_1e_8b1b7a_difflm_64)] 64
    - [[ckpt](https://huggingface.co/datasets/MDGA-3/openmoe2_ckpts/tree/main/arch_exps/ec_256e)][[log](https://huggingface.co/datasets/MDGA-1/openmoe2_logs/tree/main/expert_granularity/moeec_100b_1e_8b1b7a_difflm_256)] 256
- scratch vs. upcycling
    - [[ckpt](https://huggingface.co/datasets/MDGA-3/openmoe2_ckpts/tree/main/arch_exps/ec)][[log](https://huggingface.co/datasets/MDGA-1/openmoe2_logs/tree/main/upcycling_vs_train_from_scratch/moeec_100b_1e_8b1b7a_difflm_scratch)] scratch
    - [[ckpt](https://huggingface.co/datasets/MDGA-3/openmoe2_ckpts/tree/main/arch_exps/ec_upcycle)][[log](https://huggingface.co/datasets/MDGA-1/openmoe2_logs/tree/main/upcycling_vs_train_from_scratch/moeec_100b_1e_8b1b7a_difflm_upcycling)] upcycling
- Skip the First 2 MoE Layers
    - [[ckpt](https://huggingface.co/datasets/MDGA-3/openmoe2_ckpts/tree/main/arch_exps/ec_skiplayer)][[log](https://huggingface.co/datasets/MDGA-1/openmoe2_logs/tree/main/no_moe_first_layers/moeec_100b_1e_8b1b7a_difflm_no)] skip
    - [[ckpt](https://huggingface.co/datasets/MDGA-3/openmoe2_ckpts/tree/main/arch_exps/ec)][[log](https://huggingface.co/datasets/MDGA-1/openmoe2_logs/tree/main/no_moe_first_layers/moeec_100b_1e_8b1b7a_difflm_yes)] keep
- with and without scaling factors
    - [[ckpt](https://huggingface.co/datasets/MDGA-3/openmoe2_ckpts/tree/main/arch_exps/tc_scalingfactor)][[log](https://huggingface.co/datasets/MDGA-1/openmoe2_logs/tree/main/dynamic_scaling_factor_topk/moeec_100b_1e_8b1b7a_difflm_yes)] tc with
    - [[ckpt](https://huggingface.co/datasets/MDGA-3/openmoe2_ckpts/tree/main/arch_exps/tc)][[log](https://huggingface.co/datasets/MDGA-1/openmoe2_logs/tree/main/dynamic_scaling_factor_topk/moeec_100b_1e_8b1b7a_difflm_no)] tc without
    - [[ckpt](https://huggingface.co/datasets/MDGA-3/openmoe2_ckpts/tree/main/arch_exps/ec_scalingfactor)][[log](https://huggingface.co/datasets/MDGA-1/openmoe2_logs/tree/main/dynamic_scaling_factor/moeec_100b_1e_8b1b7a_difflm_yes)] ec with
    - [[ckpt](https://huggingface.co/datasets/MDGA-3/openmoe2_ckpts/tree/main/arch_exps/ec)][[log](https://huggingface.co/datasets/MDGA-1/openmoe2_logs/tree/main/dynamic_scaling_factor/moeec_100b_1e_8b1b7a_difflm_no)] ec without
- Batch vs. Sequence Level Expert Choice
    - [[ckpt](https://huggingface.co/datasets/MDGA-3/openmoe2_ckpts/tree/main/arch_exps/ec)][[log](https://huggingface.co/datasets/MDGA-1/openmoe2_logs/tree/main/seq_vs_batch/moeec_100b_1e_8b1b7a_difflm_batch)] batch
    - [[ckpt](https://huggingface.co/datasets/MDGA-3/openmoe2_ckpts/tree/main/arch_exps/ec_seq)][[log](https://huggingface.co/datasets/MDGA-1/openmoe2_logs/tree/main/seq_vs_batch/moeec_100b_1e_8b1b7a_difflm_seq)] seq
- Softmax vs. Sigmoid
    - [[ckpt](https://huggingface.co/datasets/MDGA-3/openmoe2_ckpts/tree/main/arch_exps/ec)][[log](https://huggingface.co/datasets/MDGA-1/openmoe2_logs/tree/main/softmax_vs_sigmoid/moeec_100b_1e_8b1b7a_difflm_softmax)] softmax
    - [[ckpt](https://huggingface.co/datasets/MDGA-3/openmoe2_ckpts/tree/main/arch_exps/ec_sigmoid)][[log](https://huggingface.co/datasets/MDGA-1/openmoe2_logs/tree/main/softmax_vs_sigmoid/moeec_100b_1e_8b1b7a_difflm_sigmoid)] sigmoid

You can refer to [this](https://github.com/JinjieNi/MegaDLMs/blob/main/examples/dlm_generation/dlm_inference.py) script to inference with the huggingface checkpoints. Due to the large amount, most small checkpoints above are still in megatron formats. You may refer to [this](https://github.com/JinjieNi/MegaDLMs/blob/main/examples/dlm_training/ckpt_conversion.sh) script to convert them (need to tweak the conversion scripts).

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
  year={2025}
  howpublished={\url{https://github.com/JinjieNi/OpenMoE2}},
}
```
