# 🗳️ Exploitation de données électorales — Présidentielle 2022

**Évaluation intermédiaire — Python pour la data science (mi-semestre 2026)**  
ENSAE Paris / INSEE

> Auteurs : **BANZOUZI MIAMPASSI Hermann** & **TCHATCHOU NJATCHA Neville**

---

## 📌 Présentation

Ce dépôt contient notre analyse des résultats du **premier tour de l'élection présidentielle française du 10 avril 2022**, réalisée dans le cadre de l'évaluation intermédiaire du cours *Python pour la data science* de Lino Galiana (INSEE).

L'objectif est d'explorer la richesse des données électorales à l'échelle communale et départementale, de calculer des indicateurs de surreprésentation géographique, et de les visualiser sous forme de graphiques et de cartes choroplèthes.

---

## 📂 Structure du dépôt

```
.
├── BANZOUZI_et_TCHATCHOU_DM_Python.ipynb   # Notebook principal (analyse complète)
└── README.md
```

---

## 📊 Contenu de l'analyse

Le notebook est organisé en trois parties :

**1. Explorations générales**
- Reconstruction du code INSEE commune à 5 caractères
- Création de la colonne `candidat` (prénom + nom)
- Calcul du nombre de candidats en lice (hors abstentions, blancs et nuls)
- Tableau des scores nationaux de chaque candidat (voix + % des suffrages exprimés)

**2. Comparaison des scores départementaux aux moyennes nationales**
- Calcul des scores par département pour chaque candidat
- Jointure avec les scores nationaux
- Calcul de la variable `surrepresentation` (écart relatif entre score local et national)
- Visualisation en graphique horizontal des top départements sur- ou sous-représentés pour un candidat donné

**3. Cartographie**
- Fond de carte des départements via `cartiflette`
- Cartes choroplèthes de la surreprésentation pour Marine Le Pen, Emmanuel Macron et Éric Zemmour

---

## 🗂️ Source des données

| Donnée | Source |
|---|---|
| Résultats par commune (1er tour 2022) | [data.gouv.fr](https://www.data.gouv.fr/fr/datasets/r/182268fc-2103-4bcb-a850-6cf90b02a9eb) |
| Fond de carte des départements | [`cartiflette`](https://github.com/InseeFrLab/cartiflette) — IGN / INSEE 2022 |

Les résultats ont été vérifiés et correspondent aux chiffres officiels certifiés par le Conseil constitutionnel (avril 2022).

---

## ⚙️ Installation et reproductibilité

### Prérequis

- Python >= 3.9
- Jupyter Notebook ou JupyterLab

### Dépendances

```bash
pip install pandas matplotlib cartiflette geopandas
```

### Lancer le notebook

```bash
jupyter notebook BANZOUZI_et_TCHATCHOU_DM_Python.ipynb
```

Le notebook est **entièrement reproductible** : un clic sur *Run All* suffit à l'exécuter de bout en bout. Les données sont téléchargées automatiquement depuis leurs sources en ligne.

---

## 📈 Aperçu des résultats

**Scores nationaux (suffrages exprimés) :**

| Candidat | Voix | Score |
|---|---|---|
| Emmanuel MACRON | 9 783 058 | 27,85 % |
| Marine LE PEN | 8 133 828 | 23,15 % |
| Jean-Luc MÉLENCHON | 7 712 520 | 21,95 % |
| Éric ZEMMOUR | 2 485 226 | 7,07 % |
| … | … | … |

**Total suffrages exprimés :** 35 132 947

---

## 📚 Références

- Cours *Python pour la data science* : [pythonds.linogaliana.fr](https://pythonds.linogaliana.fr)
- Résultats officiels du Conseil constitutionnel : [presidentielle2022.conseil-constitutionnel.fr](https://presidentielle2022.conseil-constitutionnel.fr)
- Documentation `cartiflette` : [github.com/InseeFrLab/cartiflette](https://github.com/InseeFrLab/cartiflette)
