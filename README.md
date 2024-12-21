# Small Language Model Reasoning using Multi-Agent Graph Distillation 
Reimplemention of the research paper [MAGDI: Structured Distillation of Multi-Agent Interaction Graphs Improves Reasoning in Smaller Language Models](https://arxiv.org/pdf/2402.01620v2) using structured knowledge distillation to improve reasoning of small language models from integrating multi-agent interaction graph with LLMs.  

## Pipeline  
1. Prepare MAGs Training Data - Build reasoning graphs from multi-agent interactions between LLMs i.e. teacher models.
2. Get Node Embeddings - Encode reasoning steps into numerical representations.
3. Train the Base Student Model using MAGDi - Teach the student model i.e. small language model using MAGDi objectives.
4. Evaluate the MAGDi-Augmented Model - Test the student model’s performance on reasoning tasks within benchmarks.

## Multi-Agent System
![image](https://github.com/user-attachments/assets/c5af52e2-7568-4c51-a9fb-920c698fc083)
![image](https://github.com/user-attachments/assets/032ab31b-13c5-484c-9124-a6d476e0f71a)

## Results
- MAGDi outperformed both single-teacher and multi-teacher methods on commonsense and math reasoning tasks with around 5% accuracy improvement on average.
- MAGDI-distilled models reduced the number of tokens required during inference by up to 9 times compared to teacher models.
- Demonstrated better out-of-domain performance compared to baseline distillation methods.
- Larger student models trained with MAGDI performed better, showing positive scaling with model size.
- Multi-teacher training with diverse reasoning paths led to larger improvements compared to using a single teacher.

**Benchmarks:**<br>
<img width="736" alt="image" src="https://github.com/user-attachments/assets/14b8124d-02a9-4fc3-92e6-13671e507aa9" />
