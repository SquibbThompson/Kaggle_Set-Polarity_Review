# Kaggle_Set-Polarity_Review

Book Review Polarity Analyzer

This repository contains a script that reads in a dataset of book reviews, computes a polarity ratio for each review, and then presents this data in various forms including a table, a bar chart, a scatter plot, and a histogram.

The polarity ratio is computed as the ratio of 5-star ratings to 1-star ratings for each book. The script also computes a positivity ratio as the ratio of 5-star and 4-star ratings to 1-star and 2-star ratings.
Requirements

To run the script, you need:

    Python 3.7+
    pandas
    numpy
    panel
    matplotlib
    panel

These can be installed with pip:

shell

pip install pandas numpy panel matplotlib

Dataset

The script requires a CSV file with book reviews. This file should contain the following columns:

    'title'
    'star1'
    'star2'
    'star4'
    'star5'
    'n_reviews'
    'avg_reviews'

Each of the 'starX' columns should contain the percentage of reviews with X stars, as a string ending in '%'. The 'n_reviews' column should contain the number of reviews, as a string with commas. The 'avg_reviews' column should contain the average rating.

The default file path for the dataset is '/Users/evanparsons/Downloads/Plot/final_book_dataset_kaggle2.csv'. If your dataset is in a different location, you'll need to modify the file_path variable in the script.
Output

The script will output a CSV file called 'output.csv' in the current directory. This file will contain the original data, plus the computed polarity and positivity ratios for each book.

The script also displays a panel with four tabs:

    'Data Table': A table showing the book titles, polarity ratios, number of reviews, average reviews, and positivity ratios.
    'Bar Chart': A bar chart showing the mean polarity ratio for different ranges of the number of reviews.
    'Scatter Plot': A scatter plot showing the polarity ratio vs. the number of reviews for each book.
    'CLT Histogram': A histogram of sample means of the polarity ratio, demonstrating the Central Limit Theorem.

Usage

To run the script, simply execute it with Python:

shell

python book_review_polarity.py

Note: The script performs several data cleaning operations, including removing rows with missing or infinite values. Therefore, the output may contain fewer rows than the input, depending on the quality of the input data.
