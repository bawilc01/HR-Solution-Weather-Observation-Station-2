# HR-Solution-Weather-Observation-Station-2
Solutions for MySQL and SQL Server

## PROBLEM
Query the following two values from the STATION table:

- The sum of all values in LAT_N rounded to a scale of 
decimal places.
- The sum of all values in LONG_W rounded to a scale of
decimal places.

## SQL SERVER:
SELECT CAST(ROUND(SUM(LAT_N),2) AS DECIMAL(16,2)), CAST(ROUND(SUM(LONG_W), 2) AS DECIMAL(16, 2))
FROM STATION;

OR

SELECT CAST(ROUND(SUM(LAT_N),2) AS NUMERIC(36,2)), CAST(ROUND(SUM(LONG_W), 2) AS NUMERIC(36, 2))
FROM STATION;

OR

SELECT CONVERT(DECIMAL(16,2), SUM(LAT_N)), CONVERT(DECIMAL(16, 2), SUM(LONG_W))
FROM STATION;

## MySQL:
SELECT ROUND(SUM(LAT_N), 2), ROUND(SUM(LONG_W), 2) 
FROM STATION;


