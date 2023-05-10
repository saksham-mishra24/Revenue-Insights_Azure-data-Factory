# Here is Detailed breakdown of the transformations performed in project:

## Source Tables:

Started with two tables, "bookings" and "hotels," which served as the source for your transformation.

    1. Join Transformation:

* I performed a join operation between the "bookings" and "hotels" tables based on a common column, likely "property_id," to combine the data from both tables into a single dataset.

      2. Derived Columns Transformation:

* After the join, I created several derived columns using the derived column transformation. Here are the derived columns you mentioned:

Stay_duration: Calculated based on check-in and check-out dates to determine the length of stay.
Cancelled_bookings: Derived column indicating the number of bookings that were canceled.
Checked_out: Derived column indicating the number of bookings that were checked out.
No_show: Derived column indicating the number of bookings where guests did not show up.
Select Columns Transformation:

Following the derived column transformation, you selected a subset of columns from the combined dataset. These selected columns likely represent the specific information you wanted to include in your final output.
Aggregate Transformation:

You applied the aggregate transformation to summarize the data and calculate various measures. The measures you mentioned are as follows:

Revenue_realized: Total revenue realized from the bookings.
Revenue_generated: Total revenue generated from the bookings.
Total_bookings: Total number of bookings.
Total_Cancelled_bookings: Total number of bookings that were canceled.
Total_checked_out: Total number of bookings that were checked out.
Total_no_show: Total number of bookings where guests did not show up.
Average_ratings: Average ratings given by guests.
Cancellation %: Percentage of bookings that were canceled.
NoShow%: Percentage of bookings where guests did not show up.
ADR (Average Daily Rate): Average revenue per day.
no_guests: Total number of guests.
room_category: Category of the room booked.
booking_status: Status of the booking.
Stay_duration: Duration of the stay.
The aggregation was performed by grouping the data based on the following columns:

city
Booking_id
Property_name
Property_id
category
booking_platform
Union Transformation:

After the aggregation, you used the union transformation to combine the desired columns into a single dataset.
Sink Transformation:

You used the sink transformation to load the transformed data into the ADLS Gen2 "processed" folder. This step involved storing the final output of your transformation pipeline.
Aggregated_Booking Table Join:

You joined the "aggregated_booking" table with the previously joined table (booking+hotel) to incorporate additional information or enrich the dataset.
Aggregated Function:

Following the join, you applied aggregated functions to create additional measures based on the joined dataset. The specific functions and measures created were not mentioned, so you may want to provide more details about the specific calculations you performed.
Select Columns Transformation:

After applying the aggregated functions, you selected specific columns from the joined dataset, likely choosing the relevant information for your final output.
Sink Transformation:

Finally, you used the sink transformation to store the transformed data from the joined dataset, potentially in another location or folder.

![image](https://github.com/saksham-mishra24/Revenue-Insights_Azure-data-Factory/assets/120908587/f10f683f-81bc-404e-8dc2-596ebb954e26)

![image](https://github.com/saksham-mishra24/Revenue-Insights_Azure-data-Factory/assets/120908587/f2d10e51-70e6-4ca1-9d2e-e598686bc5e7)


![image](https://github.com/saksham-mishra24/Revenue-Insights_Azure-data-Factory/assets/120908587/60b28a63-9820-4958-b2da-0a4ae31d24ac)


### joined hotel & booking - dervied - duplicate columns they isliye -- select -- aggreagte se meausres - join 

![image](https://github.com/saksham-mishra24/Revenue-Insights_Azure-data-Factory/assets/120908587/118e98af-eb84-49fa-a373-14736e6b415d)
![image](https://github.com/saksham-mishra24/Revenue-Insights_Azure-data-Factory/assets/120908587/0114c357-14fb-4e35-a1ef-68a3fde08fbe)


