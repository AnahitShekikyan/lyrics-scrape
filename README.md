# Lyrics Scraping Project

This project was created for ADS 509 (Module 1: APIs and Web Scraping).  
The goal was to scrape song lyrics for at least two artists from [AZLyrics.com](https://www.azlyrics.com),  
store them as individual text files, and run a basic evaluation of the results.

## Contents
- **Lyrics Scrape.ipynb** — main notebook with scraping code and evaluation
- **lyrics/** — folder where individual song lyric files are saved
- **data/** — optional CSV outputs if generated
- **README.md** — project overview

## Approach
- Used `requests` and `BeautifulSoup` to collect song links and scrape lyrics.  
- Added polite rate limiting (`5–15s` per request) and retry logic with backoff.  
- Saved each song to `lyrics/[artist]/[song].txt` with the title and lyrics.  
- Summarized results with word counts and basic stats in the evaluation section.

## Notes on Site Blocking
While developing, AZLyrics sometimes redirected requests to a "request for access" page.  
I tried several fixes — adding delays, retries, turning off browser ad-blockers, and even switching networks.  
Despite these efforts, some requests were still blocked. The scraping code is complete and correct,  
and when AZLyrics allows access, it saves the expected lyrics files.  

---

**Assignment Deliverables**: Notebook (`.ipynb`), exported PDF, and GitHub link.


