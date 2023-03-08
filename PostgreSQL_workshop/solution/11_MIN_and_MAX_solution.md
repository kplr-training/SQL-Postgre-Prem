# 11.MIN() and MAX()
11.1. Quel est le salaire le plus élevé versé par l'entreprise ?
```sql
SELECT MAX(salary) AS Maximum_salary
FROM salaries;
```
11.2. Quel est le salaire le plus bas payé par l'entreprise ?
```sql
SELECT MIN(salary) AS Minimum_salary
FROM salaries;
```
11.3. Quel est le numéro d'employé le plus bas dans la base de données ?
```sql
SELECT MAX(emp_no) AS lowest_emp_no
FROM employees;
```
11.4. Quel est le numéro d'employé le plus élevé de la base de données ?
```sql
SELECT MIN(emp_no) AS highest_emp_no
FROM employees;
```
