# ordinalEncoding
# 📊 Ordinal Encoding in Machine Learning

### 🚀 Converting Categorical Data into Numerical Values

![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python)
![Machine Learning](https://img.shields.io/badge/Domain-Machine%20Learning-orange)
![Scikit-learn](https://img.shields.io/badge/Library-Scikit--learn-yellow?logo=scikitlearn)
![Status](https://img.shields.io/badge/Status-Completed-success)

## 📌 About the Project

This project demonstrates **Ordinal Encoding**, a categorical data preprocessing technique used in Machine Learning.

Ordinal Encoding converts categorical values into numerical values while preserving their meaningful order. It is useful when working with features that have a natural ranking, such as education levels, product sizes, and satisfaction ratings.

The project uses Python and the `OrdinalEncoder` class from the Scikit-learn library to transform categorical data into numerical form.

## 🎯 Objectives

* Understand the concept of Ordinal Encoding.
* Convert categorical data into numerical values.
* Learn how to use `OrdinalEncoder` from Scikit-learn.
* Preserve the order of categorical values.
* Prepare data for Machine Learning models.
* Understand the importance of data preprocessing.

## 🛠️ Technologies Used

* **Python** — Programming language.
* **Pandas** — Data manipulation and analysis.
* **NumPy** — Numerical operations.
* **Scikit-learn** — Machine Learning and data preprocessing.
* **Jupyter Notebook / VS Code** — Development environment.

## 📖 What Is Ordinal Encoding?

Ordinal Encoding is a technique that assigns numerical values to categorical data according to a predefined order.

For example:

| Education Level | Encoded Value |
| --------------- | ------------: |
| High School     |             0 |
| Diploma         |             1 |
| Bachelor's      |             2 |
| Master's        |             3 |
| PhD             |             4 |

The numerical values represent the ranking of the categories.

**Note:** The order shown above is an example. The encoding order should be selected according to the meaning of the data and the requirements of the project.

## 💻 Installation

### Step 1: Install Python

Download and install Python if it is not already installed.

### Step 2: Install Required Libraries

Open your VS Code terminal and execute:

```bash
pip install pandas numpy scikit-learn jupyter
```

### Step 3: Import the Required Libraries

```python
import pandas as pd
from sklearn.preprocessing import OrdinalEncoder
```

## ⚙️ Implementation

### Example: Encoding Education Levels

```python
import pandas as pd
from sklearn.preprocessing import OrdinalEncoder

# Create sample dataset
df = pd.DataFrame({
    'Education': [
        'High School',
        "Bachelor's",
        "Master's",
        'PhD',
        'Diploma'
    ]
})

# Define the category order
education_order = [
    'High School',
    'Diploma',
    "Bachelor's",
    "Master's",
    'PhD'
]

# Create the encoder
oe = OrdinalEncoder(
    categories=[education_order]
)

# Apply ordinal encoding
df['Education_Encoded'] = oe.fit_transform(
    df[['Education']]
).astype(int)

# Display the result
print(df)
```

## 📤 Expected Output

```text
      Education  Education_Encoded
0   High School                  0
1    Bachelor's                  2
2      Master's                  3
3            PhD                  4
4       Diploma                  1
```

## 🔍 How It Works

1. **Create the dataset:** Store categorical education values in a Pandas DataFrame.
2. **Define category order:** Specify the ranking of education levels.
3. **Initialize the encoder:** Create an `OrdinalEncoder` object.
4. **Transform the data:** Convert categorical values into numerical values.
5. **Display the output:** View the original and encoded values.

## 🌟 Advantages of Ordinal Encoding

* Converts categorical data into numerical form.
* Preserves a predefined category order.
* Easy to implement using Scikit-learn.
* Useful for ordered categorical features.
* Helps prepare categorical data for Machine Learning algorithms.

## ⚠️ Limitations

* Incorrect category ordering can produce misleading representations.
* Numerical values may imply equal distances between categories, even when that is not meaningful.
* It is generally unsuitable for nominal categories with no natural order.
* Unknown categories can cause errors unless handled appropriately.

## 📂 Project Structure

```text
Ordinal-Encoding/
│
├── README.md
└── customer.csv
├── ord.ipynb
├── ord2.ipynb
├── practiceor.csv
```

## 📚 Applications

Ordinal Encoding can be used for:

* Education levels.
* Product sizes (Small, Medium, Large).
* Customer satisfaction (Low, Medium, High).
* Customer ratings.
* Risk categories (Low, Moderate, High).
* Experience levels (Beginner, Intermediate, Advanced).

## 🔗 References

* [Scikit-learn Official Documentation](https://scikit-learn.org/stable/modules/generated/sklearn.preprocessing.OrdinalEncoder.html)
* [Pandas Official Documentation](https://pandas.pydata.org/docs/)
* [Python Official Website](https://www.python.org/)

## 👨‍💻 Author

**Kaushal Prasad Yadav**

Machine Learning Learner | Python Programmer

Interested in Data Science, Machine Learning, and Data Preprocessing.

---

⭐ **If you find this project useful, consider giving the repository a star!**

📌 *This project is created for learning and practicing categorical data preprocessing in Machine Learning.*
