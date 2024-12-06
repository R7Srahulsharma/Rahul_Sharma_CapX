# Stock Movement Analysis Based on Social Media Sentiment

## **Objective**
The goal of this project is to develop a machine learning model that predicts stock movements by analyzing social media sentiment. Using Twitter as the data source, this project will:

- Scrape tweets related to stock discussions and predictions.
- Analyze sentiment from the collected data.
- Build a machine learning model to forecast stock price trends.

---

## **Features**
1. **Data Scraping**: Extract stock-related tweets using the Twitter API and preprocess them for analysis.
2. **Sentiment Analysis**: Use Natural Language Processing (NLP) techniques to classify tweets as positive, negative, or neutral.
3. **Prediction Model**: Train and evaluate a machine learning model to predict stock movements based on extracted sentiment.

---

## **Technical Requirements**

### **Languages and Libraries**
- **Python 3.x**
- Libraries:
  - `tweepy`: For accessing the Twitter API.
  - `pandas` and `numpy`: For data handling.
  - `nltk` or `TextBlob`: For sentiment analysis.
  - `scikit-learn`: For machine learning.
  - `matplotlib` or `seaborn`: For data visualization.

### **Tools**
- Twitter Developer Account for API access.
- Jupyter Notebook or IDE for development.

---

## **Setup Instructions**

### **Step 1: Clone the Repository**
Clone this repository to your local machine:
```bash
https://github.com/R7Srahulsharma/Rahul_Sharma_CapX/
```

### **Step 2: Install Dependencies**
Install the required Python libraries using:
```bash
pip install -r requirements.txt
```

### **Step 3: Configure Twitter API**
1. Create a Twitter Developer account and generate API keys.
2. Add the API keys to the `config.py` file in the following format:
```python
API_KEY = "your_api_key"
API_SECRET_KEY = "your_api_secret_key"
ACCESS_TOKEN = "your_access_token"
ACCESS_TOKEN_SECRET = "your_access_token_secret"
```

### **Step 4: Run the Scripts**
1. Scrape tweets using:
   ```bash
   python scraper.py
   ```
2. Perform sentiment analysis:
   ```bash
   python sentiment_analysis.py
   ```
3. Train and evaluate the prediction model:
   ```bash
   python model.py
   ```

---

## **Repository Structure**
```
stock-movement-analysis/
├── data/                   # Directory for scraped and processed data
├── notebooks/              # Jupyter notebooks for exploratory analysis
├── scraper.py              # Script for Twitter data scraping
├── sentiment_analysis.py   # Script for sentiment analysis
├── model.py                # Machine learning model script
├── requirements.txt        # List of dependencies
├── README.md               # Project documentation
└── config.py               # Configuration file for API keys
```

---

## **Workflow**

### 1. Data Scraping
- Use `tweepy` to collect tweets related to specific stock market keywords or hashtags (e.g., #StockMarket, $AAPL).
- Preprocess the data by removing noise, URLs, special characters, and stop words.

### 2. Sentiment Analysis
- Use `TextBlob` or `nltk` to analyze tweet sentiment.
- Classify tweets into positive, negative, or neutral categories.
- Extract features like sentiment polarity and frequency of mentions.

### 3. Prediction Model
- Train a machine learning model using the extracted sentiment features and historical stock price data.
- Evaluate the model’s performance using metrics such as accuracy, precision, recall, and F1-score.

---

## **Results and Evaluation**
 | Metric         | Class 0 | Class 1 | Accuracy | Macro Avg | Weighted Avg |
|----------------|---------|---------|----------|-----------|--------------|
| **Precision**  | 0.57    | 0.65    |          | 0.61      | 0.61         |
| **Recall**     | 0.70    | 0.52    |          | 0.61      | 0.60         |
| **F1-Score**   | 0.63    | 0.58    |          | 0.60      | 0.60         |
| **Support**    | 46      | 50      | 96       | 96        | 96           |


### **Insights**
- Positive sentiment strongly correlates with stock price increases.
- Frequent mentions of a stock are potential indicators of high market activity.

---

## **Future Improvements**
- Incorporate data from additional platforms like Reddit and Telegram.
- Use advanced NLP models for sentiment analysis.
- Implement real-time stock movement predictions.

---

## **License**
This project is licensed under the MIT License. See the `LICENSE` file for details.
