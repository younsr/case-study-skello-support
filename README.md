# Étude de cas – Data Analyst Stagiaire chez Skello

## Objectif : 

Cette étude de cas a été réalisée dans le cadre d’un processus de recrutement pour un stage de Data Analyst chez Skello.  
L’objectif est de concevoir un reporting opérationnel destiné à l’équipe Support, afin de suivre la qualité de service client via l’outil Intercom.


## Résultat final : 

- Le fichier `dashboard_skello.pbix` contient un **rapport Power BI** complet, composé de deux pages :
  1. **Vue d’ensemble du Support** : indicateurs globaux de performance (CSAT, réponses en < 5min…)
  2. **Analyse par agent** : suivi individuel des performances (conversations, délais, messages…)



## Contenu du dépôt : 

| Fichier | Description |
|--------|-------------|
| `dashboard_skello.pbix` | Dashboard complet Power BI |
| `Etude-cas-SKELLO-data-cleaned.zip` | Données nettoyées : `CONVERSATIONS_CLEAN.csv` et `CONVERSATION_PARTS_CLEAN.csv` |
| `Nettoyage.ipynb` | Script Jupyter utilisé pour le nettoyage des données (Python + pandas) |
| `README.md` | Ce fichier de présentation du projet |



## Modèle de données : 

Trois tables principales ont été créées dans Power BI :

- `Dim_Conversations` : informations sur chaque conversation Intercom
- `Fact_Messages` : tous les messages échangés (hors bots)
- `Dim_Agents` : liste des agents support identifiés

Une table calculée `RéponsesInitiales` a été ajoutée pour mesurer les délais de réponse.


## KPIs mis en place : 

### Page 1 – Vue d’ensemble Support : 

- Nombre total de conversations
- Moyenne CSAT
- Nombre de messages envoyés par les agents
- % de réponses en moins de 5 minutes

### Page 2 – Analyse par agent :

- Nombre de conversations par agent
- Moyenne CSAT par agent
- Temps de réponse moyen par agent
- Volume de messages envoyés


## Technologies utilisées : 

- **Power BI Desktop**
- **Python** (pandas) pour le prétraitement des fichiers `.csv`
- **GitHub** pour la mise à disposition du livrable


## Remarques techniques

- Les messages bots ont été exclus du périmètre, comme demandé.
- Seuls les messages de type `"Message"` ont été pris en compte.
- L’ID `ASSIGNEE_ID` a permis de filtrer les membres de l’équipe support :
  - Héloïse (5217337)
  - Justine (5391224)
  - Patrick (5440474)
  - Raphaël (5300290)


## Questions métiers ouvertes  :

- Doit-on exclure les conversations sans réponse ?
- La satisfaction CSAT est-elle toujours renseignée ?
- Veut-elle un suivi mensuel ou hebdomadaire ?


## Utilisation du projet : 

1. Télécharger le fichier `.pbix`
2. Télécharger et extraire le `.zip` dans le même dossier
3. Ouvrir le `.pbix` avec Power BI Desktop
4. Actualiser les données si besoin


## Contact : 

Ce projet a été réalisé par un candidat Data Analyst dans le cadre d’un test technique.  
Merci de votre lecture !
