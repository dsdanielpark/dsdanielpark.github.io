---
title: LLM Reports
author: Daniel Park
date: 2023-06-21
category: llm
layout: post
---

- Related Project: private 
- Project Status: 1 Alpha
- Date: 2023-06-21


### Preface

Links
- Hugging Face [Open Source LLM Leader Board](https://huggingface.co/spaces/HuggingFaceH4/open_llm_leaderboard)
- [Visuallization report of open-source LLM leader board](https://github.com/dsdanielpark/Open-LLM-Leaderboard-Report)


 Various methods have been proposed regarding the performance evaluation of Large Language Models (LLMs). To understand how LLMs are evaluated and the evaluation methods employed, we intend to examine the quantitative metrics and qualitative evaluation approaches presented in each LLM paper.
 
 Hugging Face's Open LLM Leaderboard serves as a prominent Docker space for quantitative evaluation of LLMs. Hugging Face established an online Docker space called the Open LLM Leaderboard a few days prior to the release of Falcon. It ranks open-source LLMs based on quantitative metrics for four datasets in the Docker space.

 ```python
METRICS = ["acc_norm", "acc_norm", "acc_norm", "mc2"]
BENCHMARKS = ["arc_challenge", "hellaswag", "hendrycks", "truthfulqa_mc"]
BENCH_TO_NAME = {
    "arc_challenge": AutoEvalColumn.arc.name,
    "hellaswag": AutoEvalColumn.hellaswag.name,
    "hendrycks": AutoEvalColumn.mmlu.name,
    "truthfulqa_mc": AutoEvalColumn.truthfulqa.name,
}
 ```
 **Refer: <https://huggingface.co/spaces/HuggingFaceH4/open_llm_leaderboard/blob/main/src/auto_leaderboard/load_results.py>**
 
 However, as soon as "Falcon," the LLM from Hugging Face, was released, it not only reclaimed the top position on Hugging Face's open leaderboard but also continues to dominate with its variant model, Falcon-Instruct, holding the first place. Considering that the open leaderboard was established at a certain time and metrics are included in Falcon's training set, it cannot be ruled out that the LLM was pre-trained appropriately for specific datasets and metrics. Thus, while the four datasets and metrics on the open leaderboard can serve as supplementary indicators for evaluating LLMs, it appears challenging for them to provide a fair quantitative assessment. In other words, Hugging Face's Open LLM Leaderboard might have been utilized as a marketing tool to promote Falcon.
 
 Falcon, a fine-tuned LLM based on a large-scale web dataset processed by Meta's LLAMA, is not significantly different from models such as Stanford's Alpaca and Vicuna. However, Falcon emphasizes its efficient fine-tuning using a large refined web dataset and has achieved the top position on the Open LLM Leaderboard. Subsequently, many open-source LLM developers have started competing at the decimal level by fine-tuning Meta's LLAMA to attain high rankings on the Open LLM Leaderboard. However, there hasn't been a noticeable improvement in the qualitative performance of open-source LLMs.
 
 In this context, certain reports indicate that open-source LLM models have not been demonstrating superiority. A report titled "Exploring the MIT Mathematics and EECS Curriculum Using Large Language Models," which compares the performance of LLMs on MIT's math and electrical engineering and computer science courses, highlights that open-source LLM models do not outperform past models from OpenAI. Additionally, another report called "CodeT5+: Open Code Large Language Models for Code Understanding and Generation" also suggests that open-source LLM models are not superior to davinci-002 in the field of coding.
 
 Therefore, we aim to examine the evaluation methods employed in each LLM report and prepare qualitative/quantitative indicators to objectively assess the LLM currently under development.

## Generative AI
### Open AI - GPT-4 Technical Report
- **url:** <https://arxiv.org/abs/2303.08774>
- **pdf:** <https://arxiv.org/pdf/2303.08774>
- **date:** 2023.03.15 for v1
- **abstract:** We report the development of GPT-4, a large-scale, multimodal model which can accept image and text inputs and produce text outputs. While less capable than humans in many real-world scenarios, GPT-4 exhibits human-level performance on various professional and academic benchmarks, including passing a simulated bar exam with a score around the top 10% of test takers. GPT-4 is a Transformer-based model pre-trained to predict the next token in a document. The post-training alignment process results in improved performance on measures of factuality and adherence to desired behavior. A core component of this project was developing infrastructure and optimization methods that behave predictably across a wide range of scales. This allowed us to accurately predict some aspects of GPT-4's performance based on models trained with no more than 1/1,000th the compute of GPT-4.

### Google - PaLM 2 Technical Report
- **url:** <https://arxiv.org/abs/2305.10403>
- **pdf:** <https://arxiv.org/pdf/2305.10403>
- **date:** 2023.05.17 for v1
- **abstract:** We introduce PaLM 2, a new state-of-the-art language model that has better multilingual and reasoning capabilities and is more compute-efficient than its predecessor PaLM. PaLM 2 is a Transformer-based model trained using a mixture of objectives. Through extensive evaluations on English and multilingual language, and reasoning tasks, we demonstrate that PaLM 2 has significantly improved quality on downstream tasks across different model sizes, while simultaneously exhibiting faster and more efficient inference compared to PaLM. This improved efficiency enables broader deployment while also allowing the model to respond faster, for a more natural pace of interaction. PaLM 2 demonstrates robust reasoning capabilities exemplified by large improvements over PaLM on BIG-Bench and other reasoning tasks. PaLM 2 exhibits stable performance on a suite of responsible AI evaluations, and enables inference-time control over toxicity without additional overhead or impact on other capabilities. Overall, PaLM 2 achieves state-of-the-art performance across a diverse set of tasks and capabilities. When discussing the PaLM 2 family, it is important to distinguish between pre-trained models (of various sizes), fine-tuned variants of these models, and the user-facing products that use these models. In particular, user-facing products typically include additional pre- and post-processing steps. Additionally, the underlying models may evolve over time. Therefore, one should not expect the performance of user-facing products to exactly match the results reported in this report.

### Hugging Face - Falcon
#### The RefinedWeb Dataset for Falcon LLM: Outperforming Curated Corpora with Web Data, and Web Data Only
- **url:** <https://arxiv.org/abs/2306.01116>
- **pdf:** <https://arxiv.org/pdf/2306.01116>
- **date:** 2023.06.01 for v1
- **abstract:** Large language models are commonly trained on a mixture of filtered web data and curated high-quality corpora, such as social media conversations, books, or technical papers. This curation process is believed to be necessary to produce performant models with broad zero-shot generalization abilities. However, as larger models requiring pretraining on trillions of tokens are considered, it is unclear how scalable is curation and whether we will run out of unique high-quality data soon. At variance with previous beliefs, we show that properly filtered and deduplicated web data alone can lead to powerful models; even significantly outperforming models from the state-of-the-art trained on The Pile. Despite extensive filtering, the high-quality data we extract from the web is still plentiful, and we are able to obtain five trillion tokens from CommonCrawl. We publicly release an extract of 600 billion tokens from our RefinedWeb dataset, and 1.3/7.5B parameters language models trained on it.

### Meta - LLaMA
- **url:** <https://arxiv.org/abs/2302.13971>
- **pdf:** <https://arxiv.org/pdf/2302.13971>
- **date:** 2023.02.27 for v1
- **abstract:** We introduce LLaMA, a collection of foundation language models ranging from 7B to 65B parameters. We train our models on trillions of tokens, and show that it is possible to train state-of-the-art models using publicly available datasets exclusively, without resorting to proprietary and inaccessible datasets. In particular, LLaMA-13B outperforms GPT-3 (175B) on most benchmarks, and LLaMA-65B is competitive with the best models, Chinchilla-70B and PaLM-540B. We release all our models to the research community.



### LaMDA: Language Models for Dialog Applications
Related with Google Bard
- **url:** <https://arxiv.org/abs/2201.08239>
- **pdf:** <https://arxiv.org/pdf/2201.08239>
- **date:** 2022.01.20 for v1
- **abstract:** We present LaMDA: Language Models for Dialog Applications. LaMDA is a family of Transformer-based neural language models specialized for dialog, which have up to 137B parameters and are pre-trained on 1.56T words of public dialog data and web text. While model scaling alone can improve quality, it shows less improvements on safety and factual grounding. We demonstrate that fine-tuning with annotated data and enabling the model to consult external knowledge sources can lead to significant improvements towards the two key challenges of safety and factual grounding. The first challenge, safety, involves ensuring that the model's responses are consistent with a set of human values, such as preventing harmful suggestions and unfair bias. We quantify safety using a metric based on an illustrative set of human values, and we find that filtering candidate responses using a LaMDA classifier fine-tuned with a small amount of crowdworker-annotated data offers a promising approach to improving model safety. The second challenge, factual grounding, involves enabling the model to consult external knowledge sources, such as an information retrieval system, a language translator, and a calculator. We quantify factuality using a groundedness metric, and we find that our approach enables the model to generate responses grounded in known sources, rather than responses that merely sound plausible. Finally, we explore the use of LaMDA in the domains of education and content recommendations, and analyze their helpfulness and role consistency.

### Databricks - Dolly
- **url:** <https://www.databricks.com/blog/2023/04/12/dolly-first-open-commercially-viable-instruction-tuned-llm>


## Evaluations
### Open Code LLM 
#### CodeT5+: Open Code Large Language Models for Code Understanding and Generation
- **url:** <https://arxiv.org/abs/2305.07922>
- **pdf:** <https://arxiv.org/pdf/2306.08997>
- **date:** 2023.05.13 for v1
- **abstract:** Large language models (LLMs) pretrained on vast source code have achieved prominent progress in code intelligence. However, existing code LLMs have two main limitations in terms of architecture and pretraining tasks. First, they often adopt a specific architecture (encoder-only or decoder-only) or rely on a unified encoder-decoder network for different downstream tasks. The former paradigm is limited by inflexibility in applications while in the latter, the model is treated as a single system for all tasks, leading to suboptimal performance on a subset of tasks. Secondly, they often employ a limited set of pretraining objectives which might not be relevant to some downstream tasks and hence result in substantial performance degrade. To address these limitations, we propose ``CodeT5+'', a family of encoder-decoder LLMs for code in which component modules can be flexibly combined to suit a wide range of downstream code tasks. Such flexibility is enabled by our proposed mixture of pretraining objectives to mitigate the pretrain-finetune discrepancy. These objectives cover span denoising, contrastive learning, text-code matching, and causal LM pretraining tasks, on both unimodal and bimodal multilingual code corpora. Furthermore, we propose to initialize CodeT5+ with frozen off-the-shelf LLMs without training from scratch to efficiently scale up our models, and explore instruction-tuning to align with natural language instructions. We extensively evaluate CodeT5+ on over 20 code-related benchmarks in different settings, including zero-shot, finetuning, and instruction-tuning. We observe state-of-the-art (SoTA) model performance on various code-related tasks, such as code generation and completion, math programming, and text-to-code retrieval tasks. Particularly, our instruction-tuned CodeT5+ 16B achieves new SoTA results on HumanEval code generation task against other open code LLMs.

### LLMs on MIT EECS 
#### Exploring the MIT Mathematics and EECS Curriculum Using Large Language Models
- **url:** <https://arxiv.org/abs/2306.08997>
- **date:** 2023.06.15 for v1
- **abstract:** We curate a comprehensive dataset of 4,550 questions and solutions from problem sets, midterm exams, and final exams across all MIT Mathematics and Electrical Engineering and Computer Science (EECS) courses required for obtaining a degree. We evaluate the ability of large language models to fulfill the graduation requirements for any MIT major in Mathematics and EECS. Our results demonstrate that GPT-3.5 successfully solves a third of the entire MIT curriculum, while GPT-4, with prompt engineering, achieves a perfect solve rate on a test set excluding questions based on images. We fine-tune an open-source large language model on this dataset. We employ GPT-4 to automatically grade model responses, providing a detailed performance breakdown by course, question, and answer type. By embedding questions in a low-dimensional space, we explore the relationships between questions, topics, and classes and discover which questions and classes are required for solving other questions and classes through few-shot learning. Our analysis offers valuable insights into course prerequisites and curriculum design, highlighting language models' potential for learning and improving Mathematics and EECS education.