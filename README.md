# 🧠 AI Fake News Detector (NLP + Machine Learning)

An interactive **AI-powered Fake News Detection System** built using **Python, Natural Language Processing (NLP), and Machine Learning**.
The project allows a user to enter a **news headline or full news article**, and the system predicts whether the news is **REAL or FAKE**.

This project focuses on solving a real-world problem:
👉 Detecting misinformation and misleading news spreading through social media and online platforms.

---

## 📌 Project Motivation

With the rapid growth of social media and AI-generated content, misinformation and fake news are increasing rapidly.
This project demonstrates how Machine Learning and NLP techniques can help identify unreliable or misleading news content based on linguistic patterns.

The model does **not directly verify facts from the internet**.
Instead, it classifies credibility using writing style, word patterns, and textual features.

---

## 🚀 Features

* Accepts **user input** (headline or full news article)
* Cleans and preprocesses text automatically
* Converts text into numerical features using **TF-IDF**
* Predicts whether news is:

  * 🟢 REAL NEWS
  * 🔴 FAKE NEWS
* Displays prediction with confidence score
* Runs interactively inside Jupyter Notebook

---

## 🧠 Technologies Used

* Python
* Jupyter Notebook
* Pandas
* NumPy
* Scikit-learn
* NLTK (Natural Language Toolkit)
* Matplotlib & Seaborn (visualization)

---

## 📂 Dataset

Dataset used:

**Fake and Real News Dataset (Kaggle)**
https://www.kaggle.com/datasets/clmentbisaillon/fake-and-real-news-dataset

The dataset contains two files:

* `Fake.csv` → Fake news articles
* `True.csv` → Real news articles

---

## ⚙️ Installation & Setup

### 1️⃣ Clone the Repository

```bash
git clone https://github.com/your-username/fake-news-detector.git
cd fake-news-detector
```

### 2️⃣ Install Required Libraries

```bash
pip install pandas numpy scikit-learn matplotlib seaborn nltk
```

### 3️⃣ Download Dataset

Download from Kaggle and place inside the project folder:

```
project/
│── Fake.csv
│── True.csv
│── fake_news_detection.ipynb
```

### 4️⃣ Run the Notebook

```bash
jupyter notebook
```

Open `fake_news_detection.ipynb`

Then run:

```
Kernel → Restart & Run All
```

---

## 🧪 How to Use

After running all cells, the notebook will ask:

```
Enter a news headline or full news script:
```

Example:

```
NASA confirms humans will live on Mars by 2027
```

Output:

```
Prediction: 🔴 FAKE NEWS (Confidence: 92.4%)
```

To exit:

```
exit
```

---

## 🏗️ Machine Learning Workflow

1. Data loading
2. Text preprocessing
3. Stopword removal
4. Train-test split
5. TF-IDF vectorization
6. Logistic Regression model training
7. Evaluation using:

   * Accuracy score
   * Classification report
   * Confusion matrix
8. Interactive user prediction

---

## 📊 Model Used

**Logistic Regression Classifier**

Why?

* Fast
* Efficient for text classification
* Performs well on NLP tasks
* Interpretable

---

## ⚠️ Limitations

* The model detects writing patterns, not factual truth.
* It cannot verify live news from the internet.
* Very short sentences may reduce accuracy.
* Satirical news may be misclassified.

---

## 🔮 Future Improvements

* Web interface (Flask/React website)
* Deep learning model (LSTM/BERT)
* API-based fact checking
* Multilingual support
* Fake image / deepfake detection

---

## 🎯 Learning Outcomes

Through this project I learned:

* Natural Language Processing (NLP)
* Text preprocessing techniques
* Feature extraction (TF-IDF)
* Machine Learning model training
* Model evaluation
* Interactive AI system design

---

## 👨‍💻 Author

**Ankit Kumar Panda**

---

## ⭐ If you found this project useful

Please consider giving the repository a **star ⭐** on GitHub!
