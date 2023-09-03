# 📈 Utiliser SQL dans Polars


## Introduction

Il y a plusieurs façons d'utiliser SQL dans Polars.

Une option est d'utiliser d'autres bibliothèques telles que DuckDB et pandas (cf. le notebook "Manipuler et transformer du Big Data en fichier Parquet via une interconnexion entre Polars & DuckDB pour exécuter des requêtes SQL")

Et une autre option est d'exécuter SQL sans utiliser d'autres bibliothèques.

C'est cette dernière option que je vais démontrer dans ce mini notebook.



## Philosophie de Polars

Le but de Polars est de fournir une bibliothèque DataFrame rapide comme l'éclair qui :

-Utilise tous les cœurs disponibles (du processeur de notre ordi) sur votre machine.
-Optimise les requêtes pour réduire le travail inutile et les allocations de mémoire.
-Gère des ensembles de données beaucoup plus grands que votre RAM disponible.
-possède une API cohérente et prévisible
-A un schéma strict (les types de données doivent être connus avant l'exécution de la requête).
-Polars est écrit en Rust, ce qui lui confère des performances en C/C++ et lui permet de contrôler entièrement les parties critiques en termes de performances dans un moteur de requêtes.

Ainsi, Polars se donne beaucoup de mal pour :

-Réduire les copies redondantes.
-Traverser efficacement le cache mémoire.
-Minimiser la contention dans le parallélisme.
-Traiter les données par morceaux.
-Réutiliser les allocations de mémoire.




## Ensemble de données

Datatset titanic sur kaggle



## Démarche

Cf. le notebook ci-joint.

Le code est aussi simple qu'il en a l'air :

-Créer un contexte pour que SQL travaille sur un dataframe Polars.
-Enregistrer le nom du dataframe pour qu'il soit utilisé dans votre requête SQL.
-Exécuter la requête qui renvoie un dataframe Polars.







## Conclusion

L'utilisation de SQL directement dans Polars est assez simple dans la mesure où il suffit de connaître quelques lignes de code spécifiques à Polars.

De nombreuses personnes travaillant dans le domaine des données sont familières avec SQL.

La possibilité d'utiliser SQL dans Polars aide à libérer les performances de Polars pour ceux qui ne peuvent pas le faire autrement.





