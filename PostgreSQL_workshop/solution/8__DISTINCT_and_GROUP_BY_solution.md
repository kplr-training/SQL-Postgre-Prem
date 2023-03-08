# DISTINCT et GROUP BY

8.1 Selectionner tous les prénoms dans la table **employees**.
```sql
SELECT first_name
FROM employees;
````
8.2 Obtenir le prénom (first name) dans la table **employees** et regrouper par prénom.
```sql
SELECT first_name
FROM employees
GROUP BY first_name;
```
8.3 Obtenir les prénoms différents qu'on peut trouver dans la table **employees**.
```sql
SELECT DISTINCT first_name
FROM employees;
```
8.4 Quels prénoms différents peut-on trouver dans la table **employees** ?
```sql
SELECT first_name
FROM employees
GROUP BY first_name;
```
8.5 Combien de prénoms différents peut-on trouver dans la table **employees** ?
```sql
SELECT COUNT(DISTINCT first_name)
FROM employees;
```
8.6 Combien de prénoms différents y a-t-il dans la table **employees** ? et ordonner par prénom en ordre décroissant ?
```sql
SELECT first_name, COUNT(first_name)
FROM employees
GROUP BY first_name
ORDER BY first_name DESC;
```
8.7 Combien de départements différents y a-t-il dans la base de données **employees** ? Indice : Utilisez la table **dept_emp**
```sql
SELECT COUNT(DISTINCT dept_no) AS dept_count
FROM dept_emp;
```
8.8 Récupérer une liste de combien d'employés gagnent plus de 80 000 $ et combien ils gagnent. Renommer la 2ème colonne en **emps_with_same_salary** ?
```sql
SELECT salary, COUNT(emp_no) AS emps_with_same_salary
FROM salaries
WHERE salary > 80000
GROUP BY salary
ORDER BY salary ASC;
```
