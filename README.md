#  Football Transfer Scraper

A Python tool to scrape European football club transfer data from [Transfermarkt](https://www.transfermarkt.com). This project extracts detailed information about player transfers, including fees, market values, and contract details.

##  Features

- **Comprehensive Data**: Scrapes player names, ages, nationalities, positions, market values, previous clubs, new clubs, and transfer fees.
- **Data Cleaning**: Automatically cleans and formats transfer fee data (handling loans, free transfers, etc.).
- **CSV Export**: Saves the consolidated data into a structured CSV file for easy analysis.

##  How it Works

This project uses a systematic approach to extract and clean data:

1.  **Data Fetching**:
    - Sends an HTTP GET request to Transfermarkt with a custom `User-Agent` header to mimic a real browser and avoid being blocked.

2.  **HTML Parsing**:
    - Uses **BeautifulSoup** to parse the raw HTML response.
    - Identifies specific "boxes" in the HTML structure that contain transfer tables for each club.
    - Distinguishes between **Incoming** and **Outgoing** transfer tables within each club's section.

3.  **Data Extraction**:
    - Iterates through each row (`tr`) of the transfer tables.
    - Uses **RegEx (Regular Expressions)** to precisely extract data points (like Age, Position, Market Value) from the HTML cell strings.

4.  **Data Cleaning & Formatting**:
    - **Translation**: Converts German terms (e.g., "Leihe", "ablösefrei") into English ("Loan", "no fee").
    - **Fee Standardization**: Cleans up transfer fee strings, removing unnecessary HTML tags and formatting loan fees.

5.  **Export**:
    - Consolidates all extracted lists into a **Pandas DataFrame**.
    - Exports the final dataset to a CSV file for use in Excel or further analysis.

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
