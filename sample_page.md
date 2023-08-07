## Optimizing a Trading Portfolio using Random Forest and Python

**Project description:** For this project the task was simple, create an algorithm to trade a single stock, JPM (JP Morgan Chase), and have it outperform the S&P 500 for the timeframe chosen using a starting cash balance of $100,000. To make this as realistic as possible, we chose to train our algorithm on data from January 1st, 2008 to December 31st 2009. Using a Random Forest structure, our algorithm would learn how to maximize its trading using 3 Technical Indicators: Relative Strength Index (RSI), Stochastic Oscillator Index (SOI) and Momentum (MOM). Using these 3, our algorithm would seek to maximize its value using max positions of +1000, 0, or -1000 shares. Trades could be in any form, as long as final position was conforming to the preceding rule. Following the training, the portfolio would simulate performance agianst the market by using an "out-of-sample" period. This time period would be from January 1st, 2010 to December 31st 2011.

### 1. Framing the Problem

Initially, this may seem like a straight forward task, but implementation becomes complicated quick. First, we must determine what data to use and how to execute trades. Thankfully, we were given a data file that contained all stocks on the S&P 500 from 2000 to 2012. Using this as our source of data, we then used the adjusted close price as the value of stock at any given time, t. Adjusted close is the preferred price to use for portfolio learning, as it takes into account all adjustments, such as stock split, dividends and other corporate actions that affect price. 

Following this, we then needed to break the problem into smaller steps. First, we need to read in the stock data. Second, we need to determine the SOI, RSI and MOM for that days stock data. Third, we need to develop a Random Forest Learner that translates those signals into buy, sell or hold trades. Fourth, we ned to execute those trades and record our portfolio balance. 

To illustrate the difference between the Random Forest strategy and human intuition, we decided to create to scripts. One script would follow the common wisdom regarding RSI, SOI and MOM. The other, would allow the RF Learner to determine when to buy and sell based on its in-sample learning of those indicators. 


### 2 MANUAL STRATEGY
For developing a strategy and assessing the results, the only asset that was used
was JPM. On top of this, all results were assessed against a benchmark of purchasing ūŪŪŪ shares of JPM and holding it, plus the difference of a $ūŪŪ,ŪŪŪ cash
position. Our goal was to create a strategy that could outperform the buy and
hold strategy by using the technical indicators discussed above.

For deriving a basic strategy on the indicators, we looked to the common consensus about RSI, SOI and momentum. Using a set ūŮ day window, and the given
price bands, we developed a formula to indicate when we should enter a long or
short position of the stock.
'''
𝑆𝑒𝑙𝑙 = 𝑅𝑆𝐼 > ͚͙65 & (𝑆𝑂𝐼 > ͙͛75 𝑜𝑟 𝑀𝑜𝑀 < 0 ͔)
𝐵𝑢𝑦 = 𝑅𝑆𝐼 < ͖͔65 & (𝑆𝑂𝐼 < ͖͙75𝑜𝑟 𝑀𝑜𝑀 > ͔0 )
'''
Our general thought was that we should tune SOI and MoM together, so that our
algorithm was not super sensitive to price changes. SOI can vary rapidly as we
learned in our analysis during previous workings. Because of this, we tied it to Momentum
so that it would be pulled down. 


### 3. Support the selection of appropriate statistical tools and techniques

<img src="images/dummy_thumbnail.jpg?raw=true"/>

### 4. Provide a basis for further data collection through surveys or experiments

Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium, totam rem aperiam, eaque ipsa quae ab illo inventore veritatis et quasi architecto beatae vitae dicta sunt explicabo. 

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).
