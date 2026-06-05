# Déterminants du sentiment de sécurité nocturne en France
## Analyse multivariée des données de l’European Social Survey (ESS), Vague 9

**Auteur :** Chadi Gamal  
**Date :** 5 juin 2026  

---

### 📝 Résumé
À partir des données de l’European Social Survey (ESS9), ce projet analyse l’impact de 15 facteurs (socio-démographiques, santé, valeurs) sur le sentiment de sécurité nocturne en France. La démarche combine explorations univariée et bivariée, puis une modélisation par régression linéaire multiple afin d’isoler l’effet propre de chaque variable « toutes choses égales par ailleurs » et de neutraliser les effets de confusion.

---

### 1. Introduction et démarche méthodologique
Ce projet a pour objectif d’analyser les déterminants du sentiment de sécurité des individus lorsqu’ils marchent seuls dans leur quartier après la tombée de la nuit en France. À partir des données de l’European Social Survey (ESS9), qui contient plus de 360 questions (informations socio-démographiques, opinions, aspects sociaux, politiques et religieux), j’ai sélectionné 15 facteurs susceptibles d'interagir avec ce sentiment. Ces facteurs regroupent des caractéristiques socio-démographiques, des indicateurs de santé, des opinions politiques ainsi que le système de valeurs des répondants.

La démarche d’analyse s’articule en trois étapes progressives :
* **L’analyse univariée :** pour explorer la distribution des répondants selon les différentes modalités de chaque facteur et valider la qualité des données.
* **L’analyse bivariée :** pour évaluer, à l’aide de tests de significativité statistique adaptés, l’association brute entre chaque facteur indépendant et le sentiment de sécurité nocturne.
* **L’analyse multivariée (régression linéaire multiple) :** pour isoler l’effet propre de chaque facteur « toutes choses égales par ailleurs » et neutraliser les potentiels effets de confusion.

#### Initialisation de l’environnement de travail
```r
# Pour supprimer tout ce qui est en mémoire
rm(list=ls())

# Packages requis
library(stats)      # Calculs statistiques (moyennes, régressions, etc.)
library(questionr)  # Tableaux de statistiques descriptives
library(dplyr)      # Manipulation, filtrage et nettoyage des données
