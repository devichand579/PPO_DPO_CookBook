# RLHF and DPO Implementation for Language Models

This repository contains the implementation of Reinforcement Learning from Human Feedback (RLHF) and Direct Preference Optimization (DPO) for fine-tuning language models.

## Overview
1. **Reinforcement Learning from Human Feedback (RLHF)** using Proximal Policy Optimization (PPO)
2. **Direct Preference Optimization (DPO)**

Both methods aim to improve language model outputs by incorporating human feedback, but they use different approaches:
- RLHF uses a reward model and reinforcement learning to optimize policy
- DPO directly optimizes the policy without requiring a separate reward model

## Requirements

- torch
- pandas
- transformers
- trl
- tensorboard
- datasets
- evaluate
- accelerate
- nltk
- rouge_score


## Project Structure

The notebook is organized into several sections:

1. **Setup and Installation**: Installing required libraries
2. **Data Preparation**: Loading and preprocessing datasets
3. **Reward Model Training**: Training a reward model
4. **PPO Implementation**: 
   - Setting up the model and tokenizer
   - Defining reward functions
   - Configuring the PPO trainer
   - Training loop with memory-efficient implementation
5. **DPO Implementation**:
   - Setting up preference pairs
   - Training with DPO

## PPO Training

The PPO implementation includes memory-efficient techniques to avoid Out-of-Memory (OOM) errors:

- Processing examples one at a time
- Moving tensors between CPU and GPU as needed
- Using gradient accumulation with small mini-batches
- Clearing CUDA cache frequently
- Saving checkpoints to CPU before writing to disk


## Checkpoints

Model checkpoints are saved at the end and contain:
- Model state dict
- Model name

As checkpoints are stored using pytorch , they are handled accordining to the pre-trained model while loading in compatibility with transformers library.
