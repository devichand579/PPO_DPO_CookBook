# Alignment through Model Merging

This project implements an approach to AI alignment through model merging, focusing on safety-enhanced language models using RESTA (REpresentation-level Safety Through Addition) methodology.

## Project Overview

The project is structured in four main stages, each implemented in a separate notebook:

### Stage 1: SFT Model Training
- Dataset: CodeAlpaca-20k (sahil2801/CodeAlpaca-20k)
- Training split: First 40% of dataset
- Testing split: Last 10% of dataset
- Implementation of two fine-tuning strategies:
  - Parameter Efficient Fine-tuning (PEFT)
  - Full Fine-tuning (Full-FT)
- Application of DARE (Drop and RE-scale) on SFT and PEFT models
- Output: SFT, SFT + DARE, PEFT, PEFT + DARE models

### Stage 2: Safety Vector Generation
- Dataset: unalignment/toxic-dpo-v0.2
- Implementation of safety vector extraction (𝝳safe = 𝝷base(+) - 𝝷base(~))
- Zero-shot prompting with SFT and PEFT models
- LLM Judge Implementation using meta-llama/Llama-2-7b-chat-hf
- Selection of 100 harmful samples
- Fine-tuning for safety vector generation

### Stage 3: Model Merging with Safety Vector
- Implementation of vector addition using mergekit
- Generation of safety-enhanced models:
  - SFT + RESTA
  - SFT + DARE + RESTA
  - PEFT + RESTA
  - PEFT + DARE + RESTA

### Stage 4: Evaluation and Analysis
- Safety Evaluation using SoJMINER-Group/HarmEval dataset
- Performance metrics:
  - ROUGE-L
  - METEOR
  - BLEU
- Unsafety evaluation using Llama-2-7b-chat-hf as judge
- Comparative analysis of all model variants


## Model Variants
The project produces and evaluates eight different model setups:
1. SFT
2. PEFT
3. SFT + DARE
4. PEFT + DARE
5. SFT + RESTA
6. PEFT + RESTA
7. SFT + RESTA + DARE
8. PEFT + RESTA + DARE

## Usage
1. Follow the notebooks in sequential order
2. Each notebook contains detailed instructions and implementation
3. Ensure proper setup of the Llama-2-7b-chat-hf model in bf16 precision
4. Follow the specified data splits and sampling procedures
