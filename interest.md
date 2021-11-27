# Anything else interesting?

1. Found the average time to capture products for each worker. 

```
SELECT
	CONTRACTOR,
	AVG (TIME_TAKEN) AVERAGE_TIME_TAKEN
FROM
	WORKERS
GROUP BY
	CONTRACTOR;
```
RESULTS
| Contractor      | Average_Time_Taken | 
| :---        |    :----:   |        
| Rob      | 185.5617812803684211       | 
| Pete   | 25.7988741905785124        | 
| Joy   | 89.6734735601061453        | 
