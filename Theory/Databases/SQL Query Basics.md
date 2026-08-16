
# Naming Convention 
At least for Leetcode SQL Questions:
Column = camelCase
Table = PascalCase
Keywords = ALLCAPS

# Basic Queries
```sql
#Ordering
SELECT (table/a).column (AS newName)
FROM table (alias a)
JOIN table ON condition
WHERE condition
GROUP BY condition
HAVING condition
ORDER BY column
```

### AS
Renames column

# Equality

### Null
``` mysql
IS NULL
```

