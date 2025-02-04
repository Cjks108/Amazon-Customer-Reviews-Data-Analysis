# 📊 Amazon-Customer-Reviews-Data-Analysis

## 📌 Overview
This project analyzes Amazon sales data using Python. It involves **data cleaning, exploratory data analysis (EDA), data visualization, and sentiment analysis** of customer reviews.

---

## 🗂️ Dataset Information
- **Source:** SQLite Database (`database.sqlite`)
- **Table Used:** `REVIEWS`
- **Key Columns:**
  - `UserId`: Unique identifier for each reviewer
  - `ProfileName`: Name of the reviewer
  - `Time`: Timestamp of the review (converted to datetime)
  - `Text`: Review content
  - `Summary`: Short summary of the review
  - `Score`: Rating given by the user (1 to 5)
  - `ProductId`: Unique product identifier

---

## 🛠️ Steps Performed

### 1️⃣ Data Loading 📥
- Connected to the SQLite database and extracted the `REVIEWS` table into a Pandas DataFrame.

### 2️⃣ Data Cleaning 🧹
- Removed **invalid reviews** where `HelpfulnessNumerator > HelpfulnessDenominator`.
- Eliminated **duplicate reviews** based on `UserId`, `ProfileName`, `Time`, and `Text`.
- Converted **timestamps** from UNIX format to readable datetime format.

### 3️⃣ Exploratory Data Analysis (EDA) 📊
- Identified **unique users and profile names**.
- Analyzed **user behavior**, including:
  - Number of reviews per user
  - Average review score
  - Number of products reviewed

### 4️⃣ Data Visualization 📈
- **Top 10 reviewers** based on the number of products reviewed.
- **Frequent vs. Non-Frequent reviewers**:
  - Classified users who wrote more than 50 reviews as "Frequent."
  - Compared **review scores and text lengths** between frequent and non-frequent reviewers.
- **Boxplots and bar charts** for better insights.

### 5️⃣ Sentiment Analysis 😊😠
- Used **TextBlob** to compute sentiment polarity for review summaries.
- Extracted the **most common positive and negative summaries**.

---

## 📌 Key Insights
- The dataset contains **a high number of duplicate reviews**, which needed to be removed for accurate analysis.
- Certain users reviewed **a significantly larger number of products**, indicating possible **spam or power users**.
- **Frequent reviewers** tend to write longer reviews.
- **Sentiment analysis** shows the overall tone of customer feedback and highlights common themes in positive and negative reviews.

---

## 📌 Questions Answered ❓
1. 🛍️ **How many unique users and products are there?**
2. 🏆 **Which users have reviewed the most products?**
3. 🔍 **Which products have received more than 500 reviews?**
4. ⭐ **What is the distribution of review scores among frequent and non-frequent reviewers?**
5. ✍️ **Do frequent reviewers write longer reviews?**
6. 🤖 **What is the overall sentiment of the reviews?**
7. 📢 **What are the most common positive and negative reviews?**

---

## 🔧 Technologies Used
- **Python** 🐍
- **Pandas** 🏷️ (Data manipulation)
- **Matplotlib & Seaborn** 📊 (Data visualization)
- **SQLite** 🗄️ (Database querying)
- **TextBlob** 🤖 (Sentiment Analysis)

---

## 🚀 How to Run the Project

1. **Clone the Repository**  
   ```bash
   git clone https://github.com/your-username/Amazon-Customer-Reviews-Data-Analysis.git
   cd Amazon-Customer-Reviews-Data-Analysis
   
2. **Install Dependencies** 
   Ensure Python is installed on your system. Then, install the required libraries:
  ```bash
  pip install pandas numpy matplotlib seaborn textblob

---

## 🚀 Future Improvements

- **Implement Natural Language Processing (NLP) techniques for deeper review analysis.**
- **Use machine learning models to predict product ratings based on review content.**
- **Build an interactive dashboard to explore insights dynamically.**
