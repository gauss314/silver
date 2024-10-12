# Quantitative Engineer Interview w/Live Coding Challenge

### **Section I - SS Quant Finance**

1. **Theoretical Understanding:** Write the Black & Scholes model in LaTeX, explaining model functionality and its key components

2. **Manual Implementation:** Implement B&S model manually to compute the value of an option and the probability of exercise

3. **Implied Volatility Calculation:** Develop an eficient function to compute Implied Volatility (IV) based on model, aiming for a maximum complexity of O(log(n))

4. **Iteration Estimation & Optimization:** Estimate the avearge number of iterations needed for the IV calculation method. Propose and explain at least two more efficient methods in complexity justifying your choices


### **Section II - ETL/Data Engineering**

1. **Data Retrieval via API:** Register and implement a function to interact with the Alpaca REST API, fetching BID/ASK prices for all options of a given undrlying asset within a time range of 30-180 days TTM and strikes between 75%-125% of ATM price

2. **Data Parsing Using Regex:** Use RegEx to parse tickers and extract information such as option expiry date, ticker symbol, strike price, and contract type

3. **Additional Calculations:** Calculate slippage, mark price, and TTM for each option, always prioritize a matrix-based calculation approach with Pandas to improve ETL performance at runtime

4. **IV and Probability of Exercise:** Add calculations for bid & ask IV and mark price of each option, as well as the probability of exercise

5. **Database Storage:** Save the whole options chain for AAPL, AMZN, NVDA, KO and JPM in an SQL database, making sure the table is optimized for aggregate queries and filtering. Focus on the columns for bid/ask implied volatility, model IV, and the probability of being exercised to ensure future fast and efficient access


### **Section III - BS Quant Finance**

1. **Volatility Smile Modeling:** Use machine learning techniques to model the volatility smile (IV) for each opex of each ticker from the database. Persist the trained models on disk for future use

2. **Volatility Charting:** Given a specific ticker, graph the model volatility smile across all expiries, overlaying bids and asks in terms of IV

3. **Arbitrage Analysis:** Identify arbitrage oportunities where Ask IV > Model IV or Bid IV > Model IV. Explain these oportunities in terms of whether they are ITM or OTM

4. **SQL Query for Top Oportunities:** Write an SQL query to fetch the top 10 best for arbitrage (buy/sell) for a given ticker across all expiries, highlighting the best trades based on modeled and market IV discrepancies



Notes:
During the live coding session, it is expected (and highly encouraged) that you explain why you choose one method over another. Install only the necessary packages, deliver a requirements file with the needed dependencies, and save each section in a separate file