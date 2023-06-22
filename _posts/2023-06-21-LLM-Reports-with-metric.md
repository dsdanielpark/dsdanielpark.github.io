---
title: LLM Reports with metrics
author: Daniel Park
date: 2023-06-21
category: llm
layout: post
---

- Related Project: private 
- Project Status: 1 Alpha
- Date: 2023-06-21


### 개요

관련 링크
- Hugging Face의 [Open Source LLM Leader Board](https://huggingface.co/spaces/HuggingFaceH4/open_llm_leaderboard)
- [Open Source LLM Leader Board 시각화 보고서](https://github.com/dsdanielpark/Open-LLM-Leaderboard-Report)


 Large Language Model(이하 "LLM")에 대한 성능 평가와 관련되어 다양한 방법들이 제시되고 있습니다. LLM을 어떻게 평가하였는지, 또 평가했는지 알아보기 위해 각 LLM 논문들에서 제시한 정량 지표 및 정성적인 평가방법들을 살펴보고자 합니다.
 
 허깅 페이스의 Open LLM Leader Board는 LLM을 정량적으로 평가하는 대표적인 도커 스페이스입니다.
 허깅 페이스(Hugging Face)는 팔콘(Falcon)을 출시하기에 몇 일 앞서 Open LLM Leader Board라는 온라인 도커 스페이스를 개설하고, 도커에서 4개의 데이터셋에 대한 정량적인 지표를 근거로 오픈 소스 LLM들의 순위를 메기고 있습니다. 

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
 **참고: <https://huggingface.co/spaces/HuggingFaceH4/open_llm_leaderboard/blob/main/src/auto_leaderboard/load_results.py>**
 
 그러나 '허깅페이스'의 LLM인 '팔콘'이 공개되자마자, '허깅페이스'의 오픈 리더보드에서 1위를 탈환하였을 뿐만 아니라 여전히 팔콘의 변형 모델(falcon-instruct)이 계속해서 1위를 차지하고 있습니다. 오픈 리더보드 개설 시기 뿐만 아니라 Metric들이 팔콘의 트레인 셋에 포함되어있다면, 특정 데이터셋과 Metrics에 적절하게 LLM을 미리 학습했을 가능성을 배제할 수 없기 때문에 오픈 리더보드의 4개의 데이터셋과 Metrics들이 LLM들을 평가하는 보조지표가 될 수 있지만, 공정한 정량지표가 되기에는 무리가 있어보입니다. 즉, 허깅페이스의 Open LLM Leader Board는 허깅페이스의 Falcon을 홍보하기 위한 마케팅 수단 중 하나로 사용되었을 수 있습니다.

 팔콘은 메타의 LLAMA에 후처리 된 대용량 웹 데이터를 기반으로 파인튜닝한 LLM으로 스탠포드의 알파카와 Vicuna 등의 모델등과 큰 차이는 없으나 대용량의 정제된 웹 데이터를 통해 효율적으로 파인튜닝하였다는 것을 내세우며 오픈 LLM 리더보드의 1위를 차지하였고, 이후 많은 오픈 소스 LLM 개발자들은 메타의 LLAMA를 파인튜닝하여 Open LLM Leader Board에서 높은 순위를 기록하기 위해 소숫점 단위 경쟁을 시작하였지만, 정성적으로 오픈 소스 LLM의 성능이 크게 개선되는 것을 체감하지 못하였습니다.
 
 이런 상황에서 일부 보고서에 따르면 오픈 소스 LLM 모델들이 우위를 보이지 못한다는 것을 보고하였습니다. MIT의 수학 및 전기 및 컴퓨터 공학 교육과목에 대한 LLM의 성능을 비교한 보고서인 "Exploring the MIT Mathematics and EECS Curriculum Using Large Language Models"에 따르면 오픈 소스 LLM 모델들의 성능이 Open AI의 과거 모델보다 우수하지 못하다는 내용이 소개되었습니다. 또한 "CodeT5+: Open Code Large Language Models for Code Understanding and Generation"라는 보고서에서도 오픈 소스 LLM 모델들이 코딩 영역에서 davinci-002보다도 우월하지 않다라는 내용을 보고하였습니다.

 따라서 각 LLM 보고서들의 모델 평가 방법들을 톺아보고, 현재 학습 중인 LLM을 보다 객관적으로 평가할 수 있는 정성/정량 지표들을 준비하고자 합니다.




### 01. Open AI - GPT-4 Technical Report
- **url:** <https://arxiv.org/abs/2303.08774>
- **pdf:** <https://arxiv.org/pdf/2303.08774>
- **date:** 15 Mar 2023 for v1
- **abstract:** We report the development of GPT-4, a large-scale, multimodal model which can accept image and text inputs and produce text outputs. While less capable than humans in many real-world scenarios, GPT-4 exhibits human-level performance on various professional and academic benchmarks, including passing a simulated bar exam with a score around the top 10% of test takers. GPT-4 is a Transformer-based model pre-trained to predict the next token in a document. The post-training alignment process results in improved performance on measures of factuality and adherence to desired behavior. A core component of this project was developing infrastructure and optimization methods that behave predictably across a wide range of scales. This allowed us to accurately predict some aspects of GPT-4's performance based on models trained with no more than 1/1,000th the compute of GPT-4.

### 02. Google - PaLM 2 Technical Report
- **url:** <https://arxiv.org/abs/2305.10403>
- **pdf:** <https://arxiv.org/pdf/2305.10403>
- **date:** 17 May 2023 for v1
- **abstract:** We introduce PaLM 2, a new state-of-the-art language model that has better multilingual and reasoning capabilities and is more compute-efficient than its predecessor PaLM. PaLM 2 is a Transformer-based model trained using a mixture of objectives. Through extensive evaluations on English and multilingual language, and reasoning tasks, we demonstrate that PaLM 2 has significantly improved quality on downstream tasks across different model sizes, while simultaneously exhibiting faster and more efficient inference compared to PaLM. This improved efficiency enables broader deployment while also allowing the model to respond faster, for a more natural pace of interaction. PaLM 2 demonstrates robust reasoning capabilities exemplified by large improvements over PaLM on BIG-Bench and other reasoning tasks. PaLM 2 exhibits stable performance on a suite of responsible AI evaluations, and enables inference-time control over toxicity without additional overhead or impact on other capabilities. Overall, PaLM 2 achieves state-of-the-art performance across a diverse set of tasks and capabilities. When discussing the PaLM 2 family, it is important to distinguish between pre-trained models (of various sizes), fine-tuned variants of these models, and the user-facing products that use these models. In particular, user-facing products typically include additional pre- and post-processing steps. Additionally, the underlying models may evolve over time. Therefore, one should not expect the performance of user-facing products to exactly match the results reported in this report.

### 03. Hugging Face - Falcon
#### The RefinedWeb Dataset for Falcon LLM: Outperforming Curated Corpora with Web Data, and Web Data Only
- **url:** <https://arxiv.org/abs/2306.01116>
- **pdf:** <https://arxiv.org/pdf/2306.01116>
- **date:** 1 Jun 2023 for v1
- **abstract:** Large language models are commonly trained on a mixture of filtered web data and curated high-quality corpora, such as social media conversations, books, or technical papers. This curation process is believed to be necessary to produce performant models with broad zero-shot generalization abilities. However, as larger models requiring pretraining on trillions of tokens are considered, it is unclear how scalable is curation and whether we will run out of unique high-quality data soon. At variance with previous beliefs, we show that properly filtered and deduplicated web data alone can lead to powerful models; even significantly outperforming models from the state-of-the-art trained on The Pile. Despite extensive filtering, the high-quality data we extract from the web is still plentiful, and we are able to obtain five trillion tokens from CommonCrawl. We publicly release an extract of 600 billion tokens from our RefinedWeb dataset, and 1.3/7.5B parameters language models trained on it.

### 04. Meta - LLaMA
- **url:** <https://arxiv.org/abs/2302.13971>
- **pdf:** <https://arxiv.org/pdf/2302.13971>
- **date:** 27 Feb 2023 for v1
- **abstract:** We introduce LLaMA, a collection of foundation language models ranging from 7B to 65B parameters. We train our models on trillions of tokens, and show that it is possible to train state-of-the-art models using publicly available datasets exclusively, without resorting to proprietary and inaccessible datasets. In particular, LLaMA-13B outperforms GPT-3 (175B) on most benchmarks, and LLaMA-65B is competitive with the best models, Chinchilla-70B and PaLM-540B. We release all our models to the research community.


### 05. Open Code LLM 
#### CodeT5+: Open Code Large Language Models for Code Understanding and Generation
- **url:** <https://arxiv.org/abs/2305.07922>
- **pdf:** <https://arxiv.org/pdf/2306.08997>
- **date:** 13 May 2023 for v1
- **abstract:** Large language models (LLMs) pretrained on vast source code have achieved prominent progress in code intelligence. However, existing code LLMs have two main limitations in terms of architecture and pretraining tasks. First, they often adopt a specific architecture (encoder-only or decoder-only) or rely on a unified encoder-decoder network for different downstream tasks. The former paradigm is limited by inflexibility in applications while in the latter, the model is treated as a single system for all tasks, leading to suboptimal performance on a subset of tasks. Secondly, they often employ a limited set of pretraining objectives which might not be relevant to some downstream tasks and hence result in substantial performance degrade. To address these limitations, we propose ``CodeT5+'', a family of encoder-decoder LLMs for code in which component modules can be flexibly combined to suit a wide range of downstream code tasks. Such flexibility is enabled by our proposed mixture of pretraining objectives to mitigate the pretrain-finetune discrepancy. These objectives cover span denoising, contrastive learning, text-code matching, and causal LM pretraining tasks, on both unimodal and bimodal multilingual code corpora. Furthermore, we propose to initialize CodeT5+ with frozen off-the-shelf LLMs without training from scratch to efficiently scale up our models, and explore instruction-tuning to align with natural language instructions. We extensively evaluate CodeT5+ on over 20 code-related benchmarks in different settings, including zero-shot, finetuning, and instruction-tuning. We observe state-of-the-art (SoTA) model performance on various code-related tasks, such as code generation and completion, math programming, and text-to-code retrieval tasks. Particularly, our instruction-tuned CodeT5+ 16B achieves new SoTA results on HumanEval code generation task against other open code LLMs.

### 06. LLMs on MIT EECS 
#### Exploring the MIT Mathematics and EECS Curriculum Using Large Language Models
- **url:** <https://arxiv.org/abs/2306.08997>
- **date:** 15 Jun 2023 for v1
- **abstract:** We curate a comprehensive dataset of 4,550 questions and solutions from problem sets, midterm exams, and final exams across all MIT Mathematics and Electrical Engineering and Computer Science (EECS) courses required for obtaining a degree. We evaluate the ability of large language models to fulfill the graduation requirements for any MIT major in Mathematics and EECS. Our results demonstrate that GPT-3.5 successfully solves a third of the entire MIT curriculum, while GPT-4, with prompt engineering, achieves a perfect solve rate on a test set excluding questions based on images. We fine-tune an open-source large language model on this dataset. We employ GPT-4 to automatically grade model responses, providing a detailed performance breakdown by course, question, and answer type. By embedding questions in a low-dimensional space, we explore the relationships between questions, topics, and classes and discover which questions and classes are required for solving other questions and classes through few-shot learning. Our analysis offers valuable insights into course prerequisites and curriculum design, highlighting language models' potential for learning and improving Mathematics and EECS education.