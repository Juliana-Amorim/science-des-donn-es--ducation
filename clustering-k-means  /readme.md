# Analyse Exploratoire et Clustering K-means des Lycées Français

## Objectif
Ce projet vise à explorer les données publiques ouvertes pour répondre à la question suivante :  

**Existe-t-il une association entre la composition par genre dans les lycées français et les résultats aux examens (taux d’accès au baccalauréat) ?**  

La deuxième partie du projet inclut l'application d'un modèle de régression linéaire (OLS) pour compléter l'analyse exploratoire et initier une approche de Machine Learning supervisée.

## Données
- Source : données publiques ouvertes sur les lycées français  
- Taille du dataset : environ 1 543 observations  
- Variables principales : proportion de filles/garçons, taux d’accès au baccalauréat

## Méthodologie

### 1. Analyse exploratoire des données
- Analyse de corrélation avec une heatmap  
- Visualisation avec scatterplots  

### 2. Méthodes de clustering (Unsupervised Machine Learning)
- K-means clustering pour identifier des groupes de lycées similaires

### 3. Modèle linéaire (OLS) pour complémentarité et initiation au ML supervisé
- Modèle OLS : `prop_filles ~ Taux d'accès 2nde-bac`  
- Calcul des valeurs ajustées (`yhat`) et des résidus  
- Visualisation des valeurs réelles vs valeurs ajustées  

## Résultats

### Clustering K-means
- Coefficient de corrélation (~0,3) indique une association positive faible, sans relation linéaire forte ni causalité.  
- La clusterisation met en évidence des groupes de lycées où une proportion plus élevée de filles est associée à de meilleurs résultats moyens au baccalauréat.

### Régression OLS
- Le modèle OLS montre une relation faible mais significative entre le taux d’accès au baccalauréat et la proportion de filles (R² ≈ 0,088).  
- Visualisation des valeurs ajustées confirme la tendance identifiée par la clusterisation.  
- Cette étape initie l'utilisation de modèles supervisés pour explorer les relations entre variables.

## Interprétation
- Les clusters et le modèle OLS **ne démontrent pas de relations causales**, mais permettent de structurer les données et de formuler des hypothèses.  
- Le ratio filles/garçons peut agir comme un proxy pour des variables structurelles ou institutionnelles :  
  - Contexte socio-économique  
  - Typologie et sélectivité des lycées  
  - Environnement institutionnel et attentes académiques  

> Pour aller au-delà de cette phase exploratoire et du modèle OLS, il serait nécessaire d’utiliser des modèles multivariés et de contrôler les variables institutionnelles pour identifier correctement les facteurs explicatifs.

## Comment exécuter
1. Ouvrir le notebook `Clustering k-means.ipynb` sur Google Colab ou localement  
2. Exécuter les cellules dans l’ordre pour reproduire l’analyse complète (clustering + OLS)
