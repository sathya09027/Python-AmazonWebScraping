# Amazon Product Web Scraper (Python)

## Project Overview

This project is a **Python web scraping script** that extracts product information from **Amazon** using **Beautiful Soup** and **Requests**.

## The script collects product details such as:

- Product Title
- Brand Name
- Date of Extraction

The data is then stored in a CSV file for further analysis.

This project demonstrates web scraping, data extraction, and data storage using Python.

---

## Dashboard / Output Example

Example data collected and stored in the CSV file:

| Title | Brand |	Date |
|-------|-------|------|
| Metal Detector Evolution of Man - Men's T-Shirt | Candymix | 2026-01-20 |

## Project Structure

amazon-web-scraper
│
├── AmazonWebScraper.ipynb
├── AmazonWebScraperDataset.csv
└── README.md

### Files Explanation

- AmazonWebScraper.ipynb → Jupyter Notebook containing the scraping code
- AmazonWebScraperDataset.csv → Dataset generated from the scraper
- README.md → Project documentation

---

## Tools & Technologies Used

- Python
- Jupyter Notebook
- Beautiful Soup
- Requests
- Pandas
- CSV

---

## Features

- Connects to an Amazon product page
- Extracts product title and brand
- Saves extracted data to a CSV dataset
- Automatically appends new records
- Uses a time loop to collect data continuously

---

## How the Script Works

1. Send an HTTP request to the Amazon product page.
2. Parse the HTML content using BeautifulSoup.
3. Extract the product title and brand.
4. Store the extracted data in a CSV file.
5. Append new data every few seconds using a loop.

## Example Code Snippet

``` import requests
    from bs4 import BeautifulSoup

    page = requests.get(URL, headers=headers)
    soup = BeautifulSoup(page.content, "html.parser")

    title = soup.find(id="productTitle").get_text()
    brand = soup.find(id="bylineInfo").get_text() ```

---

## Dataset Generation

The script creates and updates a CSV file:

AmazonWebScraperDataset.csv

Example dataset structure:

Title	   Brand	   Date

## Skills Demonstrated

- Web Scraping
- Python Programming
- Data Extraction
- Data Storage with CSV
- Automation with Python
- Data Handling with Pandas

## Important Note

Websites like Amazon may change their HTML structure or block automated scraping requests. If the script returns:

Title or Brand not found – page blocked or changed

It may be due to:

- HTML structure changes
- Anti-scraping protections
- Missing headers in the request

## Author

**Sathya Priya** Aspiring Data Analyst | Python & Data Enthusiast

[LinkedIn](https://www.linkedin.com/in/sathya-priya-balusami/)

---

⭐ If you found this project helpful, feel free to star the repository.
