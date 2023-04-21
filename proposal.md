# Research Proposal: Sentiment Analysis of Federal Reserve Announcements and its Impact on the S&P 500 and Sector ETFs
By _Sz-Je Wang, Sikai Wang, and Xilong Liu_


## Research Question: 
How do Federal Reserve announcements influence the stock market according to **Natural language processing**, particularly the S&P 500 and ETFs across various sectors? 


### Specific research question:
- What is the overall sentiment and intensity in the each announcements?
- How do these sentiment scores correlate with subsequent stock market movements for the S&P 500 and sector ETFs?
- Can we predict stock market reactions based on the sentiment derived from announcements? 

### Hypotheses:
- Positive sentiment score in announcements leads to a **positive** stock market reaction.
- Negative sentiment score in announcements leads to a **negative** stock market reaction.

### Predictions:
According to the hypotheses above, we believe that every time when the Federal Reserve announcements related to a piece of good news are released, the stock of companies within the S&P 500 will show a good trend and vice versa. Whether it has a piece of good news is determined by the sentiment score that we measure.

### Data Transformation:
#### High-level Overview:
- Perform sentiment analysis on the Federal Reserve announcements using natural language processing to obtain sentiment scores.
- Merge the sentiment scores with the corresponding stock and ETF returns.
- Analyze the correlation between the sentiment scores and stock market movements.

## Necessary Data
### Final Dataset
- Observation: Federal Reserve announcements, S&P 500 stocks, and sector ETFs.
- Sample Period: Recent 10 most significant Federal Reserve announcements.
- Necessary Variables: Sentiment scores, stock prices, and returns.
#### Federal Reserve announcements:
Recent 10 most viewed and important Federal Reserve announcements (https://www.federalreserve.gov/newsevents.htm) 
#### Sentiment standard:
We will create one that evolved from what we have used during the mid-term project.
#### Selected Sector ETFs:
- Financials: Financial Select Sector SPDR Fund (XLF)
- Technology: Technology Select Sector SPDR Fund (XLK)
- Healthcare: Health Care Select Sector SPDR Fund (XLV)
- Consumer Discretionary: Consumer Discretionary Select Sector SPDR Fund (XLY)
- Consumer Staples: Consumer Staples Select Sector SPDR Fund (XLP)
- Industrials: Industrial Select Sector SPDR Fund (XLI)
- Energy: Energy Select Sector SPDR Fund (XLE)
- Materials: Materials Select Sector SPDR Fund (XLB)
- Utilities: Utilities Select Sector SPDR Fund (XLU)
- Real Estate: Real Estate Select Sector SPDR Fund (XLRE)
#### Return:
We will select the stock prices for the S&P 500 and sector ETFs between one week before and one week after the announcement date for each Federal Reserve announcement. Then, we will calculate the returns for each stock and ETF. The ETF returns can be accessed through financial data providers such as Yahoo Finance (https://finance.yahoo.com/).
#### Data Storage:
##### Raw Inputs:
- Federal Reserve announcements: stored in a folder named "announcements"
- Stock prices and ETF returns: stored in a folder named "stock_data"
- Final Dataset: stored in a folder named "final_data"
#### Target variable
Our target variables are the excess returns for the S&P 500 stocks and selected sector ETFs. We aim to find the correlation between these excess returns and the sentiment scores derived from the Federal Reserve announcements.

### Related Files 
- run ipynb through the order I provide below
- download_text.ipynb (this will download the federal announcement)
- building_sample.ipynb (loading the excel which includes the returns for each sector)
- regression.ipyhb (this wil analyzing whether the federal annuocement will have effect on market returns)
- report.ipyhb (this will summarize what is going in this process and give some discussion)
- several setiment files (these files are the sentiment standard we will use when analyzing the federal announcement)
- a folder for each sector's related returns and ETF

