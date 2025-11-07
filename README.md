# Track Finance

# Detection of Fraudulent Bank Transactions

## Team 20
- Lisa Naccache (DIA 4): Team Leader  
- Hiba NEJJARI (DIA 4)  
- Neil MAHCER (DIA 4)  
- Wendy DUONG (DIA 4)  
- Cyprien MOUTON (DIA 4)  
- Safa HORMI BOUAICHI (DIA 3)  

---

## Repository Overview

This repository contains all the materials for the **WatsonIA – Banking Fraud Detection** project, developed for the **IBM Hackathon – Finance Track**.

### Quick Access
- **Code:** [Code/](./Code)
  - [2_EDA.ipynb](./Code/2_EDA.ipynb) – Exploratory Data Analysis  
  - [3_DataCleaning_and_DataPreparation.ipynb](./Code/3_DataCleaning_and_DataPreparation.ipynb) – Data Cleaning and Preparation  
  - [4_5_Machine_Learning_Modeling.ipynb](./Code/4_5_Machine_Learning_Modeling.ipynb) – **(Temporary)** Machine Learning and Model Training; contains the code for the **submission file**.  
  - [Machine_Learning_Modeling_v2.ipynb](./Code/Machine_Learning_Modeling_v2.ipynb) – **Cold start and standard version** of the machine learning workflow.  
  - [import.txt](./Code/import.txt) – Dependencies list  

- **Data:** [Data/](./Data) – Contains the raw and processed datasets as well as the submission file.

- **Documentation:** [Docs/](./Docs)
  - [ESILV Hackathon Use Cases.pdf](./Docs/ESILV%20Hackathon%20Use%20Cases.pdf)  
  - [Introduction_Context.pdf](./Docs/Introduction_Context.pdf)  
  - [Kickoff.pdf](./Docs/Kickoff.pdf)
  - [Prez IBM.pdf](./Docs/PREZ IBM.pdf) **PDF DE PRESENTATION**
  Lien du canva : https://www.canva.com/design/DAG317at_8w/Naij3IgkLQM2boZExbH4yw/edit?utm_content=DAG317at_8w&utm_campaign=designshare&utm_medium=link2&utm_source=sharebutton

- **Project Management:** [Management/tasks.md](./Management/tasks.md) – Task tracking and team responsibilities.

- **Certificates:** [certificates/](./certificates) – Hackathon participation and completion certificates.

- **Git Guide:** [GIT_PULL_PUSH_GUIDE.md](./GIT%20PULL%20PUSH%20GUIDE.md) – Instructions for pushing and pulling updates.

- **Main Project Summary:** [README.md](./README.md) – This file.


---

## Project Context

With the rapid digitalization of payments, banking frauds have become increasingly frequent and sophisticated.  
This project was carried out as part of the **IBM Hackathon – Finance Track**, with the goal of developing a **Machine Learning model** capable of automatically detecting fraudulent transactions from a realistic dataset provided by IBM (2016–2018).

---

## Objective

Develop an **Artificial Intelligence model** that predicts whether a transaction is:
- `1` → Fraudulent  
- `0` → Non-fraudulent  

The model must be robust, generalizable to new clients (cold start), and resilient to a high class imbalance (~0.15% of fraud).

---

## Data

Data provided by IBM:
- `transactions_train.csv`: Training transactions (amount, date, card, etc.)  
- `train_fraud_labels.json`: Fraud labels (1 or 0)  
- `cards_data.csv`: Payment card information  
- `users_data.csv`: User profiles (age, income, location, etc.)
- `mcc_codes.json`: MCC codes (merchant categories)

Data after modification:
- **final_dataset_FE.zip : Dataset after Feature Engineering that we use for training the models** ( zipped because it is too large for github)
- `Final Submission/fraud_predictions_final.csv`: Evaluation data (without labels) the submission file after training the model.

  <img width="539" height="602" alt="image" src="https://github.com/user-attachments/assets/b14c906f-78bb-4453-b3cd-5794281d4312" />


---

## Methodology

Our approach follows the standard **Data Science pipeline**:
1. Exploratory Data Analysis (EDA)  
2. Data Preparation and Feature Engineering  
3. Modeling (LightGBM)  
4. Evaluation and Generalization  
5. Visualization of Results (Power BI Dashboard)  
6. Final Submission (`submission.csv`)

---

## Team Roles

| Role | Members |
|:------|:---------|
| Introduction & Context | Lisa & Cyprien |
| Data Exploration | Hiba |
| Data Preparation | Hiba, Lisa & Safa |
| Machine Learning | Neil & Wendy |
| Evaluation & Generalization | Neil & Wendy |
| Dashboard & Visualization (Power BI) | Safa |
| Final Submission | Cyprien |
| Report & Presentation | All Members |

---

## Technologies Used

- **Language:** Python 3.10  
- **Main Libraries:**
  - `pandas`, `numpy` – Data manipulation  
  - `lightgbm`, `scikit-learn` – Modeling and metrics  
  - `matplotlib`, `seaborn` – Visualization  
- **Tools:**
  - Jupyter Notebook  
  - Power BI – Dashboard and data visualization  
  - IBM Watsonx – Code execution and model experimentation  
  - Git & GitHub  

---

-> **IBM Watsonx** was used for model training, testing, and evaluation within the IBM cloud environment.
