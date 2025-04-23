# Streams
Capture and track changes to tables, providing a way to monitor data transformations and identify potential quality issues in real-time. 
# Tasks
Automate the execution of SQL queries and stored procedures, including data quality checks, on a predefined schedule or based on changes in a stream. 

# Example Workflow
- A stream is created on a source table to capture data changes. 
- A task is defined to run a data quality check on the stream's data whenever changes are detected. 
- The task can utilize DMFs or custom UDFs to perform specific quality checks, such as checking for null values or duplicate entries. 
- Based on the check results, actions can be taken, such as logging errors, alerting users, or retrying the transformation process. 
