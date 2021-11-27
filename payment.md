# If the workers each earn $30 p.h. how much do we owe each one?

```
SELECT
	CONTRACTOR,
	ROUND(SUM (TIME_TAKEN) / 60 / 60 * 30, 2) EARN
FROM
	WORKERS
GROUP BY
	CONTRACTOR;
```

| Contractor      | Earn | 
| :---        |    :----:   |       
| Rob      | 528.85       | 
| Pete   | 26.01        | 
| Joy   | 133.76        | 
