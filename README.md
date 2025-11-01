# Projet SQL & Power BI : Analyse des fraudes de cartes bancaires

Ce projet présente l'analyse d'un **jeu de données sur les fraudes de cartes bancaires**, récupéré depuis Kaggle : [Credit Card Fraud Detection](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud).  

L’objectif est de **analyser les transactions pour identifier et comprendre les fraudes**, et de **produire des indicateurs exploitables** pour le reporting et la prise de décision.

---

## Objectifs

- Comprendre la structure du jeu de données et ses caractéristiques  
- Identifier les transactions frauduleuses et leurs tendances
- Produire des analyses quantitatives et synthétiques  
- Mettre en place des requêtes SQL efficaces pour extraire des insights  
- Créer un **dashboard Power BI** pour visualiser les KPIs et faciliter la prise de décision

---

## Démarche réalisée

1. **Téléchargement et import de la base**  
   - Source : Kaggle (CSV)  
   - Import dans **PostgreSQL / pgAdmin**  
   - Création de la base de données et de la table `creditcard_fraud`
  
     
<img width="1759" height="943" alt="Création table" src="https://github.com/user-attachments/assets/8331f133-3a2d-40f9-97ac-d7ffc7bff43c" />

2. **Préparation et nettoyage des données**  
   - Vérification des doublons  
   - Gestion des valeurs manquantes  
   - Typage des colonnes (`double precision` pour les montants et features, `smallint` pour la classe)  
   - Normalisation des montants pour certaines analyses  

3. **Exploration des données**  
   - Comptage total des transactions : 284,807  
   - Transactions frauduleuses : 492  
   - Colonnes principales : `Time`, `V1` à `V28` (features anonymisées), `Amount`, `Class`  

4. **Requêtes SQL pour analyses**  
   - Nombre de transactions par type  
   - Somme et moyenne des montants par `Class`  
   - Transactions suspectes (> certain montant)  
   - Agrégations pour reporting et visualisation des KPIs  

5. **Création du dashboard Power BI**  
   - Import des données nettoyées depuis PostgreSQL  
   - Visualisation des transactions par type et montant  
   - KPI pour le suivi des fraudes et indicateurs clés  
   - Graphiques interactifs pour faciliter l’analyse métier

---

