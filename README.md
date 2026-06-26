Deployement Link:-https://shakesphere-hamlet-prediction-using-lstm-nrsz3flnlebnbxoqmqihz.streamlit.app/

# Shakespeare Hamlet Next Word Prediction using LSTM

An end-to-end Deep Learning project that predicts the next word in a sentence using an LSTM (Long Short-Term Memory) neural network trained on Shakespeare's *Hamlet* text from the NLTK Gutenberg corpus.

## 📌 Project Overview

This project demonstrates how Recurrent Neural Networks (RNNs), specifically LSTMs, can be used for Natural Language Processing (NLP) tasks such as next-word prediction.

The model learns language patterns from Shakespeare's *Hamlet* and predicts the most probable next word for a given input sequence.

---

## 🚀 Features

- Text preprocessing using NLTK
- Tokenization using Keras Tokenizer
- N-gram sequence generation
- Sequence padding
- LSTM-based language model
- Next-word prediction
- Trained model saving
- Tokenizer serialization using Pickle
- Streamlit web application for interactive prediction

---

## 🛠️ Tech Stack

- Python
- TensorFlow / Keras
- NLTK
- NumPy
- Pickle
- Streamlit

---

## 📂 Project Structure

```
Shakespeare-Hamlet-Prediction-using-LSTM/
│
├── app.py                     # Streamlit application
├── experiment.ipynb           # Model development notebook
├── hamlet.txt                 # Training text
├── next_word_lstm.keras       # Trained LSTM model
├── tokenizer.pkl              # Saved tokenizer
├── requirements.txt           # Project dependencies
├── README.md
```

---

## 📖 Dataset

The model is trained on **Shakespeare's Hamlet** available in the **NLTK Gutenberg Corpus**.

Download the dataset:

```python
import nltk

nltk.download('gutenberg')

from nltk.corpus import gutenberg

text = gutenberg.raw('shakespeare-hamlet.txt')
```

---

## ⚙️ Model Architecture

```
Input Layer
      │
Embedding Layer
(100-dimensional embeddings)
      │
LSTM (150 units)
      │
Dropout (0.2)
      │
LSTM (100 units)
      │
Dense Layer (Vocabulary Size)
      │
Softmax
      │
Predicted Next Word
```

---

## 🧠 Data Preprocessing

The following preprocessing steps are performed:

- Convert text to lowercase
- Tokenization
- Create n-gram sequences
- Pad sequences
- Split into input (X) and target (y)
- One-hot encode target words

Example:

```
Input Sentence:
To be or not to be

Generated Sequences:

To be
To be or
To be or not
To be or not to
To be or not to be
```

Training example:

```
Input:
To be or not

Target:
to
```

---

## 📊 Model Training

Loss Function:

```
Categorical Crossentropy
```

Optimizer:

```
Adam
```

Evaluation Metric:

```
Accuracy
```

---

## 💻 Installation

Clone the repository

```bash
git clone https://github.com/AravindKKrishna/Shakesphere-Hamlet-Prediction-using-LSTM.git
```

Move into the project directory

```bash
cd Shakesphere-Hamlet-Prediction-using-LSTM
```

Create a virtual environment

```bash
python -m venv venv
```

Activate the environment

Windows

```bash
venv\Scripts\activate
```

Linux / macOS

```bash
source venv/bin/activate
```

Install dependencies

```bash
pip install -r requirements.txt
```

---

## ▶️ Run the Streamlit App

```bash
streamlit run app.py
```

The application will open in your browser.

---

## 💡 Example

Input

```
To be or not
```

Predicted Output

```
to
```

---

## 📈 Future Improvements

- Train on larger Shakespeare corpus
- Use Bidirectional LSTM
- Add GRU comparison
- Integrate Attention Mechanism
- Implement Beam Search decoding
- Deploy on Streamlit Cloud
- Fine-tune using pretrained word embeddings (GloVe/Word2Vec)

---

## 🎯 Learning Outcomes

Through this project, I gained hands-on experience with:

- Natural Language Processing (NLP)
- Text preprocessing
- Tokenization
- Sequence generation
- Word embeddings
- LSTM networks
- Deep Learning with TensorFlow/Keras
- Model serialization
- Streamlit deployment

---

## 👨‍💻 Author

**Aravind K Krishna**

Computer Science Engineer | AI & Data Science Enthusiast

GitHub: https://github.com/AravindKKrishna

LinkedIn: *(Add your LinkedIn profile here)*

---

## ⭐ If you found this project useful, consider giving it a star!
