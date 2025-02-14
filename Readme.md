# 🌐 Google Maps Business Data Extractor - Enterprise-Grade Web Scraper

[![Python Version](https://img.shields.io/badge/python-3.8%2B-blue)](https://www.python.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Playwright](https://img.shields.io/badge/Headless%20Browser-Playwright-blueviolet)](https://playwright.dev/)

A sophisticated web scraping solution for extracting comprehensive business intelligence from Google Maps.
![Google Maps Scraper Demo](image.png)  


## 🚀 Key Features

- **Industrial-Strength Data Extraction**
  - 📍 GPS Coordinates Extraction
  - 📞 Direct Phone Number Capture
  - 🌐 Website URL Retrieval
  - ⭐ Average Review Score Collection
  - 🏢 Full Business Address Parsing

- **Enterprise Features**
  - 🛡️ Anti-Detection Mechanisms with Headless Browsing
  - 📈 Scalable Architecture for Bulk Operations
  - 🧩 Modular Design for Easy Customization
  - 📊 Dual Output Formats (Excel & CSV)
  - ⏱️ Intelligent Pagination Handling

## 💻 Installation

```bash
# Clone repository
git clone https://github.com/yourusername/google-maps-scraper.git
cd google-maps-scraper

# Create virtual environment
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt
playwright install chromium
```

## 🏎️ Quick Start

### Single Location Extraction:

```bash
python main.py -s="Premium Coffee Shops in Manhattan" -t=250
```

### Bulk Extraction Workflow:

Add multiple search terms to `input.txt`:

```text
Luxury Apartments New York
IT Companies San Francisco
Dental Clinics London
```

Execute bulk extraction:

```bash
python main.py -t=500
```

## 📂 Output Structure

Sample extracted data structure:

| Name                | Address       | Website         | Phone       | Rating | Coordinates         |
|---------------------|--------------|----------------|-------------|--------|---------------------|
| Central Perk Cafe  | 123 Broadway | www.example.com | +1 555-0123 | 4.8    | 40.7128, -74.0060   |

Files generated in `/output` directory:

```
google_maps_data_{search_term}.xlsx
google_maps_data_{search_term}.csv
```

## ⚙️ Advanced Configuration

### Custom Search Parameters:

```python
@dataclass
class Business:
    # Add custom fields for:
    opening_hours: str = None
    total_reviews: int = None
    categories: list[str] = field(default_factory=list)
```

### Input File Management:

```text
# input.txt syntax:
"3 Star Hotels Paris" min_reviews:100
"Tech Startups Berlin" founded_after:2015
```

## ⚠️ Ethical Compliance

This tool must be used in accordance with:

- [Google Maps Terms of Service](https://www.google.com/intl/en/help/terms_maps/)
- [GDPR Regulations](https://gdpr-info.eu/)
- [CCPA Guidelines](https://oag.ca.gov/privacy/ccpa)
- Your Local Data Protection Laws

**Recommended:** Always implement rate limiting and respect `robots.txt` directives in production environments.

## 🛠️ Professional Support

For enterprise implementations and custom scraping solutions:

📧 oussemabenhassena5@gmail.com 
💼 [LinkedIn Profile](https://www.linkedin.com/in/oussema-ben-hassena-b445122a4)


