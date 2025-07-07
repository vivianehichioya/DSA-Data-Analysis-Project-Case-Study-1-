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
![Dashboard 1](https://github.com/user-attachments/assets/a7400774-b58e-474a-9174-c66de4f78b62)
![Dashboard 2](https://github.com/user-attachments/assets/c54197ff-c082-4b95-bf5d-92aee136c47d)
![Dashboard 3](https://github.com/user-attachments/assets/7f99b11f-14ca-4b11-b894-ea609acdb194)
![Dashboard 4](https://github.com/user-attachments/assets/15a5bf93-e423-42cb-aab4-b58da3826097)
![Dashboard 5](https://github.com/user-attachments/assets/3317701a-9ab9-46de-a28f-c6525d376de1)









