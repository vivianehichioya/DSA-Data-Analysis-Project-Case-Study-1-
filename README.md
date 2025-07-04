# DSA Data Analysis Project (Case Study 1)
The dataset used for this project was scraped from Amazon Product Pages. Pivot tables and calculated columns were used to analyse the dataset to generate insights that can guide product improvement, marketing strategies and customer engagement.

## Dataset Description
- Product details: name, category, price, discount, and ratings
- Customer engagement: user reviews, titles, and content
- Each row represents a unique product, with aggregated reviewer data stored as comma-separated values
- Total Records: 1,466 rows
- TotalFields: 16 columns

## Exploratory Data Analysis (EDA)
- Data Cleaning
  - Filter was used to check for null values in the dataset.
  - Null values were deleted
- Helper Columns were added
  - Main Product Category (to extract the last subcategory)
      - The code is given as: =TRIM(RIGHT(C2,LEN(C2)-FIND("@",SUBSTITUTE(C2,"|","@",LEN(C2)-LEN(SUBSTITUTE(C2,"|",""))))))
  - Potential Revenue (=actual_price_cell*rating_count_cell)


