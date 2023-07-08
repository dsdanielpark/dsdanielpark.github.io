---
title: Replit-3b and FlashAttention
author: Daniel Park
date: 2023-07-06
category: llm
layout: post
---

- Related Project: private 
- Project Status: 1 Alpha
- Date: 2023-07-06


### Replit-3b and FlashAttention
Links
- [replit-code-v1-3b](https://huggingface.co/replit/replit-code-v1-3b)
- [FlashAttention](https://arxiv.org/abs/2205.14135)



## Releated Works
### FlashAttention: Fast and Memory-Efficient Exact Attention with IO-Awareness
- **url:** <https://arxiv.org/abs/2205.14135>
- **pdf:** <https://arxiv.org/pdf/2205.14135>
- **date:** 2023.05.27 for v1
- **abstract:** Transformers are slow and memory-hungry on long sequences, since the time and memory complexity of self-attention are quadratic in sequence length. Approximate attention methods have attempted to address this problem by trading off model quality to reduce the compute complexity, but often do not achieve wall-clock speedup. We argue that a missing principle is making attention algorithms IO-aware -- accounting for reads and writes between levels of GPU memory. We propose FlashAttention, an IO-aware exact attention algorithm that uses tiling to reduce the number of memory reads/writes between GPU high bandwidth memory (HBM) and GPU on-chip SRAM. We analyze the IO complexity of FlashAttention, showing that it requires fewer HBM accesses than standard attention, and is optimal for a range of SRAM sizes. We also extend FlashAttention to block-sparse attention, yielding an approximate attention algorithm that is faster than any existing approximate attention method. FlashAttention trains Transformers faster than existing baselines: 15% end-to-end wall-clock speedup on BERT-large (seq. length 512) compared to the MLPerf 1.1 training speed record, 3× speedup on GPT-2 (seq. length 1K), and 2.4× speedup on long-range arena (seq. length 1K-4K). FlashAttention and block-sparse FlashAttention enable longer context in Transformers, yielding higher quality models (0.7 better perplexity on GPT-2 and 6.4 points of lift on long-document classification) and entirely new capabilities: the first Transformers to achieve better-than-chance performance on the Path-X challenge (seq. length 16K, 61.4% accuracy) and Path-256 (seq. length 64K, 63.1% accuracy).



### Train Short, Test Long: Attention with Linear Biases Enables Input Length Extrapolation
- **url:** <https://arxiv.org/abs/2108.12409>
- **pdf:** <https://arxiv.org/pdf/2108.12409>
- **date:** 2021.08.27 for v1