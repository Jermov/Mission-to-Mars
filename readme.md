# Mission to Mars Web App

## Project Overview
Build a Web-Based Application that will scrape several websites for the most recent data. The extracted data is stored in a NoSQL database and then loaded into a HTML page for display. 

Additionally, a Jupyter Notebook displaying the underlying code used to find the elements used to display within the webpage is required. Also, a secondary Jupyter Notebook which pulls data from a website from a table and analyzes this data to answer several questions.

Questions:
1.  How many months exist on Mars?
    A.  12
2.  How Many Martian days worth of data exist in the scraped dataset?
    A.  1,867
3.  What are the coldest and the warmest months on Mars?
    A.  Coldest= Month 3, Warmest = Month 1
4.  What Months have the lowest and highest atmospheric pressure on Mars?
    A.  Highest pressure noted at Month 9, Lowest pressure noted at Month 5
5.  About how many terrestrial (Earth) days exist in a Martian year?
    A.  About 700 Days

## Software

- Python 3.10
- splinter 0.14.0
- webdriver-manager 3.8.3
- Flask 1.1.2
- Flask-PyMongo 2.3.0
- BeautifulSoup (bs4) 4.11.1
- html5lib 1.1
- lxml 4.8.0
- Jupyter Notebooks 6.4.8
- MongoDB 6.0.1

## Scraping Mars Data

An example image of the HTML page can be viewed by clicking [here](![WebApp](https://github.com/Jermov/Mission-to-Mars/blob/main/webapp.jpg?raw=true)).

Selecting the "Scrape New Data" button will obtain the latest news, images, and facts about Mars. News titles and summaries are extracted from [NASA Mars Exploration Program News](https://data-class-mars.s3.amazonaws.com/Mars/index.html). The featured images are extracted from the [Jet Propulsion Laboratory's Space Images](https://spaceimages-mars.com/). Mars hemisphere images are extracted from [Astropedia](https://astrogeology.usgs.gov/search/results?q=hemisphere+enhanced&k1=target&v1=Mars). Finally, the Mars facts are gathered from [Galaxy Facts](https://data-class-mars-facts.s3.amazonaws.com/Mars_Facts/index.html). The scraping code used in this project is [scraping.py](https://github.com/Jermov/Mission-to-Mars/main/scraping.py).

After running [app.py](https://github.com/Jermov/Mission-to-Mars/main/app.py), the extracted data is successfully stored in MongoDB as seen in the screenshot below. A mars_app database must exist in mongo for the code to properly run. 

![mongo_mars](https://github.com/Jermov/Mission-to-Mars/main/images/MongoDB.png)

## Updating the Web App

When the 'Scrape New Data' button is selected, notice the 'featured-image' and the 'news' sections update with new data.
![Web_App](https://github.com/Jermov/Mission-to-Mars/main/images/app_success.jpeg)


