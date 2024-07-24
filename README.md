# Movie Review Data Collector

## Overview
This project collects movie review data from the New York Times API and combines it with movie details from The Movie Database (TMDB) API. It then merges, cleans, and exports the data for further analysis.

## Features
- Retrieves movie reviews from the New York Times API
- Fetches corresponding movie details from The Movie Database API
- Merges and cleans the data from both sources
- Exports the combined data to a CSV file

## Prerequisites
- Python 3.x
- Pandas library
- Requests library
- API keys for New York Times and The Movie Database

## Setup
1. Clone this repository to your local machine.
2. Install the required Python libraries:
   ```
   pip install pandas requests
   ```
3. Create a `.env` file in the project root directory with your API keys:
   ```
   NYT_API_KEY=your_nyt_api_key_here
   TMDB_API_KEY=your_tmdb_api_key_here
   ```

## Usage
1. Run the main script:
   ```
   python movie_data_collector.py
   ```
2. The script will:
   - Fetch movie reviews from the New York Times API
   - Retrieve corresponding movie details from TMDB
   - Merge and clean the data
   - Export the result to `../output/movie_reviews_data.csv`

## Data Structure
The exported CSV file contains the following key information:
- Movie title
- Review snippet from NYT
- Publication date
- Movie genres
- Budget
- Revenue
- Release date
- Average vote
- Vote count
- And more...

## Limitations
- The script is rate-limited to respect API usage guidelines
- Only reviews with "love" in the headline are collected from NYT
- The data is limited to movies reviewed by NYT and available on TMDB

## Acknowledgments
- New York Times for their Article Search API
- The Movie Database for their comprehensive movie data API
