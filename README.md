# Resume Classifier Web App

This project is a **Flask-based web application** that automatically classifies resumes into predefined job categories using a machine learning model trained on resume text data.

## 🚀 Features

* Upload and analyze single or multiple resumes in `.pdf` or `.txt` format.
* Clean and preprocess the resume content automatically.
* Predicts the resume category using a trained classifier.
* Supports 25 job categories, including **Data Science**, **Java Developer**, **HR**, **Mechanical Engineer**, and more.

## 🧠 Model

The app uses:

* `tfidf.pkl`: TF-IDF vectorizer to convert resume text into numerical features.
* `clf.pkl`: Trained classification model (likely a RandomForest, SVM, or similar) to predict resume categories.

## 📂 Supported Categories

```text
Advocate, Arts, Automation Testing, Blockchain, Business Analyst, Civil Engineer,
Data Science, Database, DevOps Engineer, DotNet Developer, ETL Developer,
Electrical Engineering, HR, Hadoop, Health and Fitness, Java Developer,
Mechanical Engineer, Network Security Engineer, Operations Manager, PMO,
Python Developer, SAP Developer, Sales, Testing, Web Designing
```

## 🖥️ Tech Stack

* Python
* Flask
* Scikit-learn (for ML)
* NLTK (for text preprocessing)
* PyPDF2 (for reading PDF files)
* HTML + Jinja2 (for templates)

## 📦 Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/your-username/resume-classifier-app.git
   cd resume-classifier-app
   ```

2. Create a virtual environment and activate it:

   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. Install dependencies:

   ```bash
   pip install -r requirements.txt
   ```

4. Place `clf.pkl` and `tfidf.pkl` in the project root (same directory as `app.py`).

5. Run the app:

   ```bash
   python app.py
   ```

6. Open your browser and visit `http://127.0.0.1:5000`.

## 📝 How It Works

* Resume files are uploaded via the home page.
* Files are read (PDFs via `PyPDF2`), and text is cleaned with NLTK.
* Text is transformed using the TF-IDF vectorizer.
* The classifier predicts a category for each resume.
* Results are displayed on a separate result page.

## 📄 File Structure

```
resume-classifier-app/
│
├── app.py              # Main Flask application
├── clf.pkl             # Trained classifier
├── tfidf.pkl           # TF-IDF vectorizer
├── templates/
│   ├── index.html      # Upload page
│   └── result.html     # Result display page
└── static/             #  for styling assets
```

## ✅ To-Do / Enhancements

* Add a frontend design (CSS/styling improvements).
* Include drag-and-drop support for uploads.
* Deploy on Heroku, Render, or AWS.

## 👩‍💻 Author

**Daya M P**

---

