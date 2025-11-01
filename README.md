# Fraude-transactions-bancaires

# Projet SQL : Analyse des fraudes de cartes bancaires

Ce projet présente l'analyse d'un **jeu de données sur les fraudes de cartes bancaires**, récupéré depuis Kaggle : [Credit Card Fraud Detection](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud).  

L’objectif est de **structurer, explorer et analyser** les transactions pour identifier et comprendre les fraudes.

---

## 1️⃣ Objectif

- Comprendre les données de transactions bancaires
- Identifier les transactions frauduleuses
- Créer des requêtes SQL pour explorer les patterns et générer des indicateurs
- Préparer le projet de manière reproductible pour un portfolio GitHub

---

## 2️⃣ Démarche réalisée

1. **Téléchargement et préparation de la base**  
   - Source : Kaggle (CSV)  
   - Import dans **PostgreSQL / pgAdmin**  
   - Création de la base de données et de la table `creditcard_fraud`  

2. **Création et nettoyage de la table**  
   - Types de colonnes adaptés (`double precision` pour les valeurs, `smallint` pour les classes)  
   - Vérification des doublons et des valeurs manquantes  

3. **Exploration des données**  
   - Comptage total des transactions : 284,807  
   - Transactions frauduleuses : 492  
   - Colonnes principales : `Time`, `V1` à `V28` (features anonymisées), `Amount`, `Class`  

4. **Requêtes SQL pour analyses**  
   - Nombre de transactions par type  
   - Somme et moyenne des montants par `Class`  
   - Transactions suspectes (> certain montant)  
   - Agrégations pour reporting

---

## 3️⃣ Structure GitHub

