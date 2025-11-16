---
permalink: /projects/benchmarking-prompt-sensitivity-in-large-language-models
title: "Benchmarking Prompt Sensitivity in Large Language Models"
author_profile: true
---

**Supervisor:** Prof. Bagheri   
**Type:** Research Publication, Natural Language Processing (NLP), Information Retrieval (IR)

## Overview
This research introduces a novel task, Prompt Sensitivity Prediction, and presents PromptSET, a comprehensive dataset designed to investigate how slight variations in prompt formulation impact Large Language Model (LLM) performance. The work addresses a critical challenge in LLM deployment: their high sensitivity to minor changes in wording, structure, or punctuation of prompts, which can lead to substantially different outputs even when the underlying information need remains unchanged.

## Research Motivation
Large language models demonstrate remarkable capabilities in generating human-like responses, yet they exhibit notable fragility when faced with prompt variations. Small modifications in phrasing can cause LLMs to fail at tasks they previously succeeded in, highlighting challenges users face when crafting effective prompts. This research systematically investigates this phenomenon, providing both a benchmark dataset and analysis of why and when LLMs struggle with prompt variations.

## Methodology
The research implements a comprehensive four-step pipeline for dataset creation and evaluation:

1. **Prompt Selection:** Starting with TriviaQA and HotpotQA question-answering datasets, the team selected 11,469 unique prompts with deterministic, concise answers suitable for objective evaluation.

2. **Variation Generation:** Using LLaMA 3.1 (8B) and Mistral-nemo models, the system generated 9 semantically similar variations for each original prompt, instructing the LLMs to rephrase while maintaining the same information need and semantic content.

3. **Quality Filtering:** Rigorous filtering removed prompts with insufficient valid variations or LLM hallucinations, ensuring high-quality, semantically equivalent variations.

4. **Response Collection and Labeling:** Both original prompts and their variations were evaluated against the LLMs, with responses compared to expected answers to label each prompt as answerable or not.

## PromptSET Dataset
The resulting dataset comprises:
- **11,469 original prompts** from TriviaQA and HotpotQA
- **9 variations per prompt** (114,690 total variations)
- **Responses from multiple LLMs** (LLaMA 3.1 8B and Mistral-nemo)
- **Ground truth labels** indicating answerability
- **70-30 train-test split** (8,028 training, 3,441 test questions)

## Benchmark Evaluation
To establish baselines for prompt sensitivity prediction, the research evaluated three categories of methods:

1. **LLM Self-Evaluation:** Direct assessment of LLMs' ability to predict whether they can accurately answer a given prompt, testing their meta-cognitive capabilities.

2. **Text Classification:** BERT-based classifiers trained to predict whether an LLM's response will satisfy the user's information need based on the prompt text.

3. **Query Performance Prediction (QPP):** Adapted pre-retrieval QPP methods including:
   - BERT-PE: Supervised QPP using contextualized embeddings
   - Specificity-based metrics: Closeness Centrality (CC), Degree Centrality (DC), PageRank, and Inverse Edge Frequency (IEF)

## Key Findings

### Baseline Performance
- **BERT-PE** demonstrated the strongest performance, particularly on HotpotQA (71.0% accuracy), suggesting supervised QPP methods are well-suited for prompt sensitivity prediction
- **Text classification** methods showed competitive results on TriviaQA (66.4% accuracy) but struggled with consistency across datasets
- **LLM self-evaluation** showed reasonable performance on TriviaQA but lacked consistency on HotpotQA
- **Specificity-based QPP methods** performed poorly, as variations were too semantically similar for specificity metrics to distinguish effectively

### Impact of Original Prompt Correctness
When the LLM correctly answers the original prompt, there is significantly higher likelihood of variations also yielding correct answers. Conversely, when the original fails, most variations (typically only 1 out of 10) succeed, displaying a descending pattern in answerability.

### Similarity and Predictability
Variations more similar to the original prompt (measured via cosine similarity of MiniLM embeddings) are more likely to generate both correct responses and accurate predictions of answerability. This suggests strong bias toward training data and reduced generalizability to novel formulations.

### Prompt Reformulation Potential
Even when both LLMs failed on the original prompt, alternative variations enabled correct responses in many cases, demonstrating that prompt reformulation can transform unanswerable prompts into answerable ones.

## Research Contributions
1. **Novel Task Definition:** Formalized the Prompt Sensitivity Prediction task with clear requirements and evaluation criteria
2. **PromptSET Dataset:** Publicly released comprehensive dataset for studying LLM sensitivity to prompt variations
3. **Benchmark Analysis:** Demonstrated that existing methods from related tasks struggle with prompt sensitivity prediction, underscoring the need for specialized approaches

## Technical Implementation
- **Models:** LLaMA 3.1 (8B parameters), Mistral-nemo
- **Frameworks:** PyTorch/Transformers for model implementations
- **Evaluation:** BERT-based classification, similarity metrics using MiniLM
- **Data Format:** JSONL with unique identifiers, prompt text, expected answers, and model responses

## Implications and Future Directions
This research reveals fundamental limitations in current LLMs' ability to consistently interpret semantically similar prompts, highlighting:
- The need for improved prompt engineering strategies
- Opportunities for developing prompt reformulation systems
- The importance of understanding how information needs should be phrased for reliable LLM responses
- Potential for training more robust models less sensitive to superficial prompt variations

## Publication Details
**Paper:** Benchmarking prompt sensitivity in large language models   
**Conference:**  European Conference on Information Retrieval, 2025 (ECIR 2025)   
**Authors:** Amirhossein Razavi, Mina Soltangheis, Negar Arabzadeh, Sara Salamat, Morteza Zihayat, Ebrahim Bagheri   
**Publisher:** [Springer, Advances in Information Retrieval 2025](https://link.springer.com/chapter/10.1007/978-3-031-88714-7_29)   
**Google Scholar:** [Google Scholar link](https://scholar.google.com/citations?view_op=view_citation&hl=en&user=AaaHZjkAAAAJ&citation_for_view=AaaHZjkAAAAJ:u5HHmVD_uO8C)   
**arXiv:** [arXiv-2502.06065](https://arxiv.org/abs/2502.06065)   

## Resources

### Source Code
The complete implementation and dataset are available on GitHub: [prompt-sensitivity](https://github.com/Narabzad/prompt-sensitivity)

### Research Paper

View the full research paper below (if the file is not showing up, please refresh the page or <a href="https://raw.githubusercontent.com/razaviah/razaviah.github.io/master/files/paper_Benchmarking_Prompt_Sensitivity_in_Large_Language_Models.pdf" target="_blank">download the paper here</a>):

<iframe src="https://docs.google.com/viewer?embedded=true&url=https://raw.githubusercontent.com/razaviah/razaviah.github.io/master/files/paper_Benchmarking_Prompt_Sensitivity_in_Large_Language_Models.pdf" width="100%" height="700px" style="border:3px solid black;"></iframe>

### Research Poster

View the research poster below (if the file is not showing up, please refresh the page or <a href="https://raw.githubusercontent.com/razaviah/razaviah.github.io/master/files/poster_Benchmarking_Prompt_Sensitivity_in_Large_Language_Models.pdf" target="_blank">download the poster here</a>):

<iframe src="https://docs.google.com/viewer?embedded=true&url=https://raw.githubusercontent.com/razaviah/razaviah.github.io/master/files/poster_Benchmarking_Prompt_Sensitivity_in_Large_Language_Models.pdf" width="100%" height="700px" style="border:3px solid black;"></iframe>
