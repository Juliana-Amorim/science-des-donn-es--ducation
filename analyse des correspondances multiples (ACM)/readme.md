# Analyse des correspondances multiples (ACM) des lycées français selon région académique

## Objectif
Ce projet vise à explorer les données publiques ouvertes pour répondre à la question suivante :

Comment les lycées des différentes régions académiques se positionnent-ils selon leurs caractéristiques socio-économiques et leurs taux de réussite au baccalauréat ?

L’objectif est de mobiliser une analyse des correspondances multiples (ACM) afin d’identifier des structures sous-jacentes et de visualiser les relations entre ces variables qualitatives.

## Données
- Source : données publiques ouvertes sur les lycées français  
- Variables principales : indicateurs socio-économiques, taux de réussite au baccalauréat, caractéristiques des établissements
- Type de variables : majoritairement qualitatives (catégorielles)

## Méthodologie

### 1. Préparation des données
- Sélection des variables pertinentes
- Transformation des variables en modalités exploitables pour l’ACM

### Analyse des correspondances multiples (ACM)
- Réduction dimensionnelle adaptée aux variables qualitatives
- Projection des données dans un espace factoriel

### Visualisation
- Construction d’une carte perceptuelle (plan factoriel)
- Analyse des distances et des proximités entre modalités
  
## Résultats

## Carte perceptuelle (ACM)
- La visualisation capture environ 15 % de l’inertie totale
- La proximité des points indique des profils similaires ou des associations fortes
- L’éloignement révèle des dynamiques contrastées entre lycées et territoires
- L’ACM met en évidence :
  - Des regroupements d’établissements partageant des caractéristiques communes
  - Des oppositions structurantes entre contextes socio-économiques
  - Des relations entre environnement social et réussite scolaire

## Interprétation
- L’ACM permet de structurer l’information contenue dans des variables qualitatives complexes
- Les résultats ne démontrent pas de relations causales, mais révèlent des associations significatives
- Les positions observées peuvent refléter :
  - Des disparités territoriales
  - Des effets de contexte socio-économique
  - Des différences structurelles entre établissements

> Cette analyse constitue une étape exploratoire. Une approche complémentaire (modèles multivariés, régression, méthodes de machine learning) serait nécessaire pour approfondir l’identification des facteurs explicatifs.

## Comment exécuter
1. Ouvrir le notebook carte_perceptuelle_analyses_de_correspondance_multiple.ipynb sur Jupyter Notebook ou Google Colab
2. Exécuter les cellules dans l’ordre pour reproduire l’analyse complète (ACM + visualisations)
