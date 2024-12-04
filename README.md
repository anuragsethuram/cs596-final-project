# Visualizing Embeddings towards Explainable AI

## Introduction to Word Embeddings and NLP

### What are Word Embeddings?
- Word embeddings are numerical representations of words in a continuous vector space, where words with similar meanings are positioned close to one another.
- These embeddings capture both the syntactic and semantic aspects of words, enabling NLP models to better understand language.

### Importance in NLP:
- **Text Representation**: Transforms text data into a numerical format that can be interpreted by machine learning models.
- **Context Awareness**: Embeddings like BERT create context-dependent representations, where the meaning of words varies based on the surrounding text.

---

## Visualizing Word Embeddings in a 2D/3D Space

### Key Steps in the Visualization Process:
1. **Tokenization**: Convert words into tokens using a tokenizer.
2. **Embedding Generation**: Use pre-trained models to generate embeddings for each word.
3. **Dimensionality Reduction**: Apply PCA (Principal Component Analysis) to compress embeddings from a high-dimensional space (such as 768 dimensions) into 2D or 3D for easier visualization.
4. **Plotting**: Visualize the embeddings using Matplotlib or Plotly, showing relationships between words.

---

## Measuring Similarity: Cosine Similarity Between Word Embeddings

### What is Cosine Similarity?
- Cosine similarity calculates the cosine of the angle between two vectors, with values ranging from -1 (completely dissimilar) to +1 (exactly the same).
- Words with similar meanings will have a smaller angle between them, resulting in a higher cosine similarity.

---

## Explainable AI (XAI) in NLP with LLMs

### What is Explainable AI?
- Explainable AI refers to approaches that enable humans to comprehend and interpret the decision-making process of AI models.
- In NLP, XAI is critical for ensuring transparency, fairness, and trustworthiness of models.

### The Role of LLMs in XAI:
- Large Language Models (LLMs) such as GPT and PaLM produce intricate outputs by processing large amounts of text. However, the reasoning behind their decisions can be unclear.

### Key Approaches for Explaining LLMs:
1. **Attention Visualization**:
   - Analyze attention weights from transformer models to understand which parts of the input text influenced the output most.
   - Example: Visualizing which words in a sentence contributed to a specific prediction or answer.

2. **Saliency Maps**:
   - Highlight important words or phrases in input text that strongly affect the model's output.
   - Example: Using saliency maps in sentiment analysis to explain why a review is classified as positive.

3. **Prompt Engineering for Interpretability**:
   - Craft prompts that explicitly ask the model to explain its reasoning.
   - Example: Adding "Explain your answer step by step" to a prompt encourages LLMs to generate interpretable outputs.

4. **Post-Hoc Explanations**:
   - Use external techniques like SHAP (SHapley Additive exPlanations) to measure the contribution of input features to predictions.
   - Example: Explaining why the model predicted "positive" for a review based on the frequency of certain words.

5. **Model-Agnostic Tools**:
   - LIME (Local Interpretable Model-Agnostic Explanations) can be applied to NLP tasks to create interpretable local approximations of the model's predictions.

### Challenges in XAI for LLMs:
- **Complexity**: The vast number of parameters in LLMs makes direct interpretation difficult.
- **Context Sensitivity**: The outputs of LLMs are highly influenced by context, which can shift rapidly with even minor changes to the input text.
- **Trade-Offs**: Enhancing explainability could potentially lower performance or necessitate simplifications that omit some of the model's nuances.

### Importance of XAI in Real-World Applications:
1. **Bias Detection**: Identify and mitigate biases in language models to ensure fairness.
2. **Regulatory Compliance**: Make sure AI models comply with transparency standards in sectors such as healthcare and finance.
3. **User Trust**: Increase user confidence by showing clear explanations for model outputs.
4. **Debugging and Optimization**: Enable developers to diagnose and improve model performance effectively.

---

## Practical Use Cases for Word Embeddings and Similarity

1. **Search and Information Retrieval**:  
   *Example*: When a user searches for "doctor," the system can also provide results for related terms such as "nurse," "hospital," and "medicine."

2. **Text Classification and Sentiment Analysis**:  
   *Example*: Categorizing product reviews as positive or negative by interpreting the context of the words used in the reviews.

3. **Question Answering Systems**:  
   *Example*: The question "What is the capital of France?" can be correctly matched with the answer "Paris" through semantic similarity.

4. **Machine Translation**:  
   *Example*: Translating the word "house" from English to "maison" in French by identifying the closest word in the target language's embedding space.

## Results
The images below display the positions of word embeddings in a three-dimensional space for three closely related words: university, college, and school.
&nbsp;
&nbsp;

![University](https://github.com/user-attachments/assets/a7238923-6b25-456f-9869-974cc6679aec)
![College](https://github.com/user-attachments/assets/ec3dbe6b-5519-4bef-879d-a89d1d4b05a8)
![School](https://github.com/user-attachments/assets/7a54798d-68ac-4d04-801b-5287a8fccf0d)

&nbsp;

In comparison, a word like "party" is much less correlated, and hence is much farther away.
![Party](https://github.com/user-attachments/assets/a6057a3b-427c-4576-8318-4e17c4a72952)
&nbsp;
&nbsp;

## Live Code
https://colab.research.google.com/drive/19PVdehyzYuo8cWeABjKdE7a4nQwpiRvt?usp=sharing

