# BalanceSheetWebScrapeinR
Extract Federal Reserve Balance Sheet (Assets Section) for Panel Analysis

A prototype scraper for balance sheet components in R. Once release dates for the Federal Reserve's balance sheet have been obtained (every Thursday around 4:30PM EST, unless Thursday is a federal holiday), it compiles the URL where each release can be found. Once the URL is constructed and read, the balance sheet is parsed to find the assets section, extracting each component until it reaches total assets. The extracted section is then cleaned and structured to generate a user-friendly data frame in which the row names represent the asset class and the observation represents that week's value.

The balance sheet data itself consists of ~300-700 rows of character strings (asset and liability names, supplemental notes) and numeric data (balances, week-to-week changes, adjustments, etc.). Overall, 582 balance sheet reports were scraped, and ~17-32 rows from those balance sheets retained.

The provisional objective of the project is to automate the analysis of balance sheets of publicly traded companies, data which is available via the SEC's EDGAR database.

This version uses base R; a streamlined version using several R packages is in the works.
