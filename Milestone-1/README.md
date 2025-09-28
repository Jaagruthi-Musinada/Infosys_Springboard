# Infosys_Springboard
## TextMorph Advanced Text Summarization and Paraphrasing

**TextMorph Advanced Text Summarization and Paraphrasing** is an NLP project designed to perform advanced text summarization and paraphrasing on large text documents. It leverages transformer models such as T5, BART, and PEGASUS to generate concise summaries and diverse paraphrases. Classical NLP techniques like bigram analysis and similarity scoring are integrated to provide deeper insights and visual representations of textual patterns. This combination of models and analysis makes the project suitable for automated text understanding and exploration.


## Methodology

**Text Inputs:**  
Two public domain literary works were selected from Project Gutenberg for analysis:  
- [Alice’s Adventures in Wonderland by Lewis Carroll](https://www.gutenberg.org/files/11/11-0.txt)  
- [The Adventures of Sherlock Holmes by Arthur Conan Doyle](https://www.gutenberg.org/files/1661/1661-0.txt)  

**Summarization:**  
T5, BART, and PEGASUS were used to generate summaries. T5 balanced summary length and content, BART retained rich context, and PEGASUS produced concise summaries. All summaries were evaluated for semantic similarity and information retention.

**Paraphrasing:**  
PEGASUS, T5-Paraphrase, and BART-Paraphrase were applied to selected sentences. PEGASUS generated highly diverse outputs, BART preserved meaning closely, and T5-Paraphrase maintained a balance of diversity and accuracy.

**Similarity Analysis:**  
Cosine similarity scores were computed using Sentence Transformers to assess alignment between original texts and their summaries or paraphrases.

**Bigram Analysis:**  
Frequent word pairs were extracted to identify recurring patterns and characteristic phrases in each text.

**Visualizations:**  
Word clouds highlighted common words in Alice’s Adventures in Wonderland, while heatmaps showed co-occurrences in The Adventures of Sherlock Holmes. Comparison plots illustrated differences between summarization and paraphrasing models, and bigram charts highlighted top recurring word pairs.


## Observations

**Summarization:**  
PEGASUS generated concise summaries that focused on the main content, BART maintained detailed context and narrative flow, and T5 offered a balanced approach between length and informativeness.

**Paraphrasing:**  
PEGASUS provided highly varied paraphrases, whereas BART maintained closer semantic alignment with the original sentences. T5-Paraphrase produced outputs that were both accurate and moderately diverse.

**Similarity Scores:**  
Analysis showed that T5 and BART summaries and paraphrases were slightly more aligned with the original texts compared to PEGASUS, reflecting their ability to retain semantic meaning.

**Bigram Analysis:**  
Common word pairs such as “said Alice” in Wonderland and “Sherlock Holmes” in Holmes were identified, providing insight into the stylistic patterns and recurring narrative elements of the texts.

**Visual Insights:**  
Word clouds highlighted dominant themes and frequently occurring words, while heatmaps illustrated the co-occurrence of characters and important narrative terms, enhancing understanding of the text’s structure.


## Conclusion
TextMorph demonstrates the effective combination of transformer-based models and classical NLP techniques to perform advanced text summarization and paraphrasing. By providing both quantitative evaluations and visual representations, the project offers a robust framework for automated text understanding. It establishes a strong foundation for further exploration of AI-driven language processing and advanced textual analysis.
