# OLS et transformation de Box-Cox pour distribution non normale

## Objectif du projet

Ce projet vise à analyser les déterminants du taux de réussite au baccalauréat dans les lycées publics en France, à partir d’un modèle de régression.

L’objectif initial est d’expliquer la variable :

**Taux d'accès 2nde-bac** (proportion d’élèves accédant au baccalauréat)

à l’aide de variables explicatives socio-économiques et structurelles.

---

## Données et variables

### Variable dépendante (Y)
- **Taux d'accès 2nde-bac** : proportion de réussite au baccalauréat  

### Variables indépendantes (X)

**Variables quantitatives :**
- `IPS voie GT` : indice de position sociale  
- `prop_filles` : distribution selon le genre

**Variables qualitatives (transformées en dummies) :**
- `Région`  

---

## Étape 1 — Modèle OLS avec encodage des variables

Dans un premier temps, j’ai estimé un modèle OLS de régression multiple en appliquant un encodage one-hot aux variables qualitatives.

**Objectif :**
- mesurer l’effet des variables explicatives sur le taux de réussite  

---

## Étape 2 — Problème de normalité des résidus

Le modèle OLS a été soumis au test de **Shapiro-Francia** :

- Résultat : rejet de l’hypothèse de normalité des résidus  

**Problème :**
- violation d’une hypothèse classique du modèle OLS  
- risque d’inférences statistiques biaisées  

---

## Étape 3 — Transformation de Box-Cox

Une transformation de Box-Cox a été appliquée à la variable dépendante afin de corriger la non-normalité.

**Objectif :**
- rapprocher la distribution des résidus de la normalité  

**Résultat :**
- la normalité des résidus n’est toujours pas vérifiée (nouveau test de Shapiro-Francia)  

---

À la suite de ces résultats, plusieurs pistes méthodologiques pourraient être envisagées :

### 1. Cas idéal : données individuelles

Si les données sont disponibles au niveau élève :
- utiliser un modèle logistique  
- variable dépendante :
  - 0 = échec  
  - 1 = réussite  

### 2. Cas actuel : variable proportionnelle (0–1)

Comme ici la variable dépendante est une proportion, plusieurs alternatives sont recommandées :

#### Option A — OLS avec erreurs robustes
- corrige les problèmes d’hétéroscédasticité  
- mais ne traite pas la nature bornée de Y  

#### Option B — Fractional Logit (recommandé)
- modèle adapté aux proportions  
- basé sur un GLM :
  - famille : binomiale ou quasi-binomiale  
  - fonction de lien : logit  

**Avantages :**
- respecte le fait que Y ∈ [0,1]  
- ne nécessite pas de connaître le nombre total d’observations  

---

## Étape suivante — Modèle multiniveau

Dans la continuité de ces réflexions, une approche plus avancée est envisagée :

### Modèle multiniveau (hierarchical model)

**Justification :**
- les données sont structurées (établissements imbriqués dans des régions)  

**Permet de :**
- capturer les effets contextuels  
- modéliser l’hétérogénéité entre groupes (ex : régions)  

---

## Conclusion

Ce projet met en évidence les limites du modèle OLS dans le cas :
- d’une variable dépendante non normale  
- et bornée (proportion)

Il ouvre vers des approches plus adaptées :
- modèles logistiques  
- GLM (fractional logit)  
- modèles multiniveaux  

---

## Technologies utilisées

- Python (statsmodels, scipy)  
- Google Colab  

**Méthodes :**
- OLS  
- Test de Shapiro-Francia  
- Transformation de Box-Cox  
- GLM (en cours)  
- Modélisation multiniveau (en cours)  

---

## Auteur

**Juliana da Costa Amorim**  
(MBA Data Science – USP/ESALQ)
