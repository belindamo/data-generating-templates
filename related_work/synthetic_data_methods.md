# Synthetic Data Generation Methods

## SynAlign: Few-shot LLM Synthetic Data with Distribution Matching

**Authors:** Jiyuan Ren et al.  
**Venue:** WWW 2025  
**Year:** 2025  
**URL:** https://arxiv.org/abs/2502.08661

### Problem
LLM-generated synthetic data often differs from real data in key language attributes (styles, tones, content proportions), causing distribution distortion when mixed with real data.

### Assumption in Prior Work
- Synthetic data can be directly mixed with real data without distribution considerations
- Quality over distribution matching is sufficient

### Novel Insight
**Distribution matching** is crucial - synthetic data generation must consider and align with the linguistic attribute distributions of real data.

### Technical Overview
- **Uncertainty Tracker**: Gaussian Process model for iterative data cluster selection
- **Latent Attribute Reasoning**: LLM summarizes linguistic attributes before synthesis  
- **Maximum Mean Discrepancy**: Objective function for learning sampling weights
- **Distribution Alignment**: Ensures synthetic data matches real data distribution

### Validation
- Significant performance improvements on multiple text prediction tasks
- Online A/B test validation on retriever systems
- Distribution matching prevents performance degradation

---

## BARE: Leveraging Base Language Models for Few-Shot Synthetic Data Generation

**Authors:** Alan Zhu et al.  
**Venue:** ArXiv 2025  
**Year:** 2025  
**URL:** https://arxiv.org/abs/2502.01697

### Problem
Current synthetic data methods require tens of thousands of seed examples and rely on instruction-tuned models, which produce insufficient diversity in few-shot settings.

### Assumption in Prior Work
- Instruction-tuned models are superior for synthetic data generation
- Large seed sets are necessary for quality generation

### Novel Insight
**Base models without post-training** offer substantially greater output diversity than instruction-tuned models, despite lower instruction-following abilities.

### Technical Overview
- **Base-Refine (BARE)**: Two-stage method combining base model diversity with instruction-tuned quality
- **Few-shot Setting**: Only 3 seed examples needed
- **Diversity Focus**: Leverages base models' untapped potential for diverse generation

### Validation
- Llama 3.1 8B with 1,000 BARE samples achieves performance comparable to SOTA similarly sized models
- 101% improvement on GSM8K for Llama 3.2 1B
- 18.4% improvement over RAFT method for RAG data generation

---

## SynthLLM: Scaling Laws of Synthetic Data for Language Models

**Authors:** Zeyu Qin et al.  
**Venue:** ArXiv 2025  
**Year:** 2025  
**URL:** https://arxiv.org/abs/2503.19551

### Problem
Web data for pre-training is rapidly depleting, and synthetic data scalability compared to raw pre-training data is unclear.

### Assumption in Prior Work
- Raw web data is irreplaceable for pre-training
- Synthetic data doesn't follow predictable scaling laws

### Novel Insight
Synthetic datasets can exhibit **predictable scalability** comparable to raw pre-training data when properly generated.

### Technical Overview
- **Graph Algorithm**: Extracts and recombines high-level concepts across documents
- **Scaling Law Adherence**: Synthetic data reliably follows rectified scaling law
- **Performance Plateaus**: Near 300B tokens for various model sizes

### Key Findings
1. Synthetic data reliably adheres to scaling laws across model sizes
2. Performance improvements plateau near 300B tokens  
3. Larger models approach optimal performance with fewer training tokens (8B model peaks at 1T tokens vs 3B model requiring 4T)
4. Superior performance and scalability vs existing synthetic methods