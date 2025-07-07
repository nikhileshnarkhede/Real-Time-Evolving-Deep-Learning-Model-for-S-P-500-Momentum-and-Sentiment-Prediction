# 📈 Real-Time Evolving Deep Learning Model for S&P 500 Momentum and Sentiment Prediction

This project presents a **real-time adaptive deep learning framework** that combines **Natural Language Processing (NLP)** and **Long Short-Term Memory (LSTM)** networks to predict the **momentum** of the **S&P 500 index** using both **historical price data** and **financial news sentiment**.

## 📌 Key Features

- 🔄 **Real-Time Retraining**: 28-day sliding window ensures the model adapts continuously to new data.
- 💬 **Sentiment Analysis**: Financial news headlines processed via a rule-based NLP system.
- 🧠 **LSTM Forecasting**: Predicts short-term stock price momentum with high precision.
- 📊 **Model Accuracy**:
  - Sentiment classification accuracy: **90.1%**
  - LSTM momentum prediction R² score: **0.97**

---

## 📂 Project Structure

\`\`\`
├── News_Perseverance_.ipynb               # Sentiment analysis and text preprocessing
├── News_Perseverance_Loaded_Model.ipynb   # Inference using pre-trained sentiment model
├── S&P500_News_Per_Day_Data.ipynb         # Merging daily sentiment with stock prices
├── Stock_Price_Momentum_Prediction_using_History_Data.ipynb # LSTM training and prediction
├── MTH 601 Project Report.docx            # Full project documentation
├── README.md                              # Project overview
\`\`\`

---

## 🧪 Methodology

### 1. **Data Collection**
- **Stock Prices**: Daily OHLCV data from Yahoo Finance (`yfinance`).
- **News Headlines**: Scraped from sources like MarketWatch and Yahoo Finance using `BeautifulSoup`, `Selenium`.

### 2. **Sentiment Analysis**
- Preprocessing: tokenization, lemmatization, stopword removal.
- Sentiment scoring: Rule-based polarity (Bullish/Bearish).
- Output: Aggregated daily sentiment scores.

### 3. **Momentum Prediction**
- Deep LSTM model trained on:
  - 28 days of adjusted closing prices
  - Corresponding sentiment scores
- Forecasts the next 7-day trend in S&P 500.

### 4. **Real-Time Updating**
- Continuous 28-day sliding window retraining to capture evolving market behavior.

---

## 📈 Results

| Component            | Metric    | Performance |
|----------------------|-----------|-------------|
| Sentiment Analysis   | Accuracy  | 90.1%       |
| Price Momentum Model | R² Score  | 0.97        |

💡 Integration of sentiment improves price forecast reliability, especially during market volatility.

---

## 💡 Use Case Example

> Following a surge in positive sentiment from tech-sector earnings, the model predicted an upward trend in the S&P 500—validated by actual market movement days later.

---

## 🔭 Future Improvements

- 🧠 Replace rule-based sentiment with **FinBERT** for deeper contextual understanding.
- 📈 Extend prediction to **multi-stock portfolios**.
- 🤖 Integrate **reinforcement learning** for trading strategies.
- ⏱ Adapt to **intraday forecasting** by refining model granularity.

---

## ⚙️ Installation & Usage

Install dependencies:

\`\`\`
pip install yfinance pandas numpy tensorflow scikit-learn nltk selenium beautifulsoup4
\`\`\`

Run notebooks in order:

1. `News_Perseverance_.ipynb` → Process and score news sentiment.
2. `S&P500_News_Per_Day_Data.ipynb` → Merge with stock prices.
3. `Stock_Price_Momentum_Prediction_using_History_Data.ipynb` → Train LSTM.
4. `News_Perseverance_Loaded_Model.ipynb` → Run predictions.

---

## 👨‍💻 Author

**Nikhilesh Narkhede**  
Graduate Student | Data Scientist | AI/ML Enthusiast
