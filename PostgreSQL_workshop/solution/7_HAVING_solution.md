# 9.Having
9.1. Récupérer une liste de tous les employés qui ont été employés à partir du 1er janvier 2000.
```sql
SELECT *
FROM employees
WHERE hire_date >= '2000-01-01';
```
Cela produira-t-il le même résultat ? :
```sql
SELECT *
FROM employees
HAVING hire_date >= '2000-01-01';
```
9.2. Corriger la réponse suivante pour extraire une liste de noms d'employés, où le nombre d'employés est supérieur à 15, en les classant par prénom:
```sql
SELECT first_name, COUNT(first_name) as names_count
FROM employees
WHERE COUNT(first_name) > 15
GROUP BY first_name
ORDER BY first_name;
```
Bonne réponse :
```sql
SELECT first_name, COUNT(first_name) as names_count
FROM employees
GROUP BY first_name
HAVING COUNT(first_name) > 15
ORDER BY first_name;
```
9.3 Récupérez une liste de numéros d'employés et le salaire moyen. Assurez-vous d'obtenir les résultats où le salaire moyen est supérieur à 120 000 $.
```sql
SELECT emp_no, AVG(salary) as average_salary
FROM salaries
GROUP BY emp_no
HAVING AVG(salary) > 120000
ORDER BY emp_no;
```
9.4 Extraire une liste de tous les noms qui ont été rencontrés moins de 200 fois. Les données concernent les personnes embauchées après le 1er janvier 1999.
```sql
SELECT emp_no, first_name, hire_date, COUNT(first_name) AS names_count
FROM employees
WHERE hire_date > '1999-01-01'
GROUP BY emp_no
HAVING COUNT(first_name) < 200
ORDER BY first_name;
```
9.5 Sélectionnez les numéros d'employés de tous les individus qui ont signé plus d'un contrat après le 1er janvier 2000.
```sql
SELECT emp_no, COUNT(from_date)
FROM dept_emp
WHERE from_date > '2000-01-01'
GROUP BY emp_no
HAVING COUNT(from_date) > 1
ORDER BY emp_no;
```
