# OLS et transformation de Box-Cox

Ce dossier présente une analyse du **taux d'accès au baccalauréat** dans les lycées publics français à l’aide de modèles de régression.

## Objectif
Évaluer la pertinence d’un modèle OLS lorsque la variable dépendante est une **proportion (bornée entre 0 et 1)**, et tester des solutions pour corriger la non-normalité des résidus.

## Méthodologie
- Régression linéaire multiple (OLS) avec encodage des variables catégorielles  
- Test de normalité des résidus (Shapiro–Francia)  
- Transformation de Box-Cox  

## Limite identifiée
La transformation de Box-Cox n’a pas permis de restaurer la normalité des résidus, ce qui met en évidence une **inadéquation du modèle OLS** pour ce type de variable.

## Ouverture
Exploration de modèles plus adaptés :
- GLM (fractional logit)  
- Modèles multiniveaux (en cours)  

## Contenu
- Notebook d’analyse (`OLS et transformation de Box-Cox pour distribution non normale.ipynb`)  
- Données utilisées  

## Enjeu
Ce travail illustre l’importance de **choisir un modèle cohérent avec la structure des données**, au-delà de l’application standard des méthodes.
