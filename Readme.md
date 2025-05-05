# Safety Alignment Resources

This repository contains implementations and resources for various AI safety alignment techniques. The repository provide collection of different techniques as well as cookbooks for some recent safety alignment methods.

## 📚 Cookbooks

Detailed implementation guides are available in the `cookbooks` directory:

- [Alignment through Model Merging](cookbooks/Alignment_through_Model_Merging/README.md) - Implementation of RESTA (REpresentation-level Safety Through Addition) methodology
- [RLHF and DPO](cookbooks/RLHF_DPO/README.md) - Direct Preference Optimization and PPO implementation for RLHF

## 📖 Research Papers

### 🔒 Model Hijacking
| Paper | Summary |
|-------|---------|
| [Two-in-one: Model Hijacking Attack](https://dl.acm.org/doi/10.5555/3620237.3620362) | Demonstrates how shared text generation models can be hijacked to produce malicious outputs while maintaining normal behavior for legitimate users. Proposes novel attack vectors and defense mechanisms for model sharing platforms. |

### ⚔️ White-Box Adversarial Attacks
| Paper | Summary |
|-------|---------|
| [HotFlip](https://aclanthology.org/P18-2006/) | Introduces first gradient-based attack for text models. Uses character-level flips to generate adversarial examples while maintaining semantic similarity. Shows vulnerabilities in character-based models. |
| [Is BERT Really Robust?](https://arxiv.org/abs/1907.11932) | Establishes strong baseline attack methods for NLP models. Shows BERT's vulnerabilities to simple word replacement strategies. Proposes TextFooler attack algorithm. |
| [Universal Adversarial Attacks](https://arxiv.org/html/2307.15043v2) | Demonstrates transferable attacks that work across different aligned LLMs. Achieves high success rates with minimal queries through universal perturbation patterns. |
| [AutoDAN](https://arxiv.org/abs/2310.04451) | Automated jailbreak prompt generation using evolutionary optimization. Can bypass content filters of commercial LLMs with high success rate. Shows systematic vulnerabilities in safety mechanisms. |

### 🎯 Black-box Adversarial Attacks
| Paper | Summary |
|-------|---------|
| [Low-Resource Languages Jailbreak](https://arxiv.org/abs/2310.02446) | Exploits LLMs' handling of low-resource languages to bypass safety filters. Shows high success rate on GPT-4 using translated harmful prompts. |
| [Refusal Training Generalization](https://arxiv.org/abs/2407.11969) | Analyzes how refusal training generalizes across tenses. Shows models often fail to maintain safety when prompts are rephrased in past tense. |
| [Few-Shot Jailbreaks](https://arxiv.org/abs/2310.06387) | Demonstrates how aligned LLMs can be jailbroken with just a few in-context examples. Proposes defense strategies through better prompt design. |
| [Black-box Text Attacks](https://arxiv.org/abs/1801.04354) | Early work on black-box attacks against text classifiers. Uses genetic algorithms to generate adversarial examples without model access. |
| [Instruction-centric Responses](https://arxiv.org/abs/2402.15302) | Analyzes ethical vulnerabilities in instruction-following LLMs. Shows how safety guardrails can be circumvented through careful prompt engineering. |
| [Twenty Queries Jailbreak](https://arxiv.org/abs/2310.08419) | Efficient black-box attack requiring only 20 queries to jailbreak LLMs. Uses optimization to find minimal successful attack sequences. |

### 🎯 Alignment Problems
| Paper | Summary |
|-------|---------|
| [General Language Assistant](https://arxiv.org/abs/2112.00861) | Uses language models as experimental platform for alignment research. Proposes framework for studying alignment challenges in realistic settings. |
| [Constitutional AI](https://arxiv.org/abs/2212.08073) | Introduces framework for training AI systems with ethical constraints. Uses AI feedback for alignment and proposes scalable approach to value learning. |
| [Alignment Paradox](https://arxiv.org/abs/2405.20806) | Identifies fundamental tensions in AI alignment. Shows how certain alignment approaches can paradoxically increase risks. |

### 👀 Scalable Oversight
| Paper | Summary |
|-------|---------|
| [Measuring Oversight Progress](https://arxiv.org/abs/2211.03540) | Proposes metrics for evaluating scalable oversight methods. Analyzes current approaches and their limitations. |
| [Weak LLMs Judging Strong LLMs](https://arxiv.org/html/2407.04622v1) | Shows smaller models can effectively evaluate larger ones. Cost-effective approach to AI oversight using model hierarchies. |
| [Debate for Supervision](https://arxiv.org/abs/2311.08702) | Uses debate between AI systems to improve oversight. Shows how adversarial debate can surface potential issues. |
| [Recursive Self-Critiquing](https://arxiv.org/abs/2502.04675) | Proposes recursive approach where AI systems critique their own outputs. Demonstrates scalability to superhuman AI capabilities. |

### 🛡️ Safety Algorithms
| Paper | Summary |
|-------|---------|
| [Homer Simpson Safety Alignment](https://arxiv.org/abs/2402.11746) | Uses task arithmetic for safety re-alignment of fine-tuned models. Novel approach to correcting unsafe behaviors post-training. |
| [SafeInfer](https://arxiv.org/abs/2406.12274) | Implements runtime safety checks during model inference. Adaptive approach that maintains performance while ensuring safety. |
| [Function Vectors](https://arxiv.org/abs/2310.15213) | Discovers interpretable directions in LLM representation space. Shows how to control model behavior through vector arithmetic. |
| [Text Generation Arithmetic](https://arxiv.org/abs/2311.14479) | Extends vector arithmetic to controlled text generation. Demonstrates compositional control over model outputs. |

### 🔍 Mechanistic Interpretability
| Paper | Summary |
|-------|---------|
| [Feed-Forward as Memory](https://arxiv.org/abs/2012.14913) | Shows transformer feed-forward layers act as key-value memories. Fundamental insight into transformer architecture. |
| [Context Learning](https://arxiv.org/abs/1905.06316) | Analyzes how contextual representations encode sentence structure. Reveals hierarchical linguistic knowledge in embeddings. |
| [BERT Pipeline](https://arxiv.org/abs/1905.05950) | Shows BERT learns traditional NLP pipeline stages in its layers. Maps neural representations to linguistic features. |
| [Latent Knowledge](https://arxiv.org/abs/2212.03827) | Method for extracting knowledge from LLMs without supervision. Novel probing techniques for model understanding. |
| [Sparse Debugging](https://arxiv.org/abs/2105.04857) | Uses sparse linear layers for interpretable networks. Enables systematic debugging of deep learning models. |
| [Tuned Lens](https://arxiv.org/abs/2303.08112) | Tool for analyzing internal predictions in transformers. Reveals how models process information across layers. |
| [Transformer Circuits](https://transformer-circuits.pub/2021/framework/index.html) | Mathematical framework for understanding transformer components. Systematic approach to circuit analysis. |
| [Induction Heads](https://transformer-circuits.pub/2022/in-context-learning-and-induction-heads/index.html) | Analyzes role of induction heads in in-context learning. Shows how transformers learn patterns from context. |

### 🗑️ Machine Unlearning
| Paper | Summary |
|-------|---------|
| [LLM Unlearning](https://arxiv.org/abs/2310.10683) | Methods for selective removal of knowledge from LLMs. Maintains model performance while forgetting specific information. |
| [Embedding-Corrupted Prompts](https://arxiv.org/abs/2406.07933) | Novel unlearning approach using embedding corruption. Efficient method requiring no model retraining. |

### 🔐 LLM Watermarking
| Paper | Summary |
|-------|---------|
| [LLM Watermarking](https://arxiv.org/abs/2301.10226) | Statistical method for watermarking LLM outputs. Provides detection guarantees with minimal impact on text quality. |
| [Robust Watermarking](https://arxiv.org/abs/2306.17439) | Develops attack-resistant watermarking scheme. Proves theoretical bounds on watermark security. |
| [Multi-bit Watermark](https://aclanthology.org/2024.naacl-long.224/) | Extends watermarking to encode multiple bits of information. Improves capacity while maintaining robustness. |

### 🔬 Causal Tracing
| Paper | Summary |
|-------|---------|
| [Factual Associations](https://arxiv.org/abs/2202.05262) | Methods for locating and editing specific facts in LLMs. Uses causal tracing to identify knowledge representations. |
| [Knowledge Editing](https://arxiv.org/abs/2104.08164) | Techniques for modifying factual knowledge in LLMs. Maintains model consistency while updating specific facts. |
