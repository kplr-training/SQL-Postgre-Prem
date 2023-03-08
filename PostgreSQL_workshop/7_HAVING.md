# 7.Having
7.1. Récupérer une liste de tous les employés qui ont été employés à partir du 1er janvier 2000.

Cela produira-t-il le même résultat ? :
```sql
SELECT *
FROM employees
HAVING hire_date >= '2000-01-01';
```
7.2. Extraire une liste de noms d'employés, où le nombre d'employés est supérieur à 15, en les classant par prénom.

7.3 Récupérez une liste de numéros d'employés et le salaire moyen. Assurez-vous d'obtenir les résultats où le salaire moyen est supérieur à 120 000 $.

7.4 Extraire une liste de tous les noms qui ont été rencontrés moins de 200 fois. Les données concernent les personnes embauchées après le 1er janvier 1999.

7.5 Sélectionnez les numéros d'employés de tous les individus qui ont signé plus d'un contrat après le 1er janvier 2000.
