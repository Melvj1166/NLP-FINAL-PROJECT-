# 🛡️ Presentation Template Content

*Here is the text to copy/paste into your Google Slides template for your 5-minute video presentation.*

---

## Slide 1: Title Slide
**Title:** Analyzing Insurance Customer Reviews using NLP
**Subtitle:** Coursework Project 2
**Names:** [Your Name] & [Partner's Name]
**Date:** March 31, 2026

---

## Slide 2: The Problem (30 sec)
**Title:** Objective & Context
- **Goal:** Extract meaningful insights from thousands of French insurance customer reviews.
- **Challenge:** Unstructured text data, mixed sentiments, and spelling errors.
- **Solution:** We built an end-to-end NLP pipeline:
  1. Data Cleaning & Exploration
  2. Embeddings & Topic Modeling
  3. Supervised Classification (Stars, Sentiment, Categories)
  4. Interactive Streamlit Dashboard

*Speaking Note: "Hello! Today we are presenting our analysis of insurance reviews. Our goal was to structure chaotic text data into actionable insights for insurers using NLP and Machine Learning."*

---

## Slide 3: Data Cleaning & Exploration (30 sec)
**Title:** Data Processing
- **Cleaning Steps:**
  - Lowercasing, removed punctuation & stopwords
  - Lemmatization (spaCy/NLTK)
  - Spelling Correction via TextBlob
- **Key Explorations:**
  - Plotted star rating distributions
  - Extracted Top N-grams (e.g., "très bien", "service client") to identify recurring themes early on.

*Speaking Note: "We started by heavily cleaning our dataset—removing noise and correcting spelling. This let us identify the most dominant terms like 'service client' right from the start."*

---

## Slide 4: Models & Machine Learning (1.5 min)
**Title:** Supervised & Unsupervised Modeling
- **Topic Modeling (LDA):**
  - Grouped reviews into 5 distinct topics (e.g., Claims, Pricing, Customer Service).
- **Word Embeddings (Word2Vec):**
  - Trained to find semantic similarities between words (e.g., "assurance" and "contrat").
  - Visualized high-dimensional relationships using PCA / t-SNE.
- **Supervised Learning:**
  - **Sentiment:** TF-IDF + Logistic Regression (Accurate & fast).
  - **Star Prediction:** Random Forest Classifier (1 to 5 stars).
  - **Category Detection:** Zero-Shot HuggingFace Pipeline (`distilbart-mnli-12-3`) requiring no labeled training data!

*Speaking Note: "For our modeling phase, we used LDA to dynamically extract topics, and trained Word2Vec embeddings to understand semantic relationships. For prediction, we compared classic TF-IDF Logistic Regression for sentiments against advanced Zero-Shot Transformers for categorizing reviews."*

---

## Slide 5: Model Comparison & Error Analysis
**Title:** Results & Error Analysis
| Model | Task | Accuracy / Result |
|-------|------|-------------------|
| TF-IDF + LR | Sentiment Classification | High accuracy, interpretable |
| TF-IDF + RF | Star Prediction (1-5) | Good baseline performance |
| DistilBART (Zero-Shot) | Topic Categorization | Highly adaptable, no training |

- **Where Models Struggle (Error Analysis):**
  - **Sarcasm:** Models fail to detect irony (e.g., "Bravo pour l'attente!").
  - **Short Texts:** 1-2 word reviews carry too little context for TF-IDF.
  - **Class Imbalance:** Skewed data towards positive ratings biased some standard predictions.

---

## Slide 6: Application Demo (2 min)
**Title:** Interactive Streamlit Dashboard
*(Insert Screenshot of your Streamlit App here)*

**Features we will demonstrate live:**
1. **Prediction App:** Enter a review -> models predict Stars, Sentiment, and Category.
2. **LIME Explanations:** Visualizing *why* the model made its decision (word weights).
3. **Insurer Analysis:** Compare average ratings and search reviews for specific insurers.
4. **RAG QA System:** Ask a question in natural language and retrieve exact context from the reviews.

*Speaking Note: "Now, the most important part: our live demonstration. As you can see on our Streamlit dashboard..." (Transition to screen recording of the app).*

---

## Slide 7: Conclusion (30 sec)
**Title:** Insights & Future Work
- **Key Takeaways:** 
  - Customer Service and Claims Processing drive the most negative sentiment.
  - Zero-shot LLMs are incredibly powerful for text classification with minimal setup.
- **Future Improvements:**
  - Integrate a heavier LLM (like GPT-4 or Llama-3) to handle sarcastic reviews better.
  - Train domain-specific word embeddings on a larger insurance dataset.

*Speaking Note: "To conclude, we successfully automated the extraction of insights from raw feedback. While classical models struggle with sarcasm, our hybrid approach provides a robust baseline for insurers to improve their services. Thank you!"*
