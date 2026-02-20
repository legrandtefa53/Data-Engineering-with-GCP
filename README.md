# End-to-End Data Engineering Project on Kaggle using GCP

## Projet

Ce projet est un pipeline **end-to-end de Data Engineering** appliqué à un dataset Kaggle. Il illustre la collecte, le traitement, le stockage et l’analyse des données en utilisant les services de **Google Cloud Platform (GCP)** et **PowerBI**. 

---

## 🛠️ Technologies et outils utilisés

* **Cloud Platform :**

  * Data source : [Kaggle](https://www.kaggle.com/datasets/bryanb/fifa-player-stats-database/versions/29/data?select=FIFA22_official_data.csv)
  * Infrastructure : Terraform
  * Data Lake : Google Cloud Storage (GCS)
  * Data Warehouse : BigQuery
  * Orchestration ETL : Cloud Composer / Airflow / Data Fusion / SQL / Python / Spark
  * Data viz : PowerBI
  * ML : Dataiku


## 🔄 Pipeline ETL

1. **Ingestion** : Récupération des données depuis Kaggle ou GCS.
2. **Transformation** :

Les princiales transformations appliquées sont : 
   * Nettoyage des données manquantes et aberrantes
   * Normalisation et typage
   * Calcul de métriques
   
3. **Loading** :

   * Stockage des données transformées dans BigQuery
   * Création de tables partitionnées et indexées pour optimiser les requêtes

Diagramme du pipeline :

<img width="845" height="174" alt="Image" src="https://github.com/user-attachments/assets/07d93bc0-2e4e-4379-98d0-724ad75e6d8c" />


---

## 📈 Analyses et visualisations

Une fois les données disponibles dans le Data warehouse, on s'y connecte depuis PowerBI et construit les tableaux de bords interactifs : 
Les main insights sont : 

<img width="884" height="523" alt="Image" src="https://github.com/user-attachments/assets/2de97af3-78bd-4c21-8c81-b4803e87cb50" />

On peut ainsi analyser assez intuitivement le nombres de joueurs, leur nationalité, la répartition de gauchers et droitiers, leur club ou encore leur âge moyen. 

Par exmple, si on s'intéresse uniquement aux joueurs sans club, on a : 

<img width="917" height="520" alt="Image" src="https://github.com/user-attachments/assets/2ff240ea-9374-4990-a222-742fd3051968" />


## 🧩 Extensions possibles

* Ajouter la surveillance et alerting sur Cloud Composer
* Intégrer un pipeline CI/CD pour le déploiement automatique
* Automatiser la mise à jour quotidienne des données
