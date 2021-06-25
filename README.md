# Mission-to-Mars

## Overview of Project

For this project, we are building a web app about the planet Mars. To do this, we are web scraping for Mars facts and images using BeautifulSoup and Splinter. Then, using Python, we create an app with Flask to display these facts and images. 

## Mars News

We first scrape [this website](https://redplanetscience.com/). This website contains the latest news regarding Mars from NASA. Here, we scraped only the most recent news headline and summary using DevTools and BeautifulSoup. 

## Featured Images

We then scraped the website from the [Jet Propulsion Laboratory](https://spaceimages-mars.com/) for the featured image of Mars. We used DevTools and Splinter to automate a browser that clicked on the featured image button and scraped the image. 

## Mars Facts

We found good Mars [facts](https://galaxyfacts-mars.com/) and decided to scrape the table containing the information on the right side of the screen. We used DevTools again to locate the HTML tags that contained the table. Then, we used Pandas to convert this table into a DataFrame using the read_html() function. 

## Hemispheres

We also found [great pictures](https://astrogeology.usgs.gov/search/results?q=hemisphere+enhanced&k1=target&v1=Mars) of the hemispheres of Mars. We scraped this website using Splinter and DevTools. We automated a browser that clicked through each link for all the hemispheres and then scraped the image and the title of the hemisphere.

## Web App

We created a database in MongoDB called mars_app that allowed us to store the data we were scraping. Then we used Flask to display the data. We created a connection between Python and MongoDB through importing PyMongo. Then we set up our app routes to display the main page and to scrape the data again if a button was clicked. We defined functions that allowed the data to be scraped again. Then we integrated MongoDB into the web app by defining a scrape_all() function. Finally, we created an HTML file to customize the appearance of the web app. We used several Bootstrap components such as adding thumbnails to the hemispheres, making the images responsive, and making the scrape new data button active. 
