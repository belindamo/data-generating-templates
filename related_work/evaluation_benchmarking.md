# LLM Evaluation and Benchmarking

## AgentIF: Benchmarking Instruction Following in Agentic Scenarios

**Authors:** Yunjia Qi et al.  
**Venue:** ArXiv 2025  
**Year:** 2025  
**URL:** https://arxiv.org/abs/2505.16944

### Problem
Agentic scenarios involve lengthy instructions with complex constraints (extended system prompts, detailed tool specifications), but LLM adherence to such instructions remains underexplored.

### Assumption in Prior Work
- Standard instruction following evaluations are sufficient for agentic applications
- Simple instructions adequately test model capabilities

### Novel Insight
**Agentic instruction following** requires evaluation with realistic, long, and complex instructions that mirror real-world agent applications.

### Technical Overview
- **AgentIF Benchmark**: First systematic evaluation for agentic instruction following
- **Realistic**: 50 real-world agentic applications
- **Long**: Average 1,723 words, max 15,630 words
- **Complex**: Average 11.9 constraints per instruction

### Key Findings
Current advanced LLMs generally perform poorly on complex agentic instructions, revealing important robustness gaps.

---

## MaXIFE: Multilingual and Cross-lingual Instruction Following Evaluation  

**Authors:** Yile Liu et al.  
**Venue:** ACL 2025  
**Year:** 2025  
**URL:** https://arxiv.org/abs/2506.01776

### Problem
Existing instruction following evaluations focus on single-language scenarios, overlooking multilingual and cross-lingual challenges.

### Assumption in Prior Work
- English-centric evaluation is sufficient
- Instruction following transfers equally across languages

### Novel Insight
**Multilingual instruction following** presents unique challenges requiring specialized evaluation across diverse languages.

### Technical Overview
- **Comprehensive Coverage**: 23 languages, 1667 verifiable instruction tasks
- **Dual Evaluation**: Rule-Based + Model-Based evaluation
- **Balance**: Efficiency and accuracy in evaluation methodology

### Impact
Establishes baseline results for multilingual instruction following and provides standardized evaluation tool.

---

## SIFo: Sequential Instruction Following Benchmark

**Authors:** Xinyi Chen et al.  
**Venue:** EMNLP 2024 Findings  
**Year:** 2024  
**URL:** https://arxiv.org/abs/2406.19999

### Problem
Evaluating multiple instruction following faces challenges: limited coherence between instructions, positional bias, and lack of objectively verifiable tasks.

### Assumption in Prior Work
- Single instruction evaluation is sufficient
- Multiple instructions don't require specialized evaluation

### Novel Insight
**Sequential instruction following** requires specialized evaluation where successful completion of multiple instructions is verifiable through the final instruction only.

### Technical Overview
- **Four Task Categories**: Text modification, question answering, mathematics, security rules
- **Sequential Verification**: Final instruction validates entire sequence completion
- **Objective Evaluation**: Eliminates subjective assessment issues

### Key Findings
- Recent/larger models significantly outperform older/smaller ones
- All models struggle with instruction sequences, revealing robustness limitations
- Validates benchmark effectiveness across model families