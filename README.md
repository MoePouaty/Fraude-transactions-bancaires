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

2. **Exploration et Analyse des données**  
   - Colonnes principales : `Time`, `V1` à `V28` (features anonymisées), `Amount`, `Class`  
   - Comptage total des transactions : 284 807  
   - Nombre et Montant des Transactions frauduleuses : 492
   - Nombre et Montant des Transactions non frauduleuses : 284 315
<p align="center">
   <img width="500" height="687" alt="Capture d&#39;écran 2025-11-02 115439" src="https://github.com/user-attachments/assets/dc4186b4-b11a-4393-a67a-e880e8e80eac" />
   <img width="500" height="683" alt="Capture d&#39;écran 2025-11-02 115334" src="https://github.com/user-attachments/assets/765970ce-cafc-43d4-b1ba-52629cf604c4" />

</p>

   - Pourcentage de transactions frauduleuses : 0,17%
   - Distribution des montants : Montant max moyen ou min en fonction du type de transaction
   - Heure de transaction avec plus de fraudes
<img width="1047" height="823" alt="transaction par temps" src="https://github.com/user-attachments/assets/d7a6d538-d647-4ccb-af29-5b780672309a" />

   
   - Statistiques des variables V1–V28 : Moyenne, écart-type

   

3. **Création du dashboard Power BI**  
   - Import des données nettoyées depuis PostgreSQL  
   - Visualisation des transactions par type et montant  
   - KPI pour le suivi des fraudes et indicateurs clés  
   - Graphiques interactifs pour faciliter l’analyse métier

---

