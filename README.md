# Web scraping demo: Scientific data about Mars exploration

__Note: Requires Chrome Driver (Selenium) to be installed__

### Step 1 - Scraping functionality
Web scraping function built using Jupyter Notebook, BeautifulSoup, Pandas, and Requests/Splinter.

URLs used:
- https://mars.nasa.gov/news/
- https://www.jpl.nasa.gov/spaceimages/?search=&category=Mars
- https://twitter.com/marswxreport?lang=en
- http://space-facts.com/mars/

### Step 2 - Serve up data from MongoDB/Flask app
#### MongoDB / Flask templating create a dynamic HTML page that displays all of the information scraped from the URLs above.

- Function contains scraping code from above to return Python dictionary 
of variables containing all of the data.

- A Flask route "/scrape" calls above scraping function, and return value is stored in MongoDB document.

- Root Flask route ("/") retrieves MongoDB document and passes its data into Flask HTML 
template, which dynamically displays the document's data in the appropriate places.