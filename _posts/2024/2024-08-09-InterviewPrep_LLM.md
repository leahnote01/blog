---
title: "(editing) Data Science Interview Prep - LLM/AI"
layout: single
classes: wide
categories: interview_Prep
read_time: True
typora-root-url: ../
tag: [interviewPrep,dataScience,statistics,interviewGoogle]
toc: true 
---

# Interview Questions & Answers

### LLM & AI

---

Questions from:

<I><b>[LinkedIn Post by Daniel Lee : LLM Interview Questions](https://www.linkedin.com/posts/danleedata_what-%F0%9D%97%9F%F0%9D%97%9F%F0%9D%97%A0-%F0%9D%97%B0%F0%9D%97%BC%F0%9D%97%BB%F0%9D%97%B0%F0%9D%97%B2%F0%9D%97%BD%F0%9D%98%81%F0%9D%98%80-are-often-asked-activity-7258899191333097474-zEe6?utm_source=share&utm_medium=member_desktop) </b></I>



---

#### LLM

#### Basic Concepts - LLM

- **Architecture & Training** 
  - Transformer Architecture (attention mechanisms
  - Pre-training vs Fine-tuning
  - Training Objectives (next token prediction)
  - Context Window and Position Embeddings
  - Tokenization Strategies
  - Model Scaling Laws
  - Parameter Efficient Fine-tuning (LoRA, QLoRA, Prefix Tuning)
- **Generation & Control**
  - Temperature and Top-p Sampling
  - Prompt Engineering Techniques
  - Few-shot Learning
  - In-context Learning
  - Chain-of-Thought Prompting
  - Hallucination Prevention



---

**Answers**

### **Architecture & Training**

1. **Transformer Architecture (Attention Mechanisms):**
   - Transformers use self-attention to weigh the importance of each word in a sequence, allowing the model to <u>capture dependencies regardless of distance</u>. This architecture has led to breakthroughs in NLP by effectively modeling long-range context.
2. **Pre-training vs. Fine-tuning:**
   - Pre-training involves training on vast datasets t<u>o develop general language understanding</u>. Fine-tuning adapts the model <u>to specific tasks</u> with a smaller, domain-specific dataset, <u>enhancing</u> performance in target areas.
3. **Training Objectives (Next Token Prediction):**
   - For language models, their main goal is to predict the next token in a sequence. This capability fosters the learning of contextual relationships within the text, enabling the model <u>to produce sequences that are both **coherent** and **accurate** in context.</u>
4. **Context Window and Position Embeddings:**
   - The context window defines <u>the maximum token length</u> the model can process at once. Position embeddings retain <u>token order</u> because Transformers inherently <u>do not depend on the order of sequences.</u>
5. **Tokenization Strategies:**
   - Tokenization splits text into <u>smaller units (tokens)</u> for model processing. Common strategies include **Byte Pair Encoding (BPE)** and WordPiece, <u>which balance vocabulary size and generalization.</u>
   - Byte Pair Encoding (BPE) is a tokenization method that compresses text by iteratively <u>merging the most frequent pairs of characters or subwords.</u> This approach creates a manageable vocabulary of subword units, allowing models to handle rare or compound words by breaking them into smaller, reusable tokens.
6. **Model Scaling Laws:**
   - Scaling laws reveal that <u>larger models (with more parameters and data) typically perform better</u>, but <u>with diminishing returns</u>. These laws guide resource allocation for optimal model size and training.
7. **Parameter Efficient Fine-tuning (LoRA, QLoRA, Prefix Tuning):**
   - Techniques like LoRA, QLoRA, and Prefix Tuning enable fine-tuning large models efficiently by adjusting only specific layers or adding lightweight adapters, making the process faster and more cost-effective.
   - **LoRA (Low-Rank Adaptation)**: LoRA fine-tunes large models by <u>injecting low-rank matrices into specific layers, adjusting only a few parameters.</u> This makes the process more efficient by minimizing memory and computational requirements.
   - QLoRA (Quantized LoRA): QLoRA combines low-rank adaptation with quantization, reducing model precision to save memory and computing costs. It’s beneficial for deploying large models on resource-constrained devices.
   - Prefix Tuning: Prefix Tuning fine-tunes models <u>by adding a learned "prefix" of virtual tokens to the input, which guides the model in task-specific ways without modifying the core model parameters</u>. This method is lightweight and effective for many NLP tasks.



------

### **Generation Control**

1. **Temperature and Top-p Sampling:**
   - **Temperature** controls randomness in generation (lower values make the output more focused, and higher values increase creativity). **Top-p sampling** (nucleus sampling) <u>selects tokens from the smallest set whose cumulative probability meets a threshold, reducing unlikely outcomes.</u>
2. **Prompt Engineering Techniques:**
   - Crafting prompts to guide model responses improves task-specific performance. Good prompts often include explicit instructions, context, or examples to direct the model effectively.
3. **Few-shot Learning:**
   - Few-shot learning <u>uses a handful of examples within a prompt to enable the model to generalize to similar tasks</u> without extensive re-training, leveraging prior knowledge from pre-training.
4. **In-context Learning:**
   - In-context learning involves showing the model a context or sequence that influences its response, allowing it to generate relevant output based on preceding examples or information.
5. **Chain-of-Thought Prompting:**
   - This method encourages the model **to think step-by-step**, improving reasoning in complex tasks by breaking down its response into <u>logical, sequential steps, which enhances interpretability and accuracy.</u>
6. **Hallucination Prevention:**
   - Techniques like **fact-checking, retrieval augmentation, and reinforcement tuning** reduce hallucinations, ensuring the model’s responses are accurate and grounded in factual information.

<bR><Br>