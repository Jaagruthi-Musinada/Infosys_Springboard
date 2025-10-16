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

# Sample text-1: Astronomy
Astronomy, one of the oldest natural sciences, is the study of celestial bodies such as stars, planets, comets, galaxies, and the universe as a whole. Since ancient times, humans have looked to the night sky with curiosity, using the movements of stars and planets to track seasons, navigate journeys, and inspire myths. Over centuries, the invention of telescopes and the advancement of physics revolutionized our understanding of the cosmos. From Galileo’s first observations of Jupiter’s moons to Edwin Hubble’s discovery of galaxies beyond the Milky Way, astronomy has continually expanded the boundaries of human knowledge. Today, it combines cutting-edge technology, data analysis, and space missions to explore cosmic phenomena like black holes, dark matter, and the origin of the universe. Radio telescopes, space observatories like the James Webb Space Telescope, and interplanetary probes have revealed breathtaking details about distant worlds and star systems. Astronomy not only answers scientific questions but also deepens philosophical ones about existence and our place in the cosmos. It drives innovation in optics, computing, and materials science while uniting humanity under a shared curiosity about the stars. As we continue to gaze into the infinite expanse, astronomy remains a bridge between wonder and discovery — a timeless pursuit of understanding the universe we inhabit.


<img width="1719" height="619" alt="image" src="https://github.com/user-attachments/assets/8a147064-f377-4339-a1ce-c53e2fa08fad" />
<img width="1062" height="334" alt="image" src="https://github.com/user-attachments/assets/42cac188-1107-4d24-9f61-b93321e7efa9" />
<img width="1070" height="333" alt="image" src="https://github.com/user-attachments/assets/0c0c7ce1-bc45-44db-be0d-fb3aef61fe39" />
<img width="1081" height="538" alt="image" src="https://github.com/user-attachments/assets/6013e027-83d3-434e-bd6d-d8ffad079068" />
<img width="1085" height="584" alt="image" src="https://github.com/user-attachments/assets/7932d4fa-8c39-4b90-9c3a-b9926537bd9e" />


# Sample text-2: Music
Music is a universal language that transcends boundaries, cultures, and generations, connecting people through rhythm, melody, and emotion. From the rhythmic beats of ancient drums to the complex symphonies of classical orchestras, music has always been an integral part of human civilization. It reflects the emotions, traditions, and identities of societies while offering comfort, joy, and expression to individuals. Different genres such as classical, jazz, rock, pop, and folk represent diverse creative approaches, each carrying unique histories and influences. Scientific studies have shown that music stimulates the brain, improves memory, and reduces stress, making it both an art and a form of therapy. In education, music enhances creativity, coordination, and emotional intelligence, shaping young minds in profound ways. The digital age has revolutionized how we create and experience music, with streaming platforms giving artists global reach and audiences instant access to millions of songs. Music also plays a vital role in films, advertisements, and social movements, amplifying messages and emotions. Whether it is a soulful tune, a patriotic anthem, or an energetic dance beat, music unites humanity through shared experiences. It remains an ever-evolving force of culture — timeless, expressive, and deeply human.

<img width="1711" height="648" alt="image" src="https://github.com/user-attachments/assets/6022fc91-dce0-4024-9365-d571e546cc22" />
<img width="1069" height="439" alt="image" src="https://github.com/user-attachments/assets/cbc9a6fd-044e-490d-8a34-5f927273431d" />
<img width="1087" height="521" alt="image" src="https://github.com/user-attachments/assets/596eaad4-fb87-46aa-8641-1ac0b7602ea9" />
<img width="1090" height="517" alt="image" src="https://github.com/user-attachments/assets/c200723e-7ade-450a-bef4-482025509add" />
<img width="1044" height="230" alt="image" src="https://github.com/user-attachments/assets/2bb0d63b-ec0f-4a01-9f0e-4ffd92d04b4e" />

<img width="1093" height="519" alt="image" src="https://github.com/user-attachments/assets/5b5ae40c-cf8b-4d48-9f61-6034a439ca20" />
<img width="1085" height="515" alt="image" src="https://github.com/user-attachments/assets/26dc5022-8e72-4993-a51e-086caa323839" />
<img width="1079" height="321" alt="image" src="https://github.com/user-attachments/assets/1b48f11c-daa0-4e08-9e9b-da44523a4e8d" />
<img width="1124" height="489" alt="image" src="https://github.com/user-attachments/assets/5a7402f2-2d99-42cb-a7ce-98429a833aa7" />


### 10 Sample Texts for Summarization 

**Sample 1- AI and Workforce:**
The recent surge in artificial intelligence has profound implications for the global workforce. Experts predict that automation will displace millions of jobs in manufacturing and data processing sectors, while simultaneously creating new roles focused on AI development, maintenance, and ethical oversight. Governments and educational institutions are urged to invest heavily in reskilling and upskilling programs to prepare the population for this transition. The key challenge lies in ensuring that the economic benefits of AI are broadly shared and do not exacerbate existing inequalities. Governments must work with private industry to make this transition equitable. This global shift requires extensive policy coordination, international agreements on data governance, and a fundamental rethinking of social safety nets to support displaced workers. The ethical dilemmas surrounding autonomous decision-making in AI systems also necessitate new regulatory frameworks to protect human rights and ensure accountability, making this one of the most complex technological transformations in human history. The long-term societal changes brought about by AI are still largely unknown, prompting urgent calls for interdisciplinary research.

**Sample 2- Renewable Energy and Storage:**
Renewable energy sources like solar and wind power are critical components of the world's strategy to combat climate change. Unlike fossil fuels, which emit greenhouse gases, these sources produce electricity with a minimal carbon footprint. However, a major hurdle remains in energy storage, as solar and wind generation is intermittent. Developing cost-effective and scalable battery technology is essential for a complete global transition to a sustainable power grid. Many countries are subsidizing research and development to accelerate this process, focusing on utility-scale storage solutions. Furthermore, advances in geothermal and tidal energy are also being explored as reliable, baseload alternatives. The integration of smart grid technologies is crucial for managing the decentralized nature of renewable power generation, requiring significant investment in infrastructure upgrades and cybersecurity measures to protect the grid from increasingly sophisticated threats. This transition requires overcoming political inertia and massive infrastructure investment to ensure reliability and affordability for all consumers worldwide, regardless of geographical location.

**Sample 3- Human Brain and Neuroscience:**
The human brain is arguably the most complex object in the known universe, consisting of billions of neurons that communicate through electrical and chemical signals. This intricate network is responsible for everything from basic involuntary functions to complex processes like consciousness, memory, and emotion. Neuroscientists use advanced imaging techniques like fMRI and EEG to map brain activity and understand how different regions interact. Continued research promises breakthroughs in treating neurological disorders such as Alzheimer's and Parkinson's disease, offering hope for millions worldwide. Recent studies have focused on neuroplasticity, revealing the brain's remarkable ability to reorganize itself by forming new neural connections throughout life. This understanding is key to developing personalized rehabilitation programs for stroke victims and individuals with traumatic brain injuries, pushing the boundaries of what is possible in cognitive recovery and mental health treatment. Understanding the intricacies of neural communication is essential for developing next-generation therapeutic strategies.

**Sample 4- Healthy Diet and Nutrition:**
A healthy diet is not merely about managing weight, but about providing the body with the necessary nutrients for optimal function. It includes a balanced intake of macronutrients (carbohydrates, proteins, fats) and micronutrients (vitamins and minerals). Processed foods, often high in sugar and unhealthy fats, contribute to a variety of chronic diseases. Embracing whole, unprocessed foods like fruits, vegetables, and lean proteins is fundamental to long-term health and well-being. Regular physical activity should also be combined with good nutrition for best results. Public health initiatives globally are targeting the reduction of sugar consumption and promoting plant-based diets rich in fiber. The impact of the gut microbiome on overall health, including mental well-being, is a rapidly expanding area of research, suggesting that dietary choices have far-reaching effects beyond physical appearance, influencing inflammation and immune system function across the lifespan. Nutritional education from an early age is vital for establishing lifelong healthy eating habits across all demographics and socio-economic groups.

**Sample 5- Quantum Computing:**
Quantum computing represents a revolutionary paradigm shift from classical computing. While classical bits store information as 0 or 1, a quantum bit (qubit) can exist in a superposition of both states simultaneously. This property, along with entanglement, allows quantum computers to perform certain calculations exponentially faster than any conventional machine. Currently, the technology is highly unstable and requires extremely low temperatures, but its eventual applications could transform fields like cryptography, material science, and drug discovery, opening up new scientific frontiers. Several governments and tech giants are in a race to achieve quantum supremacy, focusing efforts on developing more stable qubit architectures, such as superconducting circuits and trapped ions. The long-term security implications are also significant, as a large-scale quantum computer could theoretically break current public-key encryption methods, necessitating the rapid development of post-quantum cryptography standards. Research institutions are actively training the next generation of quantum engineers and physicists to lead this technological revolution in the coming decades.

**Sample 6- Great Barrier Reef and Climate Change:**
The Great Barrier Reef, the world's largest coral reef system, is a breathtaking natural wonder stretching over 2,300 kilometers off the coast of Australia. It is home to an incredible diversity of marine life, including countless species of fish, sharks, sea turtles, and dolphins. Unfortunately, the reef is severely threatened by climate change, specifically ocean acidification and rising sea temperatures that cause coral bleaching. Conservation efforts are underway globally to reduce carbon emissions and protect this fragile ecosystem for future generations. Innovative techniques, such as developing heat-resistant coral strains and deploying automated underwater vehicles to monitor reef health, are being trialed with cautious optimism. Funding for marine park management and stricter regulations on coastal development and agricultural runoff are also vital to mitigating localized human impacts that compound the existential threat posed by global climate change, requiring urgent international cooperation to safeguard the biodiversity of the entire ecosystem. Protecting the reef is a litmus test for global environmental stewardship.

**Sample 7- Reading Fiction and Cognition:**
Reading fiction is a powerful exercise for the human mind, often resulting in increased empathy and improved theory of mind. When we immerse ourselves in a novel, we are forced to see the world from different characters' perspectives, expanding our emotional intelligence. Studies show that people who regularly read fiction are better at understanding and predicting the actions of others in real-life social situations. Beyond empathy, reading also improves vocabulary, concentration, and analytical skills, which are beneficial in professional life. The cognitive benefits extend to improved memory and reduced stress levels, making it a valuable tool for lifelong learning and mental resilience. Literary scholars often explore how fiction shapes cultural narratives and moral reasoning, suggesting a deeper societal role for storytelling than mere entertainment. The choice of reading material, from classic literature to contemporary speculative fiction, can significantly influence an individual's worldview and critical thinking abilities. Encouraging reading culture is a key educational objective.

**Sample 8- Microplastics and Pollution:**
Microplastics, tiny fragments of plastic less than 5mm long, have become a pervasive global pollutant found everywhere from the deepest oceans to the highest mountains. They originate from the breakdown of larger plastic items and pose a threat to marine life, which often mistake them for food. Researchers are actively studying the long-term effects of microplastics on human health, especially as they enter the food chain. Finding sustainable alternatives to single-use plastics and improving waste management systems are urgent priorities for environmental health. The challenge is magnified by the complexity of plastics recycling, with much of the world's plastic waste still ending up in landfills or leaking into natural environments. Scientists are developing innovative enzyme-based solutions and pyrolysis technologies to efficiently break down different types of plastic polymers, offering hope for a circular economy. Global legislation restricting unnecessary plastic packaging is gaining momentum, pushing industries toward bio-degradable or infinitely reusable materials. Consumer behavior changes are equally important in mitigating this widespread environmental crisis.

**Sample 9- Cryptocurrency and Blockchain:**
The concept of cryptocurrency, decentralized digital money secured by cryptography, was popularized by the introduction of Bitcoin in 2009. Unlike traditional currencies, it is not controlled by any single bank or government, operating instead on a distributed ledger technology called blockchain. While initially met with skepticism, cryptocurrencies have gained mainstream acceptance as an asset class and a method of payment. However, they remain highly volatile and face significant regulatory challenges globally, particularly regarding consumer protection. Central banks are exploring the development of their own digital currencies (CBDCs) to modernize payment systems and maintain monetary control in the face of decentralized competition. The energy consumption associated with proof-of-work cryptocurrencies is also a major environmental concern, driving a shift towards more energy-efficient proof-of-stake mechanisms. The future of global finance is increasingly hybrid, blending traditional institutions with decentralized technology and requiring new legal frameworks to ensure market stability and prevent illicit financial activities.

**Sample 10- Plate Tectonics and Geology:**
Plate tectonics is the scientific theory that Earth's outer layer is divided into several large plates that slowly move over the mantle. This movement is the driving force behind earthquakes, volcanic eruptions, and the formation of mountain ranges. The plates interact at their boundaries: they can slide past, collide, or separate. The theory revolutionized geology, explaining many phenomena and providing a unified framework for understanding the planet's dynamic surface and its geological history. Advances in GPS technology and seismic monitoring allow scientists to measure plate movements with unprecedented accuracy, improving hazard prediction models for communities located near active fault lines and subduction zones. The slow process of continental drift has shaped not only geology but also global climate and the evolution of life on Earth, linking deep-time geological processes to contemporary ecological distribution and long-term environmental stability. Continued research into mantle convection provides critical clues about the fundamental forces driving this planetary mechanism.

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







