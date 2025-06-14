# 🧠 DermAI Diagnostics: SQL Capstone Project

This project is a full SQL-based exploration of a structured dermatology dataset. It was conducted as part of a capstone analysis to identify clinical, demographic, lifestyle, and environmental **risk factors associated with skin cancer** — particularly focusing on distinguishing **malignant vs. benign lesions** using structured metadata.

All analysis, queries, and insights were generated using **SQL only**.

---

## 🚨 Problem Statement

Skin cancer is one of the most common but preventable cancers globally. However, early detection is hindered by factors like misdiagnosis, limited symptom awareness, and poor environmental conditions. The aim of this project is to:

- Uncover clinical and demographic patterns associated with malignant lesions.
- Identify warning signs and environmental exposures that predict cancer severity.
- Create a **machine learning–ready structured dataset** using SQL.
- Enable future researchers and AI developers to use this SQL-only pipeline for **epidemiological insights** and **AI model training**.

---

## 📊 Dataset Overview

Two main tables were used:

### `table1` — **Patient_Info**

| Column                      | Description                |
| --------------------------- | -------------------------- |
| patient_id                 | Unique patient identifier  |
| gender                      | Gender (MALE/FEMALE)       |
| age                         | Patient age                |
| smoke                       | Smoker status              |
| drink                       | Alcohol consumption status |
| pesticide                   | Exposure to pesticides     |
| background_father / mother | Ethnic backgrounds         |
| cancer_history             | Family history of cancer   |
| skin_cancer_history       | Previous diagnosis         |
| has_piped_water           | Access to piped water      |
| has_sewage_system         | Access to sewage system    |

### `table2` — **Lesion_Info**

| Column                                      | Description                          |
| ------------------------------------------- | ------------------------------------ |
| lesion_id                                  | Unique lesion identifier             |
| patient_id                                 | Foreign key to Patient_Info          |
| diagnostic                                  | Type of lesion (e.g., MEL, BCC, NEV) |
| fitspatrick                                 | Skin type scale (1–6)                |
| region                                      | Body region                          |
| diameter_1 / diameter_2                   | Lesion measurements                  |
| itch, bleed, grew, hurt, changed, elevation | Symptom flags                        |
| biopsed                                     | Biopsy-confirmed flag                |

---

## 🧪 Project Workflow

```sql
1. Import & clean data (PostgreSQL)
2. Join Patient_Info and Lesion_Info via patient_id
3. Analyze:
   - Lesion characteristics
   - Environmental risk factors
   - Demographics & lifestyle
4. Build machine learning–ready dataset using SQL
5. Generate clinically relevant flags (e.g., risk level, symptom count)
