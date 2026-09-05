# Redfin-Housing-Analytics

## Project Overview
Scraped active real-estate listings for Tampa, FL directly off Redfin's search results and turned them into a price-vs-square-footage analysis.

## Tools
Python, curl_cffi, BeautifulSoup, Pandas, Matplotlib, Seaborn, regex.

## Cleaning
- Stripped `$` signs and commas from price strings and cast them to float
- Pulled numeric bed/bath/square-footage values out of mixed text fields
- Split the combined address field into street, city, state, and zip code


## What the data showed
- Price distribution is right-skewed — most listings sit at a predictable baseline tier, with a long tail of high-end properties pulling the average up.
- Price vs. square footage has a strong, clean positive relationship — square footage does most of the work in explaining price in this market.
- One $14M listing looked like a clear outlier, but comparing the median price with and without it showed it wasn't distorting the broader comparison, so I kept it in rather than dropping it.
- Bedroom count alone is a much weaker price predictor than raw square footage — space matters more than room count.

## Getting Started
1. Clone the repository: `git clone https://github.com/Shaikh-Mazher01/Redfin-Housing-Analytics.git`
2. Install dependencies: `pip install curl_cffi beautifulsoup4 pandas matplotlib seaborn`
3. Run the engine: `Redfin_Scrapping.ipynb`

## Sample Insights
* Successfully extracted and parsed hundreds of live property data points without triggering IP bans.
* Identified distinct geographic clusters where price-per-square-foot deviated significantly from the city median.

## Limitation
 
This is a single-run snapshot of a limited slice of Tampa listings, capped by Redfin's anti-bot block — not a large-scale or continuously refreshed dataset. Treat the findings as directional for this market segment, not a market-wide conclusion. A production version of this would need proxy rotation or a scheduled, lower-frequency crawl to get past the page-7 wall consistently.
