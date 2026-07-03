# Redfin-Housing-Analytics

## 📌 Project Overview
An automated data engineering pipeline designed to harvest, clean, and analyze scattered real estate listings from Redfin. This project tackles modern web scraping challenges by implementing defensive programming techniques to handle anti-bot frameworks, delivering a structured dataset optimized for property pricing and spatial density analysis.

## 🛠️ Tech Stack & Core Skills
* **Language:** Python
* **Libraries:** `curl_cffi`, `BeautifulSoup4`, `pandas`, `matplotlib`, `seaborn`, `re`
* **Core Competencies:** Advanced Web Scraping, Defensive Programming, Data Cleansing, Regex Parsing, Exploratory Data Analysis (EDA)

## 🏗️ Architecture & Features
* **Anti-Bot Resilience:** Implements `curl_cffi` to mimic realistic browser TLS fingerprints and headers, successfully bypassing modern scraping blocks.
* **Robust Parsing Engine:** Uses BeautifulSoup and complex Regular Expressions (Regex) to isolate price, square footage, bed/bath counts, and location features from raw HTML.
* **Fault-Tolerant Pipeline:** Programmed with explicit delays and error-handling wrappers to ensure continuous data collection without server overloads.
* **Analytical Insights:** Cleans and structure the scraped logs into a Pandas DataFrame to visualize regional property density and price-per-square-foot metrics.

## 🚀 Getting Started
1. Clone the repository: `git clone https://github.com/yourusername/redfin-scraper.git`
2. Install dependencies: `pip install curl_cffi beautifulsoup4 pandas matplotlib seaborn`
3. Run the engine: `python scraper.py`

## 📊 Sample Insights
* Successfully extracted and parsed hundreds of live property data points without triggering IP bans.
* Identified distinct geographic clusters where price-per-square-foot deviated significantly from the city median.
