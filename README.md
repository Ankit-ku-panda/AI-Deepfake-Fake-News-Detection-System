# AI Fake News Detection System

A text-classification project that uses Natural Language Processing, TF-IDF feature extraction and Logistic Regression to classify a news headline or article as real or fake.

[![Python](https://img.shields.io/badge/Python-3.10%2B-3776AB?logo=python&logoColor=white)](https://www.python.org/)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?logo=jupyter&logoColor=white)](https://jupyter.org/)
[![scikit-learn](https://img.shields.io/badge/scikit--learn-Logistic%20Regression-F7931E?logo=scikitlearn&logoColor=white)](https://scikit-learn.org/)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

## Overview

This project demonstrates a machine-learning workflow for detecting linguistic patterns associated with real and fake news articles.

The notebook:

1. Loads labelled real and fake news datasets.
2. Combines article titles and body text.
3. Cleans and normalizes the text.
4. Removes English stop words.
5. Converts text into TF-IDF features.
6. Trains a Logistic Regression classifier.
7. Evaluates the classifier.
8. accepts user-entered news text for interactive prediction.

The model does not browse the internet or verify facts against trusted sources. It predicts labels from patterns learned from the training dataset.

## Scope Clarification

The repository name contains “Deepfake,” but the current implementation only analyzes written news content.

It does not currently process:

- Images
- Video
- Audio
- Faces
- Voice recordings
- AI-generated media
- Deepfake files

Deepfake detection is listed as a possible future extension.

## Features

- Real-versus-fake binary text classification
- News-title and article-body preprocessing
- URL and punctuation removal
- English stop-word filtering
- TF-IDF vectorization with up to 5,000 features
- Logistic Regression classification
- Accuracy and classification-report output
- Confusion-matrix visualization
- Interactive headline or article prediction
- Reproducible train/test split using `random_state=42`

## Model Labels

| Label | Meaning |
|---:|---|
| `0` | Fake news |
| `1` | Real news |

Interactive predictions are displayed as:

```text
🟢 This looks like REAL NEWS
```

or:

```text
🔴 This looks like FAKE / MISINFORMATION
```

## Machine-Learning Workflow

```text
Fake.csv + True.csv
        ↓
Assign labels
        ↓
Combine title and article text
        ↓
Clean and normalize text
        ↓
Train/test split
        ↓
TF-IDF vectorization
        ↓
Logistic Regression training
        ↓
Evaluation and interactive prediction
```

## Text Preprocessing

The `clean_text()` function:

- Converts text to lowercase
- Removes URLs
- Removes numbers and punctuation
- Keeps English alphabetic characters
- Splits text into words
- Removes NLTK English stop words
- Rejoins the remaining words

Example:

```text
Before: Breaking: Visit https://example.com for the FULL story!
After:  breaking visit full story
```

## Tech Stack

- Python
- Jupyter Notebook
- pandas
- NumPy
- NLTK
- scikit-learn
- Matplotlib
- Seaborn
- Regular expressions

## Dataset

The project uses the **Fake and Real News Dataset**, commonly distributed through Kaggle:

- `Fake.csv` — articles labelled as fake
- `True.csv` — articles labelled as real

The repository currently includes both CSV files.

Expected columns include:

| Column | Description |
|---|---|
| `title` | News article title |
| `text` | Article body |
| `subject` | Dataset subject category |
| `date` | Article date |

Only `title` and `text` are used by the current model.

Dataset source:

[Fake and Real News Dataset on Kaggle](https://www.kaggle.com/datasets/clmentbisaillon/fake-and-real-news-dataset)

Review and follow the dataset’s terms before redistributing or using it commercially.

## Repository Structure

```text
AI-Deepfake-Fake-News-Detection-System/
├── Fake.csv
├── True.csv
├── fake_news_detection.ipynb
├── LICENSE
└── README.md
```

## Installation

Clone the repository:

```bash
git clone https://github.com/Ankit-ku-panda/AI-Deepfake-Fake-News-Detection-System.git
cd AI-Deepfake-Fake-News-Detection-System
```

Create a virtual environment:

### Windows PowerShell

```powershell
python -m venv .venv
.venv\Scripts\Activate.ps1
```

### Linux or macOS

```bash
python3 -m venv .venv
source .venv/bin/activate
```

Install the dependencies:

```bash
python -m pip install --upgrade pip
pip install jupyter pandas numpy nltk scikit-learn matplotlib seaborn
```

## Run the Project

Start Jupyter Notebook:

```bash
jupyter notebook
```

Open:

```text
fake_news_detection.ipynb
```

Run all cells in order.

The first cell downloads the NLTK English stop-word dataset:

```python
nltk.download("stopwords")
```

An internet connection may be required the first time this resource is downloaded.

## Interactive Prediction

After training, the notebook displays:

```text
Enter a news headline or full news script (or type 'exit'):
```

Enter a headline or article:

```text
A news headline or full article goes here
```

The notebook returns its predicted class.

Enter:

```text
exit
```

to stop the loop.

## Evaluation

The notebook reports:

- Accuracy
- Precision
- Recall
- F1-score
- Support
- Confusion matrix

Accuracy should not be considered alone. Check the classification report and confusion matrix to understand false-positive and false-negative behavior.

## Important Limitations

- The model identifies learned writing patterns; it does not establish factual truth.
- It does not check trusted news sources or fact-checking databases.
- It does not inspect publication reputation, author identity or supporting evidence.
- Dataset-specific language may make evaluation scores appear stronger than real-world performance.
- The datasets may contain source, topic or date biases.
- New events and writing styles may differ from the training data.
- Very short headlines may not provide enough information.
- Satire, opinion pieces and partially true claims may be misclassified.
- AI-generated text may behave differently from the original dataset.
- The current output does not include a confidence score.
- A prediction must not be used as the sole basis for moderation, censorship or legal action.

## Responsible Use

Use this project for:

- Machine-learning education
- NLP experimentation
- Misinformation research
- Defensive content-analysis prototypes

Before accepting a prediction, independently verify the claim using reliable sources and professional fact-checking practices.

## Future Improvements

- Display `predict_proba()` confidence values
- Add cross-validation
- Add model calibration
- Add hyperparameter tuning
- Save and reload the trained vectorizer and model
- Add source and publication metadata
- Add explainable feature importance
- Add multilingual text processing
- Add a Flask, FastAPI or Streamlit interface
- Integrate reputable fact-checking APIs
- Evaluate transformer models such as BERT
- Add image, audio and video models for actual deepfake detection
- Add automated tests and continuous integration

## Contributing

Contributions are welcome.

1. Fork the repository.
2. Create a branch:

   ```bash
   git checkout -b feature/your-feature
   ```

3. Commit your changes:

   ```bash
   git commit -m "Add your feature"
   ```

4. Push the branch:

   ```bash
   git push origin feature/your-feature
   ```

5. Open a pull request.

For bugs and suggestions, use the repository’s [Issues page](https://github.com/Ankit-ku-panda/AI-Deepfake-Fake-News-Detection-System/issues).

## Author

**Ankit Kumar Panda**

- GitHub: [Ankit-ku-panda](https://github.com/Ankit-ku-panda)
- Repository: [AI-Deepfake-Fake-News-Detection-System](https://github.com/Ankit-ku-panda/AI-Deepfake-Fake-News-Detection-System)

## License

The source code in this project is distributed under the [MIT License](LICENSE).

The included datasets remain subject to their original source terms and are not relicensed by the project’s MIT License.

---

If this project helped you, consider giving the repository a star.
