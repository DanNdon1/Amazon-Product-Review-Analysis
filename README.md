# Amazon-Product-Review-Analysis
This project was completed as part of a Data Analysis Training Program with IncubatorHub, under the Digital Skillup Africa (DSA) initiative. It simulates the role of a Data Analyst at RetailTech Insight, focusing on analyzing real Amazon product review data. The primary aim was to uncover insights related to customer sentiment, product performance, and pricing effectiveness.
The entire project was executed using Microsoft Excel, demonstrating key data analysis skills such as data cleaning, exploratory data analysis (EDA), analytical thinking, and dashboard reporting.

## Project Objectives
- Clean and prepare Amazon product review data for meaningful analysis
- Perform Exploratory Data Analysis (EDA) to uncover trends and patterns
- Conduct in-depth analysis through guided analytical tasks to understand:
    -  Customer behavior and sentiments
     - Rating distribution across product
     - Product performance and pricing effectiveness .

  ## Dataset Description 
The dataset contains information scraped from Amazon product pages, including: • Product details: name, category, price, discount, and ratings • Customer engagement: user reviews, titles, and content • Each row represents a unique product, with aggregated reviewer data stored as comma-separated values. **Total Records: 1,465 rows**
**TotalFields: 16 columns**

## Exploratory Data Analysis (EDA)
The EDA phase focused on understanding the raw dataset, identifying potential quality issues, and exploring general trends of the dataset. Key steps included:
Checking for and handling of data types, missing values, and duplicates outlier
Cleaning and formatting columns like  product names, prices,  Product  category, rating and others
Visualizing distributions of ratings, discounts, and price ranges.
Exploring category-level summaries and review count variations.
Reviewing category-wise summaries and identifying patterns in review counts
This phase helped ensure data readiness for deeper insights.
Key steps included:
## Checking for and handling of  missing values, duplicates  and Blank cell to ensure accuracy and data consistency.

### Checking for and Removing Duplicates
Since each row represents a unique product, the Product ID must be unique. Duplicate rows with the same Product ID and Product Name can distort key metrics such as average rating, total reviews, and total revenue during analysis. To remove duplicates, the entire dataset was selected, and the Remove Duplicates feature was applied using:
**Home > Data Tools > Remove Duplicates in Excel.**
A total of 114 duplicate rows were removed, reducing the dataset to 1,351 unique product entries.
## Handling Missing Values and Data Validation
During the exploration of the raw dataset, I used the filter tool to inspect each column for missing values, inconsistencies, and formatting errors.
In **Column H**, I identified an incorrectly formatted price value: 1,39,900 instead of the correct 1,390,900. To correct this, I filtered the column, unchecked all values, selected the incorrect entry, updated it to the correct format, and then re-applied the filter to restore the full dataset view. This ensured accuracy in subsequent Analysis 
Handling Blank Cells in Column L
**Column L** contained two blank cells, which were identified using the filter tool. These blanks were replaced with 0 using the Replace shortcut (Ctrl + H) to maintain data consistency.
**Column I contains '|'**, it was filter and replaced with 0 through filter and replace tool.
Cleaning Special Characters in Column I
**Column I** contained the character ‘|’, which was identified using the filter tool. It was then replaced with 0 using the Find and Replace function for consistency.
## Cleaning and Formatting Columns and Data Types
The Category column contained subcategories separated by the pipe symbol (|). To clean and format this column:
1. The entire column was copied to a new worksheet.
2. Using the Text to Columns feature, the data was split at each | symbol.
3. To reconstruct a meaningful main category, the **CONCATENATE** function was used along with the ISBLANK function:
**=IF(ISBLANK(C2), B2, CONCATENATE(B2, " & ", C2))**
4. The result was then copied and pasted back into the main dataset, replacing the original Category column.
This process ensured each product had a clear and consistent category label, suitable for grouping and filtering during analysis.
## Data Type Handling for Consistency
To ensure consistency and accurate analysis:
- Percentages were converted to whole numbers for easier comparison.
- Prices were formatted as numbers to enable calculations like revenue and discount analysis.
- Ratings and Review Counts were changed to numeric types for proper aggregation.
- Product IDs/Names were kept as text to preserve formatting.
These changes were necessary to avoid errors during filtering, sorting, and performing calculations, and to maintain data integrity throughout the analysis process.

### Visualizing distributions of ratings, discounts, and price
### Exploring category-level summaries and review count variations.
### Reviewing category-wise summaries and identifying patterns in review counts
This phase helped ensure data readiness for deeper insights.<br>

 :-- Raw Dataset--: | :--cleaned dataset--:


