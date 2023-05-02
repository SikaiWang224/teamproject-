# Research Proposal: Sentiment Analysis of Federal Reserve Announcements and its Impact on the Sector ETFs
By _Sz-Je Wang, Sikai Wang, and Xilong Liu_


## Research Question: 
How do Federal Reserve announcements influence the stock market according to **Natural language processing**, particularly the ETFs across various sectors? 


### Specific research question:
- What is the overall sentiment and intensity in the each announcements?
- How do these sentiment scores correlate with subsequent stock market movements for the sector ETFs?
- Can we predict stock market reactions based on the sentiment derived from announcements? 

### Hypotheses:
- Positive sentiment score in announcements leads to a **positive** stock market reaction.
- Negative sentiment score in announcements leads to a **negative** stock market reaction.

### Predictions:
According to the hypotheses above, we believe that every time when the Federal Reserve announcements related to a piece of good news are released, the stock of companies will show a good trend and vice versa. Whether it has a piece of good news is determined by the sentiment score that we measure.

### Data Transformation:
#### High-level Overview:
- Perform sentiment analysis on the Federal Reserve announcements using natural language processing to obtain sentiment scores.
- Merge the sentiment scores with the corresponding stock and ETF returns.
- Analyze the correlation between the sentiment scores and stock market movements.

## Necessary Data
### Final Dataset
- Observation: Federal Reserve announcements and sector ETFs.
- Sample Period: Recent 10 most significant Federal Reserve announcements.
- Necessary Variables: Sentiment scores, stock prices, and returns.
#### Variable
- The nearest fed announcement (event id variable)
- Excess return (return minus market return)
- Cumulative excess return for that asset during that event's time window (from t-10 up to t+10)
- Sentiment of the corresponding fed announcement
- Variable(s) that categorize the sentiment variable into smaller bins (e.g. High/Low, High/Middle/Low)

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
- Communication Services: Communication Services Select Sector SPDR Fund (XLC)
#### Return:
We will select the stock prices for the sector ETFs between one week before and one week after the announcement date for each Federal Reserve announcement. For example, if we have an announcement date at 3.10, we will be likely to collect the market price between 3.3 and 3.17 day by day. Then, we will calculate the returns for each stock and ETF. The ETF returns can be accessed through financial data providers such as Yahoo Finance (https://finance.yahoo.com/).
#### Data Storage:
##### Raw Inputs:
- Federal Reserve announcements: stored in a folder named "Fed"
- Stock prices and ETF returns: stored in a folder named "ETFdata"
- Positive and Negative Sentiment lists: stored in a folder named "Sentiment"
- Final Dataset: stored in a folder named "analysis cvs file"

#### Target variable
Our target variables are the excess returns for the selected sector ETFs. We aim to find the correlation between these excess returns and the sentiment scores derived from the Federal Reserve announcements.

### Related Files 
- Run ipynb through the order I provide below
- Download_text.ipynb (this will download the federal announcement)
- Building_sample.ipynb (loading the excel which includes the returns for each sector)
- Regression.ipyhb (this wil analyzing whether the federal annuocement will have effect on market returns)
- Report.ipyhb (this will summarize what is going in this process and give some discussion)
- Several setiment files (these files are the sentiment standard we will use when analyzing the federal announcement)
- A folder for each sector's related returns and ETF

![377 final project](https://user-images.githubusercontent.com/112531955/233749032-128a53bc-25c4-4261-9033-c1190e320473.jpg)
### Explaination
- The upper part has one sample graph we will have in the first part of our website. We can see the trend from the graph like how the announcement will have impact on the market return and EFT return.
- The defination part explains how excess ret is generated. This formula help us calculated the cumulative returns.
- The regression part notifies us that we need to apply query for different sectors.
- Also, there is a sample dataset that we will be using. It has the important variables like announcement id to distinguish companies. This also have sendiment score and returns merged. We can then find the correlation between these varibales.
- For forcasting the future, we will be able to use these relationship to know what will happen in the future market when the new federal announcement comes. 

### Website Content
#### Home:
- Introduction to the project
- Brief overview of research questions and hypotheses
- Visualization of project flowchart

#### About:
- Team members and their roles
- Project background and motivation
- Goals and objectives

#### Methodology:
- Detailed explanation of data transformation steps
- Description of sentiment analysis using Natural Language Processing
- Explanation of correlation analysis between sentiment scores and stock return

#### Data:
- Overview of dataset structure and variables
- List of selected sector ETFs
- Description of data sources and storage

#### Results:
- Presentation of key findings and insights
- Visualizations of correlations between sentiment scores and stock return
- Discussion of market predictability based on announcement sentiment

#### Conclusion:
- Summary of main findings
- Implications and potential applications
- Forecast the future market when new federal announcemet comes. 

#### Resources:
- Links to related files (Jupyter notebooks, sentiment standard files, etc.)
- Relevant research papers and articles
- External resources (Federal Reserve announcements, Yahoo Finance, etc.)

#### Contact:
- Team member contact information
- Collaboration and feedback opportunities
- Social media profiles and professional links
