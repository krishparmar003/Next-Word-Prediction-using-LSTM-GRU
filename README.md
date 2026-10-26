# 🔮 Next Word Prediction using LSTM & GRU

A Natural Language Processing project that predicts the next word in a sentence using two recurrent neural network architectures: **LSTM (Long Short-Term Memory)** and **GRU (Gated Recurrent Unit)**. Both models are trained and compared in a single notebook, saved as `.h5` files, and served through **separate Streamlit apps**.

---

## 📌 Overview

Given a sequence of words, the model predicts the most likely next word. The project walks through the full pipeline:

1. Text preprocessing and tokenization
2. Creating n-gram input sequences and padding
3. Building and training the LSTM and GRU models
4. Evaluating and comparing both models
5. Saving the trained models as `.h5` files
6. Deploying each model through its own Streamlit app

---

## ✨ Features

- Two models, one problem: **LSTM** and **GRU** trained and compared side by side
- Complete experimentation in a single notebook (`experiments.ipynb`)
- Pre-trained models saved in `.h5` format, so there is no need to retrain
- Separate Streamlit apps for the LSTM and GRU models
- Simple, interactive UI: type a phrase, get the predicted next word

---

## 🧠 Models

| Model | Description |
|-------|-------------|
| **LSTM** | Uses input, forget and output gates to capture long-range dependencies in text |
| **GRU** | A lighter variant with fewer parameters (update and reset gates), usually faster to train |

Both models share the same general architecture: `Embedding → LSTM/GRU layer(s) → Dense (softmax)`.

---

## 📁 Project Structure

```
Next-Word-Prediction-using-LSTM-GRU/
│
├── experiments.ipynb        # Data prep, training & evaluation of both LSTM and GRU
├── app_lstm.py              # Streamlit app for the LSTM model
├── app_gru.py               # Streamlit app for the GRU model
├── lstm_model.h5            # Saved LSTM model
├── gru_model.h5             # Saved GRU model
├── tokenizer.pickle         # Saved tokenizer (if used)
├── requirements.txt         # Python dependencies
└── README.md
```

> ⚠️ **Note:** File names above are placeholders. Rename them to match the actual files in your repo.

---

## 🚀 Getting Started

### Prerequisites

- **Python 3.10**
- `pip`
- Git

### 1. Clone the repository

```bash
git clone https://github.com/krishparmar003/Next-Word-Prediction-using-LSTM-GRU.git
cd Next-Word-Prediction-using-LSTM-GRU
```

### 2. Create a virtual environment

```bash
py -3.10 -m venv myenv
```

### 3. Activate the virtual environment

**Windows (Command Prompt):**
```bash
myenv\Scripts\activate
```

**Windows (PowerShell):**
```powershell
myenv\Scripts\Activate.ps1
```

**macOS / Linux:**
```bash
source myenv/bin/activate
```

### 4. Install dependencies

```bash
pip install -r requirements.txt
```

---

## ▶️ Usage

### Option A: Explore the experiments

Open the notebook to see data preprocessing, model building, training and comparison of both LSTM and GRU:

```bash
jupyter notebook experiments.ipynb
```

> Both models are trained in this notebook and their `.h5` files are saved at the end.

### Option B: Run the Streamlit apps

Each model has its own app. Run whichever you want to try:

**LSTM app**
```bash
streamlit run app_lstm.py
```

**GRU app**
```bash
streamlit run app_gru.py
```

The app opens in your browser at `http://localhost:8501`. Enter a phrase and click **Predict** to get the next word.

> To run both apps at the same time, use a different port for the second one:
> ```bash
> streamlit run app_gru.py --server.port 8502
> ```

---

## 💡 Example

| Input | Predicted Next Word |
|-------|---------------------|
| `to be or not to` | `be` |
| `the quick brown` | `fox` |

> Replace these with real outputs from your models.

---

## 🛠️ Tech Stack

- **Language:** Python 3.10
- **Deep Learning:** TensorFlow / Keras
- **NLP:** Keras Tokenizer, sequence padding
- **Web App:** Streamlit
- **Notebook:** Jupyter
- **Libraries:** NumPy, Pandas

---

## 📊 LSTM vs GRU

| Aspect | LSTM | GRU |
|--------|------|-----|
| Gates | 3 (input, forget, output) | 2 (update, reset) |
| Parameters | More | Fewer |
| Training speed | Slower | Faster |
| Accuracy | *add your result* | *add your result* |

---

## 🔮 Future Improvements

- Show top-k predictions with probabilities
- Train on a larger and more diverse corpus
- Add Bidirectional LSTM/GRU and attention
- Combine both models into a single Streamlit app with a model selector
- Deploy on Streamlit Community Cloud

---

## 🤝 Contributing

Contributions, issues and feature requests are welcome. Feel free to open an issue or submit a pull request.

---

## 👤 Author

**Krish Parmar**
- GitHub: [@krishparmar003](https://github.com/krishparmar003)

---

⭐ If you found this project useful, consider giving it a star!
