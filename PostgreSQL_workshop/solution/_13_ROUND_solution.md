# 13.ROUND()

13.1. Arrondissez le salaire moyen au nombre entier le plus proche
```sql
SELECT ROUND(AVG(salary)) AS average_salary
FROM salaries;
```
13.2. Arrondissez le salaire moyen à une précision de centimes.
```sql
SELECT ROUND(AVG(salary),2) AS average_salary
FROM salaries;

```
13.3. Arrondissez le montant moyen consacré aux salaires pour tous les contrats contrats qui ont commencé après le 1er janvier 1997, avec une précision de quelques centimes.
```sql
SELECT ROUND(AVG(salary), 2) AS average_salary
FROM salaries
WHERE from_date > '1997-01-01';

```
13.4. Trouver le milieu de la fourchette des salaires avec une précision de quelques centimes.
```sql
SELECT ROUND((MAX(salary)-MIN(salary))/2, 2) AS salary_range
FROM salaries;
```
