## 智慧旅游项目每周汇报（四）

<h3 id='1.'>一、前言</h3>


<h3 id='2.'>二、Bridging Text and Knowledge by learning Multi-Prototype Entity Mention Embedding论文学习</h3>

<h4 id='2.1.'>1. 摘要相关概念</h4>

+ [语义空间semantic space][1]:
    1. 概念：自然语言领域中的语义空间旨在创建能够正确捕获含义的自然语言的表达方式；Semantic spaces[note 1][1] in the natural language domain aim to create representations of natural language that are capable of capturing meaning.
    2. 动机：语义空间的最初动机源于自然语言的两大挑战：**Vocabulary mismatch**(一义多词)以及自然语言的**歧义**（一词多义）；
    3. 与基于规则或基于模型的、在关键字层面进行操作的方法的对比：
        + 自然语言领域中语义空间的应用旨在克服基于规则或基于模型的、在关键字层面进行操作的方法的局限性。
        + 基于规则或基于模型方法的缺点在于其脆弱性，以及创建基于规则NLP系统和创建模型学习的训练全集需要大量的人力；
        + 基于规则或基于模型的方法在关键字层面上是稳定的，但如果词汇与规则中定义的词汇存在偏差或词汇与统计模型使用的训练数据存在偏差，则这些方法就会崩溃；
    4. 研究历史：
        + In 1996, two papers were published that raised a lot of attention around the general idea of creating semantic spaces: [latent semantic analysis][2] and [Hyperspace Analogue to Language][3]
        + A breakthrough with regard to the accuracy of modelling associative relations between words (e.g. "spider-web", "lighter-cigarette", as opposed to synonymous relations such as "whale-dolphin", "astronaut-driver") was achieved by [explicit semantic analysis][4] (ESA) in 2007.
        + ESA: ESA was a novel (non-machine learning) based approach that represented words in the form of vectors with 100,000 dimensions (where each dimension represents an Article in Wikipedia). However practical applications of the approach are limited due to the large number of required dimensions in the vectors.
        + More recently, advances in neural networking techniques in combination with other new approaches (tensors) led to a host of new recent developments: [Word2vec][5] from Google, [GloVe][6] from Stanford University, and [fastText][7]from Facebook AI Research (FAIR) labs.
+ 文本text：文本是一种非结构化数据，与word对应；
+ 知识库knowledge：知识库是一种结构化数据，与entity对应；
+ 实体指称entity mention：a bunch of words that means one or more concept；
+ word embedding, entity embedding, sense embedding?

[1]: https://en.wikipedia.org/wiki/Semantic_space
[2]: https://en.wikipedia.org/wiki/Latent_semantic_analysis
[3]: https://en.wikipedia.org/wiki/Hyperspace_Analogue_to_Language
[4]: https://en.wikipedia.org/wiki/Explicit_semantic_analysis
[5]: https://en.wikipedia.org/wiki/Word2vec
[6]: https://en.wikipedia.org/wiki/GloVe_(machine_learning)
[7]: https://en.wikipedia.org/wiki/FastText

<h4 id='2.2'>2. Introduction相关概念</h4>

1. 知识图谱补充knowledge graph completion：
2. 关系抽取relation extraction:
3. 实体分类entity classification:
4. 实体链接entity linking:
5. 词义消歧word sense disambiguation：
6. 指称含义mention sense：一个指称项所指代的一个或多个意义；
7. skip-gram model and CBOW model


<h4 id='2.3'>3. Preliminaries相关概念</h4>

1. 文本语料库text corpus：
2. annotated文本语料库annotated text corpus：
3. mention boundary：


<h4 id='2.4'>4. An overview of Our Method的相关概念</h4>

1. unified optimization objective:
2. 实体链接entity linking:


<h4 id='2.5'>5. Representation Learning的相关概念</h4>

1. 分布表示Distributional representation:
2. semantic compositionality
3. Skip-Gram and CBOW model
4. softmax function
5. hierarchical softmax
6. negative sampling
7. 