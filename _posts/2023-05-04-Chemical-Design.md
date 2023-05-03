---
title: NeRF
author: Daniel Park
date: 2023-04-30
category: life
layout: post
---

> 배치성 프로그램으로 진행하고 있는 연구에 참고될만한 논문들을 자동 생성합니다. 논문들은 인용 관계로 서로 연결되어 있으며, 인용 횟수 순으로 정렬되어 있습니다. The batch program generates research papers that can be referenced in my ongoing studies. These papers are connected to each other through citation relationships and are sorted by the number of citations.


- Related Project: Private 
- Project Status: 1 Alpha
- Date: 2023-04

## Automatic Chemical Design Using a Data-Driven Continuous Representation of Molecules 
- **year:** 2016 
- **url:** https://www.semanticscholar.org/paper/88427d2143d4cff357c3b393ae7580a7b6e19940 
- **abstract:** We report a method to convert discrete representations of molecules to and from a multidimensional continuous representation. This model allows us to generate new molecules for efficient exploration and optimization through open-ended spaces of chemical compounds. A deep neural network was trained on hundreds of thousands of existing chemical structures to construct three coupled functions: an encoder, a decoder, and a predictor. The encoder converts the discrete representation of a molecule into a real-valued continuous vector, and the decoder converts these continuous vectors back to discrete molecular representations. The predictor estimates chemical properties from the latent continuous vector representation of the molecule. Continuous representations of molecules allow us to automatically generate novel chemical structures by performing simple operations in the latent space, such as decoding random vectors, perturbing known chemical structures, or interpolating between molecules. Continuous representations also allow the use of powerful gradient-based optimization to efficiently guide the search for optimized functional compounds. We demonstrate our method in the domain of drug-like molecules and also in a set of molecules with fewer that nine heavy atoms. 
- **journal:** ACS Central Science 
- **volume:** 4 
- **pages:** 268 - 276 
- **doi:** 10.1021/acscentsci.7b00572 
- **pmid:** 29532027 
- **arxivid:** 1610.02415 

![](https://dsdanielpark.github.io/assets/post/230504_chemical_design/01.png)
![](https://dsdanielpark.github.io/assets/post/230504_chemical_design/02.png)
![](https://dsdanielpark.github.io/assets/post/230504_chemical_design/03.png)


## Syntax-Directed Variational Autoencoder for Structured Data 
- **year:** 2018 
- **url:** https://www.semanticscholar.org/paper/7dd434b3799a6c8c346a1d7ee77d37980a4ef5b9 
- **abstract:** Deep generative models have been enjoying success in modeling continuous data. However it remains challenging to capture the representations for discrete structures with formal grammars and semantics, e.g., computer programs and molecular structures. How to generate both syntactically and semantically correct data still remains largely an open problem. Inspired by the theory of compiler where the syntax and semantics check is done via syntax-directed translation (SDT), we propose a novel syntax-directed variational autoencoder (SD-VAE) by introducing stochastic lazy attributes. This approach converts the offline SDT check into on-the-fly generated guidance for constraining the decoder. Comparing to the state-of-the-art methods, our approach enforces constraints on the output space so that the output will be not only syntactically valid, but also semantically reasonable. We evaluate the proposed model with applications in programming language and molecules, including reconstruction and program/molecule optimization. The results demonstrate the effectiveness in incorporating syntactic and semantic constraints in discrete generative models, which is significantly better than current state-of-the-art approaches. 
- **journal:** ArXiv 
- **volume:** abs/1802.08786 
- **pages:** null 
- **arxivid:** 1802.08786 

## GraphRNN: Generating Realistic Graphs with Deep Auto-regressive Models 
- **year:** 2018 
- **url:** https://www.semanticscholar.org/paper/e1cef464322243feb12ac3f81873c912e071a1a6 
- **abstract:** Modeling and generating graphs is fundamental for studying networks in biology, engineering, and social sciences. However, modeling complex distributions over graphs and then efficiently sampling from these distributions is challenging due to the non-unique, high-dimensional nature of graphs and the complex, non-local dependencies that exist between edges in a given graph. Here we propose GraphRNN, a deep autoregressive model that addresses the above challenges and approximates any distribution of graphs with minimal assumptions about their structure. GraphRNN learns to generate graphs by training on a representative set of graphs and decomposes the graph generation process into a sequence of node and edge formations, conditioned on the graph structure generated so far. In order to quantitatively evaluate the performance of GraphRNN, we introduce a benchmark suite of datasets, baselines and novel evaluation metrics based on Maximum Mean Discrepancy, which measure distances between sets of graphs. Our experiments show that GraphRNN significantly outperforms all baselines, learning to generate diverse graphs that match the structural characteristics of a target set, while also scaling to graphs 50 times larger than previous deep models. 
- **arxivid:** 1802.08773 

## Constrained Graph Variational Autoencoders for Molecule Design 
- **year:** 2018 
- **url:** https://www.semanticscholar.org/paper/b83e7e9a7bf59347eb9bc53ecaf139e301a8b72d 
- **abstract:** Graphs are ubiquitous data structures for representing interactions between entities. With an emphasis on the use of graphs to represent chemical molecules, we explore the task of learning to generate graphs that conform to a distribution observed in training data. We propose a variational autoencoder model in which both encoder and decoder are graph-structured. Our decoder assumes a sequential ordering of graph extension steps and we discuss and analyze design choices that mitigate the potential downsides of this linearization. Experiments compare our approach with a wide range of baselines on the molecule generation task and show that our method is more successful at matching the statistics of the original dataset on semantically important metrics. Furthermore, we show that by using appropriate shaping of the latent space, our model allows us to design molecules that are (locally) optimal in desired properties. 
- **journal:** ArXiv 
- **volume:** abs/1805.09076 
- **pages:** null 
- **arxivid:** 1805.09076 

## Constrained Generation of Semantically Valid Graphs via Regularizing Variational Autoencoders 
- **year:** 2018 
- **url:** https://www.semanticscholar.org/paper/68030c396dc2c02ffe1232f4cb177b9da93662d1 
- **abstract:** Deep generative models have achieved remarkable success in various data domains, including images, time series, and natural languages. There remain, however, substantial challenges for combinatorial structures, including graphs. One of the key challenges lies in the difficulty of ensuring semantic validity in context. For example, in molecular graphs, the number of bonding-electron pairs must not exceed the valence of an atom; whereas in protein interaction networks, two proteins may be connected only when they belong to the same or correlated gene ontology terms. These constraints are not easy to be incorporated into a generative model. In this work, we propose a regularization framework for variational autoencoders as a step toward semantic validity. We focus on the matrix representation of graphs and formulate penalty terms that regularize the output distribution of the decoder to encourage the satisfaction of validity constraints. Experimental results confirm a much higher likelihood of sampling valid graphs in our approach, compared with others reported in the literature. 
- **arxivid:** 1809.02630 

## GraphAF: a Flow-based Autoregressive Model for Molecular Graph Generation 
- **year:** 2020 
- **url:** https://www.semanticscholar.org/paper/036d743c7ca1e513adf0a91594fc8111e03dc30c 
- **abstract:** Molecular graph generation is a fundamental problem for drug discovery and has been attracting growing attention. The problem is challenging since it requires not only generating chemically valid molecular structures but also optimizing their chemical properties in the meantime. Inspired by the recent progress in deep generative models, in this paper we propose a flow-based autoregressive model for graph generation called GraphAF. GraphAF combines the advantages of both autoregressive and flow-based approaches and enjoys: (1) high model flexibility for data density estimation; (2) efficient parallel computation for training; (3) an iterative sampling process, which allows leveraging chemical domain knowledge for valency checking. Experimental results show that GraphAF is able to generate 68% chemically valid molecules even without chemical knowledge rules and 100% valid molecules with chemical rules. The training process of GraphAF is two times faster than the existing state-of-the-art approach GCPN. After fine-tuning the model for goal-directed property optimization with reinforcement learning, GraphAF achieves state-of-the-art performance on both chemical property optimization and constrained property optimization. 
- **journal:** ArXiv 
- **volume:** abs/2001.09382 
- **pages:** null 
- **arxivid:** 2001.09382 

## LATION FOR MOLECULAR OPTIMIZATION 
- **year:** 2019 
- **url:** https://www.semanticscholar.org/paper/4e5d0bbe8e488685552dc42cf572b5bb6535c6dc 
- **abstract:** We view molecular optimization as a graph-to-graph translation problem. The goal is to learn to map from one molecular graph to another with better properties based on an available corpus of paired molecules. Since molecules can be optimized in different ways, there are multiple viable translations for each input graph. A key challenge is therefore to model diverse translation outputs. Our primary contributions include a junction tree encoder-decoder for learning diverse graph translations along with a novel adversarial training method for aligning distributions of molecules. Diverse output distributions in our model are explicitly realized by low-dimensional latent vectors that modulate the translation process. We evaluate our model on multiple molecular optimization tasks and show that our model outperforms previous state-of-the-art baselines. 

## Quantifying the chemical beauty of drugs. 
- **year:** 2012 
- **url:** https://www.semanticscholar.org/paper/11bce438e2fdc7a7ae5f65c339c757f386f4f48a 
- **abstract:** S2 TL;DR: The utility of QED is extended by applying it to the problem of molecular target druggability assessment by prioritizing a large set of published bioactive compounds and may also capture the abstract notion of aesthetics in medicinal chemistry. 
- **journal:** Nature chemistry 
- **volume:** 4 2 
- **pages:** 90-8 
- **doi:** 10.1038/nchem.1243 
- **pmid:** 22270643 

## Multi-objective de novo drug design with conditional graph generative model 
- **year:** 2018 
- **url:** https://www.semanticscholar.org/paper/14f1f267731c89bbff04fce87b223d73168d8a4e 
- **abstract:** S2 TL;DR: A new de novo molecular design framework is proposed based on a type of sequential graph generators that do not use atom level recurrent units, which is much more tuned for molecule generation and has been scaled up to cover significantly larger molecules in the ChEMBL database. 
- **journal:** Journal of Cheminformatics 
- **volume:** 10 
- **pages:** null 
- **doi:** 10.1186/s13321-018-0287-6 
- **pmid:** 30043127 
- **arxivid:** 1801.07299 

## Generating Focused Molecule Libraries for Drug Discovery with Recurrent Neural Networks 
- **year:** 2017 
- **url:** https://www.semanticscholar.org/paper/1cb789ab8925bda02758bcb69eb0ed1547b5f4b9 
- **abstract:** In de novo drug design, computational strategies are used to generate novel molecules with good affinity to the desired biological target. In this work, we show that recurrent neural networks can be trained as generative models for molecular structures, similar to statistical language models in natural language processing. We demonstrate that the properties of the generated molecules correlate very well with the properties of the molecules used to train the model. In order to enrich libraries with molecules active toward a given biological target, we propose to fine-tune the model with small sets of molecules, which are known to be active against that target. Against Staphylococcus aureus, the model reproduced 14% of 6051 hold-out test molecules that medicinal chemists designed, whereas against Plasmodium falciparum (Malaria), it reproduced 28% of 1240 test molecules. When coupled with a scoring function, our model can perform the complete de novo drug design cycle to generate large sets of novel molecules for drug discovery. 
- **journal:** ACS Central Science 
- **volume:** 4 
- **pages:** 120 - 131 
- **doi:** 10.1021/acscentsci.7b00512 
- **pmid:** 29392184 

## Generative Recurrent Networks for De Novo Drug Design 
- **year:** 2017 
- **url:** https://www.semanticscholar.org/paper/517a488f06577401422cf7e03647ac6148ef4e44 
- **abstract:** Generative artificial intelligence models present a fresh approach to chemogenomics and de novo drug design, as they provide researchers with the ability to narrow down their search of the chemical space and focus on regions of interest. We present a method for molecular de novo design that utilizes generative recurrent neural networks (RNN) containing long short‐term memory (LSTM) cells. This computational model captured the syntax of molecular representation in terms of SMILES strings with close to perfect accuracy. The learned pattern probabilities can be used for de novo SMILES generation. This molecular design concept eliminates the need for virtual compound library enumeration. By employing transfer learning, we fine‐tuned the RNN′s predictions for specific molecular targets. This approach enables virtual compound design without requiring secondary or external activity prediction, which could introduce error or unwanted bias. The results obtained advocate this generative RNN‐LSTM system for high‐impact use cases, such as low‐data drug discovery, fragment based molecular design, and hit‐to‐lead optimization for diverse drug targets. 
- **journal:** Molecular Informatics 
- **volume:** 37 
- **pages:** null 
- **doi:** 10.1002/minf.201700111 
- **pmid:** 29095571 

## Optimizing distributions over molecular space. An Objective-Reinforced Generative Adversarial Network for Inverse-design Chemistry (ORGANIC) 
- **year:** 2017 
- **url:** https://www.semanticscholar.org/paper/61c05d7cab4448a1585596cc7e00ab271c442c2e 
- **abstract:** Molecular discovery seeks to generate chemical species tailored to very speciﬁc needs. In this paper, we present ORGANIC , a framework based on Objective-Reinforced Generative Adversarial Networks (ORGAN), capable of producing a distribution over molecular space that matches with a certain set of desirable metrics. This methodology combines two successful techniques from the machine learning community: a Generative Adversarial Network (GAN), to create non-repetitive sensible molecular species, and Reinforcement Learning (RL), to bias this generative distribution towards certain attributes. We explore several applications, from optimization of random physicochemical properties to candidates for drug discovery and organic photovoltaic material design. 
- **journal:** ChemRxiv 
- **volume:**  
- **pages:** null 
- **doi:** 10.26434/CHEMRXIV.5309668 

## Molecular Sets (MOSES): A Benchmarking Platform for Molecular Generation Models 
- **year:** 2018 
- **url:** https://www.semanticscholar.org/paper/404571933e3e87942768c9a5cde8a6285732ad6f 
- **abstract:** Generative models are becoming a tool of choice for exploring the molecular space. These models learn on a large training dataset and produce novel molecular structures with similar properties. Generated structures can be utilized for virtual screening or training semi-supervized predictive models in the downstream tasks. While there are plenty of generative models, it is unclear how to compare and rank them. In this work, we introduce a benchmarking platform called Molecular Sets (MOSES) to standardize training and comparison of molecular generative models. MOSES provides training and testing datasets, and a set of metrics to evaluate the quality and diversity of generated structures. We have implemented and compared several molecular generation models and suggest to use our results as reference points for further advancements in generative chemistry research. The platform and source code are available at https://github.com/molecularsets/moses. 
- **journal:** Frontiers in Pharmacology 
- **volume:** 11 
- **pages:** null 
- **doi:** 10.3389/fphar.2020.565644 
- **pmid:** 33390943 
- **arxivid:** 1811.12823 

## MolecularRNN: Generating realistic molecular graphs with optimized properties 
- **year:** 2019 
- **url:** https://www.semanticscholar.org/paper/3ccd291c8848c73ca34152e27c3ec296cfc838d0 
- **abstract:** Designing new molecules with a set of predefined properties is a core problem in modern drug discovery and development. There is a growing need for de-novo design methods that would address this problem. We present MolecularRNN, the graph recurrent generative model for molecular structures. Our model generates diverse realistic molecular graphs after likelihood pretraining on a big database of molecules. We perform an analysis of our pretrained models on large-scale generated datasets of 1 million samples. Further, the model is tuned with policy gradient algorithm, provided a critic that estimates the reward for the property of interest. We show a significant distribution shift to the desired range for lipophilicity, drug-likeness, and melting point outperforming state-of-the-art works. With the use of rejection sampling based on valency constraints, our model yields 100% validity. Moreover, we show that invalid molecules provide a rich signal to the model through the use of structure penalty in our reinforcement learning pipeline. 
- **journal:** ArXiv 
- **volume:** abs/1905.13372 
- **pages:** null 
- **arxivid:** 1905.13372 

## Hierarchical Generation of Molecular Graphs using Structural Motifs 
- **year:** 2020 
- **url:** https://www.semanticscholar.org/paper/dc7307f6e49f0ad2432be4eea92ae7f854c3cebb 
- **abstract:** Graph generation techniques are increasingly being adopted for drug discovery. Previous graph generation approaches have utilized relatively small molecular building blocks such as atoms or simple cycles, limiting their effectiveness to smaller molecules. Indeed, as we demonstrate, their performance degrades significantly for larger molecules. In this paper, we propose a new hierarchical graph encoder-decoder that employs significantly larger and more flexible graph motifs as basic building blocks. Our encoder produces a multi-resolution representation for each molecule in a fine-to-coarse fashion, from atoms to connected motifs. Each level integrates the encoding of constituents below with the graph at that level. Our autoregressive coarse-to-fine decoder adds one motif at a time, interleaving the decision of selecting a new motif with the process of resolving its attachments to the emerging molecule. We evaluate our model on multiple molecule generation tasks, including polymers, and show that our model significantly outperforms previous state-of-the-art baselines. 
- **arxivid:** 2002.03230 

## Grammar Variational Autoencoder 
- **year:** 2017 
- **url:** https://www.semanticscholar.org/paper/222928303a72d1389b0add8032a31abccbba41b3 
- **abstract:** Deep generative models have been wildly successful at learning coherent latent representations for continuous data such as video and audio. However, generative modeling of discrete data such as arithmetic expressions and molecular structures still poses significant challenges. Crucially, state-of-the-art methods often produce outputs that are not valid. We make the key observation that frequently, discrete data can be represented as a parse tree from a context-free grammar. We propose a variational autoencoder which encodes and decodes directly to and from these parse trees, ensuring the generated outputs are always valid. Surprisingly, we show that not only does our model more often generate valid outputs, it also learns a more coherent latent space in which nearby points decode to similar discrete outputs. We demonstrate the effectiveness of our learned models by showing their improved performance in Bayesian optimization for symbolic regression and molecular synthesis. 
- **arxivid:** 1703.01925 

## Application of Generative Autoencoder in De Novo Molecular Design 
- **year:** 2017 
- **url:** https://www.semanticscholar.org/paper/1241fe24e8588b8b7fbe6d119e21cf4554fcdcb8 
- **abstract:** A major challenge in computational chemistry is the generation of novel molecular structures with desirable pharmacological and physiochemical properties. In this work, we investigate the potential use of autoencoder, a deep learning methodology, for de novo molecular design. Various generative autoencoders were used to map molecule structures into a continuous latent space and vice versa and their performance as structure generator was assessed. Our results show that the latent space preserves chemical similarity principle and thus can be used for the generation of analogue structures. Furthermore, the latent space created by autoencoders were searched systematically to generate novel compounds with predicted activity against dopamine receptor type 2 and compounds similar to known active compounds not included in the trainings set were identified. 
- **journal:** Molecular Informatics 
- **volume:** 37 
- **pages:** null 
- **doi:** 10.1002/minf.201700123 
- **pmid:** 29235269 
- **arxivid:** 1711.07839 

## GuacaMol: Benchmarking Models for De Novo Molecular Design 
- **year:** 2018 
- **url:** https://www.semanticscholar.org/paper/5bfeb6901db481c08874cfe0ae807d8564513765 
- **abstract:** De novo design seeks to generate molecules with required property profiles by virtual design-make-test cycles. With the emergence of deep learning and neural generative models in many application areas, models for molecular design based on neural networks appeared recently and show promising results. However, the new models have not been profiled on consistent tasks, and comparative studies to well-established algorithms have only seldom been performed. To standardize the assessment of both classical and neural models for de novo molecular design, we propose an evaluation framework, GuacaMol, based on a suite of standardized benchmarks. The benchmark tasks encompass measuring the fidelity of the models to reproduce the property distribution of the training sets, the ability to generate novel molecules, the exploration and exploitation of chemical space, and a variety of single and multiobjective optimization tasks. The benchmarking open-source Python code and a leaderboard can be found on https://benevolent.ai/guacamol . 
- **journal:** Journal of chemical information and modeling 
- **volume:** 59 3 
- **pages:** 1096-1108 
- **doi:** 10.1021/acs.jcim.8b00839 
- **pmid:** 30887799 
- **arxivid:** 1811.09621 

## Learning Multimodal Graph-to-Graph Translation for Molecular Optimization 
- **year:** 2018 
- **url:** https://www.semanticscholar.org/paper/8ee3ba29ad49c2ded00e88ee0dad1de17cc2b309 
- **abstract:** We view molecular optimization as a graph-to-graph translation problem. The goal is to learn to map from one molecular graph to another with better properties based on an available corpus of paired molecules. Since molecules can be optimized in different ways, there are multiple viable translations for each input graph. A key challenge is therefore to model diverse translation outputs. Our primary contributions include a junction tree encoder-decoder for learning diverse graph translations along with a novel adversarial training method for aligning distributions of molecules. Diverse output distributions in our model are explicitly realized by low-dimensional latent vectors that modulate the translation process. We evaluate our model on multiple molecular optimization tasks and show that our model outperforms previous state-of-the-art baselines. 
- **journal:** ArXiv 
- **volume:** abs/1812.01070 
- **pages:** null 
- **arxivid:** 1812.01070 

## Graph Convolutional Policy Network for Goal-Directed Molecular Graph Generation 
- **year:** 2018 
- **url:** https://www.semanticscholar.org/paper/d9f836a2062864e4808e12224e2286a353498202 
- **abstract:** Generating novel graph structures that optimize given objectives while obeying some given underlying rules is fundamental for chemistry, biology and social science research. This is especially important in the task of molecular graph generation, whose goal is to discover novel molecules with desired properties such as drug-likeness and synthetic accessibility, while obeying physical laws such as chemical valency. However, designing models to find molecules that optimize desired properties while incorporating highly complex and non-differentiable rules remains to be a challenging task. Here we propose Graph Convolutional Policy Network (GCPN), a general graph convolutional network based model for goal-directed graph generation through reinforcement learning. The model is trained to optimize domain-specific rewards and adversarial loss through policy gradient, and acts in an environment that incorporates domain-specific rules. Experimental results show that GCPN can achieve 61% improvement on chemical property optimization over state-of-the-art baselines while resembling known molecules, and achieve 184% improvement on the constrained property optimization task. 
- **journal:** ArXiv 
- **volume:** abs/1806.02473 
- **pages:** null 
- **arxivid:** 1806.02473 

## MolGAN: An implicit generative model for small molecular graphs 
- **year:** 2018 
- **url:** https://www.semanticscholar.org/paper/def1049b5aae96c8e1eab0ca58d77ac9c2f0e3e9 
- **abstract:** S2 TL;DR: MolGAN is introduced, an implicit, likelihood-free generative model for small molecular graphs that circumvents the need for expensive graph matching procedures or node ordering heuris-tics of previous likelihood-based methods. 
- **journal:** ArXiv 
- **volume:** abs/1805.11973 
- **pages:** null 
- **arxivid:** 1805.11973 

## Multi-resolution Autoregressive Graph-to-Graph Translation for Molecules 
- **year:** 2019 
- **url:** https://www.semanticscholar.org/paper/3921efa210a7f413cefa1d6bb6d37764e2c9ef04 
- **abstract:** The problem of accelerating drug discovery relies heavily on automatic tools to optimize precursor molecules to afford them with better biochemical properties. Our work in this paper substantially extends prior state-of-the-art on graph-to-graph translation methods for molecular optimization. In particular, we realize coherent multi-resolution representations by interweaving trees over substructures with the atom-level encoding of the original molecular graph. Moreover, our graph decoder is fully autoregressive, and interleaves each step of adding a new substructure with the process of resolving its connectivity to the emerging molecule. We evaluate our model on multiple molecular optimization tasks and show that our model outperforms previous state-of-the-art baselines by a large margin. 
- **journal:** ArXiv 
- **volume:** abs/1907.11223 
- **pages:** null 
- **doi:** 10.26434/chemrxiv.8266745.v1 
- **arxivid:** 1907.11223 

## Inverse molecular design using machine learning: Generative models for matter engineering 
- **year:** 2018 
- **url:** https://www.semanticscholar.org/paper/175e37bca3762b3a52c6a0e153060b98a251d061 
- **abstract:** The discovery of new materials can bring enormous societal and technological progress. In this context, exploring completely the large space of potential materials is computationally intractable. Here, we review methods for achieving inverse design, which aims to discover tailored materials from the starting point of a particular desired functionality. Recent advances from the rapidly growing field of artificial intelligence, mostly from the subfield of machine learning, have resulted in a fertile exchange of ideas, where approaches to inverse molecular design are being proposed and employed at a rapid pace. Among these, deep generative models have been applied to numerous classes of materials: rational design of prospective drugs, synthetic routes to organic compounds, and optimization of photovoltaics and redox flow batteries, as well as a variety of other solid-state materials. 
- **journal:** Science 
- **volume:** 361 
- **pages:** 360 - 365 
- **doi:** 10.1126/science.aat2663 
- **pmid:** 30049875 

## SMILES, a chemical language and information system. 1. Introduction to methodology and encoding rules 
- **year:** 1988 
- **url:** https://www.semanticscholar.org/paper/3f7983818b76a5f1b5daf9b605877ed401c8e73c 
- **abstract:** (1) Klamer, A. D. “Some Results Concerning Polyominoes”. Fibonacci Q. 1965, 3(1), 9-20. (2) Golomb, S. W. Polyominoes·, Scribner, New York, 1965. (3) Harary, F.; Read, R. C. “The Enumeration of Tree-like Polyhexes”. Proc. Edinburgh Math. Soc. 1970, 17, 1-14. (4) Lunnon, W. F. “Counting Polyominoes” in Computers in Number Theory·, Academic: London, 1971; pp 347-372. (5) Lunnon, W. F. “Counting Hexagonal and Triangular Polyominoes”. Graph Theory Comput. 1972, 87-100. (6) Brunvoll, J.; Cyvin, S. J.; Cyvin, B. N. “Enumeration and Classification of Benzenoid Hydrocarbons”. J. Comput. Chem. 1987, 8, 189-197. (7) Balaban, A. T., et al. “Enumeration of Benzenoid and Coronoid Hydrocarbons”. Z. Naturforsch., A: Phys., Phys. Chem., Kosmophys. 1987, 42A, 863-870. (8) Gutman, I. “Topological Properties of Benzenoid Systems”. Bull. Soc. Chim., Beograd 1982, 47, 453-471. (9) Gutman, I.; Polansky, O. E. Mathematical Concepts in Organic Chemistry·, Springer: Berlin, 1986. (10) To3i6, R.; Doroslovacki, R.; Gutman, I. “Topological Properties of Benzenoid Systems—The Boundary Code”. MATCH 1986, No. 19, 219-228. (11) Doroslovacki, R.; ToSic, R. “A Characterization of Hexagonal Systems”. Rev. Res. Fac. Sci.-Univ. Novi Sad, Math. Ser. 1984,14(2) 201-209. (12) Knop, J. V.; Szymanski, K.; Trinajstic, N. “Computer Enumeration of Substituted Polyhexes”. Comput. Chem. 1984, 8(2), 107-115. (13) Stojmenovic, L; Tosió, R.; Doroslovaóki, R. “Generating and Counting Hexagonal Systems”. Proc. Yugosl. Semin. Graph Theory, 6th, Dubrovnik 1985; pp 189-198. (14) Doroslovaóki, R.; Stojmenovió, I.; Tosió, R. “Generating and Counting Triangular Systems”. BIT 1987, 27, 18-24. (15) Knop, J. V.; Miller, W. R.; Szymanski, K.; Trinajstic, N. Computer Generation of Certain Classes of Molecules·, Association of Chemists and Technologists of Croatia: Zagreb, 1985. 
- **journal:** J. Chem. Inf. Comput. Sci. 
- **volume:** 28 
- **pages:** 31-36 
- **doi:** 10.1021/ci00057a005 

## Generating Focussed Molecule Libraries for Drug Discovery with Recurrent Neural Networks 
- **year:** 2017 
- **url:** https://www.semanticscholar.org/paper/bfe7f183bc191665b39edd5fe62a66ae24de8319 
- **abstract:** In de novo drug design, computational strategies are used to generate novel molecules with good affinity to the desired biological target. In this work, we show that recurrent neural networks can be trained as generative models for molecular structures, similar to statistical language models in natural language processing. We demonstrate that the properties of the generated molecules correlate very well with the properties of the molecules used to train the model. In order to enrich libraries with molecules active towards a given biological target, we propose to fine-tune the model with small sets of molecules, which are known to be active against that target. Against Staphylococcus aureus, the model reproduced 14% of 6051 hold-out test molecules that medicinal chemists designed, whereas against Plasmodium falciparum (Malaria) it reproduced 28% of 1240 test molecules. When coupled with a scoring function, our model can perform the complete de novo drug design cycle to generate large sets of novel molecules for drug discovery. 
- **journal:** ArXiv 
- **volume:** abs/1701.01329 
- **pages:** null 
- **arxivid:** 1701.01329 

## Self-referencing embedded strings (SELFIES): A 100% robust molecular string representation 
- **year:** 2019 
- **url:** https://www.semanticscholar.org/paper/31b74437e2e46790f02b91933195b412684370be 
- **abstract:** The discovery of novel materials and functional molecules can help to solve some of society’s most urgent challenges, ranging from efficient energy harvesting and storage to uncovering novel pharmaceutical drug candidates. Traditionally matter engineering–generally denoted as inverse design–was based massively on human intuition and high-throughput virtual screening. The last few years have seen the emergence of significant interest in computer-inspired designs based on evolutionary or deep learning methods. The major challenge here is that the standard strings molecular representation SMILES shows substantial weaknesses in that task because large fractions of strings do not correspond to valid molecules. Here, we solve this problem at a fundamental level and introduce SELFIES (SELF-referencIng Embedded Strings), a string-based representation of molecules which is 100% robust. Every SELFIES string corresponds to a valid molecule, and SELFIES can represent every molecule. SELFIES can be directly applied in arbitrary machine learning models without the adaptation of the models; each of the generated molecule candidates is valid. In our experiments, the model’s internal memory stores two orders of magnitude more diverse molecules than a similar test with SMILES. Furthermore, as all molecules are valid, it allows for explanation and interpretation of the internal working of the generative models. 
- **journal:** Machine Learning: Science and Technology 
- **volume:** 1 
- **pages:** null 
- **doi:** 10.1088/2632-2153/aba947 

## Multi-Objective Molecule Generation using Interpretable Substructures 
- **year:** 2020 
- **url:** https://www.semanticscholar.org/paper/0cfc3ad63b8846edca9116bbef604310cacd0864 
- **abstract:** Drug discovery aims to find novel compounds with specified chemical property profiles. In terms of generative modeling, the goal is to learn to sample molecules in the intersection of multiple property constraints. This task becomes increasingly challenging when there are many property constraints. We propose to offset this complexity by composing molecules from a vocabulary of substructures that we call molecular rationales. These rationales are identified from molecules as substructures that are likely responsible for each property of interest. We then learn to expand rationales into a full molecule using graph generative models. Our final generative model composes molecules as mixtures of multiple rationale completions, and this mixture is fine-tuned to preserve the properties of interest. We evaluate our model on various drug design tasks and demonstrate significant improvements over state-of-the-art baselines in terms of accuracy, diversity, and novelty of generated compounds. 

## Hierarchical Graph-to-Graph Translation for Molecules 
- **year:** 2019 
- **url:** https://www.semanticscholar.org/paper/b4303019c36d799b193b2b3214546601a9874baa 
- **abstract:** The problem of accelerating drug discovery relies heavily on automatic tools to optimize precursor molecules to afford them with better biochemical properties. Our work in this paper substantially extends prior state-of-the-art on graph-to-graph translation methods for molecular optimization. In particular, we realize coherent multi-resolution representations by interweaving the encoding of substructure components with the atom-level encoding of the original molecular graph. Moreover, our graph decoder is fully autoregressive, and interleaves each step of adding a new substructure with the process of resolving its attachment to the emerging molecule. We evaluate our model on multiple molecular optimization tasks and show that our model significantly outperforms previous state-of-the-art baselines. 
- **journal:** arXiv: Chemical Physics 
- **volume:**  
- **pages:** null 

## Estimation of synthetic accessibility score of drug-like molecules based on molecular complexity and fragment contributions 
- **year:** 2009 
- **url:** https://www.semanticscholar.org/paper/9db40183d62ffae8f9b5a8327511840f6d16ceb1 
- **abstract:** S2 TL;DR: This method uses historical synthetic knowledge obtained by analyzing information from millions of already synthesized chemicals and considers also molecule complexity, which is sufficiently fast and provides results consistent with estimation of ease of synthesis by experienced medicinal chemists. 
- **journal:** Journal of Cheminformatics 
- **volume:** 1 
- **pages:** 8 - 8 
- **doi:** 10.1186/1758-2946-1-8 
- **pmid:** 20298526 

## Optimization of Molecules via Deep Reinforcement Learning 
- **year:** 2018 
- **url:** https://www.semanticscholar.org/paper/2ba00083a72558d45e4baecff0425ef6272f7a40 
- **abstract:** S2 TL;DR: Inspired by problems faced during medicinal chemistry lead optimization, the MolDQN model is extended with multi-objective reinforcement learning, which maximizes drug-likeness while maintaining similarity to the original molecule. 
- **journal:** Scientific Reports 
- **volume:** 9 
- **pages:** null 
- **doi:** 10.1038/s41598-019-47148-x 
- **pmid:** 31341196 
- **arxivid:** 1810.08678 

## Junction Tree Variational Autoencoder for Molecular Graph Generation 
- **year:** 2018 
- **url:** https://www.semanticscholar.org/paper/fd17bd9a5dc24a081ad9743570f50dd6750f54b2 
- **abstract:** We seek to automate the design of molecules based on specific chemical properties. In computational terms, this task involves continuous embedding and generation of molecular graphs. Our primary contribution is the direct realization of molecular graphs, a task previously approached by generating linear SMILES strings instead of graphs. Our junction tree variational autoencoder generates molecular graphs in two phases, by first generating a tree-structured scaffold over chemical substructures, and then combining them into a molecule with a graph message passing network. This approach allows us to incrementally expand molecules while maintaining chemical validity at every step. We evaluate our model on multiple tasks ranging from molecular generation to optimization. Across these tasks, our model outperforms previous state-of-the-art baselines by a significant margin. 
- **journal:** ArXiv 
- **volume:** abs/1802.04364 
- **pages:** null 
- **doi:** 10.1039/9781788016841-00228 
- **arxivid:** 1802.04364 

## Molecular de-novo design through deep reinforcement learning 
- **year:** 2017 
- **url:** https://www.semanticscholar.org/paper/d77bc27d16a362e5e1b727904c3789355dda6062 
- **abstract:** S2 TL;DR: A method to tune a sequence-based generative model for molecular de novo design that through augmented episodic likelihood can learn to generate structures with certain specified desirable properties is introduced. 
- **journal:** Journal of Cheminformatics 
- **volume:** 9 
- **pages:** null 
- **doi:** 10.1186/s13321-017-0235-x 
- **pmid:** 29086083 
- **arxivid:** 1704.07555 

## GraphVAE: Towards Generation of Small Graphs Using Variational Autoencoders 
- **year:** 2018 
- **url:** https://www.semanticscholar.org/paper/8913c23081e46a41cc7ced3c2ff379d9cd7afcde 
- **abstract:** S2 TL;DR: This work proposes to sidestep hurdles associated with linearization of discrete structures by having a decoder output a probabilistic fully-connected graph of a predefined maximum size directly at once by formulated as a variational autoencoder. 
- **doi:** 10.1007/978-3-030-01418-6_41 
- **arxivid:** 1802.03480 

## Conditional molecular design with deep generative models 
- **year:** 2018 
- **url:** https://www.semanticscholar.org/paper/bb1f2813687763cd91c795b2471cf6ef31a4e34b 
- **abstract:** Although machine learning has been successfully used to propose novel molecules that satisfy desired properties, it is still challenging to explore a large chemical space efficiently. In this paper, we present a conditional molecular design method that facilitates generating new molecules with desired properties. The proposed model, which simultaneously performs both property prediction and molecule generation, is built as a semisupervised variational autoencoder trained on a set of existing molecules with only a partial annotation. We generate new molecules with desired properties by sampling from the generative distribution estimated by the model. We demonstrate the effectiveness of the proposed model by evaluating it on drug-like molecules. The model improves the performance of property prediction by exploiting unlabeled molecules and efficiently generates novel molecules fulfilling various target conditions. 
- **journal:** Journal of chemical information and modeling 
- **volume:** 59 1 
- **pages:** 43-52 
- **doi:** 10.1021/acs.jcim.8b00263 
- **pmid:** 30016587 
- **arxivid:** 1805.00108 

## Mol-CycleGAN: a generative model for molecular optimization 
- **year:** 2019 
- **url:** https://www.semanticscholar.org/paper/90c97804c31287a35212538e85c5f34c0424341d 
- **abstract:** S2 TL;DR: Mol-CycleGAN—a CycleGAN-based model that generates optimized compounds with high structural similarity to the original ones is introduced, and in the task of optimization of penalized logP of drug-like molecules the model significantly outperforms previous results. 
- **journal:** Journal of Cheminformatics 
- **volume:** 12 
- **pages:** null 
- **doi:** 10.1186/s13321-019-0404-1 
- **pmid:** 33431006 
- **arxivid:** 1902.02119 

## Syntax-Directed Variational Autoencoder for Molecule Generation 
- **year:** 2017 
- **url:** https://www.semanticscholar.org/paper/583a2e12576ff99f3f4d3f2248420618b0f64489 
- **abstract:** Deep generative models have been enjoying success in modeling continuous data. However it remains challenging to capture the representations for discrete structures with formal grammars and semantics. How to generate both syntactically and semantically correct data still remains largely an open problem. Inspired by the theory of compiler where syntax and semantics check is done via syntax-directed translation (SDT), we propose a novel syntax-directed variational autoencoder (SD-VAE) by introducing stochastic lazy attributes. This approach converts the offline SDT check into on-the-fly generated guidance for constraining the decoder. Comparing to the state-of-the-art methods, our approach enforces constraints on the output space so that the output will be not only syntactically valid, but also semantically reasonable. We evaluate the proposed model with applications including reconstruction and molecule optimization. The results demonstrate the effectiveness in incorporating syntactic and semantic constraints in discrete generative models, which is significantly better than current state-of-the-art approaches. 

## Learning Deep Generative Models of Graphs 
- **year:** 2018 
- **url:** https://www.semanticscholar.org/paper/f32f16ca3c27ff945198c6551a5d35fae3b1a660 
- **abstract:** Graphs are fundamental data structures which concisely capture the relational structure in many important real-world domains, such as knowledge graphs, physical and social interactions, language, and chemistry. Here we introduce a powerful new approach for learning generative models over graphs, which can capture both their structure and attributes. Our approach uses graph neural networks to express probabilistic dependencies among a graph's nodes and edges, and can, in principle, learn distributions over any arbitrary graph. In a series of experiments our results show that once trained, our models can generate good quality samples of both synthetic graphs as well as real molecular graphs, both unconditionally and conditioned on data. Compared to baselines that do not use graph-structured representations, our models often perform far better. We also explore key challenges of learning generative models of graphs, such as how to handle symmetries and ordering of elements during the graph generation process, and offer possible solutions. Our work is the first and most general approach for learning generative models over arbitrary graphs, and opens new directions for moving away from restrictions of vector- and sequence-like knowledge representations, toward more expressive and flexible relational data structures. 
- **journal:** ArXiv 
- **volume:** abs/1803.03324 
- **pages:** null 
- **arxivid:** 1803.03324 

## Deep reinforcement learning for de novo drug design 
- **year:** 2017 
- **url:** https://www.semanticscholar.org/paper/4edd98e3947d8406ec95518c294721757afffb5d 
- **abstract:** We introduce an artificial intelligence approach to de novo design of molecules with desired physical or biological properties. We have devised and implemented a novel computational strategy for de novo design of molecules with desired properties termed ReLeaSE (Reinforcement Learning for Structural Evolution). On the basis of deep and reinforcement learning (RL) approaches, ReLeaSE integrates two deep neural networks—generative and predictive—that are trained separately but are used jointly to generate novel targeted chemical libraries. ReLeaSE uses simple representation of molecules by their simplified molecular-input line-entry system (SMILES) strings only. Generative models are trained with a stack-augmented memory network to produce chemically feasible SMILES strings, and predictive models are derived to forecast the desired properties of the de novo–generated compounds. In the first phase of the method, generative and predictive models are trained separately with a supervised learning algorithm. In the second phase, both models are trained jointly with the RL approach to bias the generation of new chemical structures toward those with the desired physical and/or biological properties. In the proof-of-concept study, we have used the ReLeaSE method to design chemical libraries with a bias toward structural complexity or toward compounds with maximal, minimal, or specific range of physical properties, such as melting point or hydrophobicity, or toward compounds with inhibitory activity against Janus protein kinase 2. The approach proposed herein can find a general use for generating targeted chemical libraries of novel compounds optimized for either a single desired property or multiple properties. 
- **journal:** Science Advances 
- **volume:** 4 
- **pages:** null 
- **doi:** 10.1126/sciadv.aap7885 
- **pmid:** 30050984 
- **arxivid:** 1711.10907 

## Fréchet ChemNet Distance: A Metric for Generative Models for Molecules in Drug Discovery 
- **year:** 2018 
- **url:** https://www.semanticscholar.org/paper/7d878fe31b9b57f75071586d83cdec2e8b81e039 
- **abstract:** The new wave of successful generative models in machine learning has increased the interest in deep learning driven de novo drug design. However, method comparison is difficult because of various flaws of the currently employed evaluation metrics. We propose an evaluation metric for generative models called Fréchet ChemNet distance (FCD). The advantage of the FCD over previous metrics is that it can detect whether generated molecules are diverse and have similar chemical and biological properties as real molecules. 
- **journal:** Journal of chemical information and modeling 
- **volume:** 58 9 
- **pages:** 1736-1741 
- **doi:** 10.1021/acs.jcim.8b00234 
- **pmid:** 30118593 
- **arxivid:** 1803.09518 

## Molecular generative model based on conditional variational autoencoder for de novo molecular design 
- **year:** 2018 
- **url:** https://www.semanticscholar.org/paper/e4f0bf3074d5ae6d55d22068dd50158dc81b2a0a 
- **abstract:** S2 TL;DR: A molecular generative model based on the conditional variational autoencoder that can be used to generate drug-like molecules with five target properties and to adjust a single property without changing the others and to manipulate it beyond the range of the dataset is proposed. 
- **journal:** Journal of Cheminformatics 
- **volume:** 10 
- **pages:** null 
- **doi:** 10.1186/s13321-018-0286-7 
- **pmid:** 29995272 
- **arxivid:** 1806.05805 

## Objective-Reinforced Generative Adversarial Networks (ORGAN) for Sequence Generation Models 
- **year:** 2017 
- **url:** https://www.semanticscholar.org/paper/15d739e2c184a6844bdbd9a2550d007de6ddb085 
- **abstract:** In unsupervised data generation tasks, besides the generation of a sample based on previous observations, one would often like to give hints to the model in order to bias the generation towards desirable metrics. We propose a method that combines Generative Adversarial Networks (GANs) and reinforcement learning (RL) in order to accomplish exactly that. While RL biases the data generation process towards arbitrary metrics, the GAN component of the reward function ensures that the model still remembers information learned from data. We build upon previous results that incorporated GANs and RL in order to generate sequence data and test this model in several settings for the generation of molecules encoded as text sequences (SMILES) and in the context of music generation, showing for each case that we can effectively bias the generation process towards desired metrics. 
- **journal:** ArXiv 
- **volume:** abs/1705.10843 
- **pages:** null 
- **arxivid:** 1705.10843 
