# NLP Analysis of Medical Articles

This project focuses on scraping medical articles from the MedlinePlus encyclopedia, processing the text data, and performing basic Natural Language Processing (NLP) analysis.

## Objective

The primary goal of this project is to apply web scraping and NLP techniques to a corpus of medical articles to extract insights and understand the characteristics of the text.

## Methodology

The project follows these steps:

1.  **Web Scraping:**
    -   Scrapes medical articles from the MedlinePlus encyclopedia website (`https://medlineplus.gov/encyclopedia.html`).
    -   Iterates through the alphabet from 'A' to 'R' to gather a diverse set of articles.
    -   For each letter, it fetches up to 20 articles.
    -   Extracts the title and content for each article.

2.  **Text Preprocessing:**
    -   **Tokenization:** Breaks down the text into individual words or tokens.
    -   **Lowercasing:** Converts all text to lowercase to ensure uniformity.
    -   **Stopword Removal:** Removes common words (e.g., "the", "a", "is") that do not carry significant meaning.
    -   **Lemmatization:** Reduces words to their base or dictionary form (e.g., "running" becomes "run").

3.  **Data Storage:**
    -   The scraped and preprocessed data is stored in a CSV file named `medical_articles_A_to_R.csv`.
    -   The CSV file includes the following columns: `URL`, `Title`, `Content`, `Filtered Content`, and `Lemmatized Content`.

4.  **Data Analysis and Visualization:**
    -   The processed data is loaded into a Pandas DataFrame for analysis.
    -   **Word Frequency Analysis:** Calculates the frequency of each word in the lemmatized content and identifies the top 20 most common words.
    -   **Visualization:**
        -   A bar chart is generated to visualize the frequencies of the most common words.
        -   A histogram is created to show the distribution of sentence lengths (number of words per sentence).
    -   **Statistical Analysis:**
        -   **Average Word Length:** Calculates the average length of words in the corpus.
        -   **Unique Words:** Counts the total number of unique words.
        -   **Lexical Diversity:** Measures the richness of the vocabulary by calculating the ratio of unique words to the total number of words.

## Libraries Used

-   **`requests`**: For making HTTP requests to the website.
-   **`BeautifulSoup`**: For parsing HTML and extracting data from web pages.
-   **`csv`**: For writing the scraped data to a CSV file.
-   **`nltk` (Natural Language Toolkit)**: For various NLP tasks, including tokenization, stopword removal, and lemmatization.
-   **`pandas`**: For data manipulation, analysis, and reading the CSV file.
-   **`matplotlib.pyplot`**: For creating visualizations like bar charts and histograms.
-   **`collections.Counter`**: For efficiently counting word frequencies.

## How to Run

1.  Ensure you have Python installed.
2.  Install the required libraries:
    ```bash
    pip install requests beautifulsoup4 nltk pandas matplotlib
    ```
3.  Run the Jupyter notebook `nlp_hw1/NLP_hw1.ipynb`.
