# Apply Filters to SQL Queries

## Project description
I am a security professional at a large organization. Part of my job is to investigate security issues to help keep the system secure. I recently discovered some potential security issues that involve login attempts and employee machines. My task is to examine the organization’s data in their **employees** and **log_in_attempts** tables. To do this, I'll need to use SQL filters to retrieve records from different datasets and investigate the potential security issues. The following steps demonstrate how I used SQL filters to perform various security-related tasks.

## Retrieve after-hours failed login attempts
I recently discovered a potential security incident that occurred after business hours. To investigate this, I queried the **log_in_attempts** table to review after-hours login activity and used filters in SQL to create a query that identifies all failed login attempts that occurred after 18:00.

![image](https://github.com/andrewrodgers90/apply_filters_to_SQL_queries/assets/132149730/1dc23419-cd17-40db-8dbb-24f61a4153a0)

In this example, I started by selecting all records from the **log_in_attempts** table. The line starting WHERE filters the results for records where a log-in attempt was made after 18:00, and the attempt was unsuccessful.

## Retrieve login attempts on specific dates
A suspicious event occurred on 2022-05-09. Any activity that occurred on this date, or the day before, needs to be investigated.

![image](https://github.com/andrewrodgers90/apply_filters_to_SQL_queries/assets/132149730/6b42f74c-7fbb-46d0-92db-eb9a85beb0b7)

Here, I selected all information from the **employees** table, and applied a filter to ensure that only results from the dates specified were returned.

## Retrieve login attempts outside of Mexico
The team has now been asked to investigate any log-in attempts that did not originate in Mexico.

![image](https://github.com/andrewrodgers90/apply_filters_to_SQL_queries/assets/132149730/5193b176-8766-4ce6-b920-8ad6c9bb2feb)

In my query, I start with a NOT filter, to make sure the query does not return records that meet the condition(s) established in the rest of the WHERE filter. The clause 'country LIKE 'MEX%' returns all records with countries that begin with 'MEX'. This is to make sure that records that contain 'MEX' or 'MEXICO' are returned.

## Retrieve employees in marketing

![image](https://github.com/andrewrodgers90/apply_filters_to_SQL_queries/assets/132149730/06d26f93-337c-4185-b1f9-f154b65642c4)

![image](https://github.com/andrewrodgers90/apply_filters_to_SQL_queries/assets/132149730/07a2d5c7-bd5a-4a66-9290-1e25467e1278)

## Retrieve employees in Finance or Sales

![image](https://github.com/andrewrodgers90/apply_filters_to_SQL_queries/assets/132149730/dd24fbf3-5c21-45e9-a8c4-3be8a17a06d2)

## Retrieve all employees not in IT

![image](https://github.com/andrewrodgers90/apply_filters_to_SQL_queries/assets/132149730/d46f3930-3471-4f36-ac32-7b0fc0311168)

## Summary

