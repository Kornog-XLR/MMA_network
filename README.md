# MMA network

Projet M2 MAS — Analyse des réseaux sociaux (Adrien et Nicolas).

Réseau orienté des combats UFC : chaque nœud est un combattant, chaque combat gagné est une arête **du perdant vers le gagnant**. Objectif : analyser la centralité du réseau et la comparer au classement officiel UFC.

## Contenu

- `mma.Rmd` : analyse (import, construction du graphe, sous-graphes par catégorie de poids et par période).
- `dataset_ufc/UFC dataset/` : données UFC 1994–2024.
  - `Large set/large_dataset.csv` : une ligne par combat, colonne `winner` (`Red` / `Blue`) — utilisé pour le graphe.
  - `Small set/completed_events_small.csv` : date de chaque événement (jointure par nom d'événement).

Source des données : [UFC complete dataset (Kaggle)](https://www.kaggle.com/datasets/maksbasher/ufc-complete-dataset-all-events-1996-2024).

## Utilisation

Packages R : `readr`, `dplyr`, `igraph`.

```r
install.packages(c("readr", "dplyr", "igraph"))
rmarkdown::render("mma.Rmd")
```

## Configuration locale

Chaque membre a son propre dossier racine. Avant le premier lancement :

1. copier `config_exemple.R` sous le nom `config.R` ;
2. y indiquer le chemin du dossier du projet sur sa machine (`chemin_projet`).

`config.R` est ignoré par git : il n'est jamais poussé sur le dépôt.
