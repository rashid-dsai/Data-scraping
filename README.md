LinkedIn Job Scraper

This project is a simple job-scraping tool built with Python, Playwright, and BeautifulSoup. It automatically fetches job listings from LinkedIn based on a search query and location and saves them into a CSV file.

Features

Scrapes LinkedIn job search results (title, company, location, apply link)

Works headlessly using Playwright

Saves extracted data to linked.csv

Saves full HTML content for debugging

Customizable search query, location, and max results

Requirements

Install the dependencies:

pip install playwright bs4
playwright install

How to Run

Update the query and location in the script:

fetch_jobs_from_linkedin("python", "UAE", max_results=700)


Run the script:

python linkedIn_jobs.py


Output will be saved in:

linked.csv → extracted job data

content.html → raw HTML of the page

File Output Format (CSV)

| title | company | location | apply_link |

Each scraped job is added as a new row.

Warnings

LinkedIn aggressively rate-limits scraping. Expect failures if you run too frequently.

HTML structure changes often; you’ll need to update selectors when it breaks.
