#athletic_sales_analysis

#Background


##Analyze sales data to gain insights into which cities in the U.S. have sold the most athletic wear over two years. Next, determine which retailers had the greatest total sales for athletic wear, and which retailers sold the most women's athletic footwear. Finally, determine which day and week had the highest sales for women's athletic footwear.

1. Combine and Clean the Data
Import the two CSV files, athletic_sales_2020.csv and athletic_sales_2021.csv, and read them into DataFrames.

The column titles for athletic_sales_2020.csv are:
retailer, retailer_id, invoice_date, region, state, city, product, price_per_unit, units_sold, total_sales, operating_profit, sales_method

The column titles for athletic_sales_2021.csv are:
retailer, retailer_id, invoice_date, region, state, city, product, price_per_unit, units_sold, total_sales, operating_profit, sales_method

Check that the columns in the two DataFrames have similar names and data types.

Pseudocode prompt:
 Read the CSV files into DataFrames.
Display the 2020 sales DataFrame.
Display the 2021 sales DataFrame.

Combine the two DataFrames by the rows using an inner join, and reset the index.

Pseudocode prompt:
Check the 2020 sales data types.
Check the 2021 sales data types.


Pseudocode prompt:
Combine the 2020 and 2021 sales DataFrames on the rows and reset the index. 
After combining the DataFrames, do the following:
Check if there are any null values.
Check each column’s data type.
Convert the "invoice_date" column to a datetime data type.
Confirm that the data type has been changed.


Pseudocode prompts:
# Check if any values are null.
# Check the data type of each column
# Convert the "invoice_date" to a datetime datatype
# Confirm that the "invoice_date" data type has been changed.

Notes from AI Assistant:
You can specify the format using the format parameter in the pd.to_datetime() function. For example, if your dates are in the format 'YYYY-MM-DD', you can specify the format as follows:  combined_df['invoice_date'] = pd.to_datetime(combined_df['invoice_date'], format='%Y-%m-%d')
Replace '%Y-%m-%d' with the actual format of your dates. This will help pandas parse the dates correctly and avoid the warning message.


2. Determine which Region Sold the Most Products
Use either the groupby or pivot_table function to create a multi-index DataFrame with the "region", "state", and "city" columns.


Rename the aggregated column to reflect the aggregation of the data in the column.


Sort the results in descending order to show the top five regions, including the state and city that have the greatest number of products sold. 
Pseudocode prompts:

Using groupby

Show the number products sold for region, state, and city.
Rename the sum to “Total_Products_Sold".

Show the top 5 results.

Using pivot_table

Show the number products sold for region, state, and city.
Rename the "units_sold" column to "Total_Products_Sold"

Show the top 5 results.

3. Determine which Region had the Most Sales
Use either the groupby or pivot_table function to create a multi-index DataFrame with the "region", "state", and "city" columns.
Rename the aggregated column to reflect the aggregation of the data in the column.
Sort the results in descending order to show the top five regions, including the state and city that generated the most sales. 

Pseudocode prompts:

Using goupby

Show the total sales for the products sold for each region, state, and city.
Rename the "total_sales" column to "Total Sales"


Show the top 5 results.


Using pivot_table

Show the total sales for the products sold for each region, state, and city.


Optional: Rename the "total_sales" column to "Total Sales"


Show the top 5 results.



4. Determine which Retailer had the Most Sales
Use either the groupby or pivot_table function to create a multi-index DataFrame with the "retailer", "region", "state", and "city" columns.
Rename the aggregated column to reflect the aggregation of the data in the column.
Sort the results in descending order to show the top five retailers along with their region, state, and city that generated the most sales. 

Pseudocode prompts:
Show the total sales for the products sold for each retailer, region, state, and city.
Rename the "total_sales" column to "Total Sales"


Show the top 5 results.



Show the total sales for the products sold for each retailer, region, state, and city.


Optional: Rename the "total_sales" column to "Total Sales"


Show the top 5 results.



5. Determine which Retailer Sold the Most Women's Athletic Footwear
Filter the combined DataFrame to create a DataFrame with only women's athletic footwear sales data.
Use either the groupby or pivot_table function to create a multi-index DataFrame with the "retailer", "region", "state", and "city" columns.
Rename the aggregated column to reflect the aggregation of the data in the column.
Sort the results in descending order to show the top five retailers along with their region, state, and city that sold the most women's athletic footwear. 


Pseudocode prompts:

Filter the sales data to get the women's athletic footwear sales data.

Using groupby
Show the total number of women's athletic footwear sold for each retailer, region, state, and city.
Rename the "units_sold" column to "Womens_Footwear_Units_Sold"


Show the top 5 results.


Using pivot_table

Show the total number of women's athletic footwear sold for each retailer, region, state, and city.


Rename the "units_sold" column to "Womens_Footwear_Units_Sold"


Show the top 5 results.



6. Determine the Day with the Most Women's Athletic Footwear Sales
Create a pivot table with the "invoice_date" column as the index and the "total_sales" column as the values parameter.
Rename the aggregated column to reflect the aggregation of the data in the column.
Apply the resample function to the pivot table, place the data into daily bins, and get the total sales for each day.
Sort the resampled DataFrame in descending order to show the top 10 days that generated the most women's athletic footwear sales. 

Pseudocode prompts:

Create a pivot table with the 'invoice_date' column is the index, and the "total_sales" as the values.


Optional: Rename the "total_sales" column to "Total Sales"


Show the table.
Resample the pivot table into daily bins, and get the total sales for each day.


Sort the resampled pivot table in descending order on "Total Sales".

7. Determine the Week with the Most Women's Athletic Footwear Sales
Apply resample to the pivot table above, place the data into weekly bins, and get the total sales for each week.
Sort the resampled DataFrame in descending order to show the top 10 weeks that generated the most women's athletic footwear sales. 


Pseudocode prompts:

Resample the pivot table into weekly bins, and get the total sales for each week.


Sort the resampled pivot table in descending order on "Total Sales".

