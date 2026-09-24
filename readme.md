Data Science Tools and Techniques
Technical Analysis Using R
Name: Rubeena Khera
Course: Data Science Tools and Techniques
Assignment: Technical Analysis Using R, Development Phase
Repository: https://github.com/kherainfo-lgtm/Technical-Analysis-Using-R.git

1. Project Overview
Several technical analysis indicators have been implemented in R.

The aim of the current assignment is to show the understanding of technical indicators, their calculation process, and how they are implemented in R. The implementation of the functions was based on the templates provided in the assignment.

Standard R/core functions have been used in the implementation and no technical analysis libraries have been utilized.

2. Technical Indicators Implemented
The following functions have been implemented:

Simple Moving Average (SMA) – sma()
Exponential Moving Average (EMA) – ema()
Moving Average Convergence Divergence (MACD) – macd()
Standard Deviation – stdev()
Linear Regression – linreg()
Relative Strength Index (RSI) – rsi()
Stochastic RSI (StochRSI) – stoch_rsi()
Crossover – crossover()
Crossunder – crossunder()
3. Repository Structure
The repository contains separate R script files for each technical indicator.

BDA400_Assignment5/

── sma.R
── ema.R
── macd.R
── stdev.R
── linreg.R
── rsi.R
── stoch_rsi.R
── crossover.R
── crossunder.R
── test_assignment.R
── README.md

4. Requirements
The project requires:

R or RStudio
No external technical-analysis packages are required.
The functions are implemented using standard/base R functionality.
5. How to Run the Project
Step 1 – Open the Project
Open the project folder in RStudio.

Step 2 – Set the Working Directory
Make sure the working directory is the folder containing the R files.

The working directory can be checked using:

getwd()

Step 3 – Run the Test File
Open:

test_assignment.R

Run the script using the Source button in RStudio.

The test file loads the individual R scripts and executes the implemented functions.

6. Function Descriptions
6.1 Simple Moving Average – sma()
The Simple Moving Average calculates the average of a specified number of consecutive data points.

The calculation is:

SMA = Sum of values in the period / Number of values

The implementation calculates each window manually using a loop and returns a vector containing the SMA values.

6.2 Exponential Moving Average – ema()
The Exponential Moving Average gives greater importance to recent observations.

The multiplier is calculated as:

Multiplier = 2 / (Period + 1)

The first data value is used as the initial EMA. Subsequent EMA values are calculated using the previous EMA and the current data value.

6.3 Moving Average Convergence Divergence – macd()
MACD uses two exponential moving averages.

The MACD line is calculated as:

MACD Line = Short EMA - Long EMA

The signal line is calculated by applying an EMA to the MACD line.

The histogram is calculated as:

Histogram = MACD Line - Signal Line

The function returns the MACD line, signal line, and histogram as a list.

6.4 Standard Deviation – stdev()
The standard deviation measures the amount of variation in a dataset.

The implementation:

Calculates the mean.
Calculates the difference between each value and the mean.
Squares each difference.
Calculates the variance.
Takes the square root of the variance.
The population standard deviation formula specified in the assignment is used.

6.5 Linear Regression – linreg()
The linear regression function calculates a straight-line relationship between the index values and the supplied data.

The regression equation is:

y = β0 + β1x

where:

β0 is the intercept.
β1 is the slope.
x represents the index values.
y represents the source data.
The function returns the slope, intercept, and predicted regression values.

6.6 Relative Strength Index – rsi()
RSI is a momentum indicator used to identify potential overbought and oversold conditions.

The implementation:

Calculates differences between consecutive data points.
Separates gains and losses.
Calculates initial average gains and losses.
Applies Wilder's smoothing method.
Calculates the Relative Strength value.
Calculates RSI.
The RSI formula is:

RSI = 100 - (100 / (1 + RS))

6.7 Stochastic RSI – stoch_rsi()
Stochastic RSI combines RSI with stochastic calculations.

The implementation first calculates RSI and then normalizes the RSI values between 0 and 1.

The %K line is calculated using the SMA function, and the %D line is calculated as an SMA of the %K values.

The function returns both %K and %D as a list.

6.8 Crossover – crossover()
The crossover function compares two arrays and identifies when the first array crosses the second array.

Possible results are:

"Up"
"Down"
"None"

An "Up" signal occurs when the first array moves from below or equal to the second array to above it.

A "Down" signal occurs when the first array moves from above or equal to the second array to below it.

6.9 Crossunder – crossunder()
The crossunder function identifies when the first array moves from being greater than or equal to the second array to being below it.

The function returns:

"True"
"False"

A "True" value indicates that a crossunder occurred at that position.

7. Testing
The test_assignment.R file is included to test the implemented functions.

The testing process verifies that:

The functions can be loaded successfully.
The functions accept the required inputs.
The calculations produce results.
The functions return the expected data structures.
Invalid input conditions are handled where applicable.
The individual functions can also be tested directly in RStudio.

For example:

source("sma.R")

data <- c(10, 12, 15, 20, 18)

sma(data, period = 3)

8. Implementation Constraints
Implementations have been made without any use of third-party technical-analysis library functions.

Third-party library functions such as technical analysis functions of TTR, quantmod or similar libraries were not used to implement the indicators.

All the implementations have been done using R built-in functions and loops following the assignment pseudocode.

9. Conclusion
This assignment highlights the implementation of commonly used financial technical indicators and statistical calculations in R programming.

This project offers separate functions for calculation of moving average, MACD, standard deviation, linear regression, RSI, Stochastic RSI, crossover and crossunder calculations.

These functions have been tested using sample data and have been put in separate R files as per assignment guidelines.