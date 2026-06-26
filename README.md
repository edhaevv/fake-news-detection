# 📰 Fake News Detection with RoBERTa

A fine-tuned **RoBERTa** model for binary classification of news articles as **Fake** or **Real**.

---

## 🧠 Model

- **Base model:** [`FacebookAI/roberta-base`](https://huggingface.co/FacebookAI/roberta-base)
- **Task:** Sequence Classification (Fake vs Real)
- **Framework:** HuggingFace Transformers + PyTorch

---

## 📦 Dataset

- **Source:** [Kaggle — Fake and Real News Dataset](https://www.kaggle.com/datasets/clmentbisaillon/fake-and-real-news-dataset)
- **Files:** `Fake.csv` and `True.csv`
- **Labels:** `0` = Fake, `1` = Real
- **Features used:** `text` only (title, subject, date dropped)

| Split      | Size  |
|------------|-------|
| Train      | 70%   |
| Validation | 15%   |
| Test       | 15%   |

---

## ⚙️ Training Details

| Parameter              | Value     |
|------------------------|-----------|
| Learning rate          | `2e-5`    |
| Batch size             | `16`      |
| Epochs                 | `1`       |
| Weight decay           | `0.01`    |
| Max token length       | `256`     |
| Mixed precision (fp16) | ✅        |
| Best model loaded      | ✅        |

---

## 🚀 How to Run

### 1. Clone the repo
```bash
git clone https://github.com/your-username/fake-news-detection.git
cd fake-news-detection
```

### 2. Install dependencies
```bash
pip install -r requirements.txt
```

### 3. Download the dataset
Get the dataset from [Kaggle](https://www.kaggle.com/datasets/clmentbisaillon/fake-and-real-news-dataset) and place `Fake.csv` and `True.csv` in `/content/` (or update the paths in the notebook).

### 4. Run the notebook
Open `Fake_news.ipynb` in Jupyter or Google Colab and run all cells.

---

## 📊 Evaluation

Model is evaluated using **accuracy** and a **confusion matrix** on the test set.

```
Labels: Fake (0) | Real (1)
```

---

## 📁 Project Structure

```
├── Fake_news.ipynb       # Main notebook
├── requirements.txt      # Python dependencies
├── .gitignore            # Ignored files
└── README.md             # This file
```

---

## 🛠️ Requirements

See `requirements.txt`. Main dependencies:

- `torch`
- `transformers`
- `datasets`
- `evaluate`
- `pandas`, `numpy`
- `matplotlib`, `seaborn`
- `scikit-learn`
