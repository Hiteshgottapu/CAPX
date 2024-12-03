
# **CARS24 - Stock Movement Prediction Using Twitter Sentiment Analysis**

## **Project Overview**
This project predicts stock price movements based on sentiment analysis of Twitter data. By collecting tweets related to stocks, we preprocess, analyze sentiment, and use machine learning models to forecast whether stock prices will move up or down. The aim is to leverage public sentiment as an indicator for market trends.

## **Project Structure**
```
CARS24/
├── data/
│   ├── tweets.csv                  # Raw scraped data from Twitter
│   ├── cleaned_tweets.csv          # Cleaned and preprocessed tweets
│   └── tweets_with_sentiment.csv   # Tweets with sentiment scores and categories
├── notebooks/
│   └── stock_movement_prediction.ipynb  # Jupyter Notebook for end-to-end analysis
├── README.md                       # Instructions for setup and running the project
└── requirements.txt                # List of project dependencies
```

## **Installation and Setup**

1. **Clone the Repository**
   ```sh
   git clone <your-github-repo-link>
   cd CARS24
   ```

2. **Create a Virtual Environment**
   ```sh
   python -m venv env
   ```

3. **Activate the Environment**
   - On Windows:
     ```sh
     env\Scripts\activate
     ```
   - On Linux/macOS:
     ```sh
     source env/bin/activate
     ```

4. **Install Dependencies**
   ```sh
   pip install -r requirements.txt
   ```

## **Usage Instructions**

### **1. Running the Jupyter Notebook**
To explore the project, start Jupyter Notebook:
```sh
jupyter notebook
```
Open `notebooks/stock_movement_prediction.ipynb` to see the complete pipeline from data scraping to model evaluation. Each section includes Markdown cells explaining the steps involved.

### **2. Project Workflow**
- **Data Collection**: Use the Tweepy library to scrape tweets related to stocks.
- **Data Preprocessing**: Clean text by removing noise, perform tokenization, and sentiment analysis.
- **Feature Extraction**: Vectorize tweets using TF-IDF and extract sentiment scores.
- **Model Training and Evaluation**: Train Logistic Regression, Random Forest, and a Deep Neural Network (DNN) to predict stock movements. Compare their performance using evaluation metrics such as Accuracy, Precision, Recall, and F1-score.

## **Key Features**
- **Data Scraping**: Fetch recent tweets using Tweepy for sentiment analysis.
- **Sentiment Analysis**: Assign sentiment scores to tweets to gauge market sentiment.
- **Prediction Models**: Machine Learning and Deep Learning models predict stock movements based on sentiment features.
- **Model Evaluation**: Evaluate models using cross-validation and metrics like ROC-AUC, accuracy, and SHAP for interpretability.

## **Dependencies**
- `tweepy`
- `pandas`
- `nltk`
- `textblob`
- `scikit-learn`
- `matplotlib`
- `shap`
- `torch`
- `wordcloud`

To install the dependencies, run:
```sh
pip install -r requirements.txt
```

## **Results**
- The project showed promising results, with the Voting Classifier and DNN models achieving accuracies around **93-94%** in predicting stock movement.
- **SHAP** values provided interpretability, revealing key features impacting predictions.

## **Challenges**
- **Twitter API Limits**: Handled using sleep-and-retry mechanisms.
- **Noisy Data**: Removed irrelevant tweets and cleaned text for better sentiment analysis.

## **Future Improvements**
- Integrate additional data sources like **financial news** and **Reddit posts**.
- Use advanced models like **BERT** for more accurate sentiment detection.
- Develop a real-time streaming feature for live analysis of tweets and stock trends.

## **Author**
- **Gottapu Hitesh**

---

This `README.md` provides a comprehensive overview of your project, including installation, usage, and future directions, making it easy for others to understand and use. Let me know if you need to modify anything!
