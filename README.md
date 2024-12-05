# Comparative Analysis of Prompting Techniques for Text Classification Across Multiple LLMs

<br/>

<details>
  <summary>Table of Contents</summary>
  <ul>
    <li>
      <a href="#goal">Goal</a>
    </li>
    <li>
      <a href="#methodology">Methodology</a>
      <ul>
        <li><a href="#datasets">Datasets</a></li>
        <li><a href="#models">Models</a></li>
        <li><a href="#metrics">Metrics</a></li>
      </ul>
    </li>
    <li>
      <a href="#team-members">Team Members</a>
    </li>
  </ul>
</details>

<!--
## Table of Contents
- [Goal](#goal)
- [Methodology](#methodology)
- [Team Members](#team-members)
-->

## Goal
We aim to compare prompting techniques on various datasets with different models, and to gain insight into the difference in performance between different prompting techniques on different models and datasets.

Due to the complexity of natural language, with correct categorization relying on understanding the nuanced context of a word or sentence, text classification is a challenging task for language models with no inherent understanding of language. This challenge is apparent, and even amplified, when attempting to effectively prompt these models for some specific task.

Especially with techniques like zero-shot, few-shot, and chain-of-thought, it becomes imperative to both choose an appropriate technique for the task and design an effective prompt for the model for optimal performance; yet, how can we determine which technique is "appropriate" for our task, and how do we design an "effective" prompt? What determines an "effective" prompt?

## Methodology

Contained in this repository are the notebooks used to run each experiment.

### Datasets

We use the following datasets to test our models:

- [SST-2: Stanford Sentiment Treebank v2](https://aclanthology.org/D13-1170/)
  - [Huggingface](https://huggingface.co/datasets/stanfordnlp/sst2)
- [CARER: Contextualized Affect Representations for Emotion Recognition](https://aclanthology.org/D18-1404/)
  - [Huggingface](https://huggingface.co/datasets/dair-ai/emotion)
- [Hate Speech Dataset](https://aclanthology.org/W18-5102/)
  - [GitHub](https://github.com/Vicomtech/hate-speech-dataset)

### Models

We compare the performance on the above datasets of three models: Llama 3.2, GPT-Neo, and Yi (01-ai). The models are each prompted using zero-shot, few-shot, and chain-of-thought prompting.

We obtain a baseline performance on each dataset using fine-tuned Bart and T5 models. To ensure uniformity across each experiment, and to take advantage of their training tasks, the BART and T5 models employ a text generation head. 

> **Note**: The T5 notebooks also include models with a classification head to compare against the models with the text generation head to illustrate this point; only the generative T5 models are used for baseline performances.

### Metrics

For quantitative analysis, we use the accuracy, precision, recall, and f1 score metrics. Each notebook contains performance metrics at the end of their respective tasks.

## Team Members

- Ethan Chung
- Anika Rahman Joyita
- Jayden Carl Tactay
- Samuel Yang
