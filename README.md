# 💳 WatsonIA – Détection de fraudes bancaires

## Equipe 20 :
- Lisa Naccache (DIA 4) : Chef d'équipe
- Hiba NEJJARI (DIA 4)
- Neil MAHCER (DIA 4)
- Wendy DUONG (DIA 4)
- Cyprien MOUTON (DIA 4)
- Safa HORMI BOUAICHI (DIA 3)


## 🧠 Contexte du projet
Dans un contexte de forte digitalisation des paiements, les fraudes bancaires se multiplient et deviennent de plus en plus sophistiquées.  
Ce projet a été réalisé dans le cadre du **Hackathon IBM – Track Finance**, et a pour but de concevoir un modèle de **Machine Learning** capable de détecter automatiquement les transactions frauduleuses à partir d’un dataset réaliste fourni par IBM (2016–2018).

---

## 🎯 Objectif
Développer un modèle d’**Intelligence Artificielle** permettant de prédire si une transaction est :
- `1` → **Frauduleuse**  
- `0` → **Non frauduleuse**

Le modèle doit être **robuste**, **généralisable à de nouveaux clients (cold start)** et résilient face à un fort **déséquilibre de classes (~0.15 % de fraudes)**.

---

## 🧩 Données
Données fournies par IBM :
- `transactions_train.csv` : Transactions d'entraînement (montant, date, carte, etc.)  
- `train_fraud_labels.json` : Labels de fraude (1 ou 0)  
- `cards_data.csv` : Informations sur les cartes de paiement  
- `users_data.csv` : Profils utilisateurs (âge, revenus, localisation, etc.)  
- `mcc_codes.json` : Codes MCC (types de marchands)  
- `evaluation_features.csv` : Données d’évaluation (sans label)

---

## 🚀 Méthodologie
Notre approche suit les étapes classiques d’un pipeline **Data Science** :
1. **Exploration des données (EDA)**  
2. **Préparation et Feature Engineering**  
3. **Modélisation (LightGBM)**  
4. **Évaluation & Généralisation**  
5. **Visualisation des résultats (Dashboard Power BI)**  
6. **Soumission finale (`submission.csv`)**

---

## 👥 Équipe WatsonIA
| Rôle | Membres |
|:------|:---------|
| 🧭 Introduction & Contexte | **Lisa & Cyprien** |
| 🔍 Data Exploration | **Hiba** |
| ⚙️ Data Preparation | **Hiba & Lisa & Safa** |
| 🤖 Machine Learning | **Neil & Wendy** |
| 📈 Évaluation & Généralisation | **Neil & Wendy** |
| 📊 Dashboard & Visualisation | **Safa** |
| 📁 Soumission finale | **Cyprien** |
| 📝 Rapport & Présentation | **Tous** |

---

## 🛠️ Technologies utilisées
- **Langage :** Python 3.10  
- **Librairies principales :**
  - `pandas`, `numpy` – manipulation de données  
  - `lightgbm`, `scikit-learn` – modélisation et métriques  
  - `matplotlib`, `seaborn` – visualisation  
  - `streamlit` – dashboard interactif
- **Outils :**
  - Jupyter Notebook  
  - Git & GitHub  
  - Power BI

---

## 🗂️ Structure du projet
```
finance-fraud/
├─ data/ # Données brutes (non versionnées)
├─ notebooks/ # Explorations et analyses
├─ src/
│ ├─ data.py # Chargement et nettoyage
│ ├─ features.py # Feature engineering
│ ├─ split.py # Découpage temporel / cold start
│ ├─ model.py # Entraînement du modèle
│ ├─ metrics.py # Calcul des métriques
│ └─ infer.py # Génération du fichier submission.csv
├─ dashboard/
│ └─ streamlit_app.py # Dashboard des résultats
├─ outputs/
│ ├─ models/ # Modèles sauvegardés
│ ├─ figs/ # Graphiques
│ └─ submission/ # Fichier final de prédiction
└─ README.md
```

---

## ▶️ Exécution rapide
```bash
# 1. Installer les dépendances
pip install -r requirements.txt

# 2. Lancer le notebook d’entraînement
jupyter notebook notebooks/

# 3. Générer les prédictions


# 4. Lancer le dashboard
