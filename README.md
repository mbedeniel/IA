🧊 Apprentissage par Renforcement : Résolution de Frozen Lake

Bienvenue dans ce dépôt ! Ce projet présente l'implémentation complète et l'analyse de trois algorithmes fondamentaux d'Apprentissage par Renforcement (Reinforcement Learning) appliqués à un environnement personnalisé inspiré du célèbre jeu Frozen Lake.
🎮 Qu'est-ce que Frozen Lake ?

![Démo Frozen Lake](frozen_lake.gif)

Le "Frozen Lake" (Lac Gelé) est un problème classique de navigation sur grille (Gridworld). L'agent se déplace sur une surface glissante et doit atteindre un objectif sans tomber dans les trous d'eau glacée.

Dans ce projet, l'environnement a été entièrement modélisé sur mesure :

    La Grille : Un plateau de 7x7 (49 états distincts de S00 à S66).

    Départ et Arrivée : L'agent commence en bas à droite (S66) et doit atteindre le but en haut à gauche (S00).

    Les Dangers : 7 trous parsèment le lac (S06, S22, S40, S42, S45, S55, S63).

    Les Actions : Droite, Gauche, Haut, Bas, et une action spécifique "Arriver" pour valider l'objectif.

    Système de Récompenses :

        +10 pour l'atteinte de l'objectif.

        -10 en cas de chute dans un trou.

        0 pour une case de glace standard.

🚀 Algorithmes Implémentés

J'ai développé et comparé trois approches distinctes pour résoudre ce Processus de Décision :

    Policy Iteration : Un algorithme Model-Based qui alterne entre l'évaluation de la politique actuelle et son amélioration jusqu'à convergence.

    Value Iteration : Une approche également Model-Based qui met directement à jour la valeur des états en utilisant l'opérateur d'optimalité de Bellman, convergeant plus rapidement que Policy Iteration.

    Q-learning (ε-Greedy) : Un algorithme Model-Free qui apprend par l'expérience. L'agent interagit avec l'environnement par essais et erreurs, en gérant le compromis Exploration vs Exploitation grâce au paramètre epsilon (ε).

💡 Compétences Acquises

Ce projet m'a permis de développer une solide expertise technique et théorique :

    Théorie de l'Apprentissage par Renforcement : Compréhension approfondie des Processus de Décision de Markov, de l'équation de Bellman, des méthodes basées sur les valeurs/politiques, et du dilemme exploration/exploitation.

    Programmation Python Orientée Données : Utilisation intensive de la bibliothèque Pandas pour modéliser l'environnement, les tables de transition (DataFrames de Q-Values, Q-Tables, Politiques), ainsi que Numpy pour les tirages probabilistes aléatoires.

    Data Visualization : Création de fonctions d'affichage complexes avec Matplotlib (Heatmaps avec superposition de texte et de formes géométriques pour représenter visuellement les états de la grille, et graphiques en escalier pour suivre l'évolution des algorithmes).

    Analyse d'Algorithmes : Benchmarking du temps d'exécution (via le module time), profilage de la convergence et réglage des hyperparamètres (Gamma, Alpha, Delta, Epsilon).
