# GiftWare Trade Supply — scraping sandbox

A small static website used as a practice target for a data-science class
exercise on web scraping, data cleaning and exploratory analysis.

The storefront is fictional. The catalogue behind it is derived from a real,
publicly available transaction dataset, so the figures on the site reflect
genuine trading patterns rather than random numbers.

## Source data

Derived from the **Online Retail II** dataset — transactions from a UK-based
online gift-ware retailer, December 2009 to December 2011.

> Chen, D. (2019). *Online Retail II* [Dataset]. UCI Machine Learning Repository.
> https://archive.ics.uci.edu/dataset/502/online+retail+ii

Used here for non-commercial educational purposes, with the original values
aggregated and reshaped into a product catalogue.

## Running it locally

The site is plain static HTML and needs no build step. Some parts of the page
load their content after the page opens, and browsers block that on `file://`
URLs, so open it through a local server rather than double-clicking:

```bash
python3 -m http.server 8000
```

Then visit `http://localhost:8000`.

## For students

Collect the data with a scraper you wrote and can explain. Using an AI
assistant to help you write, debug or review that code is fine and encouraged.
Asking an assistant to read the site and hand you the answers is not the
exercise.

Whatever you conclude, be ready to say where the number came from, what you
removed from the data and why, and what the data cannot tell you.
