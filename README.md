# Amazon-Data-Analytics
Craft a captivating project that blends the excitement of video games with the power of web scraping, data processing (ETL), and insightful data exploration (EDA).  Explore the vast world of Amazon using these techniques to unearth hidden treasures, transform raw data into valuable insights, and forge an engaging experience that merges the thrill of discovery with the power of data.

### Introduction 
![Amazon]()
As a global e-commerce giant and digital services provider, Amazon complements the tech experiences offered by both Samsung and iPhone.Together, the dynamic trio of Samsung, iPhone, and Amazon creates a seamless, interconnected digital experience. From the latest smartphones to smart home integration and effortless online shopping, this collaboration defines the modern intersection of technology and convenience.

The Project integrates web scraping, ETL processes, and data visualizations using Beautiful Soup, Plotly.js, and Flask. The exploration focuses on Amazon, Apple, and Samsung products, offering insights into pricing, star ratings, and global ratings, presented through interactive charts and a dynamic dashboard.

This ETL process for 'Amazon ETL & Visualizations' break into three deliverables.

Deliverable 1: Web Scaping Using Beautiful Soup.

Deliverable 2: Data Cleaning Using Jupyter Notebook.

Deliverable 3: Flask-powered API & Data Visualizations Using Plotly.js

## Deliverable 1: Web Scaping Using Beautiful Soup

This section includes web scrapping and analyzing the data using Beautiful soup and Pandas Python Data Analysis.

 ### 1.1 Prerequisites

Before you begin, ensure you have the following installed:

Python 3.6 or higher

Beautiful Soup 4

Requests (for making HTTP requests)

Pandas (for data analysis)

### 1.2 Data Sources

We scrape data from the Amazon Website URLs for Apple & Samsung Smart Phones: [URLs}(https://github.com/iM7d4/Amazon-Data-Analytics/blob/main/ETL/List%20of%20URLs.txt)

[Webpage structure](https://www.amazon.com/Apple-iPhone-14-Pro-Max/dp/B0BN94DL3R/?th=1)

## Key Insights

Summary

- Prices are in higher ranges for Apple as compared to Samsung.

- The  5 star ratings of Apple carries more weight (i.e 68.8%) than Samsung (i.e 62.4%).

- Spike in the price of the iPhone 14 Pro Max (2022) among Apple models, whereas the price of the Samsung Galaxy S Ultra shows minimal fluctuations (2023).

For Apple iPhones:

- The iPhone 1_4 has the highest star rating (4.4) among the Apple models.

- The iPhone 14 Pro Max has the highest price ($1849.0) among the Apple models.

- The iPhone 13 Pro Max has the highest number of global ratings (420) among the Apple models.

For Samsung Galaxy Phones:

-  Galaxy S23 5G has the highest star rating (4.5) among the Samsung models.

- The Galaxy S22 Ultra has the highest price ($839.99) among the Samsung models.

- The Galaxy S21 5G has the highest number of global ratings (173) among the Samsung models.
