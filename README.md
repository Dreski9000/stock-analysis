# stock-analysis
Used for Module 2 of UCB Data Science Bootcamp

### Project Overview
The purpose of this project is to create a VBA script that is capable of automating basic 
stock analysis by calculating annual aggregate trade volumes and aggregate annual returns for a
set of stocks and given years. In this set, the dataset includes a selected dozen biotech companies
along with company tickers, daily trade volumes, daily opening prices, and daily closing prices. 
Another purpose of this analysis is to analyze how a refactored code might improve efficiency and
runtime of the program.

### Results
The biotech sector as a whole (based on the included set of tickers) appears to have had a phenomenal
performance in the year of 2017, with as many as 4 out of 11 analyzed tickers getting annulized returns
greater than 100%. Only one company (TERP) had a negative return of -7%, and only one other company had 
a return less than 10% (RUN). 
![2017 Volumes and Returns](https://raw.githubusercontent.com/Dreski9000/stock-analysis/main/Resources/sa_formatted_2017.png)
2018 paints a different picture for the green industry, with 9 our of 11 company tickers returning
a negative percentage yield, and only two (ENPH, RUN) companies returning positive, albiet spectacular results.
![2018 Volumes and Returns](https://raw.githubusercontent.com/Dreski9000/stock-analysis/main/Resources/sa_formatted_2018.png)

When comparing the execution time of the original analysis script and the refactored version of the 
script, there is a very significant improvement in runtime: the refactored code runs around 40x faster
than the non-refactored version of the script. This is likely because the original script / algorithm
has to loop through the entire set of data for each ticker and each calculation, but the refactored 
version only needs to perform the loop once and stores the relevant data in array data structures; 
effectively sacrificing a small amount of memory for a huge improvement in runtime execution.
![Original Version](https://raw.githubusercontent.com/Dreski9000/stock-analysis/main/Resources/sa_original_2017.png)
![Refactored Version](https://raw.githubusercontent.com/Dreski9000/stock-analysis/main/Resources/sa_refactored_2017.png)

### Summary
The only drawback of refactoring code is the time that it takes time, but the benefits are better readability
and potentially major improvements in runtime execution. I did accidentally introduce a couple of bugs while
working on refactoring the code; they were typos; this can be taken into consideration while refactoring code,
but the improvements in runtime execution were like night and day; the refactored code ran almost instantly vs
the original code took almost half a minute to finish executing.

