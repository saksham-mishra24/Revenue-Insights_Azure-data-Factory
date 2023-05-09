Execution Steps:
Data Ingestion:

Obtain the hospitality data from the client in CSV format.
Set up an Azure Data Factory (ADF) pipeline to ingest the data into Blob Storage.
Configure the necessary connections, such as the source CSV files and the Blob Storage account.
Define any required transformations or data manipulations during the ingestion process, if applicable (e.g., data format conversions, cleansing, or filtering).
Data Transformation using Data Flow:

Create a Data Flow activity within ADF to perform advanced data transformations and processing.
Open the Data Flow and define the following steps:
Source: Read the CSV files (dates, hotels, rooms, bookings, aggregated_bookings) from Blob Storage as the source datasets.
Derived Column: Create calculated or modified columns based on specific expressions, formulas, or business rules.
Aggregate: Calculate aggregate values (e.g., sum, count, average) based on desired grouping and aggregation functions.
Union: Combine multiple datasets or sources into a unified dataset.
Select: Choose relevant columns and their order for further processing.
Define the following measures using appropriate transformations within the Data Flow:
Revenue: Calculate the total revenue generated from bookings.
Total Bookings: Count the number of bookings made.
Total Capacity: Determine the total available capacity (e.g., number of hotel rooms).
Total Successful Bookings: Count the number of bookings successfully completed.
Occupancy %: Calculate the percentage of occupied rooms or occupancy rate.
Average Rating: Compute the average rating of the hotels.
Number of Days: Calculate the duration of bookings or stays.
Total Cancelled Bookings: Count the number of bookings that were canceled.
Cancellation %: Calculate the percentage of bookings that were canceled.
Total Checked Out: Count the number of bookings that have been checked out.
Total No-show Bookings: Count the number of bookings where guests did not show up.
No-show Rate %: Calculate the percentage of no-show bookings.
ADR (Average Daily Rate): Calculate the average rate per day for bookings.
Validate and test the Data Flow to ensure the desired transformations and measures are correctly applied.
Data Sink:

Configure a sink within ADF to store the processed data.
Connect the output of the Data Flow to Azure Data Lake Storage (ADLS) Gen2 as the destination for storing the transformed data.
Set up the necessary credentials, permissions, and folder structure within ADLS Gen2 to store the processed data efficiently.
Data Visualization and Reporting:

Establish a connection between ADLS Gen2 and Power BI to access the processed data.
Design and create visualizations, dashboards, and reports in Power BI based on the defined measures:
Revenue
Total Bookings
Total Capacity
Total Successful Bookings
Occupancy %
Average Rating
Number of Days
Total Cancelled Bookings
Cancellation %
Total Checked Out
Total No-show Bookings
No-show Rate %
ADR
