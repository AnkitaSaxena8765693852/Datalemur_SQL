# Candidate Skills

#### Suppose you are given a table of candidates and their skills. How many candidates possess each of the different skills? Sort your answers based on the count of candidates, from highest to lowest.
    Assumption:
    There are no duplicates in the candidates table.


### `candidates` Table

| Column Name   | Type    |
|---------------|---------|
| candidate_id  | integer |
| skill         | varchar |

### `candidates` Example Input:

| candidate_id  | skill       |
|---------------|-------------|
| 123           | Python      |
| 123           | Tableau     |
| 123           | PostgreSQL  |
| 234           | R           |
| 234           | PowerBI     |
| 234           | SQL Server  |
| 345           | Python      |
| 345           | Tableau     |


### SQL Query for Generating the Output

```sql
SELECT skill, 
       count(candidate_id) as count
FROM candidates
GROUP by skill
ORDER by count DESC;
```

### Example Output:

| skill       | count |
|-------------|-------|
| Python      | 4     |
| Tableau     | 4     |
| PostgreSQL  | 2     |
| PowerBI     | 1     |
| R           | 1     |
| SQL Server  | 1     |
| Java        | 1     |
