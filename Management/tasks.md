# Gestion des tâches à réaliser



#### 1\. Introduction \& Contexte (WatsonIA) ==> LISA \& CYPRIEN



Rédiger l’introduction du projet, le contexte du dataset IBM, les enjeux du cold start, et la méthodologie suivie.

Présenter la problématique métier (fraude bancaire), les données disponibles et les contraintes. ??



#### 2\. Data Exploration (EDA) ==> HIBA



Explorer les fichiers (transactions\_train.csv, cards\_data.csv, users\_data.csv, mcc\_codes.json) pour comprendre la structure, les types de données, les taux de fraude, les valeurs manquantes et les anomalies.



* Identifier les variables importantes
* Détecter les problèmes de qualité de données
* Visualiser la répartition des fraudes
* Notebook d’exploration (graphiques, stats descriptives)



#### 3\. Data Preparation (Feature Engineering) ==> HIBA \& LISA



* Nettoyer, fusionner et enrichir les données avec des variables dérivées (montant log-transformé, heure, jour, week-end, MCC encodé, etc.).
* Nettoyer les NaN et doublons
* Créer de nouvelles features pertinentes
* Garantir qu’il n’y ait aucune fuite de données (no leakage)
* Script data\_preparation.py + dataset prêt pour le ML



#### 4\. Machine Learning Modeling ==> NEIL \& WENDY



* Concevoir, entraîner et évaluer un modèle capable de prédire la fraude (1 = fraude, 0 = normal).
* Choisir un modèle (LightGBM, XGBoost, Logistic Regression)
* Gérer le déséquilibre des classes (~0.15%)
* Valider avec un split temporel et cold-start client
* Calculer AUROC, AUPRC, F1-score
* Notebook ou script model\_training.py + métriques + confusion matrix



#### 5\. Evaluation \& Generalization ==> NEIL \& WENDY



* Tester la robustesse du modèle sur des clients jamais vus (cold start) et sur les données 2018.
* Évaluer la généralisation du modèle
* Ajuster le seuil optimal de classification
* Comparer plusieurs modèles si possible
* Rapport d’évaluation + choix du modèle final



#### 6\. Data Visualization \& Dashboard ==> SAFA



* Créer un dashboard interactif (Streamlit / Power BI) présentant les indicateurs clés du modèle et du dataset.
* Montrer la distribution des transactions
* Afficher taux de fraude, importance des features, courbes ROC/PR
* Visualiser les prédictions sur l’échantillon test
* streamlit\_app.py ou dashboard Power BI



#### 7\. Génération du fichier de soumission ==> CYPRIEN



* Appliquer le modèle final sur evaluation\_features.csv pour produire le fichier final de prédictions. 
* Générer submission.csv contenant :

transaction\_id, fraud\_prediction

* Vérifier le format et cohérence
* submission.csv prêt à uploader



#### 8\. Documentation \& Présentation finale ==> TOUS



* Rédiger le rapport et la présentation synthétique du projet. 
* Résumer la démarche
* Justifier les choix techniques
* Inclure des visuels clairs et concis
* PowerPoint / rapport PDF
