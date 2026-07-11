# 📈 Étude des courbes de croissance — Régression sur données réelles

SAE « Régression sur données réelles » — BUT Science des Données, IUT de Paris (2025–2026)

Étude comparative de la croissance des enfants et adolescents (5–19 ans) en **Guinée-Bissau** et en **Papouasie Nouvelle-Guinée**, à partir de données anthropométriques réelles collectées en 2020 dans plus de 90 pays.

**Auteurs :** William Houblon-Tchagam, Florent Danlos, Nathan Sokol

---

## 🎯 Objectifs

- Décrire les distributions de taille et d'âge pour 4 profils (fille/garçon × Guinée-Bissau/Papouasie N.-G.)
- Modéliser la relation taille ~ âge par **régression polynomiale**, avec sélection du degré optimal par **AIC**
- Construire des courbes de **médiane et quartiles conditionnels** (approche non paramétrique)
- Comparer statistiquement les groupes (sexe, pays) et interpréter les résultats sur le plan biologique

## 🗂️ Données

- **8 000 observations** au total (4 000 par pays, 2 000 par sexe)
- Protocole : 200 médecins tirés au sort par pays, chacun examinant 20 patients (10 filles, 10 garçons)
- Variables : `Pays`, `Sexe`, `Age` (années décimales), `Taille` (cm)

## 🧪 Méthodologie

1. **Analyse descriptive** — statistiques (moyenne, écart-type, min/max) et boîtes à moustaches par groupe
2. **Corrélation et modèle linéaire** — corrélations de Pearson âge/taille, mise en évidence des limites d'un modèle linéaire simple
3. **Régression polynomiale** — ajustement de degré 2 à 7 par moindres carrés (un modèle par profil sexe × pays), degré optimal choisi par minimisation de l'AIC
4. **Courbes non paramétriques** — médiane, 1er et 3e quartiles calculés sur 15 classes d'âge égales
5. **Tests statistiques** — tests t de Student (Taille ~ Sexe et Taille ~ Pays)

## 🔑 Résultats clés

- Les courbes suivent une **forme sigmoïde** typique de la croissance humaine (croissance rapide en enfance, plateau à l'adolescence)
- **Avance pubertaire des filles** entre 9 et 12 ans, puis rattrapage et dépassement par les garçons à partir de 13–14 ans
- Écart de taille **non significatif** entre sexes sur l'ensemble de la tranche 5–19 ans (p = 0,658), les deux effets opposés s'annulant
- Écart **significatif entre pays** (p < 0,001) : les enfants de Guinée-Bissau sont en moyenne 2,92 cm plus grands que ceux de Papouasie N.-G.

## 🛠️ Technologies

- **R** (régression linéaire/polynomiale, tests statistiques)
- Packages : `dplyr`, `knitr`
- **R Markdown** pour la génération du rapport

## 📁 Structure du dépôt

```
├── data/                # Données brutes (Data_Projet35.RData)
├── rapport/              # Rapport R Markdown (.Rmd) et rendu (.pdf)
├── slides/               # Support de présentation
└── README.md
```

## 📄 Livrables

- Rapport synthétique (~19 pages, en français, résumé en anglais)
- Slides de présentation

---

*Projet réalisé dans le cadre de la SAE « Régression sur données réelles » — BUT Science des Données, IUT de Paris – Rives de Seine, année 2025–2026.*
