# Health Resource Batch Crawler Project

## Project Overview

This project implements a web crawler to extract public health resources from health department websites across the United States. The crawler is designed to find phone numbers, addresses, and facility names, categorize and tag them, and save the results in structured formats for further analysis.

## Features

- Crawls health department websites from CSV lists by state
- Extracts and categorizes:
  - 📞 Phone numbers (CONTACT_INFO)
  - 📍 Addresses (LOCATION)
  - 🏥 Facility names (FACILITY)
- Auto-tags resources by health topic (flu, COVID-19, vaccination, etc.)
- Batch processing for multiple counties
- Saves results as JSON, CSV, and human-readable reports
- Handles errors gracefully and respects polite crawling practices

## What We Did

- Implemented a single-site crawler (`my_crawler.py`) to extract and categorize resources from one website
- Built a batch crawler (`my_batch_crawler.py`) to process multiple counties using CSV files
- Adapted the code to match the actual CSV structure in `data/websites/`
- Successfully crawled and summarized health resources for Alaska counties
- Generated detailed output files in the `output/` directory

## How to Run

1. Place your state CSV files in `data/websites/` (e.g., `us-ak.csv`)
2. Edit `my_batch_crawler.py` to set the desired state code (e.g., `state = "ak"`)
3. Run the batch crawler:
   ```bash
   python student_template/my_batch_crawler.py
   ```
4. Find results in the `output/` folder (JSON, CSV, TXT reports)

## Author

Project completed by Nik

---

This project is for educational purposes and demonstrates web scraping, data extraction, and batch processing techniques for public health data.
