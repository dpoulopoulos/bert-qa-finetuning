.. BERT on SQuAD documentation master file, created by
   sphinx-quickstart on Tue Sep 10 08:05:58 2024.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

BERT on SQuAD's
===============

.. image:: https://img.shields.io/badge/license-CC_BY--NC_4.0-green
   :target: https://creativecommons.org/licenses/by-nc/4.0/
   :alt: CC-BY-NC-4.0

.. image:: https://img.shields.io/badge/pytorch-v2.4.1-blue
   :target: https://pytorch.org/
   :alt: PyTorch

.. image:: https://img.shields.io/badge/kubeflow-v1.8-orange
   :target: https://www.kubeflow.org/
   :alt: Kubeflow: v1.8

.. image:: https://img.shields.io/badge/kubernetes-v1.29.3-orange
   :target: https://kubernetes.io/
   :alt: Kubernetes: v1.29.3

The guides in this page demonstrate how to fine-tune BERT on the SQuAD dataset to solve
Question-Answering tasks. The can run locally, on a GPU Notebook server, or leverage
`Kubeflow Pipelines (KFP) <https://www.kubeflow.org/docs/components/pipelines/>`_ to scale and
automate the experiment in a Kubeflow cluster.

About BERT
----------

`BERT (Bidirectional Encoder Representations from Transformers) <https://arxiv.org/abs/1810.04805>`_
is a revolutionary model developed by Google in 2018. Its introduction marked a significant
advancement in the field, setting new state-of-the-art benchmarks across various NLP tasks.

BERT is pre-trained on a massive amount of data, acquiring a sense of what language is and what's
the meaning of context in a document. Then, this pre-trained model can then be fine-tuned for
specific tasks such as sentiment analysis or question answering.

About SQuAD
-----------

`Stanford Question Answering Dataset (SQuAD) <https://rajpurkar.github.io/SQuAD-explorer/>`_
is a reading comprehension dataset, consisting of questions posed by crowdworkers on a set of
Wikipedia articles, where the answer to every question is a segment of text, or span, from the
corresponding reading passage, or the question might be unanswerable.

This is an example row from the SQuAD dataset:

.. code-block:: console

   Context:
   Architecturally, the school has a Catholic character. Atop the Main Building's gold dome is a
   golden statue of the Virgin Mary. Immediately in front of the Main Building and facing it, is a
   copper statue of Christ with arms upraised with the legend "Venite Ad Me Omnes". Next to the
   Main Building is the Basilica of the Sacred Heart. Immediately behind the basilica is the Grotto,
   a Marian place of prayer and reflection. It is a replica of the grotto at Lourdes, France where
   the Virgin Mary reputedly appeared to Saint Bernadette Soubirous in 1858. At the end of the main
   drive (and in a direct line that connects through 3 statues and the Gold Dome), is a simple,
   modern stone statue of Mary.
   
   Question:
   The Basilica of the Sacred heart at Notre Dame is beside to which structure?

   Answer:
   {"text": ["the Main Building"], "answer_start": [279]}


In this experiment, we use SQuAD 1.1. This version of the SQuAD dataset, contains 100,000+
question-answer pairs on 500+ articles.


.. toctree::
   :maxdepth: 1
   :caption: User Guides:

   local-setup
   kubeflow-pipelines


.. toctree::
   :maxdepth: 1
   :caption: Conceptual Guides:

   bert
   bert-qa


.. Indices and tables
.. ==================

.. * :ref:`genindex`
.. * :ref:`modindex`
.. * :ref:`search`
