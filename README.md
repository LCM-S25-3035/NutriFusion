 🥦 NutriFusion: Personalized Nutrition Intelligence

NutriFusion is a smart nutrition recommendation system that personalizes dietary suggestions based on a user’s age group and medical condition. The platform combines real-world food data with health standards to provide ingredient-level analysis, highlight nutrient gaps, and suggest healthy alternatives through AI-enabled tools.

This project leverages large-scale datasets, natural language processing, and data science pipelines to support health-aware recipe enhancement and dietary decision-making.

---

 🚀 Project Folder Structure

```
NutriFusion/
├── data/
│   ├── raw/                  # Scraped data (Edamam, OpenFoodFacts, etc.)
│   └── cleaned/              # Cleaned datasets (recipes, nutrients, age-health norms)
│
├── src/
│   ├── scrapers/             # Scripts to collect recipe and nutrition info
│   ├── preprocessor/         # Dataset cleaners, mergers, and formatters
│   ├── nlp_extractor/        # NLP/Regex ingredient extractors
│   ├── nutrient_analyzer/    # Nutrient gap calculator
│   └── recommender/          # Rule-based and ML-based ingredient suggestion
│
├── ui/                       # Streamlit or Flask-based user interface
├── tests/                    # Unit and integration tests
├── reports/                  # Milestone reports, diagrams, weekly logs
├── sonar/                    # SonarQube config and results
├── requirements.txt
├── docker-compose.yml (TBD)
└── README.md
```

---

🧠 System Modules Overview

1️⃣ Data Preparation

 Two core datasets:

   `70000_recipes_nutrients_cleaned_final.csv` — recipes with nutritional details.
   `Cleaned_Age_and_health_data.csv` — health-based recommended nutrient ranges.
 Processes:

   Standardize ingredient names, compute nutrient ratios (e.g., protein per calorie).
   Normalize age-health nutritional requirements and convert disease labels to one-hot format.

 2️⃣ NLP Ingredient Extractor

* Uses spaCy or Regex to parse free-text recipes.
* Strips quantities/units (e.g., "2 tbsp olive oil") and identifies core ingredients.
* Optional: Fine-tuned NER model from Hugging Face (`dslim/bert-base-NER`) to improve extraction accuracy.

 3️⃣ Nutrient Analyzer

* Inputs: Extracted ingredients, user's selected health condition + age range.
* Calculates total nutrients from selected recipe.
* Compares with health standards to highlight nutrient deficiencies (e.g., protein shortfall).

 4️⃣ AI Recommender

* Rule-Based Mode: Suggests ingredients high in nutrients that are lacking.
* ML Mode (Optional): Uses clustering or KNN to find similar recipes optimized for the user’s profile.

 5️⃣ User Interface

* Simple Streamlit or Flask app where users:

  * Enter a custom recipe
  * Choose their health condition and age group
  * View ingredient breakdown, nutritional gaps, and suggested additions

---

 ⚙️ Setup Instructions


# Step 1: Clone the repository
git clone https://github.com/LCM-S25-3035/NutriFusion.git
cd NutriFusion

# Step 2: Install dependencies
pip install -r requirements.txt

# Step 3: Run scrapers (optional)
cd src/scrapers
python scrape_edamam.py

# Step 4: Preprocess and clean datasets
cd ../preprocessor
python clean_merge.py
```

> ✅ Python 3.11+ is recommended for compatibility.

---

## 📦 Tech Stack

* Python 3.11+
* BeautifulSoup, Selenium (Web scraping)
* spaCy, Regex, HuggingFace Transformers (NLP)
* Pandas, NumPy (Data processing)
* Streamlit or Flask (UI)
* SonarQube (Code quality)

---

 ✅ Current Progress

**Completed:**

* ✅ Recipe and nutrition data collection from Edamam, OpenFoodFacts
* ✅ Ingredient and nutrient data cleaned, standardized, and labeled by age and disease
* ✅ Setup of static code analysis with SonarQube
* ✅ Ingredient extraction module using NLP and rule-based methods
* ✅ Weekly milestone logging and paper reviews

**In Development:**

* 🔄 Nutrient gap detection logic testing
* 🔄 Recommender system tuning (rule-based + ML)
* 🔄 Streamlit/Flask UI for end-to-end demo

---

 🧪 QA & Testing

* ✅ Code scanning with SonarQube
* 🔲 Automated unit tests (in progress)
* ✅ All datasets and scripts versioned on GitHub

---

 🔭 Future Goals

* Deploy web-based interactive UI
* Enable real-time recipe scoring and streaming ingestion via **Kafka**/**RisingWave**
* Train custom ML models for disease-specific ingredient prediction
* Build personalized meal planning APIs
* Integrate with wearable health devices or health records (future scope)

---

 💡 Vision

**NutriFusion** is built to empower users in making healthier food choices through data-driven insights. By tailoring recipes to individual health needs, it bridges the gap between generic dietary advice and personalized nutrition — one ingredient at a time.

---

📁 GitHub Repo: [NutriFusion](https://github.com/LCM-S25-3035/NutriFusion)
🗂️ Project Board: [View Progress](https://github.com/orgs/LCM-S25-3035/projects/2)

---

