# plain_text_to_sql
Convert plain text to SQL query using OpenAI API.

## How to run
The solution was created using Python version 3.10.13 on Windows 11.

1. Clone this repo
2. Run requirements.txt (`pip install -r requirements.txt`).
3. Open convert_text_to_sql.ipynb
4. Replace <insert your servername> with your SERVERNAME
4. [Optional] Make changes to other functionalities, like text to convert to SQL syntax (text_to_translate)/model used/database/schemas.
5. Run convert_text_to_sql.ipynb

## How to reproduce sample database
Follow steps from https://github.com/microsoft/sql-server-samples/tree/master/samples/databases/adventure-works, especially https://github.com/microsoft/sql-server-samples/tree/master/samples/databases/adventure-works#to-install-adventureworks.

SQL Server 2022 Express with SQL Server Management Studio 20.2 were used to upload AdventureWorks database.
You can download SQL Server from https://www.microsoft.com/pl-pl/sql-server/sql-server-downloads and Management Studio from
https://learn.microsoft.com/en-us/sql/ssms/download-sql-server-management-studio-ssms?view=sql-server-ver16#download-ssms.

## Assumptions
* Database representation (schema, table, column name and data type) is queried using SQL and then used in the prompt.
* SQL Server is used in the solution.
	* Additionally, there is provided commented code where OpenAI API is queried to generate SQL code that will return table representation in a specified SQL dialect. Keep in mind that this code wasn't tested in different SQL dialects.
