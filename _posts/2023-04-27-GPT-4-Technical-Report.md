---
title: GPT-4 Technical Report
author: Daniel Park
date: 2023-04-27
category: nlp
layout: post
---

 - **url:** <https://arxiv.org/abs/2303.08774>
 - **abstract:** By decomposing the image formation process into a sequential
    application of denoising autoencoders, diffusion models (DMs)
    achieve state-of-the-art synthesis results on image data and beyond.
    Additionally, their formulation allows for a guiding mechanism to
    control the image generation process without retraining. However,
    since these models typically operate directly in pixel space,
    optimization of powerful DMs often consumes hundreds of GPU days and
    inference is expensive due to sequential evaluations. To enable DM