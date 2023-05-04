---
title: [AUTO DRAFT] High-Resolution Image Synthesis with Latent Diffusion Models
author: Daniel Park
date: 2023-04-26
category: stablediffusion
layout: post
---
 
> 이 글은 자동 생성된 초고로, 선행연구를 훑어보고, 색인하기 위한 용도입니다. This draft is automatically generated for the purpose of skimming through prior research and indexing.
> 배치성 프로그램으로 진행하고 있는 연구에 참고될만한 논문들을 자동 생성합니다. 논문들은 인용 관계로 서로 연결되어 있으며, 인용 횟수 순으로 정렬되어 있습니다.  The batch program generates research papers that can be referenced in my ongoing studies. These papers are connected to each other through citation relationships and are sorted by the number of citations.

- Related Project: Private
- Project Status: 1 Alpha
- Author: MinWoo Park
- Date: 2023-04

## Main Paper

### High-Resolution Image Synthesis with Latent Diffusion Models
 - **abstract:** By decomposing the image formation process into a sequential
    application of denoising autoencoders, diffusion models (DMs)
    achieve state-of-the-art synthesis results on image data and beyond.
    Additionally, their formulation allows for a guiding mechanism to
    control the image generation process without retraining. However,
    since these models typically operate directly in pixel space,
    optimization of powerful DMs often consumes hundreds of GPU days and
    inference is expensive due to sequential evaluations. To enable DM
    training on limited computational resources while retaining their
    quality and flexibility, we apply them in the latent space of
    powerful pretrained autoencoders. In contrast to previous work,
    training diffusion models on such a representation allows for the
    first time to reach a near-optimal point between complexity
    reduction and detail preservation, greatly boosting visual fidelity.
    By introducing cross-attention layers into the model architecture,
    we turn diffusion models into powerful and flexible generators for
    general conditioning inputs such as text or bounding boxes and
    high-resolution synthesis becomes possible in a convolutional
    manner. Our latent diffusion models (LDMs) achieve new state of the
    art scores for image inpainting and class-conditional image
    synthesis and highly competitive performance on various tasks,
    including unconditional image generation, text-to-image synthesis,
    and super-resolution, while significantly reducing computational
    requirements compared to pixel-based DMs.
 - **container-Paper Title:** 2022 IEEE/CVF Conference on Computer Vision and
    Pattern Recognition (CVPR)
 - **doi:** 10.1109/CVPR52688.2022.01042
 - **id:** c10075b3746a9f3dd5811970e93c8ca3ad39b39d


## Related Papers

### High-resolution image synthesis with latent diffusion models
 - **type:** article-journal
 - **url:** <https://www.semanticscholar.org/paper/c10075b3746a9f3dd5811970e93c8ca3ad39b39d>
 - **volume:** null
 - **abstract:** We show that diffusion models can achieve image sample
    quality superior to the current state-of-the-art generative models.
    We achieve this on unconditional image synthesis by finding a better
    architecture through a series of ablations. For conditional image
    synthesis, we further improve sample quality with classifier
    guidance: a simple, compute-efficient method for trading off
    diversity for fidelity using gradients from a classifier. We achieve
    an FID of 2.97 on ImageNet 128$\\times$ 128, 4.59 on
    ImageNet 256$\\times$ 256, and 7.72 on ImageNet
    512$\\times$ 512, and we match BigGAN-deep even with
    as few as 25 forward passes per sample, all while maintaining better
    coverage of the distribution. Finally, we find that classifier
    guidance combines well with upsampling diffusion models, further
    improving FID to 3.94 on ImageNet 256$\\times$ 256
    and 3.85 on ImageNet 512$\\times$ 512. We release our
    code at <https://github.com/openai/guided-diffusion>
 - **container-Paper Title:** ArXiv
 - **id:** 64ea8f180d0682e6c18d1eb688afdb2027c02794


### Diffusion models beat GANs on image synthesis
 - **type:** article-journal
 - **url:** <https://www.semanticscholar.org/paper/64ea8f180d0682e6c18d1eb688afdb2027c02794>
 - **volume:** abs/2105.05233
 - **abstract:** Recently, GAN inversion methods combined with Contrastive
    Language-Image Pretraining (CLIP) enables zeroshot image
    manipulation guided by text prompts. However, their applications to
    diverse real images are still difficult due to the limited GAN
    inversion capability. Specifically, these approaches often have
    difficulties in reconstructing images with novel poses, views, and
    highly variable contents compared to the training data, altering
    object identity, or producing unwanted image artifacts. To mitigate
    these problems and enable faithful manipulation of real images, we
    propose a novel method, dubbed DiffusionCLIP, that performs
    textdriven image manipulation using diffusion models. Based on full
    inversion capability and high-quality image generation power of
    recent diffusion models, our method performs zeroshot image
    manipulation successfully even between unseen domains and takes
    another step towards general application by manipulating images from
    a widely varying ImageNet dataset. Furthermore, we propose a novel
    noise combination method that allows straightforward multi-attribute
    manipulation. Extensive experiments and human evaluation confirmed
    robust and superior manipulation performance of our methods compared
    to the existing baselines. Code is available at
    <https://github.com/gwang-kim/DiffusionCLIP.git>
 - **container-Paper Title:** 2022 IEEE/CVF Conference on Computer Vision and
    Pattern Recognition (CVPR)
 - **doi:** 10.1109/CVPR52688.2022.00246
 - **id:** 8f8dedb511c0324d1cb7f9750560109ca9290b5f


### DiffusionCLIP: Text-guided diffusion models for robust image manipulation
 - title-short: DiffusionCLIP
 - **type:** article-journal
 - **url:** <https://www.semanticscholar.org/paper/8f8dedb511c0324d1cb7f9750560109ca9290b5f>
 - **volume:** null
 - **abstract:** We present the vector quantized diffusion (VQ-Diffusion)
    model for text-to-image generation. This method is based on a vector
    quantized variational autoencoder (VQ-VAE) whose latent space is
    modeled by a conditional variant of the recently developed Denoising
    Diffusion Probabilistic Model (DDPM). We find that this latent-space
    method is well-suited for text-to-image generation tasks because it
    not only eliminates the unidirectional bias with existing methods
    but also allows us to incorporate a mask-and-replace diffusion
    strategy to avoid the accumulation of errors, which is a serious
    problem with existing methods. Our experiments show that the
    VQ-Diffusion produces significantly better text-to-image generation
    results when compared with conventional autoregressive (AR) models
    with similar numbers of parameters. Compared with previous GAN-based
    text-to-image methods, our VQ-Diffusion can handle more complex
    scenes and improve the synthesized image quality by a large margin.
    Finally, we show that the image generation computation in our method
    can be made highly efficient by reparameterization. With traditional
    AR methods, the text-to-image generation time increases linearly
    with the output image resolution and hence is quite time consuming
    even for normal size images. The VQ-Diffusion allows us to achieve a
    better trade-off between quality and speed. Our experiments indicate
    that the VQ-Diffusion model with the reparameterization is fifteen
    times faster than traditional AR methods while achieving a better
    image quality. The code and models are available at
    <https://github.com/cientgu/VQ-Diffusion.>
 - **container-Paper Title:** 2022 IEEE/CVF Conference on Computer Vision and
    Pattern Recognition (CVPR)
 - **doi:** 10.1109/CVPR52688.2022.01043
 - **id:** 194ea47df737ee5cc4240273b34a6c673a081515


### Vector quantized diffusion model for text-to-image synthesis
 - **type:** article-journal
 - **url:** <https://www.semanticscholar.org/paper/194ea47df737ee5cc4240273b34a6c673a081515>
 - **volume:** null
 - **abstract:** Employing a forward Markov diﬀusion chain to gradually map
    the data to a noise distribution, diﬀusion probabilistic models
    learn how to generate the data by inferring a reverse Markov
    diﬀusion chain to invert the forward diﬀusion process. To achieve
    competitive data generation performance, they demand a long diﬀusion
    chain that makes them computationally intensive in not only training
    but also generation. To signiﬁcantly improve the computation
    eﬃciency, we propose to truncate the forward diﬀusion chain by
    abolishing the requirement of diﬀusing the data to random noise.
    Consequently, we start the inverse diﬀusion chain from an implicit
    generative distribution, rather than a random noise, and learn its
    parameters by matching it to the distribution of the data corrupted
    by the truncated forward diﬀusion chain. Experimental results show
    our truncated diﬀusion probabilistic models provide consistent
    improvements over the non-truncated ones in terms of the generation
    performance and the number of required inverse diﬀusion steps.
 - **container-Paper Title:** ArXiv
 - **id:** a404b466126c2a83c460eded92c95297cc84af64


### Truncated diffusion probabilistic models
 - **type:** article-journal
 - **url:** <https://www.semanticscholar.org/paper/f81d707d83d5857ab82831fcdd278fc9355b8dce>
 - **volume:** abs/2202.09671
 - **abstract:** Recently most successful image synthesis models are multi
    stage process to combine the advantages of different methods, which
    always includes a VAE-like model for faithfully reconstructing
    embedding to image and a prior model to generate image embedding. At
    the same time, diffusion models have shown be capacity to generate
    high-quality synthetic images. Our work proposes a VQ-VAE
    architecture model with a diffusion decoder (DiVAE) to work as the
    reconstructing component in image synthesis. We explore how to input
    image embedding into diffusion model for excellent performance and
    find that simple modification on diffusion's UNet can achieve it.
    Training on ImageNet, Our model achieves state-of-the-art results
    and generates more photorealistic images specifically. In addition,
    we apply the DiVAE with an Auto-regressive generator on conditional
    synthesis tasks to perform more human-feeling and detailed samples.
 - **container-Paper Title:** ArXiv
 - **doi:** 10.48550/arXiv.2206.00386
 - **id:** 32b3553d7dc8a263c63d32eeec2916d1647ab178


### DiVAE: Photorealistic images synthesis with denoising diffusion decoder
 - title-short: DiVAE
 - **type:** article-journal
 - **url:** <https://www.semanticscholar.org/paper/32b3553d7dc8a263c63d32eeec2916d1647ab178>
 - **volume:** abs/2206.00386
 - **abstract:** We present Imagen Video, a text-conditional video
    generation system based on a cascade of video diffusion models.
    Given a text prompt, Imagen Video generates high definition videos
    using a base video generation model and a sequence of interleaved
    spatial and temporal video super-resolution models. We describe how
    we scale up the system as a high definition text-to-video model
    including design decisions such as the choice of fully-convolutional
    temporal and spatial super-resolution models at certain resolutions,
    and the choice of the v-parameterization of diffusion models. In
    addition, we confirm and transfer findings from previous work on
    diffusion-based image generation to the video generation setting.
    Finally, we apply progressive distillation to our video models with
    classifier-free guidance for fast, high quality sampling. We find
    Imagen Video not only capable of generating videos of high fidelity,
    but also having a high degree of controllability and world
    knowledge, including the ability to generate diverse videos and text
    animations in various artistic styles and with 3D object
    understanding. See <https://imagen.research.google/video/ for>
    samples.
 - **container-Paper Title:** ArXiv
 - **doi:** 10.48550/arXiv.2210.02303
 - **id:** 498ac9b2e494601d20a3d0211c16acf2b7954a54


### Imagen video: High definition video generation with diffusion models
 - title-short: Imagen video
 - **type:** article-journal
 - **url:** <https://www.semanticscholar.org/paper/498ac9b2e494601d20a3d0211c16acf2b7954a54>
 - **volume:** abs/2210.02303
 - **abstract:** Large text-to-image models achieved a remarkable leap in
    the evolution of AI, enabling high-quality and diverse synthesis of
    images from a given text prompt. However, these models lack the
    ability to mimic the appearance of subjects in a given reference set
    and synthesize novel renditions of them in different contexts. In
    this work, we present a new approach for\\\personalization\\\of
    text-to-image diffusion models. Given as input just a few images of
    a subject, we fine-tune a pretrained text-to-image model such that
    it learns to bind a unique identifier with that specific subject.
    Once the subject is embedded in the output domain of the model, the
    unique identifier can be used to synthesize novel photorealistic
    images of the subject contextualized in different scenes. By
    leveraging the semantic prior embedded in the model with a new
    autogenous class-specific prior preservation loss, our technique
    enables synthesizing the subject in diverse scenes, poses, views and
    lighting conditions that do not appear in the reference images. We
    apply our technique to several previously-unassailable tasks,
    including subject recontextualization, text-guided view synthesis,
    and artistic rendering, all while preserving the subject's key
    features. We also provide a new dataset and evaluation protocol for
    this new task of subject-driven generation. Project page:
    <https://dreambooth.github.io/>
 - **container-Paper Title:** ArXiv
 - **doi:** 10.48550/arXiv.2208.12242
 - **id:** d7b72963fccd86bb8c85f289d7f00c12fdc6cbfd


### DreamBooth: Fine tuning text-to-image diffusion models for subject-driven generation
 - title-short: DreamBooth
 - **type:** article-journal
 - **url:** <https://www.semanticscholar.org/paper/5b19bf6c3f4b25cac96362c98b930cf4b37f6744>
 - **volume:** abs/2208.12242
 - **abstract:** A central problem in machine learning involves modeling
    complex data-sets using highly flexible families of probability
    distributions in which learning, sampling, inference, and evaluation
    are still analytically or computationally tractable. Here, we
    develop an approach that simultaneously achieves both flexibility
    and tractability. The essential idea, inspired by non-equilibrium
    statistical physics, is to systematically and slowly destroy
    structure in a data distribution through an iterative forward
    diffusion process. We then learn a reverse diffusion process that
    restores structure in data, yielding a highly flexible and tractable
    generative model of the data. This approach allows us to rapidly
    learn, sample from, and evaluate probabilities in deep generative
    models with thousands of layers or time steps, as well as to compute
    conditional and posterior probabilities under the learned model. We
    additionally release an open source reference implementation of the
    algorithm.
 - **container-Paper Title:** ArXiv
 - **id:** 2dcef55a07f8607a819c21fe84131ea269cc2e3c


### Deep unsupervised learning using nonequilibrium thermodynamics
 - **type:** article-journal
 - **url:** <https://www.semanticscholar.org/paper/2dcef55a07f8607a819c21fe84131ea269cc2e3c>
 - **volume:** abs/1503.03585
 - **abstract:** *TL;DR:* A novel discrete diffusion probabilistic model
    prior is proposed which enables parallel prediction of
    Vector-Quantized tokens by using an unconstrained Transformer
    architecture as the backbone and facilitates unconditional
    generation of globally consistent high-resolution and diverse
    imagery at a fraction of the computational expense.
 - **doi:** 10.1007/978-3-031-20050-2_11
 - **id:** 80035bfa3f822364fbc62de6df2d5df13a0c47ff


### Unleashing transformers: Parallel token prediction with discrete absorbing diffusion for fast high-resolution image generation from vector-quantized codes
 - title-short: Unleashing transformers
 - **type:** article-journal
 - **url:** <https://www.semanticscholar.org/paper/80035bfa3f822364fbc62de6df2d5df13a0c47ff>
 - **abstract:** This paper develops a unified framework for image-to-image
    translation based on conditional diffusion models and evaluates this
    framework on four challenging image-to-image translation tasks,
    namely colorization, inpainting, uncropping, and JPEG restoration.
    Our simple implementation of image-to-image diffusion models
    outperforms strong GAN and regression baselines on all tasks,
    without task-specific hyper-parameter tuning, architecture
    customization, or any auxiliary loss or sophisticated new techniques
    needed. We uncover the impact of an L2 vs. L1 loss in the denoising
    diffusion objective on sample diversity, and demonstrate the
    importance of self-attention in the neural architecture through
    empirical studies. Importantly, we advocate a unified evaluation
    protocol based on ImageNet, with human evaluation and sample quality
    scores (FID, Inception Score, Classification Accuracy of a
    pre-trained ResNet-50, and Perceptual Distance against original
    images). We expect this standardized evaluation protocol to play a
    role in advancing image-to-image translation research. Finally, we
    show that a generalist, multi-task diffusion model performs as well
    or better than task-specific specialist counterparts. Check out
    <https://diffusion-palette.github.io/> for an overview of the results
    and code.
 - **container-Paper Title:** ACM SIGGRAPH 2022 Conference Proceedings
 - **doi:** 10.1145/3528233.3530757
 - **id:** 37c9c4e7648f639c0b36f150fc6c6c90b3682f4a


### Palette: Image-to-image diffusion models
 - title-short: Palette
 - **type:** article-journal
 - **url:** <https://www.semanticscholar.org/paper/37c9c4e7648f639c0b36f150fc6c6c90b3682f4a>
 - **volume:** null
 - **abstract:** We present Imagen, a text-to-image diffusion model with an
    unprecedented degree of photorealism and a deep level of language
    understanding. Imagen builds on the power of large transformer
    language models in understanding text and hinges on the strength of
    diffusion models in high-fidelity image generation. Our key
    discovery is that generic large language models (e.g. T5),
    pretrained on text-only corpora, are surprisingly effective at
    encoding text for image synthesis: increasing the size of the
    language model in Imagen boosts both sample fidelity and image-text
    alignment much more than increasing the size of the image diffusion
    model. Imagen achieves a new state-of-the-art FID score of 7.27 on
    the COCO dataset, without ever training on COCO, and human raters
    find Imagen samples to be on par with the COCO data itself in
    image-text alignment. To assess text-to-image models in greater
    depth, we introduce DrawBench, a comprehensive and challenging
    benchmark for text-to-image models. With DrawBench, we compare
    Imagen with recent methods including VQ-GAN+CLIP, Latent Diffusion
    Models, and DALL-E 2, and find that human raters prefer Imagen over
    other models in side-by-side comparisons, both in terms of sample
    quality and image-text alignment. See
    <https://imagen.research.google/ for an overview of the results.>
 - **container-Paper Title:** ArXiv
 - **doi:** 10.48550/arXiv.2205.11487
 - **id:** 9695824d7a01fad57ba9c01d7d76a519d78d65e7


### Photorealistic text-to-image diffusion models with deep language understanding
 - **type:** article-journal
 - **url:** <https://www.semanticscholar.org/paper/9695824d7a01fad57ba9c01d7d76a519d78d65e7>
 - **volume:** abs/2205.11487
 - **abstract:** We present high quality image synthesis results using
    diffusion probabilistic models, a class of latent variable models
    inspired by considerations from nonequilibrium thermodynamics. Our
    best results are obtained by training on a weighted variational
    bound designed according to a novel connection between diffusion
    probabilistic models and denoising score matching with Langevin
    dynamics, and our models naturally admit a progressive lossy
    decompression scheme that can be interpreted as a generalization of
    autoregressive decoding. On the unconditional CIFAR10 dataset, we
    obtain an Inception score of 9.46 and a state-of-the-art FID score
    of 3.17. On 256x256 LSUN, we obtain sample quality similar to
    ProgressiveGAN. Our implementation is available at this https URL
 - **container-Paper Title:** ArXiv
 - **id:** 289db3be7bf77e06e75541ba93269de3d604ac72


### Denoising diffusion probabilistic models
 - **type:** article-journal
 - **url:** <https://www.semanticscholar.org/paper/289db3be7bf77e06e75541ba93269de3d604ac72>
 - **volume:** abs/2006.11239
 - **abstract:** Diffusion probabilistic models (DPMs) have achieved
    remarkable quality in image generation that rivals GANs'. But unlike
    GANs, DPMs use a set of latent variables that lack semantic meaning
    and cannot serve as a useful representation for other tasks. This
    paper explores the possibility of using DPMs for representation
    learning and seeks to extract a meaningful and decodable
    representation of an input image via autoencoding. Our key idea is
    to use a learnable encoder for discovering the high-level semantics,
    and a DPM as the decoder for modeling the remaining stochastic
    variations. Our method can encode any image into a two-part latent
    code where the first part is semantically meaningful and linear, and
    the second part captures stochastic details, allowing near-exact
    reconstruction. This capability enables challenging applications
    that currently foil GAN-based methods, such as attribute
    manipulation on real images. We also show that this two-level
    encoding improves denoising efficiency and naturally facilitates
    various downstream tasks including few-shot conditional sampling.
    Please visit our page: <https://Diff-AE.github.io/>
 - **container-Paper Title:** 2022 IEEE/CVF Conference on Computer Vision and
    Pattern Recognition (CVPR)
 - **doi:** 10.1109/CVPR52688.2022.01036
 - **id:** b582edb16f5425642767cb6c26839111f867f4dc


### Diffusion autoencoders: Toward a meaningful and decodable representation
 - title-short: Diffusion autoencoders
 - **type:** article-journal
 - **url:** <https://www.semanticscholar.org/paper/b582edb16f5425642767cb6c26839111f867f4dc>
 - **volume:** null
 - **abstract:** We show that cascaded diffusion models are capable of
    generating high fidelity images on the class-conditional ImageNet
    generation benchmark, without any assistance from auxiliary image
    classifiers to boost sample quality. A cascaded diffusion model
    comprises a pipeline of multiple diffusion models that generate
    images of increasing resolution, beginning with a standard diffusion
    model at the lowest resolution, followed by one or more
    super-resolution diffusion models that successively upsample the
    image and add higher resolution details. We find that the sample
    quality of a cascading pipeline relies crucially on conditioning
    augmentation, our proposed method of data augmentation of the lower
    resolution conditioning inputs to the super-resolution models. Our
    experiments show that conditioning augmentation prevents compounding
    error during sampling in a cascaded model, helping us to train
    cascading pipelines achieving FID scores of 1.48 at 64x64, 3.52 at
    128x128 and 4.88 at 256x256 resolutions, outperforming BigGAN-deep,
    and classification accuracy scores of 63.02
 - **container-Paper Title:** J. Mach. Learn. Res.
 - **id:** 0f183bcfe65781c06b1a48a6f56e0f3c63e8e4a4


### Cascaded diffusion models for high fidelity image generation
 - **type:** article-journal
 - **url:** <https://www.semanticscholar.org/paper/0f183bcfe65781c06b1a48a6f56e0f3c63e8e4a4>
 - **volume:** 23
 - **abstract:** Generating temporally coherent high fidelity video is an
    important milestone in generative modeling research. We make
    progress towards this milestone by proposing a diffusion model for
    video generation that shows very promising initial results. Our
    model is a natural extension of the standard image diffusion
    architecture, and it enables jointly training from image and video
    data, which we find to reduce the variance of minibatch gradients
    and speed up optimization. To generate long and higher resolution
    videos we introduce a new conditional sampling technique for spatial
    and temporal video extension that performs better than previously
    proposed methods. We present the first results on a large
    text-conditioned video generation task, as well as state-of-the-art
    results on established benchmarks for video prediction and
    unconditional video generation. Supplementary material is available
    at <https://video-diffusion.github.io/>
 - **container-Paper Title:** ArXiv
 - **doi:** 10.48550/arXiv.2204.03458
 - **id:** 3b2a675bb617ae1a920e8e29d535cdf27826e999


### Video diffusion models
 - **type:** article-journal
 - **url:** <https://www.semanticscholar.org/paper/3b2a675bb617ae1a920e8e29d535cdf27826e999>
 - **volume:** abs/2204.03458
 - **abstract:** Denoising diffusion probabilistic models (DDPMs) (Ho et al.
    2020) have shown impressive results on image and waveform generation
    in continuous state spaces. Here, we introduce Discrete Denoising
    Diffusion Probabilistic Models (D3PMs), diffusion-like generative
    models for discrete data that generalize the multinomial diffusion
    model of Hoogeboom et al. 2021, by going beyond corruption processes
    with uniform transition probabilities. This includes corruption with
    transition matrices that mimic Gaussian kernels in continuous space,
    matrices based on nearest neighbors in embedding space, and matrices
    that introduce absorbing states. The third allows us to draw a
    connection between diffusion models and autoregressive and
    mask-based generative models. We show that the choice of transition
    matrix is an important design decision that leads to improved
    results in image and text domains. We also introduce a new loss
    function that combines the variational lower bound with an auxiliary
    cross entropy loss. For text, this model class achieves strong
    results on character-level text generation while scaling to large
    vocabularies on LM1B. On the image dataset CIFAR-10, our models
    approach the sample quality and exceed the log-likelihood of the
    continuous-space DDPM model.
 - **container-Paper Title:** ArXiv
 - **id:** 91b32fc0a23f0af53229fceaae9cce43a0406d2e


### Structured denoising diffusion models in discrete state-spaces
 - **type:** article-journal
 - **url:** <https://www.semanticscholar.org/paper/91b32fc0a23f0af53229fceaae9cce43a0406d2e>
 - **volume:** abs/2107.03006
 - **abstract:** Diffusion-based generative models have demonstrated a
    capacity for perceptually impressive synthesis, but can they also be
    great likelihood-based models? We answer this in the affirmative,
    and introduce a family of diffusion-based generative models that
    obtain state-of-the-art likelihoods on standard image density
    estimation benchmarks. Unlike other diffusion-based models, our
    method allows for efficient optimization of the noise schedule
    jointly with the rest of the model. We show that the variational
    lower bound (VLB) simplifies to a remarkably short expression in
    terms of the signal-to-noise ratio of the diffused data, thereby
    improving our theoretical understanding of this model class. Using
    this insight, we prove an equivalence between several models
    proposed in the literature. In addition, we show that the
    continuous-time VLB is invariant to the noise schedule, except for
    the signal-to-noise ratio at its endpoints. This enables us to learn
    a noise schedule that minimizes the variance of the resulting VLB
    estimator, leading to faster optimization. Combining these advances
    with architectural improvements, we obtain state-of-the-art
    likelihoods on image density estimation benchmarks, outperforming
    autoregressive models that have dominated these benchmarks for many
    years, with often significantly faster optimization. In addition, we
    show how to use the model as part of a bits-back compression scheme,
    and demonstrate lossless compression rates close to the theoretical
    optimum. Code is available at <https://github.com/google-research/vdm.>
 - **container-Paper Title:** ArXiv
 - **id:** e2db22251792e9dd809d5ffb0feaab50a687cdb0


### Variational diffusion models
 - **type:** article-journal
 - **url:** <https://www.semanticscholar.org/paper/e2db22251792e9dd809d5ffb0feaab50a687cdb0>
 - **volume:** abs/2107.00630
 - **abstract:** Score-based generative models can produce high quality image
    samples comparable to GANs, without requiring adversarial
    optimization. However, existing training procedures are limited to
    images of low resolution (typically below 32x32), and can be
    unstable under some settings. We provide a new theoretical analysis
    of learning and sampling from score models in high dimensional
    spaces, explaining existing failure modes and motivating new
    solutions that generalize across datasets. To enhance stability, we
    also propose to maintain an exponential moving average of model
    weights. With these improvements, we can effortlessly scale
    score-based generative models to images with unprecedented
    resolutions ranging from 64x64 to 256x256. Our score-based models
    can generate high-fidelity samples that rival best-in-class GANs on
    various image datasets, including CelebA, FFHQ, and multiple LSUN
    categories.
 - **container-Paper Title:** ArXiv
 - **id:** 1156e277fa7ec195b043161d3c5c97715da17658


### Improved techniques for training score-based generative models
 - **type:** article-journal
 - **url:** <https://www.semanticscholar.org/paper/1156e277fa7ec195b043161d3c5c97715da17658>
 - **volume:** abs/2006.09011
 - **abstract:** Recent text-to-image generation methods provide a simple
    yet exciting conversion capability between text and image domains.
    While these methods have incrementally improved the generated image
    fidelity and text relevancy, several pivotal gaps remain unanswered,
    limiting applicability and quality. We propose a novel text-to-image
    method that addresses these gaps by (i) enabling a simple control
    mechanism complementary to text in the form of a scene, (ii)
    introducing elements that substantially improve the tokenization
    process by employing domain-specific knowledge over key image
    regions (faces and salient objects), and (iii) adapting
    classifier-free guidance for the transformer use case. Our model
    achieves state-of-the-art FID and human evaluation results,
    unlocking the ability to generate high fidelity images in a
    resolution of 512x512 pixels, significantly improving visual
    quality. Through scene controllability, we introduce several new
    capabilities: (i) Scene editing, (ii) text editing with anchor
    scenes, (iii) overcoming out-of-distribution text prompts, and (iv)
    story illustration generation, as demonstrated in the story we
    wrote.
 - **container-Paper Title:** ArXiv
 - **doi:** 10.48550/arXiv.2203.13131
 - **id:** 15e234a67f30d6761f1d7670d501095d1697b69c


### Make-a-scene: Scene-based text-to-image generation with human priors
 - title-short: Make-a-scene
 - **type:** article-journal
 - **url:** <https://www.semanticscholar.org/paper/15e234a67f30d6761f1d7670d501095d1697b69c>
 - **volume:** abs/2203.13131
 - **abstract:** Diffusion models have recently been shown to generate
    high-quality synthetic images, especially when paired with a
    guidance technique to trade off diversity for fidelity. We explore
    diffusion models for the problem of text-conditional image synthesis
    and compare two different guidance strategies: CLIP guidance and
    classifier-free guidance. We find that the latter is preferred by
    human evaluators for both photorealism and caption similarity, and
    often produces photorealistic samples. Samples from a 3.5 billion
    parameter text-conditional diffusion model using classifier-free
    guidance are favored by human evaluators to those from DALL-E, even
    when the latter uses expensive CLIP reranking. Additionally, we find
    that our models can be fine-tuned to perform image inpainting,
    enabling powerful text-driven image editing. We train a smaller
    model on a filtered dataset and release the code and weights at
    <https://github.com/openai/glide-text2im.>
 - **id:** 7002ae048e4b8c9133a55428441e8066070995cb


### GLIDE: Towards photorealistic image generation and editing with text-guided diffusion models
 - title-short: GLIDE
 - **type:** article-journal
 - **url:** <https://www.semanticscholar.org/paper/7002ae048e4b8c9133a55428441e8066070995cb>
 - **abstract:** We present the Pathways Autoregressive Text-to-Image
    (Parti) model, which generates high-fidelity photorealistic images
    and supports content-rich synthesis involving complex compositions
    and world knowledge. Parti treats text-to-image generation as a
    sequence-to-sequence modeling problem, akin to machine translation,
    with sequences of image tokens as the target outputs rather than
    text tokens in another language. This strategy can naturally tap
    into the rich body of prior work on large language models, which
    have seen continued advances in capabilities and performance through
    scaling data and model sizes. Our approach is simple: First, Parti
    uses a Transformer-based image tokenizer, ViT-VQGAN, to encode
    images as sequences of discrete tokens. Second, we achieve
    consistent quality improvements by scaling the encoder-decoder
    Transformer model up to 20B parameters, with a new state-of-the-art
    zero-shot FID score of 7.23 and finetuned FID score of 3.22 on
    MS-COCO. Our detailed analysis on Localized Narratives as well as
    PartiPrompts (P2), a new holistic benchmark of over 1600 English
    prompts, demonstrate the effectiveness of Parti across a wide
    variety of categories and difficulty aspects. We also explore and
    highlight limitations of our models in order to define and exemplify
    key areas of focus for further improvements. See
    <https://parti.research.google/> for high-resolution images.
 - **container-Paper Title:** ArXiv
 - **doi:** 10.48550/arXiv.2206.10789
 - **id:** 1243e13254bb4ea1f71b4be8a3e4e54ffd02d2fe


### Scaling autoregressive models for content-rich text-to-image generation
 - **type:** article-journal
 - **url:** <https://www.semanticscholar.org/paper/1243e13254bb4ea1f71b4be8a3e4e54ffd02d2fe>
 - **volume:** abs/2206.10789
 - **abstract:** Text-to-image generation has traditionally focused on
    finding better modeling assumptions for training on a fixed dataset.
    These assumptions might involve complex architectures, auxiliary
    losses, or side information such as object part labels or
    segmentation masks supplied during training. We describe a simple
    approach for this task based on a transformer that autoregressively
    models the text and image tokens as a single stream of data. With
    sufficient data and scale, our approach is competitive with previous
    domain-specific models when evaluated in a zero-shot fashion.
 - **container-Paper Title:** ArXiv
 - **id:** 2cd605106b88c85d7d8b865b1ef0f8c8293debf1


### Zero-shot text-to-image generation
 - **type:** article-journal
 - **url:** <https://www.semanticscholar.org/paper/2cd605106b88c85d7d8b865b1ef0f8c8293debf1>
 - **volume:** abs/2102.12092
 - **abstract:** Autoregressive models and their sequential factorization of
    the data likelihood have recently demonstrated great potential for
    image representation and synthesis. Nevertheless, they incorporate
    image context in a linear 1D order by attending only to previously
    synthesized image patches above or to the left. Not only is this
    unidirectional, sequential bias of attention unnatural for images as
    it disregards large parts of a scene until synthesis is almost
    complete. It also processes the entire image on a single scale, thus
    ignoring more global contextual information up to the gist of the
    entire scene. As a remedy we incorporate a coarse-to-fine hierarchy
    of context by combining the autoregressive formulation with a
    multinomial diffusion process: Whereas a multistage diffusion
    process successively removes information to coarsen an image, we
    train a (short) Markov chain to invert this process. In each stage,
    the resulting autoregressive ImageBART model progressively
    incorporates context from previous stages in a coarse-to-fine
    manner. Experiments show greatly improved image modification
    capabilities over autoregressive models while also providing
    high-fidelity image generation, both of which are enabled through
    efficient training in a compressed latent space. Specifically, our
    approach can take unrestricted, user-provided masks into account to
    perform local image editing. Thus, in contrast to pure
    autoregressive models, it can solve free-form image inpainting and,
    in the case of conditional models, local, text-guided image
    modification without requiring mask-specific training.
 - **container-Paper Title:** ArXiv
 - **id:** 426c9d639c11514df7ba6e96d2343695561ba0eb


### ImageBART: Bidirectional context with multinomial diffusion for autoregressive image synthesis
 - title-short: ImageBART
 - **type:** article-journal
 - **url:** <https://www.semanticscholar.org/paper/426c9d639c11514df7ba6e96d2343695561ba0eb>
 - **volume:** abs/2108.08827
 - **abstract:** Denoising diffusion probabilistic models (DDPMs) have
    achieved high quality image generation without adversarial training,
    yet they require simulating a Markov chain for many steps to produce
    a sample. To accelerate sampling, we present denoising diffusion
    implicit models (DDIMs), a more efficient class of iterative
    implicit probabilistic models with the same training procedure as
    DDPMs. In DDPMs, the generative process is defined as the reverse of
    a Markovian diffusion process. We construct a class of non-Markovian
    diffusion processes that lead to the same training objective, but
    whose reverse process can be much faster to sample from. We
    empirically demonstrate that DDIMs can produce high quality samples
    $10 \times$ to $50 \times$ faster in terms of wall-clock time
    compared to DDPMs, allow us to trade off computation for sample
    quality, and can perform semantically meaningful image interpolation
    directly in the latent space.
 - **container-Paper Title:** ArXiv
 - **id:** 014576b866078524286802b1d0e18628520aa886


### Denoising diffusion implicit models
 - **type:** article-journal
 - **url:** <https://www.semanticscholar.org/paper/014576b866078524286802b1d0e18628520aa886>
 - **volume:** abs/2010.02502
 - **abstract:** A wide variety of deep generative models has been developed
    in the past decade. Yet, these models often struggle with
    simultaneously addressing three key requirements including: high
    sample quality, mode coverage, and fast sampling. We call the
    challenge imposed by these requirements the generative learning
    trilemma, as the existing models often trade some of them for
    others. Particularly, denoising diffusion models have shown
    impressive sample quality and diversity, but their expensive
    sampling does not yet allow them to be applied in many real-world
    applications. In this paper, we argue that slow sampling in these
    models is fundamentally attributed to the Gaussian assumption in the
    denoising step which is justified only for small step sizes. To
    enable denoising with large steps, and hence, to reduce the total
    number of denoising steps, we propose to model the denoising
    distribution using a complex multimodal distribution. We introduce
    denoising diffusion generative adversarial networks (denoising
    diffusion GANs) that model each denoising step using a multimodal
    conditional GAN. Through extensive evaluations, we show that
    denoising diffusion GANs obtain sample quality and diversity
    competitive with original diffusion models while being 2000× faster
    on the CIFAR-10 dataset. Compared to traditional GANs, our model
    exhibits better mode coverage and sample diversity. To the best of
    our knowledge, denoising diffusion GAN is the first model that
    reduces sampling cost in diffusion models to an extent that allows
    them to be applied to real-world applications inexpensively. Project
    page and code: <https://nvlabs.github.io/denoising-diffusion-gan.>
 - **container-Paper Title:** ArXiv
 - **id:** 0d4154cbd76c4753ba3cb7a5b89ab29bab53384f


### Tackling the generative learning trilemma with denoising diffusion GANs
 - **type:** article-journal
 - **url:** <https://www.semanticscholar.org/paper/0d4154cbd76c4753ba3cb7a5b89ab29bab53384f>
 - **volume:** abs/2112.07804
 - **abstract:** Classifier guidance is a recently introduced method to
    trade off mode coverage and sample fidelity in conditional diffusion
    models post training, in the same spirit as low temperature sampling
    or truncation in other types of generative models. Classifier
    guidance combines the score estimate of a diffusion model with the
    gradient of an image classifier and thereby requires training an
    image classifier separate from the diffusion model. It also raises
    the question of whether guidance can be performed without a
    classifier. We show that guidance can be indeed performed by a pure
    generative model without such a classifier: in what we call
    classifier-free guidance, we jointly train a conditional and an
    unconditional diffusion model, and we combine the resulting
    conditional and unconditional score estimates to attain a trade-off
    between sample quality and diversity similar to that obtained using
    classifier guidance.
 - **container-Paper Title:** ArXiv
 - **doi:** 10.48550/arXiv.2207.12598
 - **id:** af9f365ed86614c800f082bd8eb14be76072ad16


### Classifier-free diffusion guidance
 - **type:** article-journal
 - **url:** <https://www.semanticscholar.org/paper/af9f365ed86614c800f082bd8eb14be76072ad16>
 - **volume:** abs/2207.12598
 - **abstract:** Contrastive models like CLIP have been shown to learn
    robust representations of images that capture both semantics and
    style. To leverage these representations for image generation, we
    propose a two-stage model: a prior that generates a CLIP image
    embedding given a text caption, and a decoder that generates an
    image conditioned on the image embedding. We show that explicitly
    generating image representations improves image diversity with
    minimal loss in photorealism and caption similarity. Our decoders
    conditioned on image representations can also produce variations of
    an image that preserve both its semantics and style, while varying
    the non-essential details absent from the image representation.
    Moreover, the joint embedding space of CLIP enables language-guided
    image manipulations in a zero-shot fashion. We use diffusion models
    for the decoder and experiment with both autoregressive and
    diffusion models for the prior, finding that the latter are
    computationally more efficient and produce higher-quality samples.
 - **container-Paper Title:** ArXiv
 - **doi:** 10.48550/arXiv.2204.06125
 - **id:** c57293882b2561e1ba03017902df9fc2f289dea2


### Hierarchical text-conditional image generation with CLIP latents
 - **type:** article-journal
 - **url:** <https://www.semanticscholar.org/paper/c57293882b2561e1ba03017902df9fc2f289dea2>
 - **volume:** abs/2204.06125
 - **abstract:** We present Muse, a text-to-image Transformer model that
    achieves state-of-the-art image generation performance while being
    significantly more efficient than diffusion or autoregressive
    models. Muse is trained on a masked modeling task in discrete token
    space: given the text embedding extracted from a pre-trained large
    language model (LLM), Muse is trained to predict randomly masked
    image tokens. Compared to pixel-space diffusion models, such as
    Imagen and DALL-E 2, Muse is significantly more efficient due to the
    use of discrete tokens and requiring fewer sampling iterations;
    compared to autoregressive models, such as Parti, Muse is more
    efficient due to the use of parallel decoding. The use of a
    pre-trained LLM enables fine-grained language understanding,
    translating to high-fidelity image generation and the understanding
    of visual concepts such as objects, their spatial relationships,
    pose, cardinality etc. Our 900M parameter model achieves a new SOTA
    on CC3M, with an FID score of 6.06. The Muse 3B parameter model
    achieves an FID of 7.88 on zero-shot COCO evaluation, along with a
    CLIP score of 0.32. Muse also directly enables a number of image
    editing applications without the need to fine-tune or invert the
    model: inpainting, outpainting, and mask-free editing. More results
    are available at <https://muse-model.github.io>
 - **container-Paper Title:** ArXiv
 - **doi:** 10.48550/arXiv.2301.00704
 - **id:** 2a3213cb3c755f036d5dfec7261d726a819c78c1


### Muse: Text-to-image generation via masked generative transformers
 - title-short: Muse
 - **type:** article-journal
 - **url:** <https://www.semanticscholar.org/paper/2a3213cb3c755f036d5dfec7261d726a819c78c1>
 - **volume:** abs/2301.00704
 - **abstract:** In this work, we propose DiffWave, a versatile Diffusion
    probabilistic model for conditional and unconditional Waveform
    generation. The model is non-autoregressive, and converts the white
    noise signal into structured waveform through a Markov chain with a
    constant number of steps at synthesis. It is efficiently trained by
    optimizing a variant of variational bound on the data likelihood.
    DiffWave produces high-fidelity audios in Different Waveform
    generation tasks, including neural vocoding conditioned on mel
    spectrogram, class-conditional generation, and unconditional
    generation. We demonstrate that DiffWave matches a strong WaveNet
    vocoder in terms of speech quality (MOS: 4.44 versus 4.43), while
    synthesizing orders of magnitude faster. In particular, it
    significantly outperforms autoregressive and GAN-based waveform
    models in the challenging unconditional generation task in terms of
    audio quality and sample diversity from various automatic and human
    evaluations.
 - **container-Paper Title:** ArXiv
 - **id:** 34bf13e58c7226d615afead0c0f679432502940e


### DiffWave: A versatile diffusion model for audio synthesis
 - title-short: DiffWave
 - **type:** article-journal
 - **url:** <https://www.semanticscholar.org/paper/34bf13e58c7226d615afead0c0f679432502940e>
 - **volume:** abs/2009.09761
 - **abstract:** Denoising diffusion probabilistic models (DDPM) are a class
    of generative models which have recently been shown to produce
    excellent samples. We show that with a few simple modifications,
    DDPMs can also achieve competitive log-likelihoods while maintaining
    high sample quality. Additionally, we find that learning variances
    of the reverse diffusion process allows sampling with an order of
    magnitude fewer forward passes with a negligible difference in
    sample quality, which is important for the practical deployment of
    these models. We additionally use precision and recall to compare
    how well DDPMs and GANs cover the target distribution. Finally, we
    show that the sample quality and likelihood of these models scale
    smoothly with model capacity and training compute, making them
    easily scalable. We release our code at
    <https://github.com/openai/improved-diffusion>
 - **container-Paper Title:** ArXiv
 - **id:** de18baa4964804cf471d85a5a090498242d2e79f


### Improved denoising diffusion probabilistic models
 - **type:** article-journal
 - **url:** <https://www.semanticscholar.org/paper/de18baa4964804cf471d85a5a090498242d2e79f>
 - **volume:** abs/2102.09672
 - **abstract:** Diffusion models (DMs) have shown great potential for
    high-quality image synthesis. However, when it comes to producing
    images with complex scenes, how to properly describe both image
    global structures and object details remains a challenging task. In
    this paper, we present Frido, a Feature Pyramid Diffusion model
    performing a multi-scale coarse-to-fine denoising process for image
    synthesis. Our model decomposes an input image into scale-dependent
    vector quantized features, followed by a coarse-to-fine gating for
    producing image output. During the above multi-scale representation
    learning stage, additional input conditions like text, scene graph,
    or image layout can be further exploited. Thus, Frido can be also
    applied for conditional or cross-modality image synthesis. We
    conduct extensive experiments over various unconditioned and
    conditional image generation tasks, ranging from text-to-image
    synthesis, layout-to-image, scene-graph-to-image, to label-to-image.
    More specifically, we achieved state-of-the-art FID scores on five
    benchmarks, namely layout-to-image on COCO and OpenImages,
    scene-graph-to-image on COCO and Visual Genome, and label-to-image
    on COCO. Code is available at
    <https://github.com/davidhalladay/Frido.>
 - **container-Paper Title:** ArXiv
 - **doi:** 10.48550/arXiv.2208.13753
 - **id:** fd58295c7146a668caba43880fe03247c4e24b51


### Frido: Feature pyramid diffusion for complex scene image synthesis
 - title-short: Frido
 - **type:** article-journal
 - **url:** <https://www.semanticscholar.org/paper/a888dd6d8dd0087fc7d74da8a005922d0923ad2b>
 - **volume:** abs/2208.13753
 - **abstract:** Score-based generative models (SGMs) have recently
    demonstrated impressive results in terms of both sample quality and
    distribution coverage. However, they are usually applied directly in
    data space and often require thousands of network evaluations for
    sampling. Here, we propose the Latent Score-based Generative Model
    (LSGM), a novel approach that trains SGMs in a latent space, relying
    on the variational autoencoder framework. Moving from data to latent
    space allows us to train more expressive generative models, apply
    SGMs to non-continuous data, and learn smoother SGMs in a smaller
    space, resulting in fewer network evaluations and faster sampling.
    To enable training LSGMs end-to-end in a scalable and stable manner,
    we (i) introduce a new score-matching objective suitable to the LSGM
    setting, (ii) propose a novel parameterization of the score function
    that allows SGM to focus on the mismatch of the target distribution
    with respect to a simple Normal one, and (iii) analytically derive
    multiple techniques for variance reduction of the training
    objective. LSGM obtains a state-of-the-art FID score of 2.10 on
    CIFAR-10, outperforming all existing generative results on this
    dataset. On CelebA-HQ-256, LSGM is on a par with previous SGMs in
    sample quality while outperforming them in sampling time by two
    orders of magnitude. In modeling binary images, LSGM achieves
    state-of-the-art likelihood on the binarized OMNIGLOT dataset. Our
    project page and code can be found at <https://nvlabs.github.io/LSGM.>
 - **id:** ad14e11bc97cc2fed0fd344e7cb7d7ce4205bfc6


### Score-based generative modeling in latent space
 - **type:** article-journal
 - **url:** <https://www.semanticscholar.org/paper/ad14e11bc97cc2fed0fd344e7cb7d7ce4205bfc6>
 - **abstract:** Designed to learn long-range interactions on sequential
    data, transformers continue to show state-of-the-art results on a
    wide variety of tasks. In contrast to CNNs, they contain no
    inductive bias that prioritizes local interactions. This makes them
    expressive, but also computationally infeasible for long sequences,
    such as high-resolution images. We demonstrate how combining the
    effectiveness of the inductive bias of CNNs with the expressivity of
    transformers enables them to model and thereby synthesize
    high-resolution images. We show how to (i) use CNNs to learn a
    context-rich vocabulary of image constituents, and in turn (ii)
    utilize transformers to efficiently model their composition within
    high-resolution images. Our approach is readily applied to
    conditional synthesis tasks, where both non-spatial information,
    such as object classes, and spatial information, such as
    segmentations, can control the generated image. In particular, we
    present the first results on semantically-guided synthesis of
    megapixel images with transformers. Project page at
    <https://git.io/JLlvY.>
 - **container-Paper Title:** 2021 IEEE/CVF Conference on Computer Vision and
    Pattern Recognition (CVPR)
 - **doi:** 10.1109/CVPR46437.2021.01268
 - **id:** 47f7ec3d0a5e6e83b6768ece35206a94dc81919c


### Taming transformers for high-resolution image synthesis
 - **type:** article-journal
 - **url:** <https://www.semanticscholar.org/paper/47f7ec3d0a5e6e83b6768ece35206a94dc81919c>
 - **volume:** null
 - **abstract:** The integration of Vector Quantised Variational AutoEncoder
    (VQ-VAE) with autoregressive models as generation part has yielded
    high-quality results on image generation. However, the
    autoregressive models will strictly follow the progressive scanning
    order during the sampling phase. This leads the existing VQ series
    models to hardly escape the trap of lacking global information.
    Denoising Diffusion Probabilistic Models (DDPM) in the continuous
    domain have shown a capability to capture the global context, while
    generating high-quality images. In the discrete state space, some
    works have demonstrated the potential to perform text generation and
    low resolution image generation. We show that with the help of a
    content-rich discrete visual codebook from VQ-VAE, the discrete
    diffusion model can also generate high fidelity images with global
    context, which compensates for the deficiency of the classical
    autoregressive model along pixel space. Meanwhile, the integration
    of the discrete VAE with the diffusion model resolves the drawback
    of conventional autoregressive models being oversized, and the
    diffusion model which demands excessive time in the sampling process
    when generating images. It is found that the quality of the
    generated images is heavily dependent on the discrete visual
    codebook. Extensive experiments demonstrate that the proposed Vector
    Quantised Discrete Diffusion Model (VQ-DDM) is able to achieve
    comparable performance to top-tier methods with low complexity. It
    also demonstrates outstanding advantages over other vectors
    quantised with autoregressive models in terms of image inpainting
    tasks without additional training.
 - **container-Paper Title:** 2022 IEEE/CVF Conference on Computer Vision and
    Pattern Recognition (CVPR)
 - **doi:** 10.1109/CVPR52688.2022.01121
 - **id:** 64ac9c65c8f1e0a96a6d79facf548214103d0cbc


### Global context with discrete diffusion in vector quantised modelling for image generation
 - **type:** article-journal
 - **url:** <https://www.semanticscholar.org/paper/64ac9c65c8f1e0a96a6d79facf548214103d0cbc>
 - **volume:** null
 - **abstract:** We introduce a new generative model where samples are
    produced via Langevin dynamics using gradients of the data
    distribution estimated with score matching. Because gradients can be
    ill-defined and hard to estimate when the data resides on
    low-dimensional manifolds, we perturb the data with different levels
    of Gaussian noise, and jointly estimate the corresponding scores,
    i.e., the vector fields of gradients of the perturbed data
    distribution for all noise levels. For sampling, we propose an
    annealed Langevin dynamics where we use gradients corresponding to
    gradually decreasing noise levels as the sampling process gets
    closer to the data manifold. Our framework allows flexible model
    architectures, requires no sampling during training or the use of
    adversarial methods, and provides a learning objective that can be
    used for principled model comparisons. Our models produce samples
    comparable to GANs on MNIST, CelebA and CIFAR-10 datasets, achieving
    a new state-of-the-art inception score of 8.87 on CIFAR-10.
    Additionally, we demonstrate that our models learn effective
    representations via image inpainting experiments.
 - **container-Paper Title:** ArXiv
 - **id:** 965359b3008ab50dd04e171551220ec0e7f83aba


### Generative modeling by estimating gradients of the data distribution
 - **type:** article-journal
 - **url:** <https://www.semanticscholar.org/paper/965359b3008ab50dd04e171551220ec0e7f83aba>
 - **volume:** abs/1907.05600
 - **abstract:** Generative image synthesis with diffusion models has
    recently achieved excellent visual quality in several tasks such as
    text-based or class-conditional image synthesis. Much of this
    success is due to a dramatic increase in the computational capacity
    invested in training these models. This work presents an alternative
    approach: inspired by its successful application in natural language
    processing, we propose to complement the diffusion model with a
    retrieval-based approach and to introduce an explicit memory in the
    form of an external database. During training, our diffusion model
    is trained with similar visual features retrieved via CLIP and from
    the neighborhood of each training instance. By leveraging CLIP's
    joint image-text embedding space, our model achieves highly
    competitive performance on tasks for which it has not been
    explicitly trained, such as class-conditional or text-image
    synthesis, and can be conditioned on both text and image embeddings.
    Moreover, we can apply our approach to unconditional generation,
    where it achieves state-of-the-art performance. Our approach incurs
    low computational and memory overheads and is easy to implement. We
    discuss its relationship to concurrent work and will publish code
    and pretrained models soon.
 - **container-Paper Title:** ArXiv
 - **doi:** 10.48550/arXiv.2204.11824
 - **id:** a55d097b30bc881ec859a00ca00c34e33f247caf


### Retrieval-augmented diffusion models
 - **type:** article-journal
 - **url:** <https://www.semanticscholar.org/paper/33f3f31f871070f19b0c3e967a24e322bfc178f2>
 - **volume:** abs/2204.11824
 - **abstract:** Creating noise from data is easy; creating data from noise
    is generative modeling. We present a stochastic differential
    equation (SDE) that smoothly transforms a complex data distribution
    to a known prior distribution by slowly injecting noise, and a
    corresponding reverse-time SDE that transforms the prior
    distribution back into the data distribution by slowly removing the
    noise. Crucially, the reverse-time SDE depends only on the
    time-dependent gradient field, score of the
    perturbed data distribution. By leveraging advances in score-based
    generative modeling, we can accurately estimate these scores with
    neural networks, and use numerical SDE solvers to generate samples.
    We show that this framework encapsulates previous approaches in
    score-based generative modeling and diffusion probabilistic
    modeling, allowing for new sampling procedures and new modeling
    capabilities. In particular, we introduce a predictor-corrector
    framework to correct errors in the evolution of the discretized
    reverse-time SDE. We also derive an equivalent neural ODE that
    samples from the same distribution as the SDE, but additionally
    enables exact likelihood computation, and improved sampling
    efficiency. In addition, we provide a new way to solve inverse
    problems with score-based models, as demonstrated with experiments
    on class-conditional generation, image inpainting, and colorization.
    Combined with multiple architectural improvements, we achieve
    record-breaking performance for unconditional image generation on
    CIFAR-10 with an Inception score of 9.89 and FID of 2.20, a
    competitive likelihood of 2.99 bits/dim, and demonstrate high
    fidelity generation of 1024 x 1024 images for the first time from a
    score-based generative model.
 - **container-Paper Title:** ArXiv
 - **id:** 633e2fbfc0b21e959a244100937c5853afca4853


### Score-based generative modeling through stochastic differential equations
 - **type:** article-journal
 - **url:** <https://www.semanticscholar.org/paper/633e2fbfc0b21e959a244100937c5853afca4853>
 - **volume:** abs/2011.13456
 - **abstract:** We present SR3, an approach to image Super-Resolution via
    Repeated Refinement. SR3 adapts denoising diffusion probabilistic
    models (Ho et al. 2020), (Sohl-Dickstein et al. 2015) to
    image-to-image translation, and performs super-resolution through a
    stochastic iterative denoising process. Output images are
    initialized with pure Gaussian noise and iteratively refined using a
    U-Net architecture that is trained on denoising at various noise
    levels, conditioned on a low-resolution input image. SR3 exhibits
    strong performance on super-resolution tasks at different
    magnification factors, on faces and natural images. We conduct human
    evaluation on a standard 8× face super-resolution task on CelebA-HQ
    for which SR3 achieves a fool rate close to 50
 - **container-Paper Title:** IEEE Transactions on Pattern Analysis and Machine
    Intelligence
 - **doi:** 10.1109/TPAMI.2022.3204461
 - **id:** 8a1ea7b6e7e834d146ad782be5d63f57f806a9cc36094974


### Image super-resolution via iterative refinement
 - **type:** article-journal
 - **url:** <https://www.semanticscholar.org/paper/8a1ea7b6e7e834d146ad782be5d63f57f806a9cc>
 - **volume:** 45
 - **abstract:** Novel architectures have recently improved generative image
    synthesis leading to excellent visual quality in various tasks. Much
    of this success is due to the scalability of these architectures and
    hence caused by a dramatic increase in model complexity and in the
    computational resources invested in training these models. Our work
    questions the underlying paradigm of compressing large training data
    into ever growing parametric representations. We rather present an
    orthogonal, semi-parametric approach. We complement comparably small
    diffusion or autoregressive models with a separate image database
    and a retrieval strategy. During training we retrieve a set of
    nearest neighbors from this external database for each training
    instance and condition the generative model on these informative
    samples. While the retrieval approach is providing the (local)
    content, the model is focusing on learning the composition of scenes
    based on this content. As demonstrated by our experiments, simply
    swapping the database for one with different contents transfers a
    trained model post-hoc to a novel domain. The evaluation shows
    competitive performance on tasks which the generative model has not
    been trained on, such as class-conditional synthesis, zero-shot
    stylization or text-to-image synthesis without requiring paired
    text-image data. With negligible memory and computational overhead
    for the external database and retrieval we can significantly reduce
    the parameter count of the generative model and still outperform the
    state-of-the-art.
 - **id:** 0221d3f45899e226ba7840ca9b19117de3a394bc


### Semi-parametric neural image synthesis
 - **type:** article-journal
 - **url:** <https://www.semanticscholar.org/paper/0221d3f45899e226ba7840ca9b19117de3a394bc>
 - **abstract:** Diffusion models learn to restore noisy data, which is
    corrupted with different levels of noise, by optimizing the weighted
    sum of the corresponding loss terms, i.e., denoising score matching
    loss. In this paper, we show that restoring data corrupted with
    certain noise levels offers a proper pretext task for the model to
    learn rich visual concepts. We propose to prioritize such noise
    levels over other levels during training, by redesigning the
    weighting scheme of the objective function. We show that our simple
    redesign of the weighting scheme significantly improves the
    performance of diffusion models regardless of the datasets,
    architectures, and sampling strategies.
 - **container-Paper Title:** 2022 IEEE/CVF Conference on Computer Vision and
    Pattern Recognition (CVPR)
 - **doi:** 10.1109/CVPR52688.2022.01118
 - **id:** 580086afeb62eb0303611daaf6de7ca9d1ae29cd


### Perception Prioritized Training of Diffusion Models
 - **type:** article-journal
 - **url:** <https://www.semanticscholar.org/paper/580086afeb62eb0303611daaf6de7ca9d1ae29cd>
 - **abstract:** Diffusion models learn to restore noisy data which is corrupted with different levels of noise by optimizing the weighted sum of the corresponding loss terms i.e. denoising score matching loss. In this paper we show that restoring data corrupted with certain noise levels offers a proper pretext task for the model to learn rich visual concepts. We propose to prioritize such noise levels over other levels during training by redesigning the weighting scheme of the objective function. We show that our simple redesign of the weighting scheme significantly improves the performance of diffusion models regardless of the datasets architectures and sampling strategies.
 - **journal:** 2022 IEEE/CVF Conference on Computer Vision and Pattern Recognition (CVPR)
 - **volume:** null
 - **pages:** 11462-11471
 - **doi:** 10.1109/CVPR52688.2022.01118
 - **arxivid:** 2204.00227