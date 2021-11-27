# Who is the most productive - provide a report

1. Find the total capture counts for each worker.
```
SELECT
	CONTRACTOR,
	COUNT (CONTRACTOR) CAPTURE_COUNT
FROM
	WORKERS
GROUP BY
	CONTRACTOR;
```
2. Find the total time taken to capture products for each worker
```
SELECT
	CONTRACTOR,
	ROUND(SUM (TIME_TAKEN),2) TOTAL_TIME_WORKED
FROM
	WORKERS
GROUP BY
	CONTRACTOR;
```
3. Find the most productive worker.
```
SELECT
	CONTRACTOR,
	ROUND(COUNT (CONTRACTOR) / SUM (TIME_TAKEN),5) PRODUCTIVITY 
FROM
	WORKERS
GROUP BY
	CONTRACTOR;
```
4. RESULTS


| contractor      | productivity |
| :---        |    :----:   |  
| Rob      | 0.00539       |
| Pete   | 0.03876        |
| Joy   | 0.01115        |


