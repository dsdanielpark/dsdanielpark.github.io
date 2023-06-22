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
 
 이런 상황에서 일부 보고서에 따르면 오픈 소스 LLM 모델들이 우위를 보이지 못한다는 것을 보고하였습니다. MIT의 수학 및 전기 및 컴퓨터 공학 교육과목을 다루는 보고서인 "Exploring the MIT Mathematics and EECS Curriculum Using Large Language Models"에 따르면 오픈 소스 LLM 모델들의 성능이 Open AI의 과거 모델보다 우수하지 못하다는 내용이 소개되었습니다. 또한 "CodeT5+: Open Code Large Language Models for Code Understanding and Generation"라는 보고서에서도 오픈 소스 LLM 모델들이 코딩 영역에서 davinci-002보다도 우월하지 않다라는 내용을 보고하였습니다.

 따라서 각 LLM 보고서들의 모델 평가 방법들을 톺아보고, 현재 학습 중인 LLM을 보다 객관적으로 평가할 수 있는 정성/정량 지표들을 준비하고자 합니다.




### 01. Open AI - GPT-4 Technical Report
- **url:** <https://arxiv.org/abs/2303.08774>
- 
### 02. Google - PaLM 2 Technical Report
- **url:** <https://arxiv.org/abs/2305.10403>

### 03. Hugging Face - Falcon
#### The RefinedWeb Dataset for Falcon LLM: Outperforming Curated Corpora with Web Data, and Web Data Only
- **url:** <https://arxiv.org/abs/2306.01116>

### 04. Open Code LLM 
#### CodeT5+: Open Code Large Language Models for Code Understanding and Generation
- **url:** <https://arxiv.org/abs/2305.07922>

### 05. LLMs on MIT EECS 
#### Exploring the MIT Mathematics and EECS Curriculum Using Large Language Models
- **url:** <https://arxiv.org/abs/2306.08997>
