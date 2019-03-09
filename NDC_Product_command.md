## Copy the data into /neo4j-community-3.5.3/import

```
LOAD CSV WITH HEADERS from 'file:///product.txt' as row
FIELDTERMINATOR '\t'
CREATE (n:Medicine)
SET n = row

CREATE INDEX ON :Medicine(PRODUCTID)


```

## Querying
```
match(n:Medicine) return n limit 10
```
