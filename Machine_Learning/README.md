# 🤖 Machine Learning

> Machine Learning is a branch of artificial intelligence focused on building systems that **learn from data** to make predictions or decisions — without being explicitly programmed for every task.

---

## 📚 Table of Contents

- [Learning Process](#️-learning-process)
- [Types of Machine Learning](#-types-of-machine-learning)
  - [1. Supervised Learning](#1-supervised-learning-labeled-data)
  - [2. Unsupervised Learning](#2-unsupervised-learning-no-labels)
  - [3. Reinforcement Learning](#3-reinforcement-learning-reward-signals)
  - [4. Semi / Self-Supervised Learning](#4-semi--self-supervised-learning-hybrid)
- [Tools](#️-tools)

---

## ⚙️ Learning Process

### 1. Data Preprocessing

Before feeding data to a model, it needs to be cleaned and prepared.

| Step | Description |
| ------ | ------------- |
| Import | Load raw data from CSV, DB, API, etc. |
| Clean | Handle missing values, remove duplicates |
| Split | Divide into **training set** and **test set** |

**Key concepts:**

- `Matrix of features` — the input columns (X)
- `Dependent Variable vector` — the output column (y)

#### Feature Scaling

> Always applied **per column**, never across rows.

Two main techniques:

**Normalization** — rescales values to `[0, 1]`

$$X_{norm} = \frac{X - X_{min}}{X_{max} - X_{min}}$$

Use when: data doesn't follow a normal distribution (e.g. image pixel values).

**Standardization** — rescales values to roughly `[-3, +3]`

$$X_{std} = \frac{X - \mu}{\sigma}$$

Use when: data follows a normal distribution, or when outliers are present. More robust than normalization in most cases.

---

### 2. Modelling

1. **Build** — choose an algorithm
2. **Train** — fit the model on training data
3. **Predict** — run the model on new/unseen data

---

### 3. Evaluation

1. Calculate **performance metrics** (accuracy, RMSE, F1, etc.)
2. Make a **verdict** — is the model good enough? overfit? underfit?

---

## 🧠 Types of Machine Learning

---

### 1. Supervised Learning (labeled data)

> The training data comes with **labels** — correct answers that guide the model. Like a teacher grading homework.

The model learns by comparing its predictions to the correct answers and adjusting itself to minimize mistakes.

#### i. Classification — predicting a *category*

Assigns input to one of several discrete categories.

- **Binary** — two classes (spam / not spam)
- **Multi-class** — many classes (handwritten digits 0–9)

**Examples:** Fraud detection, disease diagnosis, image recognition

#### ii. Regression — predicting a *continuous number*

Predicts a numerical output value on a continuous scale.

**Examples:** House price prediction, weather forecasting, sales forecasting

#### Regression Algorithms

| # | Algorithm |
| --- | ----------- |
| 1 | Simple Linear Regression |
| 2 | Multiple Linear Regression |
| 3 | Polynomial Regression |
| 4 | Support Vector Regression (SVR) |
| 5 | Decision Tree Regression |
| 6 | Random Forest Regression |

**Other common supervised algorithms:**
Linear Regression, Logistic Regression, Decision Trees, Random Forests, SVM, Neural Networks

---

### 2. Unsupervised Learning (no labels)

> No labels at all — the model finds hidden structure in data entirely on its own. Like organizing a library with no catalog.

#### Clustering

Groups similar data points without knowing the groups in advance.

**Examples:** Customer segmentation, document grouping

#### Dimensionality Reduction

Compresses data while preserving important information.

**Example algorithms:** PCA (Principal Component Analysis), Autoencoders

#### Association Rules

Finds things that frequently appear together.

**Example:** People who buy bread often also buy butter.

**Common algorithms:** K-Means, DBSCAN, PCA, Autoencoders

---

### 3. Reinforcement Learning (reward signals)

> No dataset at all. An **agent** interacts with an **environment**, takes actions, and receives **rewards or penalties**. The goal is learning a **policy** that maximizes cumulative reward over time.

Think of it like training a dog — reward good behavior, discourage bad behavior.

**Examples:** Game-playing AI (Chess, Go), robotics, self-driving cars

---

### 4. Semi / Self-Supervised Learning (hybrid)

**Semi-supervised** — small amount of labeled data + large amount of unlabeled data. The model uses labeled examples to bootstrap, then applies what it learned to unlabeled data. Useful because labeling data is expensive and time-consuming.

**Self-supervised** — the model creates its *own* labels from raw data. For example, hiding a word in a sentence and training itself to predict the missing word. This is what powers modern LLMs like GPT and BERT — they train on the entire internet without human annotation.

---

## 🛠️ Tools

| Library | Purpose |
| --------- | --------- |
| `NumPy` | Numerical computing, arrays, matrices |
| `Pandas` | Data manipulation and analysis |
| `Matplotlib` | Data visualization and plotting |
| `Scikit-learn` | ML algorithms, preprocessing, evaluation |

---

## 📝 Notes

 > **Feature Scaling**

- **Apply**

  - always applied to columns

- **Don't Apply**

  - never applied to across columns (not applied to data inside row)

  - No need to apply feature scaling in multiple regression

  - when dependent variable takes binary values like 0 & 1 - becaus they are already in range

> **Support Vector Regression**

**The Rule to Remember**

StandardScaler  →  needs 2D input for both X and y

SVR.fit()       →  needs 1D for y specifically

X  →  always 2D  →  shape (n_samples, n_features)

y  →  always 1D  →  shape (n_samples,)

- `SVR.fit()` expects y to be a 1D array:

## 🔗 Links

> Datasets to practice - [Machine Learning Repository](https://archive.ics.uci.edu/)
