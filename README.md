# DecodeAtlas

A picture guide to how frontier LLMs are laid out across accelerators while they generate
tokens: how many devices serve one decode replica, and how the model is split across them.

**Read it at [williamtoner.net/DecodeAtlas](https://williamtoner.net/DecodeAtlas/).**

| Section | What it shows |
|---|---|
| Opening chart | Each major lab against the deployment layouts it has said it uses |
| 01 | The four ways to split a model across chips |
| 02–04 | One server split 8 ways; servers in a line (the 2023 GPT-4 leak); Google's TPU grid |
| 05 | Wide expert parallelism, as DeepSeek, Kimi, Meituan and Huawei Cloud run it |
| 06 | Prefill and decode on separate machines; attention and experts on separate machines |
| 07 | How many chips work on one copy of each model |

[`report.md`](report.md) is the long-form research report behind the page, with a citation and a
confidence label (official, third-party, leak, estimate) for every number.

The page is a single `index.html` with hand-drawn SVG. It has no build step and no dependencies
beyond web fonts.

Information current to 22 October 2026.
