# RA task1_20250405
# AR Buyer - Customer Name Matching

This project aims to identify potential matches between a firm's largest customers and its main sources of accounts receivable (AR buyers) using fuzzy name matching techniques.

## Folder Structure
- `fuzzy_match.ipynb`: Jupyter notebook containing all Python code and annotations.
- `data/`:  – Folder containing:
  - `ar-sale-buyer-match_forShuning.zip`: Raw data of sellers, customers, and AR buyers.
  - `China-City-List-latest.csv`: Chinese city/province name list for location matching.
  - `df_fuzzymatch.csv`: fuzzy score for the AR buyer and customer that are in the same city.
  - `df_fuzzymatch85.csv`: selected data when threshold for fuzzy score is 85.
  - `df_fuzzymatch90.csv`: selected data when threshold for fuzzy score is 90.

## Methodology

1. Extract location names (province/city) from customer and AR buyer names.
2. Filter out unmatched locations.
3. Use `fuzzywuzzy` to compute name similarity scores.
4. Choose a threshold to retain likely matches (e.g. score ≥ 85).
5. Output a final matched list for manual review.

## Dependencies

Make sure the following Python packages are installed:
- `pandas`
- `jieba`
- `fuzzywuzzy`
 
