## Optimizing a Trading Portfolio using Random Forest and Python

**Project description:** For this project the task was simple, create an algorithm to trade a single stock, JPM (JP Morgan Chase), and have it outperform the S&P 500 for the timeframe chosen. To make this as realistic as possible, we chose to train our algorithm on data from January 1st, 2008 to December 31st 2009. Using a Random Forest structure, our algorithm would learn how to maximize its trading using 3 Technical Indicators: Relative Strength Index (RSI), Stochastic Oscillator Index (SOI) and Momentum (MOM). Using these 3, our algorithm would seek to maximize its value using max positions of +1000, 0, or -1000 shares. Trades could be in any form, as long as final position was conforming to the preceding rule. Following the training, the portfolio would simulate performance agianst the market by using an "out-of-sample" period. This time period would be from January 1st, 2010 to December 31st 2011. 

### 1. Framing the Problem

Initially, this may seem like a straight forward task, but implementation becomes complicated quick. First, we must determine what data to use and how to execute trades. Thankfully, we were given a data file that contained all stocks on the S&P 500 from 2000 to 2012. Using this as our source of data, we then used the adjusted close price as the value of stock at any given time, t. Adjusted close is the preferred price to use for portfolio learning, as it takes into account all adjustments, such as stock split, dividends and other corporate actions that affect price. 

```javascript
if (isAwesome){
  return true
}
```

### 2. Assess assumptions on which statistical inference will be based

```javascript
if (isAwesome){
  return true
}
```

### 3. Support the selection of appropriate statistical tools and techniques

<img src="images/dummy_thumbnail.jpg?raw=true"/>

### 4. Provide a basis for further data collection through surveys or experiments

Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium, totam rem aperiam, eaque ipsa quae ab illo inventore veritatis et quasi architecto beatae vitae dicta sunt explicabo. 

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).
