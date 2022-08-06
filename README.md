# NETWORK-OF-INFLUENCE-ON-THE-STOCK-MARKET-AND-ITS-IMPACT-ON-RISK-ANALYSIS
The goal of this research is to better understand the relationships between cryptocurrencies  and stock indexes, including how cryptocurrencies are interconnected. Preliminary  visualization revealed a trend of market movement across all cryptocurrencies, indicating a  substantial correlation. Initial analysis focusses on finding the correlation between the stock  indexes and cryptocurrencies value returns. Another objective is to study the volatility of the  asset value measured by standard deviation of each asset for a short period and to further  calculate the correlation between them. In order to express relationships between assets in a  pictorial format, graphs are used. The assets are represented by the graph vertices, and the  relationships between them are shown by edges in the graph. Further, centrality is crucial in  identifying important nodes. Two measures will be considered, Eigen-vector centrality (measuring likelihood of visitation to a node) and betweenness centrality (counting the  instance in which counts the instances in which a node acts as a bridge facilitating the  quickest and shortest route between two nodes). The tests were carried out on four indexes (three stock indexes and one crypto index) and six well-known cryptocurrencies based on  the quantity and accessibility of historical trading data. The results of the research based on  the time series of price returns, points to a strong relationship between Ethereum and  Bitcoin in cryptocurrencies, but Dow Jones and S&amp;P 500 have the strongest correlation  when it comes to stock indices. The moving average of volatility showed that cci30 is  highly volatile compared to other stock indexes and all six crypto currencies are highly  volatile. The network graph demonstrates the interconnectedness and clustering of the  selected cryptocurrency currencies. It’s evident that Bitcoin functions as a central node,  which means it has the highest likelihood of appearing on a random path in the graph.

# Methodology

## Data collection

The primary data collection process includes collection historic trading data of six crypto 
currencies namely Cardano (ADA), Bitcoin (BTC), Ethereum (ETH), Binance (BNB),
Dogecoin (DOGE), Ripple (XRP) (source: Yahoo Finance). The choice of these six 
cryptocurrencies follows a three-tier approach of top, middle and lower tier currencies 
(Gandal 2016), (Bouri 2017a). "Top-tier" cryptocurrencies include Bitcoin, and Ethereum, 
which have market capitalizations over 100B USD. Ripple and Cardano with market 
capitalizations under 100B USD but greater than 30B USD (Yahoo finance). Lower tier 
currencies are Litecoin and Dogecoin with market capitalizations below 30B USD.Three 
stock market indexes NASDAQ(IXIC), Dow Jones (DJI), SP500(GSPC) and a crypto 
market index Cryptocurrency index (cci30). The data included volume, open, high, low, 
closing and dates. 
Most people view the S&P 500 (The Standard and Poor's 500 is a stock market index 
tracking the stock performance of 500 large companies listed on US exchanges) as a crucial 
benchmark index for the American stock market and overall global economy. In addition to 
Dow Jones, which until recently served as the primary indicator of the U.S. economy's 
health but only comprises 30 firms and is confined with in the short number of industries it 
covers and Nasdaq which is a capitalization-weighted index with more than 3,000 equities 
as constituents, which means that it assigns weightings based on the market caps of the 
individual companies. Whereas the selected cryptocurrencies are from the top traded list of 
cryptocurrencies curated to the availability of historic data on the analysis time frame.
The Cci30 is a regulations-based index that is intended to quantify the overall development, 
daily movement, and long-term movement of the blockchain industry objectively. It 
achieves this by keeping track of the 30 biggest cryptocurrencies, omitting stable coins, by 
market capitalization. Crypto and stock datasets were downloaded from yahoo finance 
whereas cryptocurrency index data was downloaded from cci30 website (cci30). All data 
was collected in csv format

## Data pre-processing

After defining the Time period, which is considered for this analysis, all data is imported to 
Mathematica notebook. As part of understanding data, the raw data is plotted in Table form
and the dimensions of the data is checked as all data should be in same dimension for 
further analysis. The data required for initial analysis is the Date and the Closing price. So, a 
function is defined to clean the data and select the date and closing value as the raw data had
unwanted columns. Using this ‘deleteColumn’ function all non-essential columns are 
deleted. This clean data is then analysed in table form and the header strings “Dates” and 
“Closing” at the first row is removed using part function and from the resultant clean data,
as it’s string value and will not go well with the timeseries creation. A timeseries (a list of 
values, such as x1, x2 or a list of time-value pairs, such as (t1, x1), (t2, x2),) is formed. Here 
the values for xi are closing value and ti are dates.

# Plotting Data
The Timeseries of all crypto data are grouped into a list and all indexes into another for 
better visualisation. ’DateListPlot’ (also known as a time series plot, that traverse value vi
sequentially from left to right. Irrespective of the data's original sequence, the line presents 
the dates in chronological order before presenting the data). This is used as an initial analysis method to find if there are any trends. Then Histogram is plotted adjacently to 
respective list plots to compare the frequencies of those values, attached to each bin.




There is a clear connection between all three stock indexes as expected specifically SP500 
and Nasdaq where both indexes had a steady growth till the pandemic from where it drops 
and then gain back its momentum whereas for Dow jones it is evident that there is a bigger
dip due to pandemic. Less diversification and number of stocks compared to the former 
indexes could be one reason. Contrary to comparatively stable stock indexes, the cci30 
remains unstable. It is apparent that the crypto index hit its high thriving on the pandemic 
instabilities in stock market. This could be an initial indicator of the flow of wealth from 
stock to crypto. Over the period, this crypto bull market plummeted to its all-time low from 
2021.

The plot of all Six cryptocurrencies shows a similar trend. All six currencies show Rapid 
increase from 2021 reaching their all-time. After which had a dramatic drop down on their 
price in 2022

## Correlation
Correlation examines how two variables vary in relation to each other to determine the link, 
or association, between them. Statistical correlation is also defined as the simultaneous 
change of two variables and is often depicted by linear correlations. Correlation does not 
always imply causality. This is because a correlation does not mean that a set of variables 
cause each other to change; rather, it only shows how they are related. A positive correlation 
indicates that this linear relationship is positive and that the two variables are increasing or 
decreasing in the same direction. A negative correlation is the inverse of a positive 
correlation, in which the connection has a negative coefficient, and the variables vary in 
opposite ways.
The correlation coefficient is an important statistical indicator of a correlation and how the 
two variables are indeed correlated (or not). The number, which is represented by letter r, 
falls between -1 and +1.
Pearson correlation coefficient formula is the most used correlation measurement. The 
coefficient (r), which must have a value between -1 and +1, is used to indicate the linear 
relationship between two variables x and y.
ρ (x, y) = Σ[(xi – x̄) * (yi – ȳ)] / (σx * σy)
Where, x̄ = Mean of x variable, ȳ = Mean of y variable. Standard Deviation of x is 
calculated as x = (xi – x̄) and y = (yi – ȳ).
To justify the dates of evaluation, the crypto data is further reduced to business days data as,
stock market runs only on weekdays using TimeSeriesResample function (commonly used 
to change inconsistent time series to steady ones. Aligning time series is another application 
for this). The dates are stored in a variable and a new list is created with all timeseries. The
dimensions of these dataset are rechecked before proceeding to correlation. The data set is 
transposed and checks for correlation and is plotted.

