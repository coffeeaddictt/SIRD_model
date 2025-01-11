# Simulation du Modèle SIRD avec Évaluation par MSE

Ce projet consiste à simuler l'évolution d'une épidémie à l'aide du modèle SIRD (Susceptibles, Infectés, Rétablis, Décès). L'objectif principal est de mieux comprendre l'impact des interventions, telles que la réduction du taux de transmission (beta), sur la dynamique épidémique. De plus, ce projet analyse le nombre de reproduction de base (R0) afin de mieux saisir les mécanismes de propagation d'une épidémie et l'effet des mesures de contrôle.

## Principales Fonctionnalités

## Simulation du Modèle SIRD :
Le projet simule la progression d'une épidémie, à la fois avec et sans intervention.
Il compare les données observées avec les données simulées pour évaluer la précision du modèle.
Visualisation avec Matplotlib :
Génère des graphiques pour visualiser et comparer les scénarios avec ou sans intervention.
Permet de suivre l'évolution des populations Susceptibles, Infectées, Rétablies et Décédées au fil du temps.
Manipulation des Données avec Pandas :
Lit et traite les données épidémiques à partir d’un fichier CSV.
Permet de manipuler facilement les données observées pour les intégrer dans le modèle.
Optimisation des Paramètres :
Utilise l’Erreur Quadratique Moyenne (MSE) pour ajuster les paramètres beta (taux de transmission), gamma (taux de récupération) et mu (taux de mortalité).
Trouve les valeurs optimales des paramètres pour que le modèle s’ajuste le mieux aux données réelles.
Pourquoi utiliser la MSE ?

## L’Erreur Quadratique Moyenne (MSE) est une métrique essentielle dans ce projet, car elle :

Permet de minimiser les écarts entre les données observées et simulées.
Met davantage l’accent sur les grandes erreurs grâce à son principe de pénalisation quadratique.
Aide à identifier rapidement les valeurs des paramètres beta, gamma et mu qui reproduisent fidèlement les dynamiques épidémiques.
Ce qu’il faut retenir

## Explication du paramètre R0 :
Quand R0 < 1 : Une personne infectée contamine, en moyenne, moins d'une autre personne avant de guérir ou de mourir. Dans ce cas, l'épidémie s'éteint progressivement. <br>
Quand R0 > 1 : Une personne infectée contamine plus d'une autre personne en moyenne. Cela conduit à une propagation rapide et exponentielle de l'épidémie.<br>
## Impact des Interventions :
Sans Intervention :
L'épidémie suit son cours naturel.
Si R0 > 1, les cas augmentent rapidement, atteignent un pic, puis diminuent à mesure que les personnes se rétablissent ou décèdent.
Cela conduit à des pics d’infections élevés et une surcharge des ressources médicales, entraînant un taux de mortalité plus important.<br>
Avec Intervention :
Les mesures comme la distanciation sociale ou le port du masque réduisent beta, ce qui diminue R0.
Lorsque R0 est réduit en dessous de 1, cela ralentit la propagation de l’épidémie, réduit le pic d’infections et diminue le nombre de décès.
Par exemple, une réduction de 50 % de beta peut faire passer R0 de 2 à 1 ou moins, stoppant ainsi l’épidémie.<br>

Comparaison des Scénarios :
Sans Intervention :
Croissance exponentielle des cas avec un pic d’infections rapide et élevé.
Surcharge des systèmes de santé, entraînant un taux de mortalité accru.<br>
Avec Intervention :
Propagation plus lente de l’épidémie.
Pic d’infections plus faible, avec une durée d’épidémie potentiellement plus longue, mais plus contrôlable.
Moins de décès grâce à un système de santé moins saturé.<br>

## Outils Utilisés

Matplotlib : Pour générer des graphiques qui permettent de visualiser les scénarios et d’analyser les dynamiques épidémiques.
Pandas : Pour lire et manipuler facilement les données observées dans un fichier CSV.

## Conclusion

Ce projet met en évidence l'importance des interventions pour contrôler une épidémie. En réduisant beta, nous diminuons R0, ce qui ralentit ou arrête la propagation du virus. Voici les principaux enseignements du projet :

Calculer R0 pour comprendre le potentiel de propagation d'une épidémie.
Comparer les scénarios avec ou sans intervention pour montrer l'impact des mesures préventives.
Utiliser des simulations pour aider à prendre des décisions en santé publique.

## Visualisations :
Des graphiques permettent de comparer les données observées et simulées, en analysant les scénarios avec et sans intervention. Ces visualisations montrent clairement l'effet des interventions sur la dynamique épidémique.

## Bibliographie

Voici les références qui nous ont aidé à comprendre les concepts mathématiques, à implémenter le modèle SIRD en Python, et à explorer les dynamiques épidémiques :

Dridk - Introduction aux équations différentielles appliquées :
https://dridk.me/equation-differentielle.html <br>
Data Science Stack Exchange - Implémentation du modèle SIRD en Python :
https://datascience.stackexchange.com/questions/130751/implementing-the-sird-model-in-python <br>
SciPython - Modèle SIR et ses applications :
https://scipython.com/book/chapter-8-scipy/additional-examples/the-sir-epidemic-model/ <br>
IntechOpen - Modèles mathématiques des épidémies :
https://www.intechopen.com/chapters/1181954 <br>
Cours PDF - Analyse approfondie des modèles SIR :
https://drive.google.com/file/d/1OAtX_E2IgZ5hkujncIyyB7ulcn2PoTwJ/view?usp=sharing <br>
YouTube - Tutoriel sur les modèles épidémiques :
https://www.youtube.com/watch?v=mwJXjxMTwAw