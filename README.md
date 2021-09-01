# Your Personal Financial Planner

![image](https://user-images.githubusercontent.com/80294571/130264699-5f7795f0-9dc8-4b0a-a411-6f57328a4862.png)

## Table of Contents:
[Background](https://github.com/jharvey09/Your_Personal_Financial_Planner#background)

[Steps](https://github.com/jharvey09/Your_Personal_Financial_Planner#steps)

[Resources](https://github.com/jharvey09/Your_Personal_Financial_Planner#resources)

[Steps_Breakdown](https://github.com/jharvey09/Your_Personal_Financial_Planner#steps_breakdown)

[Retirement Planning](https://github.com/jharvey09/Your_Personal_Financial_Planner#retirement-planning)

[Summary](https://github.com/jharvey09/Your_Personal_Financial_Planner#summary)

### Index:
[Collect Crypto Prices Using the *requests* Library](https://github.com/jharvey09/Your_Personal_Financial_Planner#collect-crypto-prices-using-the-requests-library)

[Collect Investments Data Using Alpaca: SPY (stocks) and AGG (bonds)](https://github.com/jharvey09/Your_Personal_Financial_Planner#collect-investments-data-using-alpaca-spy-stocks-and-agg-bonds)

[Savings Health Analysis](https://github.com/jharvey09/Your_Personal_Financial_Planner#savings-health-analysis)

[Retirement Analysis](https://github.com/jharvey09/Your_Personal_Financial_Planner#retirement-analysis)

##### Current value of Bitcoin & Ethereum portfolio:
![image](https://user-images.githubusercontent.com/80294571/131722065-210e3df3-9665-4dfb-ab28-6ff3a56746d8.png)

##### Current value of AGG/SPY portfolio:
![image](https://user-images.githubusercontent.com/80294571/131722464-80772c8e-752c-4ec0-bd72-29612f72e523.png)

  
### Background:
In this project, I will use Python to create two tools, assisted by other functions; and libraries used for financial planning. I'm building a **"Personal Finance Planner";** that allows users to visualize their savings composed by investments split between shares and cryptocurrencies. 

The first will be a *personal finance planner* that will allow users to visualize their savings composed by investments in shares and cryptocurrencies to assess if they have enough money as an emergency fund.
The second tool will be a retirement planning tool that will use the **Alpaca API** to fetch historical closing prices for a retirement portfolio composed of stocks and bonds, then run **Monte Carlo simulations** to project the portfolio performance at 30 years. I will then use the Monte Carlo data to calculate the expected portfolio returns given a specific initial investment amount.

### Steps:
To develop the personal finance planner prototype, you need the following information to compose the analysis:
The average household income for each member of the credit union is $12,000.
Every union member has a savings portfolio composed of cryptocurrencies, stocks, and bonds:
Assume the number of crypto assets: 1.2 BTC and 5.3 ETH.
Assume the shares in stocks and bonds: 50 SPY (stocks) and 200 AGG (bonds).
##### Collect Crypto Prices Using the *requests* Library:
First, Create two variables called my_btc and my_eth. Set them equal to 1.2 and 5.3, respectively. Use the requests library to fetch the current price of US dollars of bitcoin *(BTC)* and ethereum *(ETH)*, using the Alpaca API. Parse the API JSON response to select only the crypto prices and store each as a variable. Compute the portfolio value of cryptocurrencies and print the results.
##### Collect Investments Data Using Alpaca: SPY (stocks) and AGG (bonds):
***"Important: Remember to create a _.env file_ in your working directory to store the values of your Alpaca API key and Alpaca secret key."***
First, create two variables named my_agg and my_spy and set them equal to 200 and 50, respectively. Set the Alpaca API key and secret key variables, then program the Alpaca API object using the *tradeapi.REST* function from the *Alpaca SDK*. Format the current date as ISO format. Change the date set to the current date. Next, get the current closing prices for SPY and AGG using Alpaca's *get_barset()* function. Transform the function's response to a Pandas DataFrame and preview the data. Pick the SPY and AGG close prices from **Alpaca's _get_barset()_ DataFrame** response and store them as Python variables. Print the closing values for validation. Compute the value in dollars of the current amount of shares and print the results.

#### Savings Health Analysis:
In this section, I will assess the financial health of the credit union's members. First, I will create a variable called *monthly_income* and set the value at 12000. I want to create a DataFrame to analyze savings health, called df_savings. It will consist of two rows, first row will hold crypto assets the other row will hold the total value of shares. The DataFrame will house one column named *amount* with two rows for crypto and shares are index values.
##### Savings Health Analysis Visual:

![image](https://user-images.githubusercontent.com/80294571/131722568-eb63f78e-9517-4dfb-ab01-4696c4c93be6.png)

#### Steps_Breakdown:
1. Collect Crypto Prices Using *(requests)* Library
2. The Alpaca Markets API was used to pull historical stocks and bonds information
3. An *"Emergency Fund"* can be created by taking the monthly salary and multilplying it by 3 months
4. Collect Investment Data Using Alpaca: SPY/ AGG Stocks
5. Saving Health Analysis
6. Run Monte Carlo Simulation
7. Retirement Analysis

Current value of Bitcoin & Ethereum portfolio

![image](https://user-images.githubusercontent.com/80294571/131722065-210e3df3-9665-4dfb-ab28-6ff3a56746d8.png)

Current value of AGG/SPY portfolio

![image](https://user-images.githubusercontent.com/80294571/131722464-80772c8e-752c-4ec0-bd72-29612f72e523.png)

Savings Health Analysis:

![image](https://user-images.githubusercontent.com/80294571/131722568-eb63f78e-9517-4dfb-ab01-4696c4c93be6.png)

Plotted to a Pie Chart:

![image](https://user-images.githubusercontent.com/80294571/131725253-e63f458a-3621-4a07-b477-d9c1eea6bd5a.png)


### Retirement Planning:
#### Monte Carlo Simulation:
For this portion, use the Alpaca API to fetch historical closing prices for a retirement portfolio and then use the MCForecastTools toolkit to create Monte Carlo simulations to project the portfolio performance at 30 years. Use the Alpaca API to fetch five years of historical closing prices for a traditional 40/60 portfolio using the SPY and AGG tickers to represent the 60% stocks (SPY) and 40% bonds (AGG) composition of the portfolio. Make sure to convert the API output to a DataFrame and preview the output. Configure and execute a Monte Carlo Simulation of 500 runs and 30 years for the 40/60 portfolio. Plot the simulation results and the probability distribution/confidence intervals.
#### Retirement Analysis:
Fetch the summary statistics from the Monte Carlo simulation results. Make the initial investment $20,000, calculate the expected portfolio returns in dollars at the 95% lower and upper confidence intervals. Calculate the portfolio returns at the 95% lower and upper confidence intervals based on a 50% increase in the initial investment.

##### Retirement Planning-Monte Carlo Simulation Outcomes:

![image](https://user-images.githubusercontent.com/80294571/130265959-4ad8b38c-7fac-4275-a47c-bd3f8857fcf2.png)

### Personal Savings Analysis:

![image](https://user-images.githubusercontent.com/80294571/130266195-b24a721a-f769-47b0-aa44-ae3f0e5ef82a.png)

#### Bar Graph:

![image](https://user-images.githubusercontent.com/80294571/130266354-6e5b85a8-8554-471a-ac6e-7a1f9c4d725b.png)

### Summary:
I adjusted the portfolio to either include more risk (a higher stock than bond ratio) or maximize the initial investment and rerun the retirement analysis to see what it would take to retire in 5 or 10 years instead of 30!
Calculate the five years worth of historical data used for SPY & AGG with the aide of the Alpaca API applying the **(get_barset())** function. as well as the Monte Carlo simulation configuration that was adjusted to 30 years *(MCForecastTools)*
#### Short Term Retirement Projections-Monte Carlo Simuations (Line Plots):
##### 10 Year Simulation: 

![image](https://user-images.githubusercontent.com/80294571/130267586-1a45fc8d-bb40-4d15-b0fd-0d3248237e99.png)


##### 5 Year Simulation:

![image](https://user-images.githubusercontent.com/80294571/130267153-1e56bb6f-b33d-4d39-b0da-9c8250f0acdd.png)

### Resources:
1. Alpaca Markets API
2. Alternative Free Crypto API



