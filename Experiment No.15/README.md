# Experiment 15 — Text Data Preprocessing and NLP Techniques in Python

##**Name:** Jai Pratap
##**PRN:** 25070123056
**Branch:** ENTC A3

---

## Aim

To study and apply preprocessing techniques and Natural Language Processing (NLP) methods for analyzing text data.

---

## Tools & Libraries

| Tool | Purpose |
|---|---|
| Python 3.x | Core programming language |
| Google Colab / Jupyter Notebook | Development environment |
| NLTK | Natural language processing operations |
| Pandas | Data manipulation and structuring |
| NumPy | Numerical operations |

---

## Theory

### What is Text Data?

Text data is unstructured information expressed as words, sentences, or documents. Unlike numerical data, it has no predefined format — making it significantly more complex to analyze. Common sources include emails, social media posts, product reviews, news articles, and chat conversations.

Since computers cannot inherently understand human language, text must first be cleaned and converted into a structured form before any analysis or model building can take place. This process is called **text preprocessing**.

---

## Part 1 — Text Preprocessing Techniques

Text preprocessing transforms raw, messy text into a clean and consistent format, improving the accuracy and efficiency of downstream analysis.

---

### 1. Text Cleaning
The first step in any preprocessing pipeline. Removes elements that add noise without contributing meaning — punctuation marks, special characters (`@`, `#`, `$`), extra whitespace, and irrelevant symbols. The result is leaner, more readable text.

---

### 2. Lowercasing
Converts all text to lowercase to enforce uniformity across the dataset.

> `"Data Science"` → `"data science"`

Without this step, `"Data"` and `"data"` would be treated as entirely different tokens, causing duplication and skewed analysis.

---

### 3. Tokenization
Breaks text into smaller units called **tokens** — typically individual words or sentences.

> `"Natural language processing is useful"` → `["Natural", "language", "processing", "is", "useful"]`

Tokenization allows each component of a text to be analyzed independently.

---

### 4. Stop Word Removal
Stop words are high-frequency words that carry little meaningful information — such as *is*, *the*, *and*, *in*, and *of*. Removing them reduces dataset size, speeds up processing, and keeps the focus on content-bearing words.

---

### 5. Stemming
Reduces words to their root form by stripping suffixes. Fast and straightforward, though the output is not always a grammatically valid word.

| Word | Stem |
|---|---|
| playing | play |
| running | run |
| studies | studi |

---

### 6. Lemmatization
Converts words to their base dictionary form (lemma) by considering the word's meaning and grammatical context. More accurate than stemming and always produces valid words — better suited for advanced NLP tasks.

| Word | Lemma |
|---|---|
| running | run |
| better | good |
| studies | study |

---

## Part 2 — NLP Techniques

Natural Language Processing (NLP) is a branch of Artificial Intelligence that enables computers to understand, interpret, and derive meaning from human language.

---

### 1. Tokenization
Also a foundational NLP step — breaking large bodies of text into manageable units for further processing and analysis.

---

### 2. Part-of-Speech (POS) Tagging
Identifies the grammatical role each word plays within a sentence — noun, verb, adjective, adverb, and so on.

**Example:** `"Python is powerful"`

| Word | POS Tag |
|---|---|
| Python | Noun |
| is | Verb |
| powerful | Adjective |

POS tagging helps models understand sentence structure and linguistic meaning.

---

### 3. Named Entity Recognition (NER)
Detects and classifies real-world entities mentioned in text — such as people, locations, organizations, and dates.

**Example:** `"Elon Musk founded SpaceX."`

| Entity | Type |
|---|---|
| Elon Musk | Person |
| SpaceX | Organization |

NER is widely used in information extraction and automated data organization.

---

### 4. Sentiment Analysis
Determines the emotional tone or opinion expressed in a piece of text, classifying it as positive, negative, or neutral.

> Review: *"This phone is excellent."* → **Sentiment: Positive**

Commonly applied to customer feedback analysis and social media monitoring.

---

### 5. Text Vectorization
Converts text into numerical representations that machine learning algorithms can process.

| Technique | Description |
|---|---|
| **Bag of Words (BoW)** | Represents text by word frequency counts |
| **TF-IDF** | Weighs words by frequency relative to their uniqueness across documents |

Both approaches transform text into numeric vectors, making it compatible with computational models.

---

## Applications of NLP

NLP powers a wide range of real-world systems, including chatbots and virtual assistants, machine translation tools, spam detection filters, sentiment analysis platforms, search engines, and recommendation systems.

---

## Conclusion

Text preprocessing and NLP techniques form the backbone of any intelligent text-based application. Preprocessing cleans and structures raw language data, while NLP techniques extract meaning, patterns, and insight from it. Together, they enable computers to process human language reliably — driving everything from search engines to conversational AI.
