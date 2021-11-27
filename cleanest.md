# Who provides the cleanest data

1. Find the worker that input the most non-alphanumericals in the SKU column of the output table.
```
SELECT CONTRACTOR, COUNT(*) ERRORS
FROM OUTPUT 
INNER JOIN WORKERS ON WORKERS.CORRECT_ID = OUTPUT.CORRECT_ID
WHERE SKU ~ '[^a-zA-Z0-9]'
GROUP BY CONTRACTOR;
```
2. RESULTS

| Contractor      | Errors | 
| :---        |    :----:   |  
| Rob      | 31       | 
| Pete   | 18        | 
| Joy   | 26        | 
