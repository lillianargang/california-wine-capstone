## California Wine Trends

This project analyzes California wine grapes using USDA Excel sheet data and Google Trends API to uncover patterns and insights in wine popularity over time.


To visualize changes, it is recommended you create linecharts to answer questions over time and barcharts for overall quantities. To do this, you will need matplotlib and seaborn.

Excel:
The Excel data must remain in the data folder in order to function properly. How to:
1. Place all Excel data files inside the data folder.
2. Name your unique file path accordingly in the file_path variable.

Google Trends:
Google Trends API requires a simple set-up. You will first install pytrends if you have not already, and the code will run accordingly.
https://pypi.org/project/pytrends/

Rolling averages are best for smoothing the mass of data that Google Trends API will pull for you. .rolling() with a window of 12 (12 months in a year) is ideal.
https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.rolling.html


Key Terms:
Bearing Acreage - Used to describe any vine that can produce grape, and enter the market. Used most of the time.
Non-Bearing Acreage - Used to understand new interest in grape production. i.e. an increase in plantings supposes an interest in investment in that grape variety.
Total Acreage - Used to describe total interest in a grape over time, only used for broad analysis.

Variety - The type of grape
County - Where the grape is grown in California

EDA
1. What is the Total Bearing Acreage for all years, across all varieties?
2. How many unique varieties are found in each county, across all years?
3. By year, how many unique varieties are found in each county?
4. Over 20 years, there are 12 grapes that alternate as being within the Top 10 varieties with the highest bearing acreage. What are those grapes? (Note: DO NOT use aggregated totals such as TOTAL WINE or TOTAL RED/WHITE, OTHER WINE or OTHER RED/WHITE)
5. What's the total bearing acreage per year, for each of the Top 12?

Data Questions (USDA Wine Acreage)
1. What is the bearing acreage per year for Pinot Noir and Merlot? What is the non-bearing acreage per year?
2. Note increases or decreases for Pinot and Merlot. We will compare them to two of the Top Varieties, for context. How does Merlot's bearing acreage trajectory compare to Chardonnay? What about Pinot to Cabernet Sauvignon?
3. What is the absolute difference in acreage changes, for Pinot, Merlot, Chardonnay, and Cabernet? What is the mean difference (average increase or decrease in acreage) for each of these grapes? Do the same for percent changes, checking how each year compares to the last.
4. Create a scatterplot for bearing acreage percents for Pinot and Merlot, and see what it looks like. From there, use .corr() to determine if there is a mathmatical correlation between Pinot's changes and Merlot's changes in percent over time.

Data Questions (Google Trends API)
1. Of the grapes in the project (Pinot, Merlot, Cabernet, Chardonnay), does their seach history appear to rise/fall with bearing acreage, or not? If you are curious about other grapes, you can check.
2. Of the Top Varieities, are there any grapes that also seem to rise/fall with their given bearing acreage?