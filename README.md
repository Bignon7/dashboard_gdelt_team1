# Dashboard Streamlit — Benin Insights Challenge

Application interactive développée pour le hackathon iSHEERO x DataCamp Donates 2026. Ce tableau de bord permet de visualiser et d'analyser la présence et le traitement médiatique du Bénin dans les médias internationaux en 2025 grâce aux données GDELT.

[![Streamlit App](https://streamlit.io)](https://team1-dashboard.streamlit.app/)

## Fonctionnalités

- Analyse des événements GDELT 2025 liés au Bénin (coopération, conflits verbaux/matériels).
- Suivi du ton moyen (sentiment) et de l'indice de Goldstein de la couverture médiatique.
- Répartition linguistique des mentions et identification des thématiques majeures (GKG).
- Filtrage dynamique par mois, type d'événement, type d'interaction et sentiment.
- Connexion directe et sécurisée à Google BigQuery.

## Architecture des données

L'application requiert un accès au projet Google Cloud Platform suivant :
- Projet : gdelt-494812
- Dataset : benin_2025
- Tables consultées : `events_clean`, `gkg_clean`, `mentions_clean`

## Installation et Lancement local

1. Cloner le dépôt GitHub.
2. Installer les dépendances requises (Streamlit, Pandas, NumPy, Plotly, Google Cloud BigQuery).
3. Créer un fichier `.streamlit/secrets.toml` à la racine de votre projet pour y ajouter vos identifiants GCP sous la forme suivante :

```toml
[gcp_service_account]
type = "service_account"
project_id = "gdelt-494812"
# ... 
```

4. Lancer l'application localement :
```bash
streamlit run dashboard/app.py
```
