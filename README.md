# Education counselling
 
## Project Structure 
Education_counselling/
│
├── mlmodel/
│   ├── model.py           # Model training and saving
│   ├── career.csv         # Dataset used for training
│   └── career.pkl         # Trained ML model (saved)
│
├── templates/             # Frontend HTML templates
│   ├── index.html
│   ├── login.html
│   ├── register.html
│   └── result.html
│
├── static/                # CSS, images
│   └── style.css
│
├── app.py                 # Flask web app backend
└── requirements.txt       # Python dependencies


---

##  Tech Stack Used (ML & Python)

| Component                    | Description                                                                 |
| ---------------------------- | --------------------------------------------------------------------------- |
| **Python**                   | Main programming language                                                   |
| **Pandas**                   | Used for loading and preprocessing tabular data (`read_csv`, `.iloc`, etc.) |
| **Scikit-learn (`sklearn`)** | Machine learning library used for:                                          |

* Label encoding
* Data splitting
* Model training (`LogisticRegression`, `RandomForestClassifier`, `DecisionTreeClassifier`) |
  \| **Pickle** | Used to save and load the trained model |
  \| **Streamlit** (outside this folder) | For deployment as a web app |

---

##  ML Features Used

From the file [`model.py`](https://github.com/Rhitwika1/Education_counselling/blob/main/mlmodel/model.py):

### ➤ Input Features:

These are extracted from the CSV file `career.csv` and passed to the model:

* **Class** (likely 10 or 12)
* **Stream** (e.g., Science, Arts, Commerce)
* **Gender**
* **Interests**
* **Marks (percentage)**

You are using `LabelEncoder` to convert categorical data like interests, stream, and gender into numerical form.

---

### ➤ Output:

The trained model predicts the **best-fit stream/career option** for the student — saved in a variable called `career` or `prediction`.

---

## ML Models Trained

In `model.py`, these models are being trained and evaluated:

1. **Logistic Regression**
2. **Random Forest Classifier**
3. **Decision Tree Classifier**

Accuracy is compared across models, and one model is saved as `career.pkl`.

---

## Deployment-Ready Format

Once trained, the model is saved using `pickle.dump()` so it can be loaded in your Streamlit app.

---


