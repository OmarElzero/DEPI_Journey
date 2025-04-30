# Python Project for Data Science Quiz

## Web Scraping and APIs

1. **What Python library is primarily used for parsing HTML and XML documents during web scraping?**
   - [ ] Pandas
   - [ ] Requests
   - [x] BeautifulSoup
   - [ ] Scrapy

2. **Which Python library is commonly used to make HTTP requests to web servers?**
   - [ ] HTML5lib
   - [x] Requests
   - [ ] BeautifulSoup
   - [ ] HTTPParser

3. **In web scraping, what does the `find_all()` method in BeautifulSoup do?**
   - [ ] Finds the first occurrence of an element
   - [x] Finds all occurrences of specified elements
   - [ ] Finds all links on a webpage
   - [ ] Finds all images on a webpage

4. **What is the correct way to create a BeautifulSoup object from an HTML document?**
   ```python
   response = requests.get('https://example.com')
   ```
   - [ ] `soup = BeautifulSoup(response)`
   - [x] `soup = BeautifulSoup(response.text, 'html.parser')`
   - [ ] `soup = BeautifulSoup.parse(response.content)`
   - [ ] `soup = BeautifulSoup.read_html(response.text)`

5. **What is an API in the context of data collection?**
   - [ ] A programming language used for data analysis
   - [x] A set of rules and protocols that allow different software applications to communicate with each other
   - [ ] A database management system
   - [ ] A web scraping tool

6. **What format is most commonly returned by modern web APIs?**
   - [ ] XML
   - [ ] CSV
   - [x] JSON
   - [ ] HTML

7. **What Python library is commonly used to handle and parse JSON data?**
   - [ ] BeautifulSoup
   - [ ] XMLParser
   - [ ] JSONParser
   - [x] The built-in `json` module

8. **Which pandas function directly reads HTML tables from a webpage into DataFrames?**
   - [ ] `pd.read_html_tables()`
   - [ ] `pd.scrape_tables()`
   - [x] `pd.read_html()`
   - [ ] `pd.parse_html()`

9. **What does the HTTP status code 429 typically indicate when making API requests?**
   - [ ] Success
   - [ ] Server error
   - [ ] Resource not found
   - [x] Too many requests (rate limiting)

10. **What is the purpose of the `yfinance` library?**
    - [ ] To create financial visualizations
    - [x] To access financial market data from Yahoo Finance
    - [ ] To predict stock prices using machine learning
    - [ ] To manage financial databases

11. **What ethical consideration is important when scraping websites?**
    - [ ] Always scrape as much data as possible
    - [ ] Ignore the website's terms of service
    - [x] Respect the website's robots.txt file and rate limits
    - [ ] Share scraped data with as many people as possible

12. **When storing API credentials in a Python script, what is the best practice?**
    - [ ] Hard-code them directly in the script
    - [ ] Share them in public repositories
    - [x] Store them in environment variables or a separate configuration file
    - [ ] Include them in code comments

13. **What is a common way to handle pagination when scraping websites with multiple pages of content?**
    - [ ] Only scrape the first page
    - [x] Use a loop to iterate through page numbers in the URL
    - [ ] Create a new scraper for each page
    - [ ] Manually copy and paste content from each page

14. **Which of the following is NOT a common challenge in web scraping?**
    - [ ] Websites with dynamic content loaded via JavaScript
    - [ ] Websites with anti-scraping measures
    - [ ] Websites that frequently change their HTML structure
    - [x] Websites with too much static content

15. **What is the purpose of adding a delay between requests when scraping a website?**
    - [ ] To give your computer time to process the data
    - [x] To avoid overwhelming the server and potentially being blocked
    - [ ] To save battery power
    - [ ] To allow time for the internet connection to stabilize

## Answer Key
1. BeautifulSoup
2. Requests
3. Finds all occurrences of specified elements
4. `soup = BeautifulSoup(response.text, 'html.parser')`
5. A set of rules and protocols that allow different software applications to communicate with each other
6. JSON
7. The built-in `json` module
8. `pd.read_html()`
9. Too many requests (rate limiting)
10. To access financial market data from Yahoo Finance
11. Respect the website's robots.txt file and rate limits
12. Store them in environment variables or a separate configuration file
13. Use a loop to iterate through page numbers in the URL
14. Websites with too much static content
15. To avoid overwhelming the server and potentially being blocked