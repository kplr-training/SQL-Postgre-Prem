# 5.COUNT()

7.1 Combien d'employés compte l'entreprise ?
```sql
SELECT COUNT (emp_no) AS Num_of_employees
FROM employees;
```
7.2 Y a-t-il un employé sans prénom ?  
```sql
SELECT * 
FROM employees
WHERE first_name IS NULL;
```
ou bien :
```sql
SELECT COUNT(first_name) AS FirstName_Count
FROM employees;
```
7.3 Combien d'enregistrements y a-t-il dans la table **salaries** ?
```sql
SELECT COUNT(*)
FROM salaries;
```
7.4 Combien de contrats annuels d'une valeur supérieure ou égale à 100.000 $ ont été enregistrés dans le tableau **salaries** ?
```sql
SELECT COUNT(*)
FROM salaries
WHERE salary >= 100000;
```
7.5 Combien de fois avons-nous payé des salaires à des employés ?
```sql
SELECT COUNT(salary) AS salary_count
FROM salaries;
```
Cela devrait donner le même résultat que ci-dessus:
```sql
SELECT COUNT(from_date)
FROM salaries;
```
