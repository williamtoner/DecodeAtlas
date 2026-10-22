# DecodeAtlas

A picture guide to how frontier LLMs are laid out across accelerators while they generate
tokens: how many devices serve one decode replica, and how the model is split across them.

**Read it at [williamtoner.net/DecodeAtlas](https://williamtoner.net/DecodeAtlas/).**

| Section | What it shows |
|---|---|
| Hero | Accelerators per decode instance for 23 models, from model-card recipes to disclosed deployments |
| 01 | Why decode is memory-bound, and why MoE pushes the critical batch out by *E/k* |
| 02 | Tensor, pipeline and expert parallelism, and data-parallel attention |
| 03–05 | One server at TP8; deep pipelines (the 2023 GPT-4 leak); 2D weight sharding on TPUs |
| 06–07 | How the KV cache's shape picks the attention layout; DeepSeek's wide expert parallelism |
| 08–09 | Prefill/decode disaggregation; attention–FFN disaggregation |
| 10–11 | Scale-up domains (NVL72, TPU pods, supernodes); the throughput vs speed-per-user curve |
| 12 | Lab by lab, including what the closed labs do and do not disclose |

[`report.md`](report.md) is the long-form research report behind the page, with a citation and a
confidence label (official, third-party, leak, estimate) for every number.

The page is a single `index.html` with hand-drawn SVG. It has no build step and no dependencies
beyond web fonts.

Information current to 22 October 2026.
