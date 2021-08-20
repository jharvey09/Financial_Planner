# Your Personal Financial Planner
This project was created in Python using two tools that are used for financial planning. Creating a Personal Finance Planner that allowed users to visualize their savings composed by investments split between shares and cryptocurrencies. 
Also creating a Retirement Planning Tool that will use the Alpaca API to grab historical closing prices for a projected retirement portfolio composed of stocks and bonds, later running a few different Monte Carlo simulations to project the portfolio performance at 30 years. 

![image](https://user-images.githubusercontent.com/80294571/130264699-5f7795f0-9dc8-4b0a-a411-6f57328a4862.png)

# Resources:
1. Alpaca Markets API
2. Alternative Free Crypto API

### Steps:
1. Collect Crypto Prices Using [requests] Library
2. The Alpaca Markets API was used to pull historical stocks and bonds information
3. An "Emergency Fund" can be created by multilplying 3 months of salary
4. Collect Investment Data Using Alpaca: SPY/ AGG Stocks
5. Saving Health Analysis
6. Run Monte Carlo Simulation
7. Retirement Analysis

#### Retirement Planning:
To calculate the five years worth of historical data used for SPY & AGG with the aide of the Alpaca API applying the [get_barset()] fucntion. as well as the Monte Carlo simulation configuration that was adjusted to 30 years [MCForecastTools]

##### Retirement Planning-Monte Carlo Simulation Outcomes:
![image](https://user-images.githubusercontent.com/80294571/130265959-4ad8b38c-7fac-4275-a47c-bd3f8857fcf2.png)


### Personal Savings Analysis:
![image](https://user-images.githubusercontent.com/80294571/130266195-b24a721a-f769-47b0-aa44-ae3f0e5ef82a.png)

#### Bar Graph:
![image](https://user-images.githubusercontent.com/80294571/130266354-6e5b85a8-8554-471a-ac6e-7a1f9c4d725b.png)

## Short Term Retirement Projections-Monte Carlo Simuations [Line Plots]:
#### 10 Year Simulation: 
![image](https://user-images.githubusercontent.com/80294571/130267586-1a45fc8d-bb40-4d15-b0fd-0d3248237e99.png)



#### 5 Year Simulation:
![image](https://user-images.githubusercontent.com/80294571/130267153-1e56bb6f-b33d-4d39-b0da-9c8250f0acdd.png)



