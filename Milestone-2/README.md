# Advanced Text Summarization Project: Extractive vs. Abstractive Evaluation

This project explores and rigorously evaluates **Advanced Text Summarization** techniques, comparing modern deep learning models (Abstractive) with classic NLP methods (Extractive) across various quality and performance metrics. The goal is to provide a comprehensive, interactive tool for choosing the optimal summarization model based on specific content needs.

***

## 1. Project Goal and Scope

The primary objective was to deploy and evaluate both **abstractive and extractive summarization models** using a diverse corpus of source texts.

### Key Deliverables:
* **Dual Summarization Paradigms:** Implementation of both Abstractive (generating new sentences) and Extractive (selecting key sentences) techniques.
* **Comprehensive Evaluation:** Use of a multi-dimensional metric framework, including ROUGE, Semantic Similarity, and Readability scores.
* **Interactive Deployment:** Creation of two distinct, interactive User Interfaces (`Section A` and `Section B`) within a Google Colab environment for real-time testing.
* **Extensive Testing:** Evaluation across 10+ sample texts sourced from diverse domains, specifically analyzing results for **Astronomy** and **Music** paragraphs.
* **Performance Analysis:** Visualization of results with plots (Bar Charts, Radar Plots) and a final analysis determining which model performs best for specific categories.

***

## 2. Models Implemented

The project selected a mix of state-of-the-art and foundational models to cover a broad spectrum of summarization capabilities and computational cost.

| Model | Type | Architecture / Note |
| :--- | :--- | :--- |
| **Phi-1.5** | Large Language Model (LLM) | Focuses on high-quality, coherent abstractive summaries. Also utilized in a controlled extractive mode. |
| **TinyLlama-1.1B-Chat** | Large Language Model (LLM) | A smaller model focused on faster generation and resource efficiency. Used for both abstractive and extractive tasks. |
| **Gemma-2B-IT** | Large Language Model (LLM) | A modern, high-performance open-source model optimized for instruction following. Used for both abstractive and extractive tasks. |
| **BART-Large-CNN** | Fine-tuned Encoder-Decoder | Excellent baseline for high-quality, abstractive summaries and high compression. |
| **TextRank (Embeddings)** | Graph-Based Algorithm | A classical, unsupervised extractive method prioritized for speed. |

***

## 3. Evaluation Metrics

Performance was measured using a multi-faceted approach combining lexical overlap, semantic similarity, and human-readability proxies.

| Metric | Category | Interpretation |
| :--- | :--- | :--- |
| **ROUGE-1 / ROUGE-2** | Quality (Overlap) | Measures the overlap of unigrams (ROUGE-1) and bigrams (ROUGE-2) between the generated and reference summaries. Higher is better. |
| **Semantic Similarity** | Quality (Meaning) | Measures how close the meaning of the generated summary is to the reference text using embeddings (e.g., BERTScore proxy). Higher is better. |
| **Readability** | Style | Flesch-Kincaid Grade Level (Lower scores indicate easier reading). Lower is often preferred for general audience. |
| **Time (sec)** | Speed | Time taken to generate the summary. Lower is better. |
| **Compression** | Efficiency | Percentage reduction in size from the original text (higher % = shorter summary). |

***

## 4. Comparative Performance Analysis

The following table summarizes the performance of all models on the **Astronomy (A)** and **Music (M)** domain texts.

| Metric | TinyLlama (Abs) | Phi-1.5 (Abs) | **Gemma-2B-IT (Abs)** | BART-Large-CNN (Abs) | TextRank (Ext) | Phi-1.5 (Ext) | TinyLlama (Ext) |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| **ROUGE-2 (A)** | 0.579 | **0.756** | 0.233 | 0.449 | 0.689 | **0.833** | 0.782 |
| **Semantic Sim. (A)** | **0.928** | 0.869 | 0.640 | 0.811 | 0.919 | 0.917 | 0.897 |
| **Time (sec) (A)** | 7.54 | 6.49 | 2.47 | **1.46** | **0.07** | 7.78 | 8.08 |
| **ROUGE-2 (M)** | 0.807 | **0.897** | 0.293 | 0.370 | 0.620 | 0.774 | 0.827 |
| **Semantic Sim. (M)** | 0.941 | **0.960** | 0.821 | 0.862 | 0.913 | 0.929 | 0.935 |
| **Compression (M)** | 29.5% | 17.6% | 65.3% | **75.6%** | 51.8% | 6.2% | 16.1% |

***
# Sample text: Astronomy
Astronomy, one of the oldest natural sciences, is the study of celestial bodies such as stars, planets, comets, galaxies, and the universe as a whole. Since ancient times, humans have looked to the night sky with curiosity, using the movements of stars and planets to track seasons, navigate journeys, and inspire myths. Over centuries, the invention of telescopes and the advancement of physics revolutionized our understanding of the cosmos. From Galileo’s first observations of Jupiter’s moons to Edwin Hubble’s discovery of galaxies beyond the Milky Way, astronomy has continually expanded the boundaries of human knowledge. Today, it combines cutting-edge technology, data analysis, and space missions to explore cosmic phenomena like black holes, dark matter, and the origin of the universe. Radio telescopes, space observatories like the James Webb Space Telescope, and interplanetary probes have revealed breathtaking details about distant worlds and star systems. Astronomy not only answers scientific questions but also deepens philosophical ones about existence and our place in the cosmos. It drives innovation in optics, computing, and materials science while uniting humanity under a shared curiosity about the stars. As we continue to gaze into the infinite expanse, astronomy remains a bridge between wonder and discovery — a timeless pursuit of understanding the universe we inhabit.

## Section A: Summarize with All Models output
<img width="1719" height="619" alt="image" src="https://github.com/user-attachments/assets/8a147064-f377-4339-a1ce-c53e2fa08fad" />
<img width="1062" height="334" alt="image" src="https://github.com/user-attachments/assets/42cac188-1107-4d24-9f61-b93321e7efa9" />
<img width="1070" height="333" alt="image" src="https://github.com/user-attachments/assets/0c0c7ce1-bc45-44db-be0d-fb3aef61fe39" />
<img width="1081" height="538" alt="image" src="https://github.com/user-attachments/assets/6013e027-83d3-434e-bd6d-d8ffad079068" />
<img width="1085" height="584" alt="image" src="https://github.com/user-attachments/assets/7932d4fa-8c39-4b90-9c3a-b9926537bd9e" />






## 5. Model Output Analysis by Category

### **Best for High-Quality Abstractive Summaries (ROUGE/Semantic)**

* **Overall Winner: Phi-1.5 (Abstractive)**
    * **Astronomy:** Achieved the highest ROUGE-2 score (0.756), indicating the best word-level overlap and fluency compared to the reference.
    * **Music:** Also scored the highest in both ROUGE-2 (0.897) and Semantic Similarity (0.960).
    * **Conclusion:** Phi-1.5 is the top choice for tasks where the summary needs to be creative, highly fluent, and accurately convey the core meaning, even if it results in a longer output (lower compression).

### **Best for Speed and Computational Efficiency**

* **Overall Winner: TextRank (Extractive - Embeddings)**
    * **Performance:** Consistently outperformed all other models in processing time, requiring only **0.07 seconds (Astronomy)** and **0.02 seconds (Music)**.
    * **Conclusion:** TextRank is the optimal model for low-latency, high-throughput applications where real-time performance is paramount, such as quickly generating highlights for news feeds or large document indexing.

### **Best for Concise/High-Compression Summaries**

* **Top LLM for Compression: Gemma-2B-IT (Abstractive)**
    * **Performance:** Gemma demonstrated the highest compression rates among the LLMs (73.6% for Astronomy and 65.3% for Music), meaning it produced the shortest summaries in terms of word count. Its performance in ROUGE/Semantic Similarity was lower, suggesting it prioritized brevity over detail.
    * **Conclusion:** Gemma-2B-IT is excellent for use cases requiring a very brief, rapid, one-to-two sentence overview where high fidelity (ROUGE) is not the top metric.
* **Overall Compression Winner: BART-Large-CNN (Abstractive)**
    * **Performance:** Achieved the highest overall compression rate on the Music text (75.6%), offering the shortest output length. This is an efficient benchmark model for producing succinct outputs quickly (Time: 0.92-1.46 sec).

### **Context-Specific Analysis (Fidelity vs. Task)**

The testing confirmed that the best model depends heavily on the content domain:

* **For Factual/Technical Content (Astronomy):**
    * **Phi-1.5 (Extractive)** excelled in ROUGE-2 (0.833). This suggests that for conveying scientific facts, simply **selecting the key original sentences** (extractive LLM mode) results in a better summary (higher ROUGE-2 score) than trying to paraphrase and synthesize (abstractive mode), because factual precision requires quoting the source text accurately.
    * **TinyLlama (Abstractive)** had the best Semantic Similarity (0.928), indicating it may be the best at retaining the *meaning* of the complex concepts, even if its paraphrasing differs slightly from the reference text (lower ROUGE-2).

* **For Expressive/Descriptive Content (Music):**
    * **Phi-1.5 (Abstractive)** led across ROUGE and Semantic Similarity. This highlights the strength of Abstractive models for descriptive texts, where generating fluent, varied, and coherent human-like sentences is beneficial for the summary's quality. Extractive methods struggle here because the best points are often spread across multiple paragraphs, making simple selection difficult.

