# DISTINCT et GROUP BY

8.1 Obtenir les différents noms dans la table **employees**.

Même résultat : Obtenir le prénom (first name) dans la table **employees** et regrouper par prénom.
```sql
SELECT first_name
FROM employees
GROUP BY first_name;
```

8.2 Combien de noms différents peut-on trouver dans la table **employees** ?

8.3 Combien de prénoms différents peut-on trouver dans la table **employees** ?

8.4 Combien de prénoms différents peut-on trouver dans la table **employees** ?

8.5 Combien de prénoms différents y a-t-il dans la table **employees** ? et ordonner par prénom en ordre décroissant ?

8.6 Combien de départements différents y a-t-il dans la base de données **employees** ?
Indice : Utilisez la table dept_emp

8.7 Récupérer une liste de combien d'employés gagnent plus de 80 000 $ et combien ils gagnent. Renommer la 2ème colonne en emps_with_same_salary ?
