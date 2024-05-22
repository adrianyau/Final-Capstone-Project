Group by age groups:

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

Group by marital status:

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


Group by education fields:

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

Group by departments:

```sql
SELECT department
FROM hr_analytics
GROUP BY department
```
|department|
|----------|
|Human Resources|
|Research & Development|
|Sales     |

Group by jole roles:

```sql
SELECT jobrole
FROM hr_analytics
GROUP BY jobrole
ORDER BY jobrole
```
|jobrole|
|-------|
|Healthcare Representative|
|Human Resources|
|Laboratory Technician|
|Manager|
|Manufacturing Director|
|Research Director|
|Research Scientist|
|Sales Executive|
|Sales Representative|


