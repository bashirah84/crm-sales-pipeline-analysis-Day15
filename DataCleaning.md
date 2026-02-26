# Data Cleaning and Structuring

## Handling Missing Values
- Filled or removed nulls in critical columns (e.g., Order Date) to maintain analysis integrity.

## Correcting Data Types
- Converted Latitude and Longitude from text to numbers for mapping purposes.
- Ensured numeric columns (Organisation Size, Deal Value) are recognized as numbers.

## Removing Duplicates
- Checked for duplicate records based on Lead ID and Organisation.
- Removed duplicates to prevent skewed analysis.

## Standardizing Text Columns
- Corrected inconsistent text entries in Country, Industry, and Organisation columns.
- Standardized capitalization and removed trailing spaces.

## Validating Data Consistency
- Verified logical consistency across columns (e.g., Deal Status matches Lead progression).
- Checked for outliers or erroneous values in numeric columns.
