# scraping_demo
## Web scraping demo: Scientific data about Mars exploration

__Note: Requires Chrome Driver (Selenium) to be installed__

### Step 1 - Scraping functionality
Web scraping using Jupyter Notebook, BeautifulSoup, Pandas, and Requests/Splinter.

URLs used:
- https://mars.nasa.gov/news/
- https://www.jpl.nasa.gov/spaceimages/?search=&category=Mars
- https://twitter.com/marswxreport?lang=en
- http://space-facts.com/mars/

### Step 2 - Serve up data from MongoDB/Flask app
- Used MongoDB with Flask templating to create a new HTML page that displays all of the 
information that was scraped from the URLs above.

- Created scraping function that used scraping code from above and returned Python dictionary 
containing all of the data.

- A Flask route "/scrape" calls scraping function.

- Return value is stored in MongoDB document

- Root Flask route ("/") queries Mongo database and passes the Mars data into an HTML 
template to display the data.

- HTML template dynamically displays all of the data from the Mongo document in the appropriate places.