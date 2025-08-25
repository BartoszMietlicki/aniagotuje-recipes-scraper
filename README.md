# AniaGotuje Recipes Scraper

Python notebook project that collects recipe links and content from **AniaGotuje.pl** and returns everything in a single DataFrame (no file output).

## Description
This notebook performs the full data-collection workflow:
- automatically gathers all recipe categories and links to individual recipes,
- for each recipe extracts: title & intro, ingredients list, step-by-step description, preparation times, number of portions, energy value, and diet type,
- fetches pages in parallel (with simple retry for HTTP 429 limits) and merges results into one **DataFrame** shown at the end (`df_full`).

## Usage
- **Colab:** open the notebook → [Colab](https://colab.research.google.com/drive/16vtPFiU6ftd2vZAU-77HwGbIuhrg7A1b)  
- **Kaggle:** open the notebook → [Kaggle](https://www.kaggle.com/code/bartekmietlicki/aniagotuje-recipes-scraper)  
- **Locally:** requires Python **3.10+** and the libraries `requests`, `beautifulsoup4`, `lxml`, `pandas`, `tqdm`.

## Compatibility & version notes
- Initially created in **April 2025**, aligned with the site’s structure and library versions at that time.  
- **August 2025 update:** removed aggressive `SoupStrainer` (after BeautifulSoup changes it trimmed required nodes), switched to full-page parsing with small selector fallbacks, and refined the Kaggle-friendly setup.

If the site or libraries change again and something breaks, please contact the author.

## Ethics & legality of scraping
This is a **student/educational** project. Please use it responsibly:
- respect the site’s Terms of Service,
- avoid overloading the server (reasonable request rate),
- comply with copyright and database rights.

## Contributions & contact
Have improvement ideas or noticed the project is out of date? **Contact the author.**
