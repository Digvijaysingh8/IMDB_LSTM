# 🎬 IMDB Movie Review Sentiment Analysis Using LSTM

## 📌 Overview

This project uses Natural Language Processing (NLP) and Deep Learning to classify IMDB movie reviews as **positive or negative**. It uses an LSTM (Long Short-Term Memory) neural network built with TensorFlow and Keras to learn patterns in review text and predict sentiment.

## 🎯 Objectives

- Understand and preprocess textual data.
- Convert text into numerical sequences using tokenization.
- Apply padding to create fixed-length input sequences.
- Build and train an LSTM-based sentiment classification model.
- Predict sentiment for new movie reviews.

## 🛠️ Technologies Used

- Python
- Pandas
- Regular Expressions
- TensorFlow
- Keras
- Natural Language Processing (NLP)
- Deep Learning

## 📂 Dataset

The project uses a dataset containing **50,000 IMDB movie reviews** labeled as positive or negative.

Each review contains:
- `review`: The movie review text.
- `sentiment`: The sentiment label (`positive` or `negative`).

The dataset is loaded from `IMDB Dataset.csv`.

## ⚙️ Project Workflow

1. **Data Loading:** Load and explore the IMDB review dataset using Pandas.
2. **Text Preprocessing:** Remove HTML tags from review text using regular expressions.
3. **Tokenization:** Convert words into integer indexes using the Keras Tokenizer.
4. **Sequence Padding:** Pad or truncate reviews to a fixed length of 220 tokens.
5. **Label Encoding:** Convert positive sentiment to `1` and negative sentiment to `0`.
6. **Model Building:** Create an LSTM-based neural network.
7. **Model Training:** Train the model using binary cross-entropy loss.
8. **Sentiment Prediction:** Generate positive-class probabilities for new movie reviews.

## 🧠 Model Architecture

The model consists of the following layers:

| Layer | Configuration | Purpose |
|---|---|---|
| Embedding | 32 dimensions | Learns vector representations of tokens |
| LSTM | 50 units | Learns sequential patterns in text |
| Dense | 1 unit, Sigmoid | Predicts positive sentiment probability |

**Training configuration:**
- Vocabulary limit: 14,000 words
- Maximum sequence length: 220 tokens
- Batch size: 64
- Training epochs: 2

## 🔍 Prediction

The trained model returns a probability between `0` and `1`.

- Probability ≥ 0.5: Positive sentiment
- Probability < 0.5: Negative sentiment

The notebook demonstrates predictions on five custom movie reviews.

## 🚀 Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/YOUR_USERNAME/imdb-sentiment-analysis.git
cd imdb-sentiment-analysis
```

### 2. Install dependencies

```bash
pip install pandas numpy tensorflow jupyter
```

### 3. Add the dataset

Place `IMDB Dataset.csv` in the dataset directory expected by the notebook, or update the CSV path to match your local setup.

### 4. Run the notebook

Open Jupyter Notebook:

```bash
jupyter notebook
```

Then open and run `imdb.ipynb` from top to bottom.

## 📊 Results

The notebook's saved training outputs show accuracy increasing from approximately **71.35% to 88.43%** across two training epochs.

These figures represent training accuracy, not held-out test accuracy. A separate test-set evaluation is needed to establish how well the model generalizes to unseen reviews.

## 📚 Key Learnings

- Text preprocessing and HTML tag removal.
- Vocabulary creation and tokenization.
- Numerical representation of textual data.
- Sequence padding and truncation.
- Embedding layers and LSTM networks.
- Binary sentiment classification and probability-based prediction.

## 🔮 Future Improvements

- Implement a proper train/test split.
- Fit the tokenizer using training data only.
- Evaluate the model on unseen reviews.
- Add precision, recall, F1-score, and a confusion matrix.
- Experiment with different sequence lengths, embedding dimensions, and model architectures.
- Build a simple web interface for real-time sentiment prediction.

## 👨‍💻 Author

**Your Name**

Connect with me on [LinkedIn](YOUR_LINKEDIN_URL).

## 📄 Acknowledgements

This project uses Python's TensorFlow/Keras ecosystem for text preprocessing and deep learning. Refer to the original IMDB dataset source and its terms of use before redistributing the dataset.

- [IMDB Movie Review Dataset](https://ai.stanford.edu/~amaas/data/sentiment/)
- [Keras Documentation](https://keras.io/)
- [TensorFlow Documentation](https://www.tensorflow.org/)

