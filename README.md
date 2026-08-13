# 📊 Atelier Pandas – Analyse de données de capteurs IoT

![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-3.x-150458?logo=pandas&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-2.x-013243?logo=numpy&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?logo=jupyter&logoColor=white)

Manipulation, exploration et nettoyage d'un jeu de données de capteurs IoT
avec **Pandas**, en préparation d'un futur système de Machine Learning de
détection d'anomalies.

---

## 🧭 Contexte

Une entreprise dispose de plusieurs bâtiments équipés de **capteurs IoT**.
Chaque capteur relève régulièrement la **température**, l'**humidité**, la
**pression**, la **consommation énergétique**, ainsi que son **état** et le
**bâtiment** concerné, avec la **date et l'heure** de la mesure.

Avant de transmettre ces données à un système de Machine Learning capable de
**détecter des situations anormales**, il faut les **préparer, explorer et
nettoyer**. C'est l'objet de cet atelier.

---

## 🎯 Objectifs

- Découvrir les structures de base de Pandas (`Series`, `DataFrame`)
- Importer et explorer un jeu de données réel
- Sélectionner, filtrer, trier et manipuler des colonnes
- Analyser les données par groupes (`groupby`)
- Gérer les **valeurs manquantes** et les **doublons**
- Calculer des **statistiques descriptives**
- Exporter les données nettoyées (CSV / JSON)

---

## 📁 Structure du projet

```
atelier_pandas_iot/
│
├── data/
│   └── mesures_capteurs.csv          # jeu de données brut (fourni)
│
├── notebooks/
│   └── atelier_pandas_iot.ipynb      # notebook principal de l'atelier
│
├── exports/
│   ├── donnees_nettoyees.csv         # données nettoyées (généré)
│   └── donnees_nettoyees.json        # données nettoyées (généré)
│
├── .gitignore
└── README.md
```

---

## 📦 Le jeu de données

Le fichier `data/mesures_capteurs.csv` contient **605 mesures** et **9 colonnes** :

| Colonne        | Description                                   |
|----------------|-----------------------------------------------|
| `id_mesure`    | Identifiant unique de la mesure               |
| `date_heure`   | Date et heure du relevé                        |
| `id_capteur`   | Identifiant du capteur                         |
| `batiment`     | Bâtiment concerné (B001 à B004)               |
| `temperature`  | Température mesurée (°C)                       |
| `humidite`     | Humidité relative (%)                          |
| `pression`     | Pression (hPa)                                 |
| `consommation` | Consommation énergétique                       |
| `etat`         | État du capteur (`OK`, `ALERTE`, `ERREUR`)    |

> Le jeu de données contient volontairement des **valeurs manquantes** et des
> **doublons**, qui sont traités dans le notebook.

---

## ⚙️ Prérequis

- **Python 3.x**
- **VS Code** avec l'extension **Jupyter** (ou Jupyter Notebook / JupyterLab)
- Les bibliothèques **pandas** et **numpy**

---

## 🚀 Installation et mise en place

1. **Cloner le dépôt**
```bash
   git clone https://github.com/khadija470/atelier_pandas_iot.git
   cd atelier_pandas_iot
```

2. **Créer et activer un environnement virtuel**
```bash
   python -m venv .venv

   # Windows (Git Bash)
   source .venv/Scripts/activate

   # Windows (PowerShell / CMD)
   .venv\Scripts\activate

   # Linux / macOS
   source .venv/bin/activate
```

3. **Installer les dépendances**
```bash
   pip install pandas numpy notebook
```

4. **Ouvrir le notebook**

   Ouvrir `notebooks/atelier_pandas_iot.ipynb` dans VS Code, puis sélectionner
   le **kernel** correspondant à l'environnement `.venv`.

---

## 📓 Contenu du notebook

Le notebook est organisé en **13 parties**, chacune documentée
(objectif, syntaxe, exemple) :

| Partie | Thème |
|--------|-------|
| 1 | Series |
| 2 | DataFrame |
| 3 | Exploration |
| 4 | Sélection (`loc` / `iloc`) |
| 5 | Manipulation des colonnes |
| 6 | Filtrage |
| 7 | Tri |
| 8 | Analyse (`groupby`) |
| 9 | Gestion des valeurs manquantes |
| 10 | Gestion des doublons |
| 11 | Statistiques descriptives |
| 12 | Exportation (CSV / JSON) |
| 13 | Bonus – Détection de mesures anormales |

---

## 📤 Résultats

À l'issue de l'atelier, les données nettoyées sont exportées dans le dossier
`exports/` aux formats **CSV** et **JSON**, prêtes à alimenter un pipeline de
Machine Learning.

---

## 👩‍💻 Auteur

**Khadija Ngom** — Atelier réalisé dans le cadre d'une formation en
Intelligence Artificielle.
