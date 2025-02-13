Project1_Group3
Project one group three consolidates lessons from modules 1-9. 
---
# [Presentation](https://github.com/KingCam12/Project1_Group3/blob/464c408acfe722c7f025ba08bc5a1d6e3f471265/PROJECT%201%20GROUP%203%20PRESENTATION%20.pdf)
---
## Project Description

##### **Team members**

Alexander Iruthaya, Aannd Bhagwat, Cameron Burgess, Jean Clark, Usha Hariharan

### <p align="center">Project Objectives

We are interested in learning more about a possible correlation between a company's AI initiatives and it's stock price and market valuation relative to overall market trends.

**Hypothesis: AI has signifigantly impacted the stock values and trading volumes for companies with AI development focus.** 

### Scope

Selected a time frame January 1, 2018 to October 1, 2024 and data files from four key companies.
The following companies data were selected for the analysis and compared against the S&P500.

**Apple(AAPL), Google(GOOGL), Microsoft(MSFT), Facebook/META(META)**
 
### Input

1697 data points collected for each stock for the time period defined above in the scope. 

### Major Events selected for Segmented Analysis

November 30, 2022 - Release of [ChatGPT](https://chatgpt.com/) by OpenAI with industry wide impact

March 31, 2023 - Release of [Gemini/Bard](https://gemini.google.com/app) by Google(GOOGL) 

November 1, 2023 - Release of [Copilot](https://copilot.microsoft.com/) + by Microsoft(MSFT)

### Output
The preformance was compared for total return for the time period and annualized return for time period and return from each event to the end and from total market from S&P500 for the same time period.

<div>

<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th></th>
      <th>Total Returns</th>
      <th>Annualized Returns</th>
      <th>Total Returns (ChatGPT)</th>
      <th>Total Returns (Gemini)</th>
      <th>Total Returns (Copilot+)</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>AAPL</th>
      <th>Close</th>
      <td>441.042627</td>
      <td>29.882271</td>
      <td>57.400528</td>
      <td>41.297761</td>
      <td>33.931137</td>
    </tr>
    <tr>
      <th>GOOGL</th>
      <th>Close</th>
      <td>209.072795</td>
      <td>21.534390</td>
      <td>64.224190</td>
      <td>59.886244</td>
      <td>31.158569</td>
    </tr>
    <tr>
      <th>MSFT</th>
      <th>Close</th>
      <td>400.639910</td>
      <td>28.192786</td>
      <td>68.652500</td>
      <td>49.254251</td>
      <td>24.339000</td>
    </tr>
    <tr>
      <th>FB</th>
      <th>Close</th>
      <td>215.533022</td>
      <td>26.201640</td>
      <td>384.707883</td>
      <td>170.095308</td>
      <td>83.562607</td>
    </tr>
    <tr>
      <th>S&amp;P 500</th>
      <th>Close</th>
      <td>113.756904</td>
      <td>13.287790</td>
      <td>41.233447</td>
      <td>40.229868</td>
      <td>35.976177</td>
    </tr>
  </tbody>
</table>
</div>


![image](https://github.com/user-attachments/assets/e8daea6b-2979-4cac-b322-db9920459207)

####  Volume Change as effect of ChatGPT release

<table border="1" class="dataframe">
  <thead>
    <tr>
      <th></th>
      <th>AAPL</th>
      <th>GOOGL</th>
      <th>MSFT</th>
      <th>FB</th>
    </tr>
    <tr>
      <th></th>
      <th>Volume</th>
      <th>Volume</th>
      <th>Volume</th>
      <th>Volume</th>
    </tr>
    <tr>
      <th>Date</th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>2022-11-29</th>
      <td>83763800</td>
      <td>20061700</td>
      <td>17956300</td>
      <td>23899200</td>
    </tr>
    <tr>
      <th>2022-11-30</th>
      <td>111380900</td>
      <td>43647500</td>
      <td>47594200</td>
      <td>43348600</td>
    </tr>
    <tr>
      <th>2022-12-01</th>
      <td>71250400</td>
      <td>28687100</td>
      <td>26041500</td>
      <td>36551400</td>
    </tr>
  </tbody>
</table>
</div>



#### Percentage Change in Volume as effect of ChatGPT release

<table border="1" class="dataframe">
  <thead>
    <tr>
      <th></th>
      <th>AAPL</th>
      <th>GOOGL</th>
      <th>MSFT</th>
      <th>FB</th>
    </tr>
    <tr>
      <th></th>
      <th>Volume(%)</th>
      <th>Volume(%)</th>
      <th>Volume(%)</th>
      <th>Volume(%)</th>
    </tr>
    <tr>
      <th>Date</th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>2022-11-29</th>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>2022-11-30</th>
      <td>32.970209</td>
      <td>117.566308</td>
      <td>165.055719</td>
      <td>81.380967</td>
    </tr>
    <tr>
      <th>2022-12-01</th>
      <td>-36.029966</td>
      <td>-34.275503</td>
      <td>-45.284299</td>
      <td>-15.680322</td>
    </tr>
  </tbody>
</table>
</div>

### Installation Instructions 

Prerequisites needed 
```
!pip install prophet
!pip install yfinance
# Dependencies
import pandas as pd
import os
from datetime import datetime
from pathlib import Path
%matplotlib inline
import matplotlib.pyplot as plt
import numpy as np
import yfinance as yf
```

---

##### Added csv files and pulled individual stock data and S&P 500 index
##### Google launched GEMINI - the AI chatbot - on March 31, 2023
##### Microsoft lauched Copilot+ on November 1, 2023

---

## <p align="center"> Summary


### Group Three’s Project involves analysis of US stock market data from 2018 to date to locate if salient correlations exist between major real-time AI innovation announcements and stock prices of MSFT, GOOG, FB, and AAPL.

### The methodology involves analyzing individual prices of these four against S&P index values from 2018 to date.

### Each company’s AI philosophy and corresponding investments are researched for contextual validity.

### Each company’s real-time stock price changes based on its AI investments and niche AI projects.

### Analyzed data is visualized in correlation tables and graphs, and values are expressed in percent changes.

### Based on analyses, projections, and estimates of stock valuation and their possible connections to AI initiatives represent key findings of the study.

### Events of specific relevance are OpenAI's release of ChatGPT on November 30, 2022, GOOGL's Gemini on March 31, 2023 and MSFT's Copilot+ launch on November 1, 2023.

### MSFT completed its acquisition of Nuance accelerating industry cloud strategy for healthcare in 2022

Added revised csv datasets from YahooFinance
Worked on Data exploration and analysis

---
### <p align="center"> Analysis

**<p align="center">- The stock pricing trend matched the overall market for these companies**

**<p align="center">- The total and annual returns were significantly higher than the S&P500 overall market return**

**<p align="center">- The returns were higher for returns for the prospective companies making the three AI announcments than the other companies**

**<p align="center">- The share return for Facebook/Meta was adnormally higher than the other comanpanies**

**<p align="center">- After each of the three AI announcments all of these shares significantly higher trading volume than the averages - most significant being after ChatGPT**

**<p align="center">- These spikes were higher for the respective companies that made the AI releases**

###### Data References 

- [yahoo finance](https://finance.yahoo.com/)

- [Kaggle (for S&P500)](https://www.kaggle.com/datasets/andrewmvd/sp-500-stocks)

- [alphavantage Co](https://www.alphavantage.co/)

---
