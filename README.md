# SKUvantage Excel Test
Convert spreadsheet into sql to query workers data for SKUvantage.

1. Find the correct SKU ID by extracting only numbers from SKU in the output table to match SKUid in the workers table and create a relational database.
```
=REGEXREPLACE(C3,"\D+", "")
```
