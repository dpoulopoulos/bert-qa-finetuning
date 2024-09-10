# Fine-tune BERT on SQuAD

> Fine-Tuning BERT for Question-Answering on Kubeflow.

[![License](https://img.shields.io/badge/docs-passing-green)](https://dpoulopoulos.github.io/bert-qa-finetuning/)
[![License](https://img.shields.io/badge/license-CC_BY--NC_4.0-green)](https://creativecommons.org/licenses/by-nc/4.0/)
[![Pytorch](https://img.shields.io/badge/pytorch-v2.4.1-blue)](#pytorch)
[![Kubeflow](https://img.shields.io/badge/kubeflow-v1.8-orange)](#kubeflow)
[![Kubernetes](https://img.shields.io/badge/kubernetes-v1.29.3-orange)](#kubernetes)

This repository contains the code for fine-tuning BERT on the SQuAD dataset to
solve Question-Answering tasks. The can run locally, on a GPU Notebook server,
or leverage [Kubeflow Pipelines (KFP)](https://www.kubeflow.org/docs/components/pipelines/)
to scale and automate the experiment in a Kubeflow cluster.

# About BERT

[BERT (Bidirectional Encoder Representations from Transformers)](https://arxiv.org/abs/1810.04805)
is a revolutionary model developed by Google in 2018. Its introduction marked a
significant advancement in the field, setting new state-of-the-art benchmarks
across various NLP tasks.

BERT is pre-trained on a massive amount of data, acquiring a sense of what
language is and what's the meaning of context in a document. Then, this
pre-trained model can then be fine-tuned for specific tasks such as sentiment
analysis or question answering.

# About SQuAD

[Stanford Question Answering Dataset (SQuAD)](https://rajpurkar.github.io/SQuAD-explorer/)
is a reading comprehension dataset, consisting of questions posed by
crowdworkers on a set of Wikipedia articles, where the answer to every question
is a segment of text, or span, from the corresponding reading passage, or the
question might be unanswerable.

SQuAD `1.1`, the previous version of the SQuAD dataset, contains 100,000+
question-answer pairs on 500+ articles.

# How to use this repository

This repository contains the following files:

- `bert-squad.ipynb`: Jupyter Notebook to fine-tune BERT on SQuAD.
- `pipeline.ipynb`: Jupyter Notebook to create, compile, and submit a Kubeflow
   Pipeline for the experiment.

To run the code locally, you can use the Jupyter Notebook `bert-squad.ipynb`.
You will need a GPU to run the notebook, as BERT is computationally expensive.

If you have access to a Kubeflow cluster, you can use the `pipeline.ipynb` to
create, compile, and submit a Kubeflow Pipeline to fine-tune BERT. The pipeline
will scale the experiment across multiple nodes in the cluster, running steps in
parallel, and caching repeated ones to save time and resources.

For more information on how to use the notebooks, please refer to the
[documentation](https://dpoulopoulos.github.io/bert-qa-finetuning/).
