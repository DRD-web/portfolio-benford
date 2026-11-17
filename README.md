# Portfolio Benford — Repérer les montants atypiques dans les comptes annuels d'entreprises

Projet en cours.

## Question

Dans les comptes annuels d'entreprises françaises, quels montants ou quelles entreprises
s'écartent de la distribution attendue des premiers chiffres (loi de Benford), et
mériteraient une vérification en priorité ?

Un écart à la loi de Benford n'est pas une preuve de fraude : c'est un signal qui aide à
choisir quoi contrôler en premier.

## Données

[Données financières détaillées des entreprises (format parquet) — BceInpiDetail](https://www.data.gouv.fr/datasets/6587efa36e80ab61d5792fdd),
publiées sur data.gouv.fr sous Licence Ouverte 2.0.

Le fichier (environ 2,6 Go) n'est pas inclus dans ce dépôt. Pour reproduire l'analyse,
téléchargez-le depuis la page ci-dessus et placez-le dans le dossier `data/`.

## Outils

- DuckDB : requêtes SQL directement sur le fichier parquet
- Python (pandas) : calculs statistiques
- Power BI : restitution (à venir)

## Installation

Python 3.13.

    python -m venv .venv
    .venv\Scripts\activate        # Windows
    source .venv/bin/activate     # macOS / Linux
    pip install -r requirements.txt

## Structure

    data/        données sources (non versionnées)
    notebooks/   notebooks/   bacs à sable locaux (non versionnés)
    src/         code réutilisable
