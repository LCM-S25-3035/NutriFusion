 🥦 NutriFusion

NutriFusion is a health-focused data platform designed to provide personalized nutrition and recipe recommendations based on age and medical conditions. It collects, cleans, and prepares real-world nutrition and health-related datasets through an intelligent big data pipeline to support AI-powered food guidance tools.

---

🚀 Project Structure

```
NutriFusion/

├── data/
│   └── raw/                     # Raw scraped datasets from APIs and websites
│   └── cleaned/                 # Cleaned datasets ready for analysis
│
├── src/
│   ├── scrapers/               # Web scraping scripts using BeautifulSoup, Selenium
│   ├── preprocessor/           # Scripts for cleaning, merging, and formatting datasets
│   └── eda/                    # Exploratory Data Analysis and visualizations
│
├── tests/                      # Test scripts for validation
│
├── reports/                    # Documentation and milestone reports
│
├── sonar/                      # Static analysis and code quality config
│
├── requirements.txt
├── docker-compose.yml (TBD)
└── README.md
```



🧠 How It Works (Pipeline Overview)

NutriFusion uses multiple tools and services to collect, process, and organize data relevant to nutrition and health personalization:

🔹 Data Collection Pipeline

Scraping Sources:

APIs: Edamam, OpenFoodFacts, Spoonacular
Websites: SeriousEats, EatingWell, Yummly, Kaggle

Tools Used:

  * `BeautifulSoup`, `Selenium` for scraping
  * `Pandas`, `Jupyter Notebook` for processing
  * `SonarQube` for static code analysis

  Data Format:

  * Datasets are stored in CSV format
  * Cleaned datasets are structured by health conditions and age groups

---

 ⚙️ Setup & Run Instructions

 1. Clone the Repository

bash
git clone https://github.com/LCM-S25-3035/NutriFusion.git
cd NutriFusion
```

2. Install Dependencies

```bash
pip install -r requirements.txt
```

> Ensure Python 3.11+ is installed.

3. Run Scrapers

Navigate to the scrapers directory and run the scraping scripts.

```bash
cd src/scrapers
python scrape_edamam.py
```

4. Preprocess Datasets

```bash
cd ../preprocessor
python clean_merge.py
```

---

📦 Technologies Used

* Python 3.11+
* BeautifulSoup & Selenium (Web Scraping)
* Pandas (Data Wrangling)
* SonarQube (Code Quality)
* Jupyter (EDA & Documentation)

---

✅ Progress Overview

✔ Completed

 ✅ Data scraping from Edamam, OpenFoodFacts, and other sources
 ✅ Dataset cleaning: removed duplicates, fixed encodings, translated non-English data
 ✅ Organized nutrition data by health condition and age group
 ✅ Setup SonarQube and ran code analysis
 ✅ Conducted exploratory data analysis (EDA)

🧪 In Progress

 Data preprocessing and transformation
 Integration with ML models
 Model building and deployment research
 Research paper review and documentation

---

 🧪 QA & Testing

 ✅ Static code analysis via SonarQube
 ❌ Test cases are still under development
 ✅ GitHub commits available for each member

---

## 🔭 Future Scope

* ML-based personalized diet recommendation system
* UI for selecting user preferences and viewing results
* Integration with streaming tools (e.g., Kafka, RisingWave)
* Deployment of dashboards and APIs
* Live scraping with automation support

---

 💡 Summary

NutriFusion is a scalable, data-driven nutrition analytics platform aiming to help users make informed dietary choices through intelligent content delivery. By merging real-world data with personalized health needs, it paves the way for AI-assisted health guidance.

---

GitHub Repo: [https://github.com/LCM-S25-3035/NutriFusion](https://github.com/LCM-S25-3035/NutriFusion)
Project Board: [Link](https://github.com/orgs/LCM-S25-3035/projects/2)



