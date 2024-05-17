```sql
SELECT agegroup
FROM hr_analytics
GROUP BY agegroup
ORDER BY agegroup
```
|agegroup|
|--------|
|18-25   |
|26-35   |
|36-45   |
|46-55   |
|55+     |

```sql
SELECT maritalstatus
FROM hr_analytics
GROUP BY maritalstatus
ORDER BY maritalstatus
```
|maritalstatus|
|-------------|
|Married      |
|Divorced     |
|Single       |

```sql
SELECT educationfield
FROM hr_analytics
GROUP BY educationfield
ORDER BY educationfield
```
|educationfield|
|--------------|
|Human Resources|
|Life Sciences |
|Marketing     |
|Medical       |
|Other         |
|Technical Degree|

