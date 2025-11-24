# football-transfer-scraper
 A Python tool to scrape and analyze European football transfer data from Transfermarkt.
 This project extracts detailed information about player transfers, including fees, market values, and contract details.

## 🚀 Features

- **Comprehensive Data**: Scrapes player names, ages, nationalities, positions, market values, previous clubs, new clubs, and transfer fees.
- **Data Cleaning**: Automatically cleans and formats transfer fee data (handling loans, free transfers, etc.).
- **CSV Export**: Saves the consolidated data into a structured CSV file for easy analysis.

## 🛠️ Technologies Used

- **Python 3.x**
- **[Pandas](https://pandas.pydata.org/)**: For data manipulation and CSV export.
- **[BeautifulSoup4](https://www.crummy.com/software/BeautifulSoup/)**: For parsing HTML content.
- **[Requests](https://docs.python-requests.org/)**: For making HTTP requests to Transfermarkt.
- **RegEx**: For pattern matching and string extraction.

## 📋 Prerequisites

Ensure you have Python installed. You will need the following libraries:

```bash
pip install requests pandas beautifulsoup4
```

## 💻 Usage

1.  **Clone the repository** (if applicable) or download the script.
2.  **Run the notebook/script**:
    Open `webscrapingtransfermarkt.ipynb` in Jupyter Notebook or run the Python script.
3.  **Output**:
    The script will generate a CSV file named `webscraping transfermarkt.csv` in your Documents folder:
    `/Users/piyushnandwani/Documents/webscraping transfermarkt.csv`

    > **Note**: You may need to adjust the output path in the script to match your preferred directory.
