
Scraping latest papers from [arXiv.org](https://arxiv.org/): Searching for citations
====================

This script scrapes the latest papers from specified categories on arXiv, extracts the text from their PDFs,
and searches for citations of a specified author within those papers. Then it prints the number of citations 
found in each paper, the total number of citations, and the percentage of papers that cite the author.

## Output example:

`Getting paper identifiers XXXX.YYYYY from listing: https://arxiv.org/list/astro-ph/new
Scraping paper: https://arxiv.org/pdf/2406.01666.pdf
Number of citations: 10 (++++++++++)
Scraping paper: https://arxiv.org/pdf/2406.01673.pdf
Number of citations: 2 (++)
Scraping paper: https://arxiv.org/pdf/2406.01683.pdf
Number of citations: 1 (+)
Scraping paper: https://arxiv.org/pdf/2406.01831.pdf
Number of citations: 19 (+++++++++++++++++++)
Scraping paper: https://arxiv.org/pdf/2406.02072.pdf
Number of citations: 1 (+)
Scraping paper: https://arxiv.org/pdf/2402.18515.pdf
Number of citations: 2 (++)
Scraping paper: https://arxiv.org/pdf/2405.19195.pdf
Total number of citations: 35
6/122 (4.9 %) of papers cite the author Calzetti, D.`

![citations](https://github.com/ianpaga/scrape_papers_arXiv/assets/57350668/b843e6b4-246c-4ca2-94ae-f478fafe6391)

## Workflow:
1. Fetches identifiers of the latest papers from arXiv in specified categories.
2. Constructs the URLs to access the PDFs of these papers.
3. Downloads each PDF and extracts its text.
4. Searches the extracted text for citations of the specified author.
5. Prints the number of citations found in each paper along with a visual representation using plus signs.
6. Displays the total number of citations and the percentage of papers that cite the author.
7. Removes the temporary PDF file after processing.
8. Plots the number of citations for each paper that has at least one citation.
9. Plots a pie chart showing the proportion of papers with at least one citation and papers with no citations.

## Usage:
1. Set the 'author' variable to the name of the author you want to search for.
2. Run the script.

## Requirements: 
1. PyPDF2 can be installed by running pip install PyPDF2 in the terminal.
2. Matplotlib can be installed by running pip install matplotlib in the terminal.
