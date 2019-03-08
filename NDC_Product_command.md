## copy the data into /Users/vtssogari/Downloads/neo4j-community-3.5.3/import

```
LOAD CSV WITH HEADERS from 'file:///product.txt' as row
FIELDTERMINATOR '\t'
CREATE (n:Medicine)
SET n = row
```

## Querying
```
match(n:Medicine) return n limit 10
```
