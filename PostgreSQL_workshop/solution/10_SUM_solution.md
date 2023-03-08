# 8.SUM()
8.1. Récupérer le montant total que l'entreprise a versé en salaire ?
```sql
SELECT SUM(salary) as total_salary
FROM salaries;
```
8.2. Que retourne la requête suivante ? Pourquoi ?
```sql
SELECT SUM(*)
FROM salaries;
```
Elle retourne une erreur (SUM  does not exist) car la fonction sum prend en paramètre une colonne numérique.

8.3  Quelle est la somme totale consacrée aux salaires pour tous les contrats contrats débutant après le 1er janvier 1997 ?
```sql
SELECT SUM(salary) AS total_salary
FROM salaries
WHERE from_date > '1997-01-01'
```
