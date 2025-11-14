---
permalink: /projects/query-performance-prediction-via-llm-generated-query-variations
title: "Query Performance Prediction via LLM-Generated Query Variations"
author_profile: true
---

**Supervisor:** Prof. Ensan
**Type:** Academic Project (Neural Networks, Information Retrieval)

## Overview
This project focuses on predicting query performance in information retrieval systems by leveraging large language models (LLMs) to generate semantically similar query variations. The system combines modern LLM capabilities with traditional BM25 ranking algorithms to analyze how different query formulations affect retrieval effectiveness across document collections, with a particular focus on the MS MARCO dataset.

## Methodology
The project implements a comprehensive evaluation framework consisting of four interconnected modules:

1. **LLM Query Generator:** Utilizes Ollama framework to create semantically equivalent query reformulations, exploring how different phrasings of the same information need impact retrieval performance.
2. **BM25 Index Builder:** Constructs and maintains BM25 search indices for efficient document retrieval from the MS MARCO collection.
3. **Results Processing:** Manages the execution of original and generated query variations, collecting retrieval results for comparative analysis.
4. **Evaluation Framework:** Computes correlation metrics between query variations and their performance, assessing the predictive power of LLM-generated variations.

## Key Technologies
- **Programming Language:** Python (96.2%)
- **LLM Framework:** Ollama for query generation
- **Retrieval Algorithm:** BM25 ranking
- **Dataset:** MS MARCO (Microsoft Machine Reading Comprehension)
- **Infrastructure:** GPU-accelerated processing (8GB+ VRAM)

## Evaluation
The evaluation methodology encompasses:
- **Correlation Analysis:** Measuring performance consistency across query variations
- **Retrieval Effectiveness:** Comparing document ranking quality between original and generated queries
- **Semantic Similarity:** Assessing how semantic equivalence relates to retrieval performance
- **Statistical Validation:** Analyzing correlation metrics to validate QPP predictions

## Key Findings
- Developed an automated pipeline for generating and evaluating query variations using LLMs
- Demonstrated the relationship between semantically similar queries and their retrieval performance patterns
- Provided insights into how query reformulation affects information retrieval effectiveness
- Created a reproducible framework for query performance prediction research

## Personal Contributions
- Designed and implemented the four-module evaluation framework
- Integrated LLM-based query generation with traditional IR metrics
- Developed automated pipeline for processing MS MARCO dataset
- Conducted comprehensive performance analysis and correlation studies
- Created visualization tools for results interpretation

## Technical Implementation
The system is designed for efficiency and reproducibility:
- **Processing Time:** Approximately 4 hours for full pipeline execution
- **Resource Requirements:** 8GB+ GPU VRAM, ~12GB disk space
- **Automation:** Single-script execution via `bash ./run.sh`
- **Pre-computed Results:** Available in the `./results/` directory for accessibility

## Conclusion
This project bridges modern LLM capabilities with traditional information retrieval evaluation, offering a novel approach to query performance prediction. By systematically analyzing how semantically similar query variations perform across a large-scale dataset, the work contributes to understanding the relationship between query formulation and retrieval effectiveness, with potential applications in query optimization and search system design.

## Source Code
The complete implementation is available on GitHub: [qpp-with-llm](https://github.com/razaviah/qpp-with-llm)

## Project Report

View the detailed project report below (if the file is not showing up, please refresh the page or <a href="https://raw.githubusercontent.com/razaviah/razaviah.github.io/master/files/Query_Performance_Prediction_via_LLM-Generated_Query_Variations.pdf" target="_blank">download the report here</a>):

<iframe src="https://docs.google.com/viewer?embedded=true&url=https://raw.githubusercontent.com/razaviah/razaviah.github.io/master/files/Query_Performance_Prediction_via_LLM-Generated_Query_Variations.pdf" width="100%" height="700px" style="border:3px solid black;"></iframe>
