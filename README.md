# Belib-reseau-de-recharge
Projet Open Data — Analyse et Cartographie du Réseau Belib' (Paris)


Ce projet a été réalisé sous Navicat (MySQL) pour la structuration de la base de données BELIB et sous Power BI pour le développement des mesures DAX, des indicateurs clés (KPI) et des tableaux de bord analytiques du réseau de recharge pour véhicules électriques de Paris.

⚡ Projet Open Data — Analyse et Cartographie du Réseau Belib' (Paris)

📌 1. Contexte et Objectifs du Projet

Ce projet s'inscrit dans le cadre du TP de Data Visualisation. Il vise à concevoir une chaîne décisionnelle complète (Open Data -> MySQL -> Power BI) pour analyser en temps réel et de manière temporelle l'offre, la tension d'usage et la santé opérationnelle du réseau de bornes de recharge pour véhicules électriques Belib' à Paris.

🛠️ 2. Architecture Technique & Données

Source des données : Open Data Paris (Données statiques et flux de disponibilité des stations).
Stockage et Traitement : Base de données relationnelle MySQL.
Modélisation : Schéma en étoile séparant le référentiel descriptif (dim_statique) et les mesures d'état (fait_dispo), enrichi par la suite pour l'historisation temporelle (dim_statique_temporelle et fait_dispo_temporelle).
Outil de Restitution : Power BI Desktop (.pbix)

📊 3. Structure du Tableau de Bord (6 Pages)

Le rapport Power BI se compose de 5 onglets thématiques :

Caractéristiques : Vue d'ensemble de la volumétrie des stations et répartition de l'offre technique (types de prises, puissances).
Cartographie : Représentation géographique interactive des points de charge sur le territoire parisien.
Clusters : Corrélation entre le taux d'occupation et la puissance moyenne des points de recharge
KPIs Opérationnels : Suivi de la disponibilité globale, taux d'indisponibilité et identification des bornes en panne ou maintenance.
Utilisations (1/2) : Analyse de la répartition de l'usage et de la charge à l'instant 
T (initialisé à 12h00).
Utilisations (2/2) : Analyse temporelle et comparative de la tension du réseau grâce aux snapshots journaliers (8h00, 15h00, 17h00).

⚙️ 4. Guide d'Installation et de Reproductibilité

Clonage du projet : Récupérer l'arborescence et les sources de données brutes dans le répertoire /data.
Base de données : Exécuter les scripts SQL de création des tables et des vues d'historisation situés dans le dossier /sql.
Visualisation : Ouvrir le fichier Power BI Belib_temporelle.pbix, configurer la connexion ODBC vers la base MySQL locale, puis lancer l'actualisation des données.
