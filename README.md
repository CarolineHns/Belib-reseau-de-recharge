# Belib-reseau-de-recharge
Projet Open Data — Analyse et Cartographie du Réseau Belib' (Paris)


Ce projet a été réalisé sous Navicat (MySQL) pour la structuration de la base de données BELIB et sous Power BI pour le développement des mesures DAX, des indicateurs clés (KPI) et des tableaux de bord analytiques du réseau de recharge pour véhicules électriques de Paris.

⚡ Projet Open Data — Analyse et Cartographie du Réseau Belib' (Paris)

📌 1. Contexte et Objectifs du Projet

Ce projet s'inscrit dans le cadre du TP de Data Visualisation. Il vise à concevoir une chaîne décisionnelle complète (Open Data -> MySQL -> Power BI) pour analyser en temps réel et de manière temporelle l'offre, la tension d'usage et la santé opérationnelle du réseau de bornes de recharge pour véhicules électriques Belib' à Paris.

🛠️ 2. Architecture Technique & Données

Source des données : Open Data Paris (Données statiques et flux de disponibilité des stations).
Stockage et Traitement : Base de données relationnelle MySQL
Modélisation : Schéma en étoile séparant le référentiel descriptif (dim_statique) et les mesures d'état (fait_dispo), enrichi par la suite pour l'historisation temporelle (dim_statique_temporelle et fait_dispo_temporelle)
Outil de Restitution : Power BI Desktop (.pbix)

📊 3. Structure du Tableau de Bord (6 Pages)

Le rapport Power BI se compose de 6 onglets thématiques :

Caractéristiques : Vue d'ensemble de la volumétrie des stations et répartition de l'offre technique (types de prises, puissances)
Cartographie : Représentation géographique interactive des points de charge sur le territoire parisien
Clusters : Corrélation entre le taux d'occupation et la puissance moyenne des points de recharge
KPIs Opérationnels : Suivi de la disponibilité globale, taux d'indisponibilité et identification des bornes en panne ou maintenance
Utilisations (1/2) : Analyse de la répartition de l'usage et de la charge à l'instant T (initialisé à 12h00)
Utilisations (2/2) : Analyse temporelle et comparative de la tension du réseau grâce aux snapshots journaliers (8h00, 15h00, 17h00)

⚙️ 4. Guide d'Installation et de Reproductibilité

Clonage du projet : Récupérer l'arborescence et les sources de données brutes dans le répertoire /data
Base de données : Exécuter les scripts SQL de création des tables et des vues d'historisation situés dans le dossier /sql
Visualisation : Ouvrir le fichier Power BI Belib_temporelle.pbix, configurer la connexion ODBC vers la base MySQL locale, puis lancer l'actualisation des données


<img width="1351" height="796" alt="Caractéristiques" src="https://github.com/user-attachments/assets/888b4a45-ea94-4ab8-9b05-3f78eb861b11" />

<img width="1327" height="795" alt="Carto" src="https://github.com/user-attachments/assets/4eef1177-5eb3-49d3-8d23-4a5526b8f90e" />

<img width="1325" height="792" alt="Clusters" src="https://github.com/user-attachments/assets/4ae64606-92c8-4f92-be82-f155ab7a25ef" />

<img width="1352" height="797" alt="KPIs opérationnels" src="https://github.com/user-attachments/assets/cefa1713-0e47-4354-bafe-747f5d614fbd" />

<img width="1351" height="790" alt="Utilisations 1" src="https://github.com/user-attachments/assets/2cddd2d6-e340-43f0-a354-8f47979ba013" />

<img width="1347" height="797" alt="Utilisations 2" src="https://github.com/user-attachments/assets/9db679fa-edf5-459b-8e24-ce0a1dcf2c6b" />
