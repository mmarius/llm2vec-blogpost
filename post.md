# LLM2Vec: Large Language Models Are Secretly Powerful Text Encoders

*Authors: Parishad BehnamGhader\*, Vaibhav Adlakha\*, Marius Mosbach, Dzmitry Bahdanau, Nicolas Chapados, Siva Reddy*


Text embedding models convert a piece of text such as a search query, a document, or pieces of code into a sequence of real-valued numbers. Given such embeddings, we can measure the similarity or relatedness of pieces of text which facilitates various important applications such as search, clustering, retrieval, and classification.

With the widespread availability of large decoder-only language models (LLMs) such as GPT-4, LLaMA2, Mistral-7B, or StarCoder2, a pressing question in the NLP research community is how to best use these models to construct powerful text embeddings. 

We are excited to present [LLM2Vec: Large Language Models Are Secretly Powerful Text Encoders](link), a simple and efficient solution to transform *any* decoder-only LLM into a powerful text encoder.

Below we give an overview of LLM2Vec and provide a hands-on tutorial that walks you through the steps of transforming a decoder-only LLM into a powerful text encoder.

## A simple and efficient recipe

At its core, LLM2Vec consists of three simple steps: 1) enabling bidirectional attention, 2) adaptation via masked next token prediction (MNTP), and 3) adaptation via unsupervised contrastive learning.

Adapting a model with the LLM2Vec approach is highly efficient and works with parameter-efficient fine-tuning methods such as LoRA. Additionally, the adaptation can be performed using a general domain corpus such as Wikipedia, requires only a few hundred training steps, and can be run on a single GPU.

![The three steps of the LLM2Vec approach.](./images/overview.png "LLM2Vec overview")

## State-of-the-art performance

LLM2Vec is not only simple and efficient, it also leads to state-of-the-art performance on the challenging Massive Text Embeddings benchmark (MTEB), both in the unsupervised and supervised setting (among models trained only on publicly available data).  

### Unsupervised results

We apply LLM2Vec to some of the best-performing LLMs available and evaluate the resulting text embedding models on MTEB. In the unsupervised setting, i.e., without using any labeled training data for contrastive learning, our LLM2Vec transformed models achieve a new state-of-the-art performance of $56.80$, outperforming previous unsupervised approach by a large margin.

![Unsupervised MTEB results.](./images/unsupervised.png "Unsupervised MTEB results")

### Supervised results

LLM2Vec does not only provide state-of-the-art performance in the unsupervised setting, it can also be easily combined with supervised contrastive learning. As our results show, applying LLM2Vec before supervised contrastive learning leads to a substantial improvement. Moroever, LLM2Vec in combination with Mistral-7B, the currently best-performing 7B parameter language model, leads to a new state-of-the-art performance of $64.80$ on MTEB among models trained only with publicly available data. 

![Supervised MTEB results.](./images/supervised.png "Supervised MTEB results")

## Highly sample-efficient

LLM2Vec transformed models are not only capable of achieving state-of-the-art performance, they also require less training data to perform well, compared to training models without the LLM2vec transformation.

![LLM2Vec is highly sample-efficient.](./images/sample_efficient.png "LLM2Vec is sample-efficient")

These results make us particularly excited about challenging real-world scenarios where large amounts of labeled data might be costly to aquire.

## Use it on your own data

We have made it very easy for you to use our LLM2Vec transformed models. The example code snipped below shows how to ...

```
1. code goes here # comment
2. code goes here # comment
```

To learn how to apply LLM2Vec to your own models, take a look at our tutorial which walks you through an example.

----

Research: [text](link)

Code: [text](link)

Tutorial: [text](link)
