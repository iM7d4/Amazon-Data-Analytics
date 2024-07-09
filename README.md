# Amazon-Data-Analytics
Craft a captivating project that blends the excitement of video games with the power of web scraping, data processing (ETL), and insightful data exploration (EDA).  Explore the vast world of Amazon using these techniques to unearth hidden treasures, transform raw data into valuable insights, and forge an engaging experience that merges the thrill of discovery with the power of data.

### Introduction 
![Amazon](images/logo.gif) <br>
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

We scrape data from the Amazon Website URLs for Apple & Samsung Smart Phones: [URLs](https://github.com/iM7d4/Amazon-Data-Analytics/blob/main/ETL/List%20of%20URLs.txt)

[Webpage structure](https://www.amazon.com/Apple-iPhone-14-Pro-Max/dp/B0BN94DL3R/?th=1)

### 1.3 How We Extracted and Stored Data  

Defines a list of URLs for iPhone and Samsung products on Amazon.

Defines a function scrape_amazon_product to extract relevant information from Amazon product pages using BeautifulSoup and requests.

The function extracts product title, price, star ratings, number of global ratings, customer stars percentages, and features and ratings.

It also contains a function extract_model_number to extract the model number from the product title.

The script showcases a systematic approach to web scraping.

Defines dictionaries 'iphone_scraped_data' and 'samsung_scraped_data' to store scraped data for iPhone & Samsung products.

Loops through each brand's URLs, calls the scrape_amazon_product function, and stores the scraped data in the dictionaries. Saves the scraped data to JSON and CSV files.

Creates DataFrames 'scraped_iphone_df' and 'scraped_samsung_df' from the scraped data. Splits the 'title' column into multiple columns based on commas. Saves the modified DataFrames to CSV files.

![Apple Scraped Data](images/apple_scraped.png)

![Samsung Scraped Data](images/samsung_scraped.png)

## Deliverable 2: Deliverable 2: Data Cleaning Using Jupyter Notebook

This section includes data cleaning so that the cleaned data can be utitlized for analysis using Pandas

### 2.1 Prerequisites

Before you begin, ensure you have the following installed:

Python 3.6 or higher

Regular Expressions

Data Analysis ( Pandas, Numpy, Scikit-learn )

### 2.2 Data Sources

We use the data resources from two files 'scraped_iphone_data.csv' and 'scraped_samsung_data.csv' using Pandas.

### 2.3 How We Cleaned The Data

Drops unnecessary columns.

Extracts and converts storage capacity, color, price, star ratings, global ratings, and customer stars percentages to appropriate data types using regular expressions.

Creates new columns, including 'brand,' 'model_year,' and reorders columns with appropriate names.

Saves cleaned 'iphone_samsung_df' data to JSON and CSV files.

![Merged Cleaned Data](images/merged_cleaned_data.png)

## Deliverable 3: Flask-powered API & Data Visualizations Using Plotly.js

This section includes utilization of Flask and Plotly.js for API calls and visualization dashboards

### 3.1 Prerequisites

Before you begin, ensure you have the following installed:

Flask (Imports the Flask framework, allowing the creation of a web application)

jsonify ( Python dictionaries to JSON responses, and render_template facilitates rendering HTML templates )

render_template  (facilitates rendering HTML templates)

HTML, CSS, Bootsrap ( for structure and style web page)

JavaScript ( for dynamic behavior)

Sweetalert ( for Dashboard POPUP BOXES)

D3.js ( for data manipulation)

Plotly ( for interactive graphs )

### 3.2 Flask API Routes

#### Home Page Route (@app.route("/")): 

Renders the "index.html" template when users access the home page ("/").

#### iPhone and Samsung Details API Routes:

The below routes read merged iPhone and Samsung data from a CSV file, converts it to JSON, and returns it as a JSON response:

/api/iphone_samsung_details

/api/iphone_details

/api/samsung_details


### 3.3 Data Visualizations

#### 3.3.1 SweetAlert JS Library

Displays a SweetAlert notification when the page loads.

Includes a SweetAlert popup to display a success message when the page loads, providing a user-friendly experience.


![SweetAlert](images/sweetalert.png)


#### 3.3.2 Product Selection and Dashboard Initialization:

Created a dropdown menu to select different iPhone and Samsung models.
Upon selection, populates demographic information, builds pie charts, and bar charts for the selected product.

Also, initializes specific charts for Apple and Samsung brands.
Populating Product Information:
Retrieves specific information (brand, color, price, storage capacity) for the selected product and displays it.

Constructs a pie chart displaying the distribution of star ratings for the selected product.
Building Bar Chart for Product Star Ratings:


#### 3.3.3 Bar Chart for Apple Samsung Product & Price 

Constructs a bar chart displaying the prices of Apple & Samsung phones.

Bar chart displaying the distribution of star ratings for Samsung brand models.
![Bar Chart](images/bar_chart.png)

#### 3.3.4 Line Chart for Model Years


Line chart showing the evolution of brand models over different model years for both Apple and Samsung with respect to price.
![Line Chart](images/line_chart.png)

#### 3.3.5 Bubble Chart for Global Ratings

Bubble chart showing the relationship between global ratings, price, and brand models for both Apple and Samsung.

The size of each bubble is determine by the corresponding overall "star_ratings".
![Bubble Chart](images/bubble_chart.png)

### 3.3 Dashboard Layout

![Product Dashboard](images/product_dashboard.png) <br>
![Brand Dashboard](images/brand_dashboard.png)

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
