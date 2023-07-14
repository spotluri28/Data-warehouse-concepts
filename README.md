# Data-warehouse-concepts

Slowly Changing Dimension (SCD) in Data Warehouse

A Slowly Changing Dimension (SCD) is a dimension that stores and manages both current and historical data overtime in data warehouse. It is considered and implemented as one of the most critical ETL task in tracking the history of dimension records.

Slowly Changing Dimension (SCD) are dimensions that changes slowly over time, rather than regular bases. In data warehouse environment, there may be requirement to keep track of the change in dimension value and are used to report historical data at any given of time.

We can implement slowly changing dimension (SCD) using various approaches such as:

1.	Type 0: Always retains original

2.	Type 1: Keeps latest data, old data is overwritten

	Type 2: Keeps the history of old data by adding new row
	Type 3: Adds new attribute to store changed value
	Type 4: Uses separate history table
	Type 6: combination of type 1, 2 and 3
Type 0:
This refers to attributes that never change and will not be updated in the data warehouse. An example of SCD Type 0 would be a record we would not expect to ever change such as date of birth or an employee’s start date with a company. As a result, we would not expect this dimension to change in our data warehouse.
SCD Type 0 refers to a methodology where no historical data is stored or tracked for slowly changing dimensions. It means that when changes occur in the dimension data, the existing records are simply updated with the new values, overwriting the previous values without preserving any historical information.
This type of SCD is generally used for reference data where classifiers such as date of birth or employee’s start date etc., is used. There is rarely a need to delete or update the underlying data.
Attributes of dimension which never change their value.
Original values of attributes remain the same.
![image](https://github.com/spotluri28/Data-warehouse-concepts/assets/17102088/6f76923b-eaa0-440c-897c-44078c05e4d3)
