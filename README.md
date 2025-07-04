# 🥗 CalorieLens

## 📖 Project Overview

Calories Food Advisor is an AI-driven application designed to analyze meal images and provide calorie estimates along with a health assessment. The app leverages Google's Gemini Pro Vision model to recognize food items from photos and deliver insights about nutrition and health balance. Users can simply upload a photo of their meal and instantly learn how many calories they’re consuming and whether the meal is balanced or high in certain nutrients.

## ⚙️ How It Works

* **Image Upload:** Users upload a food photo via a Streamlit web interface.
* **Image Processing:** The uploaded image is converted into the required byte format and MIME type using a custom function.
* **LLM Integration:** The image and a carefully crafted prompt are sent to Gemini Pro Vision, which:

  * Identifies individual food items.
  * Estimates calorie counts for each item.
  * Calculates total meal calories.
  * Provides a short health verdict on the meal’s overall balance.
* **Result Display:** Streamlit displays the AI-generated list of food items, their calorie estimates, the meal’s total calories, and a health analysis.

## 🌐 Tech Stack

* Python
* Streamlit
* Google Generative AI (Gemini Pro Vision)
* python-dotenv
* LangChain
* PyPDF2
* ChromaDB

## 🔒 Security

All sensitive credentials, including API keys for Gemini Pro Vision, are stored securely in a `.env` file and excluded from version control.

## 📁 Project Structure

```
HEALTH MANAGEMENT APP/
│
├── health.py                # Main Streamlit application
├── requirements.txt         # Python dependencies
├── .env                     # Environment variables (API keys)
├── .gitignore               # Files/folders to ignore in Git
├── LICENSE.txt              # License file (MIT)
├── README.md                # Project documentation
├── thali.jpg                # Example food image
└── venv/                    # Virtual environment
```

## 🚀 How to Run

### 1. Clone the Repository

```bash
git clone https://github.com/kunalmishravitb/CalorieLens.git
cd CalorieLens
```

### 2. Create a Virtual Environment

```bash
conda create -n venv python=3.10 -y
conda activate venv
```

### 3. Install Requirements

```bash
pip install -r requirements.txt
```

### 4. Configure Environment Variables

Create a `.env` file with the following:

```
GOOGLE_API_KEY="your_gemini_pro_vision_api_key"
```

### 5. Run the Application

```bash
streamlit run health.py
```

Navigate to `http://localhost:8501` to use the app.

## 💡 Key Features

* Identifies multiple food items from a single meal photo.
* Estimates calorie count for each item and the entire meal.
* Provides a quick health assessment of meal composition.
* Handles complex plates like Indian thalis.
* Easy-to-use web interface built with Streamlit.

## 🙌 Why This Matters

Calories Food Advisor bridges AI and everyday health tracking. It transforms meal tracking into an effortless process, empowering individuals to make informed dietary decisions. Whether managing weight, tracking nutrition, or simply staying conscious about health, this tool offers practical, real-world value.
