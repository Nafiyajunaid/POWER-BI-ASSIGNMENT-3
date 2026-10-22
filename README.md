# POWER-BI-ASSIGNMENT-3
Data Transformation:
● Restrict the "List of Orders" table to only the first 500 rows.
Home > Keep Rows > Keep Top Rows > 500.
● Ensure the “Order Date” column in the “List of Orders” table is set to data type 'Date'.
Transform > Data Type > Date
● Change the data type of “Amount” and “Target” columns to ‘Fixed Decimal Number’.
 Select Columns > Transform > Data Type > Fixed Decimal Number
● Format the "CustomerName" column into proper case, ensuring consistentcapitalization for each word.
Transform > format > Capitalise each Word
● Merge the "State" and "City" columns to create a new column named "Location" inthe format ‘City, State’.
Select both columns > Transform > Merge Columns > By comma 
● Create a new custom column named "Profit Margin" as the percentage of "Profit"
divided by "Amount".
Add custum column > =[profit]/[Amount]
Change data type to percentage

● Add a new conditional column named "Profit Status" based on the values in the "Profit" column. The conditions are as follows: if the profit is less than 0, the label should be "Loss"; if the profit equals 0, the label should be "Break-Even"; and if the profit is greater than 0, the label should be "Profit".
Add column > Conditional column > Add conditions one by one
Profit	is less than	0	Loss
Profit	equals	0	Break-Even
Profit	is greater than	0	Profit

Merging Data (Joins):
● Merge the "List of Orders" and "Order Details" tables into a new single table named "Orders Data" based on the "Order ID" relationship.
Home > Merge Queries > Merge Queries as New.First table: List of Orders Second table: Order Details .Select the Order ID column in both tables.Choose the Left Outer join type.Rename the new query to Orders Data.

Handling Missing Data & Duplicate Data:
● Identify missing values in the data and determine a strategy to address them.
Select a table. Go to View. Enable Column quality. There was no missing values
● Check for duplicate rows and define a strategy to handle duplicates.
Select list of Orders table.Home > Remove Rows > Remove Duplicates.

Sorting and Filtering Data:
● In the ‘Orders Data’ table, utilize sorting and filtering techniques on columns like Order Date, State or Category to analyze data based on specific criteria:
◆ Sort the orders by Order Date in descending order to analyze recent trends.
Select the Orders Data table.Click the dropdown arrow on the Order Date column.Select Sort Descending.
◆ Filter the orders to focus only on a specific state (e.g., Tamil Nadu) for regional analysis.
Find the State column.Click its filter dropdown.Uncheck Select All.Select Tamil Nadu.

Grouping and Aggregating Data:
● Duplicate the “Order Details” table and calculate the count of each Order ID, average profit by Category or total amount by Sub-Category.
Order Details > Duplicate. Home > Group By.
Group by	Order ID >New column name	: Count > Operation	Count Rows
Group by	Category > New column name: Average Profit > Operation	Average > Column	Profit
Group by	Sub-Category > New column name	Total Amount > Operation	Sum > Column	Amount

● Duplicate the “Sales Target” table and aggregate the total target amount by Month of
Order Date.
Sales Target >  Duplicate.  Home > Group By.
Group by	Month > New column name	Total > Operation	Sum Column	Target 

Data Modeling:
● Establish a relationship between the “List of Orders” and “Order Details” tables using
the ‘Order ID’ column.
Drag Order ID from List of Orders onto Order ID in Order Details.

● Build a relationship between the “Order Details” and “Sales Target” tables based on
the ‘Category’ column. Click "Manage relationships" and ensure this relationship is
active.
Drag Category from Sales Target onto Category in Order Details. relationship is
active.
