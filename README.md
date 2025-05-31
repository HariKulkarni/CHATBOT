# 🏥 Disease Prediction and Hospital Recommendation Chatbot

This is a Flask-based AI chatbot system that helps users **predict diseases** based on symptoms and **recommends nearby hospitals** using intelligent search and machine learning techniques.

---

## 🚀 Features

- 🔒 **User Authentication** (Register & Login)
- 🤖 **Disease Prediction** using symptom input via chat interface
- 📊 **ML Integration** with `RandomForest` model for disease classification
- 🔍 **Symptom Search** and disease info fetch using DuckDuckGo API
- 📂 **Interactive Web UI** built with HTML templates and Flask routing
- 🧠 **Natural Conversation Flow** via chatbot-style logic and state management
- 🏥 **Hospital Recommendation** via search suggestions

---

## 🛠️ Technologies Used

- **Backend**: Flask, SQLAlchemy, SQLite
- **ML Libraries**: scikit-learn, joblib, pandas, numpy
- **Web Scraping/Search**: duckduckgo_search
- **Front-end**: HTML (templates), Bootstrap (optional)
- **Model**: Trained RandomForest classifier for disease prediction

---

## 📁 Project Structure

```
├── app.py                 # Main Flask application
├── database.db            # SQLite database for user authentication
├── dataset.xlsx           # Dataset containing symptoms and disease labels
├── model/
│   └── random_forest.joblib   # Trained model for disease prediction
├── templates/             # HTML templates (index, login, register, chatbot pages)
├── static/                # Static files (CSS, JS, images)
├── msgConstant.py         # Welcome greeting messages
├── req.txt                # Python dependencies
└── README.md              # Project documentation
```

---

## ⚙️ Setup Instructions

1. **Install Dependencies**

```bash
pip install -r req.txt
```

2. **Run the Flask App**

```bash
python app.py
```

3. **Access the App**

Open your browser and go to: [http://localhost:3000](http://localhost:3000)

---

## 📋 Usage Workflow

1. **Register/Login**
2. Navigate to the chatbot page `/user`
3. Follow the conversation:
   - Enter your name, age
   - Choose to **predict a disease** or **check symptoms** of a known disease
   - Enter symptoms (comma-separated)
4. Bot predicts disease and suggests nearby hospitals using Google search

---

## 🧠 AI & ML Details

- Model: RandomForestClassifier
- Feature Space: Symptom presence (binary features)
- Vectorization: `CountVectorizer` for textual similarity
- Similarity Matching: `cosine_similarity` for symptom-disease relevance

---

## ✅ Example Use Case

**Input**:
- Name: John
- Age: 25
- Symptoms: headache, nausea, fever

**Output**:
- Predicted Disease: Typhoid Fever
- Recommended Action: Google search link for nearest hospitals

---

## 📌 Notes

- Ensure `random_forest.joblib` exists inside `/model/`
- Make sure your browser allows popups for search results
- `dataset.xlsx` must be well-formatted with `Symptoms` and `Disease` columns

---

## 👨‍💻 Author

- Developed by **Harish**
- Project Title: *Disease Prediction Chatbot with Hospital Suggestion*
