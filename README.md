# YouTube Comments Sentiment Analysis
This work was done by Muhammad Iskandar Java as a programmer and myself Ulima Inas Shabrina as a cat, i help meowing meow meow meow 🐈
The workflow includes scraping comments, pre-processing and labeling data, splitting datasets, training machine learning models, and evaluating their performance.

## 1. YouTube Comments Scraping

**Notebook:** `1_youtube_comments_scrapp.ipynb`

### Description

This notebook scrapes comments from YouTube videos and filters out empty comments.

### Key Sections

- **Scraping Comments:**
  - Uses the YouTube Data API to fetch comments.
  - Extracts relevant fields `comment text, author, and timestamp`.
  
- **Filtering Comments:**
  - Removes empty or irrelevant comments from the fetched data.

## 2. Labeling and Pre-processing

**Notebook:** `2_labeling_pre_process.ipynb`

### Description

Pre-processes the scraped YouTube comments and assigns labels for sentiment analysis.

### Key Sections

- **Reading Comments:**
  - Loads the comments dataset from a CSV file or other sources.
  - Ensures the data is in the correct format for further processing.
  
- **Labeling:**
  - Assigns sentiment labels (positive, negative, neutral) to each comment.
  - Automated labelling sentiment analysis.

## 3. Data Splitting

**Notebook:** `3_splitting.ipynb`

### Description

Splits the labeled data into training and testing datasets.

### Key Sections

- **Reading Labeled Data:**
  - Loads the pre-processed and labeled comments dataset.
  - Ensures the data is correctly labeled and formatted.
  
- **Splitting Data:**
  - Divides the dataset into training and test sets.

## 4. Class Label Counting

**Notebook:** `class_counter.ipynb`

### Description

Counts the frequency of each class label in the combined training and test datasets.

### Key Sections

- **Reading Data:**
  - Reads the combined training and test datasets.
  - Uses `pandas` to handle the data.
  
- **Counting Labels:**
  - Counts the frequency of each class label using `value_counts()`.
  - Prints the counts and the total number of samples.

## 5. Multinomial Naive Bayes (MNB) Model

**Notebook:** `MNB.ipynb`

### Description

Trains a Multinomial Naive Bayes (MNB) model for sentiment classification.

### Key Sections

- **Loading Data:**
  - Reads the training and test datasets.
  
- **Training Model:**
  - Trains a Multinomial Naive Bayes classifier on the training data.
  - Uses features term frequency-inverse document frequency (TF-IDF) vectors.
  
- **Evaluating Model:**
  - Evaluates the classifier's performance on the test data.
  - Prints metrics accuracy, precision, recall, and F1 score.

## 6. RoBERTa Model

**Notebook:** `roberta.ipynb`

### Description

Trains a RoBERTa model for sentiment classification.

### Key Sections

- **Tokenization:**
  - Tokenizes the input text using a pre-trained tokenizer from the `transformers` library.
  - Ensures the text is in the correct format for the RoBERTa model.
  
- **Training Model:**
  - Trains a RoBERTa model for sequence classification.
  - Uses training arguments learning rate, number of epochs, and evaluation strategy.
  
- **Evaluating Model:**
  - Evaluates the model's performance using metrics accuracy, F1 score, and precision.
