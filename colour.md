# How many different colours of product does each person capture.

```
SELECT
	CONTRACTOR,
    COLOUR,
	COUNT (COLOUR)
FROM
	WORKERS
INNER JOIN OUTPUT ON WORKERS.CORRECT_ID = OUTPUT.CORRECT_ID
GROUP BY
		CONTRACTOR,
    COLOUR
ORDER BY CONTRACTOR;
```

RESULTS

| Contractor      | Colour | Count     |
| :---        |    :----:   |          ---: |
| Joy      | Red       |  54  |
| Joy   | Green        |   106  |
| Joy      | Blue       |  18  |
| Pete   | Red        |  39    |
| Pete      | Blue       |  12  |
| Pete   | Green        |   70    |
| Rob      | Green       |  208  |
| Rob   | Blue        |   33    |
| Rob      | Red       |  101 |
