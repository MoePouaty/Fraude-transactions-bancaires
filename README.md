# Projet SQL & Power BI : Analyse des fraudes de cartes bancaires

Ce projet présente l'analyse d'un **jeu de données sur les fraudes de cartes bancaires**, récupéré depuis Kaggle : [Credit Card Fraud Detection](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud).  

L’objectif est d'**analyser les transactions pour identifier et comprendre les fraudes**, et de **produire des indicateurs exploitables** pour le reporting et la prise de décision.

---

## Objectifs

- Comprendre la structure du jeu de données et ses caractéristiques  
- Identifier les transactions frauduleuses et leurs tendances
- Mettre en place des requêtes SQL efficaces pour extraire des insights  
- Créer un **dashboard Power BI** pour visualiser les KPIs et faciliter la prise de décision

---

## Démarche réalisée

1. **Téléchargement, préparation et import de la base**  
   - Source : Kaggle (CSV)
   - Vérification des doublons et Gestion des valeurs manquantes  
   - Import dans **PostgreSQL / pgAdmin**  
   - Création de la base de données et de la table `creditcard_fraud`
   - Typage des colonnes (`double precision` pour les montants et features, `smallint` pour la classe)  
  <img width="1050" height="874" alt="Création_table_sql" src="https://github.com/user-attachments/assets/a061140a-3f5d-45ed-9883-bbde41983cd4" />

2. **Exploration des données**  
   - Comptage total des transactions : 284,807  
   - Transactions frauduleuses : 492  
   - Colonnes principales : `Time`, `V1` à `V28` (features anonymisées), `Amount`, `Class`  

3. **Requêtes SQL pour analyses**  
   - Nombre de transactions par type  
   - Somme et moyenne des montants par `Class`  
   - Transactions suspectes (> certain montant)  
   - Agrégations pour reporting et visualisation des KPIs  

4. **Création du dashboard Power BI**  
   - Import des données nettoyées depuis PostgreSQL  
   - Visualisation des transactions par type et montant  
   - KPI pour le suivi des fraudes et indicateurs clés  
   - Graphiques interactifs pour faciliter l’analyse métier

---

