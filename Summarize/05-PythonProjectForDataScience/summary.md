# Python Project for Data Science

## Introduction to Data Collection

Data collection is a fundamental step in any data science project. Before any analysis can be performed, you need to gather the relevant data. This module covers various methods of data collection:

- **Database**: Retrieving data from structured databases
- **Open Source**: Using publicly available datasets
- **Data Companies**: Purchasing data from specialized providers
- **APIs (Application Programming Interfaces)**: Accessing data programmatically through web services
- **Web Scraping**: Extracting data directly from websites

## APIs for Data Collection

### What are APIs?
An API (Application Programming Interface) is a set of rules and protocols that allows different software applications to communicate with each other. In data science, APIs enable you to retrieve data from external services in a structured format.

### Working with APIs in Python
Python provides various libraries for interacting with APIs:

1. **The `requests` Library**:
   - Makes HTTP requests to API endpoints
   - Handles response data
   - Manages authentication

2. **API Authentication**:
   - API keys
   - OAuth tokens
   - Session-based authentication

3. **Common Response Formats**:
   - JSON (JavaScript Object Notation)
   - XML (eXtensible Markup Language)
   - CSV (Comma-Separated Values)

### Example: Currency API
```python
import requests

url = 'https://api.currencyapi.com/v3/latest?apikey=YOUR_API_KEY'
response = requests.get(url)
data = response.json()

# Accessing specific data points
usd_to_eur = data['data']['EUR']['value']
```

### Example: Financial Data APIs
Libraries like `yfinance` provide specialized interfaces for financial data:

```python
import yfinance as yf

# Get stock information
tesla = yf.Ticker("TSLA")

# Get historical market data
hist = tesla.history(period="max")
```

## Web Scraping

### What is Web Scraping?
Web scraping is the process of extracting data from websites. It involves making HTTP requests to a website's server, downloading the HTML content, and parsing it to extract the desired information.

### Web Scraping with BeautifulSoup

BeautifulSoup is a powerful Python library for parsing HTML and XML documents. It provides simple methods for navigating, searching, and modifying the parse tree.

#### Web Scraping Process:

1. **Request**: Download the HTML content from a website
2. **Parse**: Convert the HTML into a BeautifulSoup object
3. **Extract**: Navigate and search the HTML structure to find the desired data
4. **Clean & Format**: Process the extracted data into a usable format

#### Example Web Scraping Workflow:

```python
import requests
from bs4 import BeautifulSoup
import pandas as pd

# 1. Send an HTTP request to the website
url = "https://example.com/table-data"
response = requests.get(url)

# 2. Parse the HTML content
soup = BeautifulSoup(response.text, 'html.parser')

# 3. Extract data from HTML
table = soup.find('table')
rows = table.find_all('tr')

# 4. Process and structure the data
data = []
for row in rows[1:]:  # Skip header row
    columns = row.find_all('td')
    data.append([column.text.strip() for column in columns])

# 5. Create a DataFrame
df = pd.DataFrame(data, columns=['Column1', 'Column2', 'Column3'])
```

### Key BeautifulSoup Functions

1. **Finding Elements**:
   - `find()`: Returns the first matching element
   - `find_all()`: Returns all matching elements
   
2. **Navigation**:
   - Parent/child relationships
   - Sibling navigation
   - Descendant navigation

3. **Filtering by Attributes**:
   - Tag name
   - CSS class
   - HTML id
   - Custom attributes

### Alternative: Using pandas for HTML Tables

The pandas library provides a convenient function `read_html()` for extracting tables directly from web pages:

```python
import pandas as pd

url = "https://en.wikipedia.org/wiki/World_population"
tables = pd.read_html(url, match="10 most densely populated countries")
population_data = tables[0]
```

## Data Visualization

After collecting data, visualization is a key step in understanding and communicating insights:

### Using Plotly for Interactive Visualizations

```python
import plotly.express as px

# Create an interactive line chart
fig = px.line(
    data_frame=stock_data, 
    x='Date', 
    y='Close',
    title='Stock Price Over Time'
)
fig.show()
```

### Creating Dashboards

Combining multiple visualizations into dashboards helps present a comprehensive view of the data:

```python
from plotly.subplots import make_subplots
import plotly.graph_objects as go

# Create a figure with multiple subplots
fig = make_subplots(
    rows=2, 
    cols=1,
    shared_xaxes=True,
    subplot_titles=("Historical Share Price", "Trading Volume")
)

fig.add_trace(
    go.Scatter(x=stock_data.Date, y=stock_data.Close, name="Share Price"),
    row=1, col=1
)

fig.add_trace(
    go.Bar(x=stock_data.Date, y=stock_data.Volume, name="Volume"),
    row=2, col=1
)

fig.update_layout(height=600, width=800, title_text="Stock Analysis Dashboard")
fig.show()
```

## Project Structure Best Practices

When undertaking a data collection project:

1. **Define Clear Objectives**: Know what data you need and why
2. **Choose Appropriate Methods**: Select the right data collection approach (API vs. web scraping)
3. **Handle Ethics and Legality**: Respect terms of service, rate limits, and data privacy laws
4. **Implement Error Handling**: Account for possible failures in data retrieval
5. **Document Your Process**: Keep records of data sources and collection methods
6. **Ensure Reproducibility**: Create scripts that can be rerun to refresh data
7. **Plan for Data Storage**: Determine where and how to store collected data

## Ethical Considerations

When collecting data, always consider:

- Website terms of service and robots.txt files
- Rate limiting to avoid overwhelming servers
- Data privacy regulations like GDPR or CCPA
- Proper attribution of data sources
- Secure storage of sensitive information

## Common Challenges and Solutions

1. **Dynamic Websites**: Content loaded via JavaScript may require specialized tools like Selenium
2. **Authentication**: Some websites require login credentials to access data
3. **Anti-Scraping Measures**: Websites may employ CAPTCHAs or IP blocking
4. **Data Quality**: Web-scraped data often needs significant cleaning
5. **Changes to Structure**: Website redesigns can break scraping scripts

## Conclusion

Data collection through APIs and web scraping forms the foundation of many data science projects. Mastering these techniques allows data scientists to access diverse datasets beyond what's readily available in standard databases or CSV files. However, always approach data collection ethically and legally, respecting the rights of data providers and subjects.