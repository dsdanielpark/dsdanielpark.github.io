---
title: AUTO DRAFT - Attention-Based Molecule Modeling
author: Daniel Park
date: 2023-04-30
category: life
layout: post
---

> 이 글은 자동 생성된 초고로, 선행연구를 훑어보고, 색인하기 위한 용도입니다. This draft is automatically generated for the purpose of skimming through prior research and indexing.
> 배치성 프로그램으로 진행하고 있는 연구에 참고될만한 논문들을 자동 생성합니다. 논문들은 인용 관계로 서로 연결되어 있으며, 인용 횟수 순으로 정렬되어 있습니다. The batch program generates research papers that can be referenced in my ongoing studies. These papers are connected to each other through citation relationships and are sorted by the number of citations.


- Related Project: Private 
- Project Status: 1 Alpha
- Date: 2023-04



Paper and domain search for molecular modeling

## Main Paper

### Attention-Based Graph Neural Network for Molecular Solubility Prediction
 - **url:** <https://pubs.acs.org/doi/10.1021/acsomega.2c06702>
 - **abstract:** Drug discovery (DD) research is aimed at the discovery of new medications. Solubility is an important physicochemical property in drug development. Active pharmaceutical ingredients (APIs) are essential substances for high drug efficacy. During DD research, aqueous solubility (AS) is a key physicochemical attribute required for API characterization. High-precision in silico solubility prediction reduces the experimental cost and time of drug development. Several artificial tools have been employed for solubility prediction using machine learning and deep learning techniques. This study aims to create different deep learning models that can predict the solubility of a wide range of molecules using the largest currently available solubility data set. Simplified molecular-input line-entry system (SMILES) strings were used as molecular representation, models developed using simple graph convolution, graph isomorphism network, graph attention network, and AttentiveFP network. Based on the performance of the models, the AttentiveFP-based network model was finally selected. The model was trained and tested on 9943 compounds. The model outperformed on 62 anticancer compounds with metric Pearson correlation R2 and root-mean-square error values of 0.52 and 0.61, respectively. AS can be improved by graph algorithm improvement or more molecular properties addition.


## Related Papers

### A self-attention based message passing neural network for predicting molecular lipophilicity and aqueous solubility

 - **url:** <https://jcheminf.biomedcentral.com/articles/10.1186/s13321-020-0414-z>
 - **abstract:** Efficient and accurate prediction of molecular properties, such as lipophilicity and solubility, is highly desirable for rational compound design in chemical and pharmaceutical industries. To this end, we build and apply a graph-neural-network framework called self-attention-based message-passing neural network (SAMPN) to study the relationship between chemical properties and structures in an interpretable way. The main advantages of SAMPN are that it directly uses chemical graphs and breaks the black-box mold of many machine/deep learning methods. Specifically, its attention mechanism indicates the degree to which each atom of the molecule contributes to the property of interest, and these results are easily visualized. Further, SAMPN outperforms random forests and the deep learning framework MPN from Deepchem. In addition, another formulation of SAMPN (Multi-SAMPN) can simultaneously predict multiple chemical properties with higher accuracy and efficiency than other models that predict one specific chemical property. Moreover, SAMPN can generate chemically visible and interpretable results, which can help researchers discover new pharmaceuticals and materials. The source code of the SAMPN prediction pipeline is freely available at Github (<https://>github.com/tbwxmu/SAMPN).


### MoleculeAttentionTransformer
 - **url:** <https://arxiv.org/abs/2002.08264>
 - **abstract:** Designing a single neural network architecture that performs competitively across a range of molecule property prediction tasks remains largely an open challenge, and its solution may unlock a widespread use of deep learning in the drug discovery industry. To move towards this goal, we propose Molecule Attention Transformer (MAT). Our key innovation is to augment the attention mechanism in Transformer using inter-atomic distances and the molecular graph structure. Experiments show that MAT performs competitively on a diverse set of molecular prediction tasks. Most importantly, with a simple self-supervised pretraining, MAT requires tuning of only a few hyperparameter values to achieve state-of-the-art performance on downstream tasks. Finally, we show that attention weights learned by MAT are interpretable from the chemical point of view.


### Generating Focused Molecule Libraries for Drug Discovery with Recurrent Neural Networks 
- **year:** 2017 
- **url:** <https://www.semanticscholar.org/paper/1cb789ab8925bda02758bcb69eb0ed1547b5f4b9>
- **abstract:** In de novo drug design, computational strategies are used to generate novel molecules with good affinity to the desired biological target. In this work, we show that recurrent neural networks can be trained as generative models for molecular structures, similar to statistical language models in natural language processing. We demonstrate that the properties of the generated molecules correlate very well with the properties of the molecules used to train the model. In order to enrich libraries with molecules active toward a given biological target, we propose to fine-tune the model with small sets of molecules, which are known to be active against that target. Against Staphylococcus aureus, the model reproduced 14% of 6051 hold-out test molecules that medicinal chemists designed, whereas against Plasmodium falciparum (Malaria), it reproduced 28% of 1240 test molecules. When coupled with a scoring function, our model can perform the complete de novo drug design cycle to generate large sets of novel molecules for drug discovery. 
- **journal:** ACS Central Science 
- **volume:** 4 
- **pages:** 120 - 131 
- **doi:** 10.1021/acscentsci.7b00512 
- **pmid:** 29392184 

### Deep learning for molecular generation and optimization - a review of the state of the art 
- **year:** 2019 
- **url:** <https://www.semanticscholar.org/paper/b2029e552d620600fd6f542ba0e11e39d42c3431>
- **abstract:** We review a recent groundswell of work which uses deep learning techniques to generate and optimize molecules. 
- **journal:** ArXiv 
- **volume:** abs/1903.04388 
- **pages:** null 
- **doi:** 10.1039/C9ME00039A 
- **arxivid:** 1903.04388 

### The cornucopia of meaningful leads: Applying deep adversarial autoencoders for new molecule development in oncology 
- **year:** 2016 
- **url:** <https://www.semanticscholar.org/paper/0b309c0725c717989f6d6ae485fbab521e72d903>
- **abstract:** Recent advances in deep learning and specifically in generative adversarial networks have demonstrated surprising results in generating new images and videos upon request even using natural language as input. In this paper we present the first application of generative adversarial autoencoders (AAE) for generating novel molecular fingerprints with a defined set of parameters. We developed a 7-layer AAE architecture with the latent middle layer serving as a discriminator. As an input and output the AAE uses a vector of binary fingerprints and concentration of the molecule. In the latent layer we also introduced a neuron responsible for growth inhibition percentage, which when negative indicates the reduction in the number of tumor cells after the treatment. To train the AAE we used the NCI-60 cell line assay data for 6252 compounds profiled on MCF-7 cell line. The output of the AAE was used to screen 72 million compounds in PubChem and select candidate molecules with potential anti-cancer properties. This approach is a proof of concept of an artificially-intelligent drug discovery engine, where AAEs are used to generate new molecular fingerprints with the desired molecular properties. 
- **journal:** Oncotarget 
- **volume:** 8 
- **pages:** 10883 - 10890 
- **doi:** 10.18632/oncotarget.14073 
- **pmid:** 28029644 

### Syntax-Directed Variational Autoencoder for Structured Data 
- **year:** 2018 
- **url:** <https://www.semanticscholar.org/paper/7dd434b3799a6c8c346a1d7ee77d37980a4ef5b9>
- **abstract:** Deep generative models have been enjoying success in modeling continuous data. However it remains challenging to capture the representations for discrete structures with formal grammars and semantics, e.g., computer programs and molecular structures. How to generate both syntactically and semantically correct data still remains largely an open problem. Inspired by the theory of compiler where the syntax and semantics check is done via syntax-directed translation (SDT), we propose a novel syntax-directed variational autoencoder (SD-VAE) by introducing stochastic lazy attributes. This approach converts the offline SDT check into on-the-fly generated guidance for constraining the decoder. Comparing to the state-of-the-art methods, our approach enforces constraints on the output space so that the output will be not only syntactically valid, but also semantically reasonable. We evaluate the proposed model with applications in programming language and molecules, including reconstruction and program/molecule optimization. The results demonstrate the effectiveness in incorporating syntactic and semantic constraints in discrete generative models, which is significantly better than current state-of-the-art approaches. 
- **journal:** ArXiv 
- **volume:** abs/1802.08786 
- **pages:** null 
- **arxivid:** 1802.08786 

### Automatic Chemical Design Using a Data-Driven Continuous Representation of Molecules 
- **year:** 2016 
- **url:** <https://www.semanticscholar.org/paper/88427d2143d4cff357c3b393ae7580a7b6e19940>
- **abstract:** We report a method to convert discrete representations of molecules to and from a multidimensional continuous representation. This model allows us to generate new molecules for efficient exploration and optimization through open-ended spaces of chemical compounds. A deep neural network was trained on hundreds of thousands of existing chemical structures to construct three coupled functions: an encoder, a decoder, and a predictor. The encoder converts the discrete representation of a molecule into a real-valued continuous vector, and the decoder converts these continuous vectors back to discrete molecular representations. The predictor estimates chemical properties from the latent continuous vector representation of the molecule. Continuous representations of molecules allow us to automatically generate novel chemical structures by performing simple operations in the latent space, such as decoding random vectors, perturbing known chemical structures, or interpolating between molecules. Continuous representations also allow the use of powerful gradient-based optimization to efficiently guide the search for optimized functional compounds. We demonstrate our method in the domain of drug-like molecules and also in a set of molecules with fewer that nine heavy atoms. 
- **journal:** ACS Central Science 
- **volume:** 4 
- **pages:** 268 - 276 
- **doi:** 10.1021/acscentsci.7b00572 
- **pmid:** 29532027 
- **arxivid:** 1610.02415 

### Planning chemical syntheses with deep neural networks and symbolic AI 
- **year:** 2018 
- **url:** <https://www.semanticscholar.org/paper/ef8ab2a0be51a0cd04c2c0f01adfae956a2a84af>
- **abstract:** *TL;DR:* This work combines Monte Carlo tree search with an expansion policy network that guides the search, and a filter network to pre-select the most promising retrosynthetic steps that solve for almost twice as many molecules, thirty times faster than the traditional computer-aided search method. 
- **journal:** Nature 
- **volume:** 555 
- **pages:** 604-610 
- **doi:** 10.1038/nature25978 
- **pmid:** 29595767 

### A de novo molecular generation method using latent vector based generative adversarial network 
- **year:** 2019 
- **url:** <https://www.semanticscholar.org/paper/20b248b56af9a0d1abbda300f0a275a874c7148c>
- **abstract:** *TL;DR:* A new deep learning architecture, LatentGAN, which combines an autoencoder and a generative adversarial neural network for de novo molecular design is proposed, indicating that both methods can be used complementarily. 
- **journal:** Journal of Cheminformatics 
- **volume:** 11 
- **pages:** null 
- **doi:** 10.1186/s13321-019-0397-9 
- **pmid:** 33430938 

### Generating Focussed Molecule Libraries for Drug Discovery with Recurrent Neural Networks 
- **year:** 2017 
- **url:** <https://www.semanticscholar.org/paper/bfe7f183bc191665b39edd5fe62a66ae24de8319>
- **abstract:** In de novo drug design, computational strategies are used to generate novel molecules with good affinity to the desired biological target. In this work, we show that recurrent neural networks can be trained as generative models for molecular structures, similar to statistical language models in natural language processing. We demonstrate that the properties of the generated molecules correlate very well with the properties of the molecules used to train the model. In order to enrich libraries with molecules active towards a given biological target, we propose to fine-tune the model with small sets of molecules, which are known to be active against that target. Against Staphylococcus aureus, the model reproduced 14% of 6051 hold-out test molecules that medicinal chemists designed, whereas against Plasmodium falciparum (Malaria) it reproduced 28% of 1240 test molecules. When coupled with a scoring function, our model can perform the complete de novo drug design cycle to generate large sets of novel molecules for drug discovery. 
- **journal:** ArXiv 
- **volume:** abs/1701.01329 
- **pages:** null 
- **arxivid:** 1701.01329 

### On failure modes in molecule generation and optimization. 
- **year:** 2019 
- **url:** <https://www.semanticscholar.org/paper/8abe4a49c00c45c1afe10428f2ed24efc6dc4086>
- **abstract:** *TL;DR:* This work highlights some unintended failure modes in molecular generation and optimization and how these evade detection by current performance metrics. 
- **journal:** Drug discovery today. Technologies 
- **volume:** 32-33 
- **pages:** 55-63 
- **doi:** 10.1016/j.ddtec.2020.09.003 
- **pmid:** 33386095 

### Constrained Graph Variational Autoencoders for Molecule Design 
- **year:** 2018 
- **url:** <https://www.semanticscholar.org/paper/b83e7e9a7bf59347eb9bc53ecaf139e301a8b72d>
- **abstract:** Graphs are ubiquitous data structures for representing interactions between entities. With an emphasis on the use of graphs to represent chemical molecules, we explore the task of learning to generate graphs that conform to a distribution observed in training data. We propose a variational autoencoder model in which both encoder and decoder are graph-structured. Our decoder assumes a sequential ordering of graph extension steps and we discuss and analyze design choices that mitigate the potential downsides of this linearization. Experiments compare our approach with a wide range of baselines on the molecule generation task and show that our method is more successful at matching the statistics of the original dataset on semantically important metrics. Furthermore, we show that by using appropriate shaping of the latent space, our model allows us to design molecules that are (locally) optimal in desired properties. 
- **journal:** ArXiv 
- **volume:** abs/1805.09076 
- **pages:** null 
- **arxivid:** 1805.09076 

### Estimation of synthetic accessibility score of drug-like molecules based on molecular complexity and fragment contributions 
- **year:** 2009 
- **url:** <https://www.semanticscholar.org/paper/9db40183d62ffae8f9b5a8327511840f6d16ceb1>
- **abstract:** *TL;DR:* This method uses historical synthetic knowledge obtained by analyzing information from millions of already synthesized chemicals and considers also molecule complexity, which is sufficiently fast and provides results consistent with estimation of ease of synthesis by experienced medicinal chemists. 
- **journal:** Journal of Cheminformatics 
- **volume:** 1 
- **pages:** 8 - 8 
- **doi:** 10.1186/1758-2946-1-8 
- **pmid:** 20298526 

### Optimization of Molecules via Deep Reinforcement Learning 
- **year:** 2018 
- **url:** <https://www.semanticscholar.org/paper/2ba00083a72558d45e4baecff0425ef6272f7a40>
- **abstract:** *TL;DR:* Inspired by problems faced during medicinal chemistry lead optimization, the MolDQN model is extended with multi-objective reinforcement learning, which maximizes drug-likeness while maintaining similarity to the original molecule. 
- **journal:** Scientific Reports 
- **volume:** 9 
- **pages:** null 
- **doi:** 10.1038/s41598-019-47148-x 
- **pmid:** 31341196 
- **arxivid:** 1810.08678 

### Junction Tree Variational Autoencoder for Molecular Graph Generation 
- **year:** 2018 
- **url:** <https://www.semanticscholar.org/paper/fd17bd9a5dc24a081ad9743570f50dd6750f54b2>
- **abstract:** We seek to automate the design of molecules based on specific chemical properties. In computational terms, this task involves continuous embedding and generation of molecular graphs. Our primary contribution is the direct realization of molecular graphs, a task previously approached by generating linear SMILES strings instead of graphs. Our junction tree variational autoencoder generates molecular graphs in two phases, by first generating a tree-structured scaffold over chemical substructures, and then combining them into a molecule with a graph message passing network. This approach allows us to incrementally expand molecules while maintaining chemical validity at every step. We evaluate our model on multiple tasks ranging from molecular generation to optimization. Across these tasks, our model outperforms previous state-of-the-art baselines by a significant margin. 
- **doi:** 10.1039/9781788016841-00228 
- **arxivid:** 1802.04364 

### Molecular de-novo design through deep reinforcement learning 
- **year:** 2017 
- **url:** <https://www.semanticscholar.org/paper/d77bc27d16a362e5e1b727904c3789355dda6062>
- **abstract:** *TL;DR:* A method to tune a sequence-based generative model for molecular de novo design that through augmented episodic likelihood can learn to generate structures with certain specified desirable properties is introduced. 
- **journal:** Journal of Cheminformatics 
- **volume:** 9 
- **pages:** null 
- **doi:** 10.1186/s13321-017-0235-x 
- **pmid:** 29086083 
- **arxivid:** 1704.07555 

### Quantifying the chemical beauty of drugs. 
- **year:** 2012 
- **url:** <https://www.semanticscholar.org/paper/11bce438e2fdc7a7ae5f65c339c757f386f4f48a>
- **abstract:** *TL;DR:* The utility of QED is extended by applying it to the problem of molecular target druggability assessment by prioritizing a large set of published bioactive compounds and may also capture the abstract notion of aesthetics in medicinal chemistry. 
- **journal:** Nature chemistry 
- **volume:** 4 2 
- **pages:** 90-8 
- **doi:** 10.1038/nchem.1243 
- **pmid:** 22270643 

### Multi-objective de novo drug design with conditional graph generative model 
- **year:** 2018 
- **url:** <https://www.semanticscholar.org/paper/14f1f267731c89bbff04fce87b223d73168d8a4e>
- **abstract:** *TL;DR:* A new de novo molecular design framework is proposed based on a type of sequential graph generators that do not use atom level recurrent units, which is much more tuned for molecule generation and has been scaled up to cover significantly larger molecules in the ChEMBL database. 
- **journal:** Journal of Cheminformatics 
- **volume:** 10 
- **pages:** null 
- **doi:** 10.1186/s13321-018-0287-6 
- **pmid:** 30043127 
- **arxivid:** 1801.07299 

### Reinforced Adversarial Neural Computer for de Novo Molecular Design 
- **year:** 2018 
- **url:** <https://www.semanticscholar.org/paper/b4151c385bd30e352c18c0135981e56560ecf744>
- **abstract:** In silico modeling is a crucial milestone in modern drug design and development. Although computer-aided approaches in this field are well-studied, the application of deep learning methods in this research area is at the beginning. In this work, we present an original deep neural network (DNN) architecture named RANC (Reinforced Adversarial Neural Computer) for the de novo design of novel small-molecule organic structures based on the generative adversarial network (GAN) paradigm and reinforcement learning (RL). As a generator RANC uses a differentiable neural computer (DNC), a category of neural networks, with increased generation capabilities due to the addition of an explicit memory bank, which can mitigate common problems found in adversarial settings. The comparative results have shown that RANC trained on the SMILES string representation of the molecules outperforms its first DNN-based counterpart ORGANIC by several metrics relevant to drug discovery: the number of unique structures, passing medicinal chemistry filters (MCFs), Muegge criteria, and high QED scores. RANC is able to generate structures that match the distributions of the key chemical features/descriptors (e.g., MW, logP, TPSA) and lengths of the SMILES strings in the training data set. Therefore, RANC can be reasonably regarded as a promising starting point to develop novel molecules with activity against different biological targets or pathways. In addition, this approach allows scientists to save time and covers a broad chemical space populated with novel and diverse compounds. 
- **journal:** Journal of chemical information and modeling 
- **volume:** 58 6 
- **pages:** 1194-1204 
- **doi:** 10.1021/acs.jcim.7b00690 
- **pmid:** 29762023 

### Generative Recurrent Networks for De Novo Drug Design 
- **year:** 2017 
- **url:** <https://www.semanticscholar.org/paper/517a488f06577401422cf7e03647ac6148ef4e44>
- **abstract:** Generative artificial intelligence models present a fresh approach to chemogenomics and de novo drug design, as they provide researchers with the ability to narrow down their search of the chemical space and focus on regions of interest. We present a method for molecular de novo design that utilizes generative recurrent neural networks (RNN) containing long short‐term memory (LSTM) cells. This computational model captured the syntax of molecular representation in terms of SMILES strings with close to perfect accuracy. The learned pattern probabilities can be used for de novo SMILES generation. This molecular design concept eliminates the need for virtual compound library enumeration. By employing transfer learning, we fine‐tuned the RNN′s predictions for specific molecular targets. This approach enables virtual compound design without requiring secondary or external activity prediction, which could introduce error or unwanted bias. The results obtained advocate this generative RNN‐LSTM system for high‐impact use cases, such as low‐data drug discovery, fragment based molecular design, and hit‐to‐lead optimization for diverse drug targets. 
- **journal:** Molecular Informatics 
- **volume:** 37 
- **pages:** null 
- **doi:** 10.1002/minf.201700111 
- **pmid:** 29095571 

### De Novo Design of Bioactive Small Molecules by Artificial Intelligence 
- **year:** 2018 
- **url:** <https://www.semanticscholar.org/paper/ab1d44fe7ee9165974a2487b6d10ddaba6c26549>
- **abstract:** Generative artificial intelligence offers a fresh view on molecular design. We present the first‐time prospective application of a deep learning model for designing new druglike compounds with desired activities. For this purpose, we trained a recurrent neural network to capture the constitution of a large set of known bioactive compounds represented as SMILES strings. By transfer learning, this general model was fine‐tuned on recognizing retinoid X and peroxisome proliferator‐activated receptor agonists. We synthesized five top‐ranking compounds designed by the generative model. Four of the compounds revealed nanomolar to low‐micromolar receptor modulatory activity in cell‐based assays. Apparently, the computational model intrinsically captured relevant chemical and biological knowledge without the need for explicit rules. The results of this study advocate generative artificial intelligence for prospective de novo molecular design, and demonstrate the potential of these methods for future medicinal chemistry. 
- **journal:** Molecular Informatics 
- **volume:** 37 
- **pages:** null 
- **doi:** 10.1002/minf.201700153 
- **pmid:** 29319225 

### GraphVAE: Towards Generation of Small Graphs Using Variational Autoencoders 
- **year:** 2018 
- **url:** <https://www.semanticscholar.org/paper/8913c23081e46a41cc7ced3c2ff379d9cd7afcde>
- **abstract:** *TL;DR:* This work proposes to sidestep hurdles associated with linearization of discrete structures by having a decoder output a probabilistic fully-connected graph of a predefined maximum size directly at once by formulated as a variational autoencoder. 
- **journal:** ArXiv 
- **volume:** abs/1802.03480 
- **pages:** null 
- **doi:** 10.1007/978-3-030-01418-6_41 
- **arxivid:** 1802.03480 

### Optimizing distributions over molecular space. An Objective-Reinforced Generative Adversarial Network for Inverse-design Chemistry (ORGANIC) 
- **year:** 2017 
- **url:** <https://www.semanticscholar.org/paper/61c05d7cab4448a1585596cc7e00ab271c442c2e>
- **abstract:** Molecular discovery seeks to generate chemical species tailored to very speciﬁc needs. In this paper, we present ORGANIC , a framework based on Objective-Reinforced Generative Adversarial Networks (ORGAN), capable of producing a distribution over molecular space that matches with a certain set of desirable metrics. This methodology combines two successful techniques from the machine learning community: a Generative Adversarial Network (GAN), to create non-repetitive sensible molecular species, and Reinforcement Learning (RL), to bias this generative distribution towards certain attributes. We explore several applications, from optimization of random physicochemical properties to candidates for drug discovery and organic photovoltaic material design. 
- **journal:** ChemRxiv 
- **volume:**  
- **pages:** null 
- **doi:** 10.26434/CHEMRXIV.5309668 

### ChemTS: an efficient python library for de novo molecular generation 
- **year:** 2017 
- **url:** <https://www.semanticscholar.org/paper/4e2b1abef1eddf24eef8bb2e1fe920a162db26bc>
- **abstract:** Abstract Automatic design of organic materials requires black-box optimization in a vast chemical space. In conventional molecular design algorithms, a molecule is built as a combination of predetermined fragments. Recently, deep neural network models such as variational autoencoders and recurrent neural networks (RNNs) are shown to be effective in de novo design of molecules without any predetermined fragments. This paper presents a novel Python library ChemTS that explores the chemical space by combining Monte Carlo tree search and an RNN. In a benchmarking problem of optimizing the octanol-water partition coefficient and synthesizability, our algorithm showed superior efficiency in finding high-scoring molecules. ChemTS is available at <https://github.com/tsudalab/>ChemTS. Graphical Abstract 
- **journal:** Science and Technology of Advanced Materials 
- **volume:** 18 
- **pages:** 972 - 976 
- **doi:** 10.1080/14686996.2017.1401424 
- **pmid:** 29435094 
- **arxivid:** 1710.00616 

### Molecular Sets (MOSES): A Benchmarking Platform for Molecular Generation Models 
- **year:** 2018 
- **url:** <https://www.semanticscholar.org/paper/404571933e3e87942768c9a5cde8a6285732ad6f>
- **abstract:** Generative models are becoming a tool of choice for exploring the molecular space. These models learn on a large training dataset and produce novel molecular structures with similar properties. Generated structures can be utilized for virtual screening or training semi-supervized predictive models in the downstream tasks. While there are plenty of generative models, it is unclear how to compare and rank them. In this work, we introduce a benchmarking platform called Molecular Sets (MOSES) to standardize training and comparison of molecular generative models. MOSES provides training and testing datasets, and a set of metrics to evaluate the quality and diversity of generated structures. We have implemented and compared several molecular generation models and suggest to use our results as reference points for further advancements in generative chemistry research. The platform and source code are available at <https://github.com/molecularsets/moses>.
- **journal:** Frontiers in Pharmacology 
- **volume:** 11 
- **pages:** null 
- **doi:** 10.3389/fphar.2020.565644 
- **pmid:** 33390943 
- **arxivid:** 1811.12823 

### Hierarchical Generation of Molecular Graphs using Structural Motifs 
- **year:** 2020 
- **url:** <https://www.semanticscholar.org/paper/dc7307f6e49f0ad2432be4eea92ae7f854c3cebb>
- **abstract:** Graph generation techniques are increasingly being adopted for drug discovery. Previous graph generation approaches have utilized relatively small molecular building blocks such as atoms or simple cycles, limiting their effectiveness to smaller molecules. Indeed, as we demonstrate, their performance degrades significantly for larger molecules. In this paper, we propose a new hierarchical graph encoder-decoder that employs significantly larger and more flexible graph motifs as basic building blocks. Our encoder produces a multi-resolution representation for each molecule in a fine-to-coarse fashion, from atoms to connected motifs. Each level integrates the encoding of constituents below with the graph at that level. Our autoregressive coarse-to-fine decoder adds one motif at a time, interleaving the decision of selecting a new motif with the process of resolving its attachments to the emerging molecule. We evaluate our model on multiple molecule generation tasks, including polymers, and show that our model significantly outperforms previous state-of-the-art baselines. 
- **arxivid:** 2002.03230 

### Grammar Variational Autoencoder 
- **year:** 2017 
- **url:** <https://www.semanticscholar.org/paper/222928303a72d1389b0add8032a31abccbba41b3>
- **abstract:** Deep generative models have been wildly successful at learning coherent latent representations for continuous data such as video and audio. However, generative modeling of discrete data such as arithmetic expressions and molecular structures still poses significant challenges. Crucially, state-of-the-art methods often produce outputs that are not valid. We make the key observation that frequently, discrete data can be represented as a parse tree from a context-free grammar. We propose a variational autoencoder which encodes and decodes directly to and from these parse trees, ensuring the generated outputs are always valid. Surprisingly, we show that not only does our model more often generate valid outputs, it also learns a more coherent latent space in which nearby points decode to similar discrete outputs. We demonstrate the effectiveness of our learned models by showing their improved performance in Bayesian optimization for symbolic regression and molecular synthesis. 
- **arxivid:** 1703.01925 

### Application of Generative Autoencoder in De Novo Molecular Design 
- **year:** 2017 
- **url:** <https://www.semanticscholar.org/paper/1241fe24e8588b8b7fbe6d119e21cf4554fcdcb8>
- **abstract:** A major challenge in computational chemistry is the generation of novel molecular structures with desirable pharmacological and physiochemical properties. In this work, we investigate the potential use of autoencoder, a deep learning methodology, for de novo molecular design. Various generative autoencoders were used to map molecule structures into a continuous latent space and vice versa and their performance as structure generator was assessed. Our results show that the latent space preserves chemical similarity principle and thus can be used for the generation of analogue structures. Furthermore, the latent space created by autoencoders were searched systematically to generate novel compounds with predicted activity against dopamine receptor type 2 and compounds similar to known active compounds not included in the trainings set were identified. 
- **journal:** Molecular Informatics 
- **volume:** 37 
- **pages:** null 
- **doi:** 10.1002/minf.201700123 
- **pmid:** 29235269 
- **arxivid:** 1711.07839 

### GuacaMol: Benchmarking Models for De Novo Molecular Design 
- **year:** 2018 
- **url:** <https://www.semanticscholar.org/paper/5bfeb6901db481c08874cfe0ae807d8564513765>
- **abstract:** De novo design seeks to generate molecules with required property profiles by virtual design-make-test cycles. With the emergence of deep learning and neural generative models in many application areas, models for molecular design based on neural networks appeared recently and show promising results. However, the new models have not been profiled on consistent tasks, and comparative studies to well-established algorithms have only seldom been performed. To standardize the assessment of both classical and neural models for de novo molecular design, we propose an evaluation framework, GuacaMol, based on a suite of standardized benchmarks. The benchmark tasks encompass measuring the fidelity of the models to reproduce the property distribution of the training sets, the ability to generate novel molecules, the exploration and exploitation of chemical space, and a variety of single and multiobjective optimization tasks. The benchmarking open-source Python code and a leaderboard can be found on <https://benevolent.ai/guacamol>
- **journal:** Journal of chemical information and modeling 
- **volume:** 59 3 
- **pages:** 1096-1108 
- **doi:** 10.1021/acs.jcim.8b00839 
- **pmid:** 30887799 
- **arxivid:** 1811.09621 

### Learning Deep Generative Models of Graphs 
- **year:** 2018 
- **url:** <https://www.semanticscholar.org/paper/f32f16ca3c27ff945198c6551a5d35fae3b1a660>
- **abstract:** Graphs are fundamental data structures which concisely capture the relational structure in many important real-world domains, such as knowledge graphs, physical and social interactions, language, and chemistry. Here we introduce a powerful new approach for learning generative models over graphs, which can capture both their structure and attributes. Our approach uses graph neural networks to express probabilistic dependencies among a graph's nodes and edges, and can, in principle, learn distributions over any arbitrary graph. In a series of experiments our results show that once trained, our models can generate good quality samples of both synthetic graphs as well as real molecular graphs, both unconditionally and conditioned on data. Compared to baselines that do not use graph-structured representations, our models often perform far better. We also explore key challenges of learning generative models of graphs, such as how to handle symmetries and ordering of elements during the graph generation process, and offer possible solutions. Our work is the first and most general approach for learning generative models over arbitrary graphs, and opens new directions for moving away from restrictions of vector- and sequence-like knowledge representations, toward more expressive and flexible relational data structures. 
- **journal:** ArXiv 
- **volume:** abs/1803.03324 
- **pages:** null 
- **arxivid:** 1803.03324 

### Deep reinforcement learning for de novo drug design 
- **year:** 2017 
- **url:** <https://www.semanticscholar.org/paper/4edd98e3947d8406ec95518c294721757afffb5d>
- **abstract:** We introduce an artificial intelligence approach to de novo design of molecules with desired physical or biological properties. We have devised and implemented a novel computational strategy for de novo design of molecules with desired properties termed ReLeaSE (Reinforcement Learning for Structural Evolution). On the basis of deep and reinforcement learning (RL) approaches, ReLeaSE integrates two deep neural networks—generative and predictive—that are trained separately but are used jointly to generate novel targeted chemical libraries. ReLeaSE uses simple representation of molecules by their simplified molecular-input line-entry system (SMILES) strings only. Generative models are trained with a stack-augmented memory network to produce chemically feasible SMILES strings, and predictive models are derived to forecast the desired properties of the de novo–generated compounds. In the first phase of the method, generative and predictive models are trained separately with a supervised learning algorithm. In the second phase, both models are trained jointly with the RL approach to bias the generation of new chemical structures toward those with the desired physical and/or biological properties. In the proof-of-concept study, we have used the ReLeaSE method to design chemical libraries with a bias toward structural complexity or toward compounds with maximal, minimal, or specific range of physical properties, such as melting point or hydrophobicity, or toward compounds with inhibitory activity against Janus protein kinase 2. The approach proposed herein can find a general use for generating targeted chemical libraries of novel compounds optimized for either a single desired property or multiple properties. 
- **journal:** Science Advances 
- **volume:** 4 
- **pages:** null 
- **doi:** 10.1126/sciadv.aap7885 
- **pmid:** 30050984 
- **arxivid:** 1711.10907 

### Learning Multimodal Graph-to-Graph Translation for Molecular Optimization 
- **year:** 2018 
- **url:** <https://www.semanticscholar.org/paper/8ee3ba29ad49c2ded00e88ee0dad1de17cc2b309>
- **abstract:** We view molecular optimization as a graph-to-graph translation problem. The goal is to learn to map from one molecular graph to another with better properties based on an available corpus of paired molecules. Since molecules can be optimized in different ways, there are multiple viable translations for each input graph. A key challenge is therefore to model diverse translation outputs. Our primary contributions include a junction tree encoder-decoder for learning diverse graph translations along with a novel adversarial training method for aligning distributions of molecules. Diverse output distributions in our model are explicitly realized by low-dimensional latent vectors that modulate the translation process. We evaluate our model on multiple molecular optimization tasks and show that our model outperforms previous state-of-the-art baselines. 
- **journal:** ArXiv 
- **volume:** abs/1812.01070 
- **pages:** null 
- **arxivid:** 1812.01070 

### druGAN: An Advanced Generative Adversarial Autoencoder Model for de Novo Generation of New Molecules with Desired Molecular Properties in Silico. 
- **year:** 2017 
- **url:** <https://www.semanticscholar.org/paper/3b1115226eb73af88681fc2dac9bd35ff01c8991>
- **abstract:** Deep generative adversarial networks (GANs) are the emerging technology in drug discovery and biomarker development. In our recent work, we demonstrated a proof-of-concept of implementing deep generative adversarial autoencoder (AAE) to identify new molecular fingerprints with predefined anticancer properties. Another popular generative model is the variational autoencoder (VAE), which is based on deep neural architectures. In this work, we developed an advanced AAE model for molecular feature extraction problems, and demonstrated its advantages compared to VAE in terms of (a) adjustability in generating molecular fingerprints; (b) capacity of processing very large molecular data sets; and (c) efficiency in unsupervised pretraining for regression model. Our results suggest that the proposed AAE model significantly enhances the capacity and efficiency of development of the new molecules with specific anticancer properties using the deep generative models. 
- **journal:** Molecular pharmaceutics 
- **volume:** 14 9 
- **pages:** 3098-3104 
- **doi:** 10.1021/acs.molpharmaceut.7b00346 
- **pmid:** 28703000 

### Fréchet ChemNet Distance: A Metric for Generative Models for Molecules in Drug Discovery 
- **year:** 2018 
- **url:** <https://www.semanticscholar.org/paper/7d878fe31b9b57f75071586d83cdec2e8b81e039>
- **abstract:** The new wave of successful generative models in machine learning has increased the interest in deep learning driven de novo drug design. However, method comparison is difficult because of various flaws of the currently employed evaluation metrics. We propose an evaluation metric for generative models called Fréchet ChemNet distance (FCD). The advantage of the FCD over previous metrics is that it can detect whether generated molecules are diverse and have similar chemical and biological properties as real molecules. 
- **journal:** Journal of chemical information and modeling 
- **volume:** 58 9 
- **pages:** 1736-1741 
- **doi:** 10.1021/acs.jcim.8b00234 
- **pmid:** 30118593 
- **arxivid:** 1803.09518 

### Graph Convolutional Policy Network for Goal-Directed Molecular Graph Generation 
- **year:** 2018 
- **url:** <https://www.semanticscholar.org/paper/d9f836a2062864e4808e12224e2286a353498202>
- **abstract:** Generating novel graph structures that optimize given objectives while obeying some given underlying rules is fundamental for chemistry, biology and social science research. This is especially important in the task of molecular graph generation, whose goal is to discover novel molecules with desired properties such as drug-likeness and synthetic accessibility, while obeying physical laws such as chemical valency. However, designing models to find molecules that optimize desired properties while incorporating highly complex and non-differentiable rules remains to be a challenging task. Here we propose Graph Convolutional Policy Network (GCPN), a general graph convolutional network based model for goal-directed graph generation through reinforcement learning. The model is trained to optimize domain-specific rewards and adversarial loss through policy gradient, and acts in an environment that incorporates domain-specific rules. Experimental results show that GCPN can achieve 61% improvement on chemical property optimization over state-of-the-art baselines while resembling known molecules, and achieve 184% improvement on the constrained property optimization task. 
- **arxivid:** 1806.02473 

### Molecular generative model based on conditional variational autoencoder for de novo molecular design 
- **year:** 2018 
- **url:** <https://www.semanticscholar.org/paper/e4f0bf3074d5ae6d55d22068dd50158dc81b2a0a>
- **abstract:** *TL;DR:* A molecular generative model based on the conditional variational autoencoder that can be used to generate drug-like molecules with five target properties and to adjust a single property without changing the others and to manipulate it beyond the range of the dataset is proposed. 
- **journal:** Journal of Cheminformatics 
- **volume:** 10 
- **pages:** null 
- **doi:** 10.1186/s13321-018-0286-7 
- **pmid:** 29995272 
- **arxivid:** 1806.05805 

### Entangled Conditional Adversarial Autoencoder for de Novo Drug Discovery. 
- **year:** 2018 
- **url:** <https://www.semanticscholar.org/paper/00747ad8ecbaa2478f929747c78b312647df9e68>
- **abstract:** Modern computational approaches and machine learning techniques accelerate the invention of new drugs. Generative models can discover novel molecular structures within hours, while conventional drug discovery pipelines require months of work. In this article, we propose a new generative architecture, entangled conditional adversarial autoencoder, that generates molecular structures based on various properties, such as activity against a specific protein, solubility, or ease of synthesis. We apply the proposed model to generate a novel inhibitor of Janus kinase 3, implicated in rheumatoid arthritis, psoriasis, and vitiligo. The discovered molecule was tested in vitro and showed good activity and selectivity. 
- **journal:** Molecular pharmaceutics 
- **volume:** 15 10 
- **pages:** 4398-4405 
- **doi:** 10.1021/acs.molpharmaceut.8b00839 
- **pmid:** 30180591 

### MolGAN: An implicit generative model for small molecular graphs 
- **year:** 2018 
- **url:** <https://www.semanticscholar.org/paper/def1049b5aae96c8e1eab0ca58d77ac9c2f0e3e9>
- **abstract:** eep generative models for graph-structured data offer a new angle on the problem of chemical synthesis: by optimizing differentiable models that directly generate molecular graphs, it is pos-sible to side-step expensive search procedures in the discrete and vast space of chemical structures. We introduce MolGAN, an implicit, likelihood-free generative model for small molecular graphs that circumvents the need for expensive graph matching procedures or node ordering heuris-tics of previous likelihood-based methods. Our method adapts generative adversarial networks (GANs) to operate directly on graph-structured data. We combine our approach with a reinforce-ment learning objective to encourage the genera-tion of molecules with specific desired chemical properties. In experiments on the QM9 chemi-cal database, we demonstrate that our model is capable of generating close to 100% valid com-pounds. MolGAN compares favorably both to recent proposals that use string-based (SMILES) representations of molecules and to a likelihood-based method that directly generates graphs, al-beit being susceptible to mode collapse. 
- **journal:** ArXiv 
- **volume:** abs/1805.11973 
- **pages:** null 
- **arxivid:** 1805.11973 

### Deep learning enables rapid identification of potent DDR1 kinase inhibitors 
- **year:** 2019 
- **url:** <https://www.semanticscholar.org/paper/d44ac0a7fd4734187bccafc4a2771027b8bb595e>
- **abstract:** *TL;DR:* A machine learning model allows the identification of new small-molecule kinase inhibitors in days and is used to discover potent inhibitors of discoidin domain receptor 1 (DDR1), a kinase target implicated in fibrosis and other diseases, in 21 days. 
- **journal:** Nature Biotechnology 
- **volume:** 37 
- **pages:** 1038 - 1040 
- **doi:** 10.1038/s41587-019-0224-x 
- **pmid:** 31477924 

### Inverse molecular design using machine learning: Generative models for matter engineering 
- **year:** 2018 
- **url:** <https://www.semanticscholar.org/paper/175e37bca3762b3a52c6a0e153060b98a251d061>
- **abstract:** The discovery of new materials can bring enormous societal and technological progress. In this context, exploring completely the large space of potential materials is computationally intractable. Here, we review methods for achieving inverse design, which aims to discover tailored materials from the starting point of a particular desired functionality. Recent advances from the rapidly growing field of artificial intelligence, mostly from the subfield of machine learning, have resulted in a fertile exchange of ideas, where approaches to inverse molecular design are being proposed and employed at a rapid pace. Among these, deep generative models have been applied to numerous classes of materials: rational design of prospective drugs, synthetic routes to organic compounds, and optimization of photovoltaics and redox flow batteries, as well as a variety of other solid-state materials. 
- **journal:** Science 
- **volume:** 361 
- **pages:** 360 - 365 
- **doi:** 10.1126/science.aat2663 
- **pmid:** 30049875 

### Objective-Reinforced Generative Adversarial Networks (ORGAN) for Sequence Generation Models 
- **year:** 2017 
- **url:** <https://www.semanticscholar.org/paper/15d739e2c184a6844bdbd9a2550d007de6ddb085>
- **abstract:** In unsupervised data generation tasks, besides the generation of a sample based on previous observations, one would often like to give hints to the model in order to bias the generation towards desirable metrics. We propose a method that combines Generative Adversarial Networks (GANs) and reinforcement learning (RL) in order to accomplish exactly that. While RL biases the data generation process towards arbitrary metrics, the GAN component of the reward function ensures that the model still remembers information learned from data. We build upon previous results that incorporated GANs and RL in order to generate sequence data and test this model in several settings for the generation of molecules encoded as text sequences (SMILES) and in the context of music generation, showing for each case that we can effectively bias the generation process towards desired metrics. 
- **journal:** ArXiv 
- **volume:** abs/1705.10843 
- **pages:** null 
- **arxivid:** 1705.10843 

### Automatic Chemical Design using Variational Autoencoders 
- **year:** 2016 
- **url:** <https://www.semanticscholar.org/paper/694709d8b50f80a7117ff9f431bcb2311412bbc6>
- **abstract:** We train a variational autoencoder to convert discrete representations of molecules to and from a multidimensional continuous representation. This continuous representation allow us to automatically generate novel chemical structures by performing simple operations in the latent space, such as decoding random vectors, perturbing known chemical structures, or interpolating between molecules. Continuous representations also allow the use of powerful gradient-based optimization to efficiently guide the search for optimized functional compounds. We demonstrate our method in the design of drug-like molecules as well as organic light-emitting diodes. 

### The rise of deep learning in drug discovery. 
- **year:** 2018 
- **url:** <https://www.semanticscholar.org/paper/89213307256d538942fab6b4ac7ab0dee6936582>
- **abstract:** *TL;DR:* The first wave of applications of deep learning in pharmaceutical research has emerged in recent years, and its utility has gone beyond bioactivity predictions and has shown promise in addressing diverse problems in drug discovery. 
- **journal:** Drug discovery today 
- **volume:** 23 6 
- **pages:** 1241-1250 
- **doi:** 10.1016/j.drudis.2018.01.039 
- **pmid:** 29366762 
