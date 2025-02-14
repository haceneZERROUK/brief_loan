# # Van ThorZer - SBA Loan Default Prediction

## Contexte

Van ThorZer est une entreprise de data science spécialisée dans la prévision de la capacité des petites entreprises à rembourser leurs prêts garantis par la **United States Small Business Administration (US SBA)**. L'US SBA, fondée en 1953, a pour mission d'aider les petites entreprises à accéder au crédit, créant ainsi des opportunités d'emploi et réduisant le chômage aux États-Unis. De nombreuses start-ups, comme **FedEx** et **Apple**, ont prospéré grâce aux prêts SBA. Cependant, certaines entreprises ont fait défaut sur leurs prêts, et il est essentiel de prédire cette probabilité pour mieux orienter les décisions de financement.

## Objectif du Projet

L'objectif de ce projet est de prédire la probabilité qu'une entreprise, qui sollicite un prêt garanti par la SBA, soit capable de le rembourser. Il s'agit d'un problème de **classification binaire**, où les sorties possibles sont :

- **P I F (1)** : Le prêt doit être accordé (l'entreprise sera capable de rembourser)
- **CHGOFF (0)** : Le prêt ne doit pas être accordé (l'entreprise fera défaut)

### Datasets

Les données utilisées pour ce projet proviennent de différentes sources, notamment les informations financières des petites entreprises, leurs performances passées, et des variables économiques globales. Les données sont prétraitées et nettoyées avant d'être utilisées pour l'entraînement des modèles.

## Méthodologie

### 1. **Analyse Exploratoire des Données (EDA)**

- **Objectifs** : Identifier les tendances, la distribution des variables, les relations entre les variables, et la présence de valeurs manquantes ou aberrantes.
- **Techniques** : Visualisation de données (graphiques, boxplots, histogrammes), statistiques descriptives.

### 2. **Modélisation et Prédiction**

Nous avons utilisé plusieurs techniques de classification pour prédire si une entreprise sera en mesure de rembourser son prêt :

- **Régression Linéaire** : Bien que ce modèle ne soit pas conçu spécifiquement pour la classification, il nous a permis de poser une première estimation de la relation entre les variables.
  
- **Arbre de Décision (Decision Tree)** : Permet de diviser les données en sous-ensembles basés sur des décisions conditionnelles. Simple à comprendre et à interpréter.
  
- **Forêt Aléatoire (Random Forest)** : Un ensemble d'arbres de décision, qui améliore la précision en réduisant la variance.
  
- **LightGBM (Light Gradient Boosting Machine)** : Un modèle de boosting optimisé pour une grande échelle de données, offrant un excellent compromis entre vitesse et performance.
  
- **XGBoost** : Un autre algorithme de boosting largement utilisé pour ses capacités à traiter des données complexes avec une excellente performance en termes de précision.
  
- **CatBoost** : Un algorithme de boosting, optimisé pour les données catégorielles, qui a donné de très bons résultats sur notre jeu de données.

### 3. **Évaluation des Modèles**

Les performances des différents modèles ont été évaluées à l'aide des métriques suivantes :

- **Accuracy** : La proportion des prédictions correctes.
- **Précision et Rappel (Precision & Recall)** : Indicateurs essentiels pour évaluer la performance des modèles sur un jeu de données déséquilibré.
- **AUC-ROC** : Une mesure de la capacité du modèle à distinguer entre les classes (0 et 1).

### 4. **Sélection du Modèle Final**

Après avoir comparé les résultats des différents modèles, nous avons sélectionné celui offrant le meilleur compromis entre performance et interprétabilité pour notre cas d'utilisation.

## Résultats et Conclusion

Nous avons trouvé que **CatBoost** et **XGBoost** sont les modèles les plus performants dans la prédiction du défaut de remboursement des prêts, offrant un **AUC** élevé et des résultats robustes. Le modèle retenu sera mis en production pour aider l'US SBA à prendre des décisions éclairées concernant l'octroi des prêts.

## Déploiement

Le modèle sera intégré dans un système de production pour être utilisé en temps réel, afin de prédire si une entreprise pourra rembourser son prêt ou non, en fonction des données financières fournies.

## Logo

![Van ThorZer Logo](/Logo_Vanthorzer.png)

---

**Van ThorZer - le groupe se compose de :
Samuel Thorez
gauthier Vannesson
Hacène Zerrouk**
