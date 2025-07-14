# Scrapster

**Tagline**: Scrapster: Web-powered contact extraction from websites with a sleek Flask interface.

## Overview

Scrapster is a robust Flask-based web application designed to scrape critical contact information from websites, transforming the original Tkinter-based desktop app into an accessible online tool. It enables users to input a list of URLs and extract structured data, including website names, URLs, countries, email addresses, phone numbers, and social media handles (Instagram and Facebook) formatted as `@username`. Built with a focus on efficiency and user-friendliness, Scrapster leverages multithreading to process multiple URLs concurrently, ensuring fast and reliable scraping. The intuitive web interface, styled with Bootstrap and a navy-black theme, mirrors the desktop version's functionality while offering seamless online access. Key features include a dynamic results table, real-time progress updates, a detailed scraping report, and the ability to export data to Excel. Users can start or stop the scraping process at any time, with session management to support concurrent usage. The app intelligently identifies countries using website content, TLDs, and phone number country codes, and employs sophisticated logic to extract valid phone numbers and emails from homepages, contact pages, and other relevant sections. Social media handles are neatly extracted from URLs (e.g., `@profile` from `https://instagram.com/profile`), ensuring clean output. Scrapster is ideal for businesses, researchers, or anyone needing to aggregate contact data efficiently, with all functionality preserved from the original desktop app in a modern, web-accessible format.

## Features

- **URL Input**: Input multiple website URLs via a textarea for batch processing.
- **Data Extraction**: Scrapes website name, URL, country, email, phone number, and Instagram/Facebook handles (`@username` format).
- **Intelligent Country Detection**: Identifies countries using website text, TLDs, and phone number country codes.
- **Multithreaded Scraping**: Processes multiple URLs concurrently for efficiency, with a configurable maximum of 10 threads.
- **Dynamic Web Interface**: Responsive Bootstrap-based UI with a navy-black theme, featuring a results table, progress updates, and a report section.
- **Real-time Updates**: Polls server for progress and results, updating the UI dynamically during scraping.
- **Stop Functionality**: Allows users to halt scraping at any time without losing partial results.
- **Excel Export**: Exports scraped data to an Excel file, saved in a session-specific file for download.
- **Session Management**: Supports concurrent users with unique session IDs.
- **Robust Scraping Logic**: Extracts phone numbers and emails from homepages, contact pages, and up to 5 relevant pages, with validation using `phonenumbers` library.
- **Social Media Handle Extraction**: Converts Instagram/Facebook URLs to `@username` format, ignoring invalid or homepage links.
- **Error Handling**: Gracefully handles failed requests, invalid URLs, and missing data, ensuring reliable operation.

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/scrapster.git
   cd scrapster
