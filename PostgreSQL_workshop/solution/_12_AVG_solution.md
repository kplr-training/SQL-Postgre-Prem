# 12.AVG()
12.1. Combien l'entreprise a-t-elle versé en moyenne aux salariés ?
```sql
SELECT AVG(salary) as average_salary
FROM salaries;
```
12.2. Quel est le salaire annuel moyen versé aux employés qui ont commencé à travailler après le 1er janvier 1997 ?
```sql
SELECT AVG(salary) as average_salary
FROM salaries
WHERE from_date > '1997-01-01'
```
