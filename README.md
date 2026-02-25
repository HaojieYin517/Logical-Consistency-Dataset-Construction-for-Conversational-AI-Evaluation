# Logical-Consistency-Dataset-Construction-for-Conversational-AI-Evaluation

## Overview
This repository contains my contribution to a course project on **logical consistency tracking in conversational AI**.  
The project investigates whether language models can correctly update their reasoning when users revise previously stated information during multi-turn dialogue.

The full project dataset was constructed from multiple sources and generation strategies. This repository focuses on my implemented components within that pipeline.

## My Contribution

### SNLI-based Dialogue Generation
Natural Language Inference (SNLI) sentences are used as scenario seeds to construct multi-turn AI–user dialogues.  
Prompt constraints enforce sequential reasoning, ensuring each user query depends on prior model responses and forms a coherent logical chain.

### Logic Modification Dataset Pipeline
A semi-automated workflow is implemented to generate structured datapoints consisting of:

- Original multi-turn dialogue  
- User revision introducing a logical shift  
- Sample correct revised response  
- Sample incorrect revised response  
- Extracted logic chains for comparison  

All datapoints are stored in **JSONL format** to support scalable processing and experimentation.

### T5 Fine-tuning Experiments
The constructed dataset is further used to explore fine-tuning **FLAN-T5** for improved logical adaptation under user revisions, studying whether supervised exposure to logical shifts can enhance reasoning consistency.

## Dataset Objective
The dataset is designed to benchmark model ability to:

- Detect logical changes introduced by users  
- Update reasoning chains consistently  
- Avoid contradictions with prior dialogue context  

This work contributes a structured resource for evaluating dynamic reasoning in conversational AI.
