# AmazonScraper
A Scraper built using scrapy module for scrapping Amazon products data.


## Things it scrape
- Product Title
- Product ImageUrl
- Product Price
- Product Rating
- Product Description
- Product Brand
- Product Colour
- Check if Product is In Stock

## How to Run

1. Download the zip file and extract it in a directory or clone the repository.
2. Navigate to the extracted directory and install these two packages(ignore if already installed). If pillow is already installed but still it's showing ModuleNotFoundError, try to uninstall pillow then install again.
```
$ pip install Scrapy
```
```
$ pip install pillow
```

3. Now run the below command to start scraping.
```
$ scrapy crawl amazon_scraper -a category="men glasses" -a pages=1 -o ./data/data.json
```
3. ***category*** argument is used as a search keyword, and ***pages*** argument controls the number of page to be scrapped by the crawler.
4. Result is written to a json file inside the data folder.

## Why Scrapy and not some other libraries like BeautifulSoup?
Scrapy and BeautifulSoup have different purposes. BeautifulSoup is basically a library for parsing and extracting data from HTML.
<br></br>
Scrapy, on the other hand, is a framework that goes far beyond data extraction. Scrapy provides builtin solutions for the most common issues that we’ll find while scraping websites, such as: redirections, retrying certain types of requests, HTTP caching, filtering duplicated requests, auto-throttling to avoid overloading the servers, preserving sessions/cookies across multiple requests, among many other features.
<br></br>
Scrapy supports both CSS selectors and XPath expressions for data extraction. In fact, we could even use BeautifulSoup or PyQuery as the data extraction mechanism in our Scrapy spiders.

## What else can we do?
- Many other features are available in scrapy like we can even download the image of the product.
- We can control the delay for requests.
- Can scrape the reviews of the Product.
- This project is just for a demo purpose to show the power of Scrapy framework.
