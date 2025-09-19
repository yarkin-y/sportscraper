# sportscraper

Scrapers for football (soccer) data websites such as **FIFAIndex**, with plans to support Sofascore, Understat, Transfermarkt, and more.

---

## Features
- Scrape team lists, player lists, and detailed player stats from [FIFAIndex](https://www.fifaindex.com/).
- Output results directly to CSV files.
- Retry logic and Selenium stealth to reduce scraping errors.
- Command-line interface (CLI) and Python API.

---

## Installation
Currently published under the name sportscraper-yarkin (distribution name),
but you import it as sportscraper in Python.
```bash
pip install sportscraper-yarkin
```
## Usage
You can use sportscraper directly in your Python code to fetch teams, players, and player stats from FIFAIndex.

```python
from sportscraper.fifaindex import run_full_scrape

# Scrape FIFA 19 Premier League (league_id=13) teams, players, and stats
teams_csv, players_csv, stats_csv = run_full_scrape(
    start_year_infix=19,   # FIFA 19
    end_year_infix=19,     # stop at FIFA 19
    league_id=13,          # 13 = Premier League
    outdir="./out",        # output directory for CSVs
    headless=True          # run browser in headless mode
)

print("Teams saved to:", teams_csv)
print("Players saved to:", players_csv)
print("Stats saved to:", stats_csv)
```


I still have many other sources of football data that I want to include within this account, so if you would like to support me, you can buy me a coffee here!

https://buymeacoffee.com/yarkin_y
