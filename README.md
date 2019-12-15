# Mission_to_Mars
  Web-Scraping-and-Document-Databases


In this project, I built a web application that scrapes various websites for data related to the Mission to Mars and displays the information in a single HTML page.

Step 1 - Scraping
Completed my initial scraping using Jupyter Notebook, BeautifulSoup, Pandas, and Requests/Splinter.

- Created a Jupyter Notebook file called mission_to_mars.ipynb and use this to complete all of your scraping and analysis tasks. The following outlines is what was scraped.

NASA Mars News

- Scraped the NASA Mars News Site and collected the latest News Title and Paragraph Text.

- Used splinter to navigate the site and find the image url for the current Featured Mars Image and assigned the url string to a variable called featured_image_url.


Mars Weather

Visited the Mars Weather twitter account here and scraped the latest Mars weather tweet from the page. Saved the tweet text for the weather report as a variable called mars_weather.


Mars Facts


Visited the Mars Facts webpage here and use Pandas to scrape the table containing facts about the planet including Diameter, Mass, etc.


Used Pandas to convert the data to a HTML table string.



Mars Hemispheres


Visited the USGS Astrogeology site here to obtain high resolution images for each of Mar's hemispheres.


Saved both the image url string for the full resolution hemisphere image, and the Hemisphere title containing the hemisphere name. Used a Python dictionary to store the data using the keys img_url and title.


Appended the dictionary with the image url string and the hemisphere title to a list. 




Step 2 - MongoDB and Flask Application
Used MongoDB with Flask templating to create a new HTML page that displays all of the information that was scraped from the URLs above.


Started by converting your Jupyter notebook into a Python script called scrape_mars.py with a function called scrape that will execute all of your scraping code from above and return one Python dictionary containing all of the scraped data.

- Created a route called /scrape that will import my scrape_mars.py script and call my scrape function.

Store the return value in Mongo as a Python dictionary.



- Created a root route / that will query my Mongo database and pass the mars data into an HTML template to display the data.


- Created a template HTML file called index.html that will take the mars data dictionary and display all of the data in the appropriate HTML elements.
