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
- Helper Columns were added using calculated columns.
  - Main Product Category - to extract the last subcategory
      - formula used: =TRIM(RIGHT(C2,LEN(C2)-FIND("@",SUBSTITUTE(C2,"|","@",LEN(C2)-LEN(SUBSTITUTE(C2,"|",""))))))
  - Potential Revenue
      - (=actual price cell * rating count cell)
  - Price range buckets, gotten by creating a group table and apply
      - formula used: =VLOOKUP($E2,$V$3:$W$9,2,1), where E2=actual price, $V$3:$W$9 = the group table range with absolute referencing
  - Rating review combined
      - =rating + (rating_count / MAX(rating count range)
   
## Data Analysis
Pivot table was used.

## Results
1. Average Discount Percentage by Category: Cable connection protectors, earpads and phone charms had the highest average discounted percentage while basic, coloured paper and 9 others had the lowest average discounted percentage (0.00)
2. Number of Products Listed Under Each Category: USB Cables had the highes number listed (233), followed by Smart watches (78), smart phone (68) and smart televisions (63).
3. Total number of reviews by category: USB Cables had the highes number of reviews (231), followed by Smart watches (78), smart phone (68) and smart televisions (63).
4. Highest Rated Product: Mice and USB cables (5 ratings each)

 
	





