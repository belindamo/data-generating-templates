# Template-Based Data Generation Methods

## TemplateMath: Training and Evaluating Language Models with Template-based Data Generation

**Authors:** Yifan Zhang et al.  
**Venue:** ArXiv 2024  
**Year:** 2024  
**URL:** https://arxiv.org/abs/2411.18104

### Problem
Large-scale, high-quality, domain-specific datasets for mathematical reasoning are scarce, limiting sophisticated reasoning abilities in LLMs.

### Assumption in Prior Work
Mathematical reasoning datasets must be:
- Manually created by experts
- Limited in scope and scale
- Difficult to generate systematically

### Novel Insight
LLMs (GPT-4) can automatically generate parameterized meta-templates, which can then synthesize virtually unlimited high-quality mathematical problems and solutions.

### Technical Overview
- **Meta-template Generation**: GPT-4 creates parameterized templates
- **Template-based Data Generation (TDG)**: Systematic synthesis of problems/solutions
- **TemplateGSM Dataset**: 7M+ grade school math problems with code-based and natural language solutions

### Impact
- Alleviates scarcity of large-scale mathematical datasets
- Elevates data augmentation using GPT-4 for meta-template generation
- Provides effectively unlimited data generation potential

---

## TarGEN: Targeted Data Generation with Large Language Models

**Authors:** Himanshu Gupta et al.  
**Venue:** ArXiv 2023  
**Year:** 2023  
**URL:** https://arxiv.org/abs/2310.17876

### Problem
Synthetic datasets often suffer from lack of diversity and added noise, limiting their effectiveness for training.

### Assumption in Prior Work
- Synthetic data generation requires specific task instances as seeds
- Quality control is difficult in automated generation

### Novel Insight
**Seedless generation**: Multi-step prompting strategy that doesn't require specific task instances, with self-correction capabilities for label reliability.

### Technical Overview
- **Multi-step Prompting**: TarGEN prompting strategy
- **Self-correction**: LLMs rectify incorrectly labeled instances during creation
- **Broad Applicability**: Works beyond task replication

### Validation
- 1-2% points better performance than original datasets on SuperGLUE
- T5-3B yields impressive OpenLLM leaderboard results
- Similar/higher complexity and diversity compared to original data

---

## GLAN: Generalized Instruction Tuning for Language Models

**Authors:** Haoran Li et al.  
**Venue:** ArXiv 2024  
**Year:** 2024  
**URL:** https://arxiv.org/html/2402.13064v1

### Problem
Prior instruction tuning relies on seed examples or existing datasets, limiting scalability and coverage.

### Assumption in Prior Work
Instruction datasets must be constructed from:
- Existing examples or seed data
- Human-curated content
- Task-specific training data

### Novel Insight
Use pre-curated **taxonomy of human knowledge and capabilities** as input to generate large-scale synthetic instruction data across all disciplines, inspired by human education systems.

### Technical Overview
- **Knowledge Taxonomy**: Systematic decomposition of human knowledge into fields, sub-fields, disciplines
- **Syllabus Design**: LLM-generated syllabus for each subject
- **Comprehensive Coverage**: Instructions across entire spectrum of human knowledge

### Impact
Excels across multiple dimensions without using task-specific training data:
- Mathematical reasoning
- Coding
- Academic exams  
- Logical reasoning
- General instruction following