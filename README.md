Metadata Completeness ETL Pipeline

Technologies: SSIS, SQL Server, Power BI, JSON, C#, ACRCloud, Shazam, OLAF, Custom APIs

Overview
Designed and implemented a robust SSIS package to clean, merge, and enrich music recognition metadata from multiple sources, including APIs, manual recognition, and partner systems (e.g., Shazam, OLAF).

Data Extraction
•	Retrieve song recognition data from a third-party API in JSON format.
Data Ingestion
•	Import JSON data into SQL Server using SSIS (SQL Server Integration Services) with C# script.

Data Merging
•	Merge recognition data from multiple sources:
o	Third-party API
o	Manual recognition
o	Shazam recognition
o	OLAF recognition

Data Cleaning & Transformation in SSIS
•	Exclude false positives from the dataset.
•	Filter duplicate or low-confidence records:
o	Remove records with the same date and time but short duration.
•	Extend play duration for overlapping records:
o	If records overlap and share the same ISRC or Title-Artist combination.
o	If records overlap with Shazam and share the same ISRC or Title-Artist.
o	If records overlap with OLAF and have the same Title-Artist.
•	After extension, recheck for overlaps and remove the record with the shorter duration.

Final Data Insertion
•	Insert the cleaned and merged data into the final metadata table.

Data Export
•	Export the final dataset into a CSV file for reporting or further use.

Power BI Reporting
•	Visualize the final data using Power BI, including:
o	Total recognitions per platform (API, Shazam, OLAF, Manual).
o	Average play duration and overlap adjustments.
o	Before vs. After Cleaning comparisons.
o	Top-recognized songs and artists.
o	Recognition trends over time (daily, weekly, monthly).
o	False positive rate and cleaning impact metrics.


Screenshot


##Author
Arslan Munir  
[LinkedIn](https://www.linkedin.com/in/muhammad-arslan-munir-243a2822/)  
Davis, California, USA
 
