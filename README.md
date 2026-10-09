# DS 680 - Natural Language Processing

Homework assignments and exercises for DS 680.

## Assignments

### Module 2 - Tokenization, POS Tagging, and N-Grams

**Notebook:** `M2_Tokenization_POS_NGrams.ipynb`

Topics:
- Word and sentence tokenization with NLTK
- Text normalization
- Porter stemming
- Part-of-speech tagging
- Bigrams and trigrams
- Frequency distributions

### Module 6 - Sentiment Analysis and Text Classification

**Notebook:** `M6_Sentiment_Analysis.ipynb`

Topics:
- Text cleaning and preprocessing
- Duplicate detection and removal
- Sentiment classification using IMDb movie reviews
- TF-IDF feature extraction
- Logistic regression classification
- Feedforward neural networks using PyTorch
- Model training and validation
- Model evaluation using accuracy, precision, recall, and F1-score
- Confusion matrices and model comparison
- Overfitting and model checkpointing

## Environment Setup

The assignments were developed using Python 3.12, VS Code, and WSL Ubuntu.

### 1. Clone the Repository

```bash
git clone git@github.com:matthowarth26/ds_680_nlp_hw.git
cd ds_680_nlp_hw
```

### 2. Create and Activate a Virtual Environment

```bash
python3 -m venv .venv
source .venv/bin/activate
```

### 3. Install Dependencies

**Module 2: Tokenization, POS Tagging, and N-Grams**

```bash
python -m pip install nltk ipykernel
```

NLTK datasets and models may also need to be downloaded:

```python
import nltk

nltk.download("punkt")
nltk.download("punkt_tab")
nltk.download("averaged_perceptron_tagger_eng")
```

Depending on the installed NLTK version, the POS tagger may require `averaged_perceptron_tagger` instead.

**Module 6: Sentiment Analysis**

```bash
python -m pip install pandas numpy matplotlib scikit-learn torch ipykernel
```

PyTorch can run on the CPU, so a compatible NVIDIA GPU is not required.

### 4. Run the Notebooks

Open the repository in VS Code:

```bash
code .
```

Select the Python kernel associated with `.venv/bin/python` and open the notebook for the corresponding assignment.

For Module 6, download the IMDb movie review dataset (https://www.geeksforgeeks.org/nlp/dataset-for-sentiment-analysis/) and save it as:

`data/IMDB-Dataset.csv`

The dataset must contain the columns `review` and `sentiment`, with sentiment labels `positive` and `negative`.

Run the notebook cells sequentially to reproduce the preprocessing, training, and evaluation workflow.

## Repository Notes

- Each assignment is maintained in a separate Jupyter notebook.
- Datasets are excluded from GitHub and must be downloaded separately.
- Virtual environments and temporary Python files are excluded from version control.