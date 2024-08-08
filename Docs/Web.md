# Web Scraper User Documentation

## Overview
The Web Scraper tool is a powerful utility that allows you to easily extract webpage data by simply providing a URL and choosing from three different scraping methods: Single Page, Recursive, and Sitemap. Whether you need data from a single page, a whole network of interconnected pages, or a well-structured sitemap, this tool can handle it all.

## Getting Started

### 1. Providing a URL
The first step in using the web scraper is to provide the URL of the webpage you want to scrape. This URL will serve as the starting point for the scraping process, regardless of which method you choose.

### 2. Choosing a Scraping Method
Once you've provided the URL, you can choose one of the following scraping methods:

#### A. Single Page Scraping
- **Description:** This method extracts all the data from the specific webpage you provided. It’s the simplest and quickest option, ideal for when you only need content from a single page.
- **How It Works:** The scraper fetches and processes all the text from the webpage without following any further links.

#### B. Recursive Scraping
- **Description:** This method is designed to go deeper into the web of interconnected pages. It starts from the provided URL and follows links to other pages, capturing content up to two levels deep (our current default setting). This is useful for gathering content from related pages or sections of a website.
- **How It Works:**
  1. The scraper begins by extracting content from the provided URL.
  2. It then identifies and follows all internal links on that page, extracting content from the linked pages.
- **Use Case:** Ideal for scraping articles that are linked together, blogs with multiple posts connected, or any situation where related content is spread across a few interconnected pages.
- **What not to expect:**
  1. Only internal webpages will be scraped, meaning it will ignore all the URLs pointing to files or other domains.
  2. Internal URLs that are child URLs of the provided base URL will be scraped.

#### C. Sitemap Scraping
- **Description:** This method utilizes the website's sitemap, a webpage that lists all the pages on a website, to methodically scrape content from multiple pages. It's a highly efficient way to scrape large websites where you want to ensure that no pages are missed.
- **How It Works:**
  1. The user will provide the URL of the Sitemap webpage where all the webpage links are present.
  2. It then sequentially processes each URL listed in the sitemap, extracting content from each webpage.
- **Use Case:** Best suited for scraping entire websites, such as e-commerce sites, documentation pages, or any website with a structured sitemap that outlines all the available pages.
