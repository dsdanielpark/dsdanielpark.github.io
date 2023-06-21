---
title: LLM Reports with metric
author: Daniel Park
date: 2023-06-21
category: llm
layout: post
---

- Related Project: private 
- Project Status: 1 Alpha
- Date: 2023-06-21


일주일간 코딩테스트 2차 전 마지막 업데이트

### 개요

관련 링크
- Hugging Face의 [Open Source LLM Leader Board](https://huggingface.co/spaces/HuggingFaceH4/open_llm_leaderboard)
- [Open Source LLM Leader Board 시각화 보고서](https://github.com/dsdanielpark/Open-LLM-Leaderboard-Report)


 Large Language Model(이하 "LLM")에 대한 성능 평가와 관련되어 다양한 방법들이 제시되고 있습니다. LLM을 어떻게 평가하였는지, 또 평가했는지 알아보기 위해 각 LLM 논문들에서 제시한 정량 지표 및 정성적인 평가방법들을 살펴보고자 합니다.
 
 허깅 페이스(Hugging Face)는 팔콘(Falcon)을 출시하기에 몇 일 앞서 Open LLM Leader Board라는 온라인 도커 스페이스를 개설하고, 도커에서 4개의 데이터셋에 대한 결과를 기반으로 오픈 소스 LLM들의 정량적인 평가를 기반으로 순위를 나열하였습니다. 
 
 그러나 오픈 소스 LLM 진영에서 허깅페이스의 팔콘이 공개되자마자, 팔콘이 허깅페이스의 오픈 리더보드에서 1위를 탈환하였을 뿐만 아니라 여전히 팔콘의 변형 모델(falcon-instruct)이 1위를 고수하는 현 상황에 대해서 저는 오픈 리더보드의 정량지표들에 대한 공정성에 의구심이 들었습니다.

 팔콘은 메타의 LLAMA에 정제된 대용량 웹 사이트 데이터를 학습한 LLM으로 기존의 스탠포드 알파카와 Vicuna 등등 LLAMA 파인튜닝 모델과 크게 다르지 않음에도 불구하고, 공개와 동시에 오픈 리더보드 1위 탈환과 동시에 약간의 변형 LLM 모델들이 오픈 리더보드에서 계속 1위를 차지하고 있습니다. 
 
 또한 많은 오픈진영의 LLM 개발자들은 메타의 LLAMA를 파인튜닝하여 Open LLM Leader Board에서 높은 순위를 기록하기 위해 소숫점 단위 경쟁을 하기 시작하였지만, Open AI의 chat GPT 3.5 이상의 정성적으로 뛰어난 모델들이 등장하지 않고 있습니다.
 
 이런 와중에 오픈 소스 LLM들의 성능이 Open AI의 Chat GPT 3.5 터보에도 미치지 못한다는 보고서가 공개되었고(Exploring the MIT Mathematics and EECS Curriculum Using Large Language Models), 오픈 소스 LLM 모델들이 코딩 영역에서 davinci-002보다도 우월하지 않다는 논문이 공개되었습니다. (CodeT5+: Open Code Large Language Models for Code Understanding and Generation)

 따라서 각 보고서의 LLM 평가방법들을 톺아보고, 현재 학습 중인 저의 LLM의 방향에 대해서 고민하고자 합니다.




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
