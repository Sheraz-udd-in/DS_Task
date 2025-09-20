# Analysis of Trader Behavior and Profitability in Relation to Market Sentiment

This project analyzes a dataset of historical cryptocurrency trades and correlates it with market sentiment data (Fear and Greed Index) to understand how different market moods influence trader behavior and profitability.

## Project Steps and Analysis

1.  **Import Libraries and Load Data**: Necessary libraries like pandas, matplotlib, and seaborn were imported, and the historical trading data (`historical_data.csv`) and fear and greed index data (`fear_greed_index.csv`) were loaded.

2.  **Data Cleaning and Preprocessing**:
    *   Timestamps in both datasets were converted to datetime objects.
    *   A 'date' column was extracted from the timestamps for merging.
    *   The 'Closed PnL' column in the trading data was converted to a numeric type, coercing errors to handle non-numeric values.

3.  **Merge the Datasets**: The trading data and sentiment data were merged based on the 'date' column to associate each trade with the prevailing market sentiment. Rows with missing sentiment classification or Closed PnL were removed.

4.  **Analysis and Visualization**: Several aspects of trader behavior and profitability were analyzed in relation to market sentiment:

    *   **Overall Profitability by Market Sentiment**: The average 'Closed PnL' was calculated for each sentiment category.
    *   **Trading Direction (Long vs. Short) by Sentiment**: The proportion of BUY (Long) and SELL (Short) trades was examined for each sentiment.
    *   **Trade Size by Market Sentiment**: The distribution of 'Size USD' and 'Size Tokens' was visualized using box plots across different sentiments.
    *   **Trade Duration by Market Sentiment**: The duration of trades was calculated and its distribution across sentiments was visualized using a box plot.
    *   **Most Traded Coins by Sentiment**: The number of trades for each coin within each sentiment category was counted to identify the most active coins.
    *   **Profitability by Coin and Sentiment**: The average 'Closed PnL' for each coin within each sentiment category was calculated.
    *   **Account Profitability by Sentiment**: The total 'Closed PnL' for individual accounts was aggregated by sentiment.
    *   **Trading Frequency by Sentiment**: The total number of trades in each sentiment category was counted.

5.  **Summarize Insights**: The key findings from the analysis were synthesized into a summary.

## Summary of Key Findings

*   **Overall Profitability:** Average profitability varied significantly by market sentiment, with 'Greed' being the most profitable on average, while 'Fear' was the least profitable.
*   **Trading Direction:** The distribution of BUY (Long) and SELL (Short) trades showed some variation across sentiments, with 'Greed' sentiment showing a higher percentage of SELL trades compared to other sentiments.
*   **Trade Size and Duration:** Visual analysis using box plots suggested that the distribution of trade sizes (USD and Tokens) and trade durations might differ across sentiments, indicating potential variations in median size, presence of outliers, and holding periods.
*   **Most Traded Coins:** The most actively traded coins varied depending on market sentiment. While major coins like ETH and BTC were consistently traded, the prominence of altcoins and meme coins shifted. 'Extreme Greed' was dominated by major coins and some trending alt/meme coins, 'Fear' saw high volume in specific tickers like "HYPE", "@107", and "SOL" alongside BTC/ETH, and 'Greed' and 'Neutral' had their own distinct mixes of established and newer tokens.
*   **Profitability by Coin and Sentiment:** Analysis at the coin level revealed that the average profitability of trading specific coins can be highly dependent on the prevailing market sentiment.
*   **Account Profitability:** Individual account profitability varied significantly with market sentiment, with some accounts performing better in specific sentiment conditions than others.
*   **Trading Frequency:** The number of trades varied considerably across different sentiment periods, with 'Fear' exhibiting the highest trading frequency (133,545 trades), suggesting increased activity or volatility during these times, followed by 'Greed' (36,021), 'Neutral' (7,042), and 'Extreme Greed' (6,884).

## Insights and Potential Next Steps

*   The strong relationship between market sentiment and trading behavior suggests that integrating sentiment analysis into trading strategies could potentially improve profitability and risk management.
*   Further investigation into the specific assets that perform well or poorly under different sentiment conditions, and the characteristics of accounts that are profitable across various sentiments, could provide deeper insights into successful trading approaches.
