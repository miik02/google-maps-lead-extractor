# Google Maps Lead Extractor 🗺️ 🚀

An advanced, highly resilient web scraper built with Python and Playwright, designed to extract structured B2B lead data (local businesses) from Google Maps. 

Unlike standard scraping scripts that rely on volatile CSS classes, this architecture is engineered for long-term stability by targeting semantic ARIA roles and internal data attributes.

## 🧠 Technical Highlights & Architecture

- **CSS Obfuscation Bypass:** Google Maps frequently recompiles its frontend, generating random, obfuscated CSS classes (e.g., `XltNde tTVLSc`). This scraper completely ignores volatile classes.
- **Semantic DOM Targeting:** The extraction logic relies on Accessibility (ARIA) tags (`role="feed"`, `role="article"`) and internal Google attributes (`data-item-id`), ensuring a near 0% failure rate when the UI updates.
- **Dynamic Lazy Loading & Infinite Scroll:** Implements automated scrolling within specific container nodes (`role="feed"`) to trigger network requests and load hidden DOM elements efficiently.
- **Master-Detail Data Extraction:** Navigates the complex master-detail layout of Maps by extracting clean anchor URLs (`href`) from article cards and visiting them directly, bypassing UI animation bugs.

## 📊 Extracted Data Points

For every business listing, the scraper reliably extracts:
- Business Name (`<h1>`)
- Full Address (`data-item-id="address"`)
- Phone Number (`data-item-id^="phone:tel:"`)
- Website URL (`data-item-id="authority"`)
- Rating & Total Reviews

## 🛠️ Technology Stack
- **Python 3.10+**
- **Playwright** (for headless browser automation and dynamic DOM interaction)
- **Pandas** (for data cleaning and exporting to `.xlsx` / `.csv`)

## 🚀 Quick Start
*(To be updated with installation instructions and usage commands)*

---
*Disclaimer: This project is strictly for educational purposes and portfolio demonstration. All extracted data is publicly available information.*
