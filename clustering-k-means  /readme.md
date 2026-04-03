Analyse Exploratoire et Clustering K-means des Lycées Français
Objectif

Ce projet vise à explorer les données publiques ouvertes pour répondre à la question suivante :

Existe-t-il une association entre la composition par genre dans les lycées français et les résultats aux examens de fin de scolarité (taux d’accès au baccalauréat) ?
Données

    Source : données publiques ouvertes sur les lycées français
    Taille du dataset : environ 1 543 observations
    Variables principales : proportion de filles/garçons, taux d’accès au baccalauréat

Méthodologie

    Analyse exploratoire des données
        Analyse de corrélation avec une heatmap
        Visualisation avec scatterplots
    Méthodes de clustering (Unsupervised Machine Learning)
        K-means clustering pour identifier des groupes de lycées similaires

Résultats

    Le coefficient de corrélation (~0,3) indique une association positive faible entre la proportion de filles et le taux d’accès au baccalauréat, sans relation linéaire forte ni causalité démontrée.
    La clusterisation met en évidence des groupes de lycées où une proportion plus élevée de filles est associée à de meilleurs résultats moyens au baccalauréat.

Interprétation

    Les clusters ne démontrent pas de relations causales, mais permettent de structurer les données et de formuler des hypothèses.
    Le ratio filles/garçons peut agir comme un proxy pour des variables structurelles ou institutionnelles telles que :
        Contexte socio-économique
        Typologie et sélectivité des lycées
        Environnement institutionnel et attentes académiques

    Aller au-delà de cette analyse exploratoire nécessiterait des modèles multivariés et un contrôle des variables institutionnelles pour identifier correctement les facteurs explicatifs.

Comment exécuter

    Ouvrir le notebook Clustering k-means.ipynb sur Google Colab ou localement
    Exécuter les cellules dans l’ordre pour reproduire l’analyse
