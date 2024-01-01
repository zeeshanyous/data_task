## Objective

In this assignment, you will build an ETL pipeline by performing the following tasks:

1. Read data from a CSV file (`employee_details.csv`. `department_details.csv`)
2. Merge both csv files
2. Transform the data
3. Load the data into a MongoDB database

## Instructions

### 1. Reading Data from CSV

Read CSV as in-memory data structure such as a Pandas DataFrame.

### 2. Transforming the Data

Perform the following transformation tasks:

1. Convert the `BirthDate` from the format `YYYY-MM-DD` to `DD/MM/YYYY`.
2. Do some cleaning on `FirstName` and `LastName` columns when needed and remove any leading/trailing spaces.
3. Merge the `FirstName` and `LastName` columns into a new column named `FullName`.
4. Calculate each employee's age from the `BirthDate` column using as reference **Jan 1st, 2024**. Add a new column named `Age` to store the computed age.
5. Add a new column named `SalaryBucket` to categorize the employees based on their salary as follows:
  - `A` for employees earning below `50.000`
  - `B` for employees earning between `50.000` and `100.000`
  - `C` for employees earning above `100.000`
6. Drop columns `FirstName`, `LastName`, and `BirthDate`.

### 3. Loading the Data into Local MongoDB

Connects to the MongoDB database and inserts the given data into a predefined collection. Ensure that your function creates indexes, if required, to improve performance.

## Deliverables

Upon the completion of the assignment, you should have an ETL pipeline that reads data from a CSV file (`employee_details.csv`,`department_details.csv`), performs the required transformations, and loads the transformed data into a MongoDB database
