# Memorama API

API pour le site web Memorama permettant de rechercher des documents académiques et de détecter les plagiats.

L'API est développée avec :

- ExpressJS
- PassportJS pour l'authentification

## Fonctionnalités

- Recherche de documents par mots-clés, auteur, etc.
- Accès à une large base de données de publications académiques
- Détection de similarité entre deux documents pour vérifier s'il y a plagiat
- Sauvegarde et partage de documents
- Espace personnel pour gérer ses recherches et documents

## Installation

### Prérequis

- Node.js
- NPM

### Instructions

1. Cloner le repository

```bash

git clone https://github.com/PhoenixMputu/api-memorama.git

```
2. Installer les dépendances

```bash
npm install

```

3. Lancer le serveur de développement

```bash

npm run dev

```

L'API écoute par défaut sur le port 8080.

## Routes

### POST /auth/google

Route pour l'authentification avec Google via Passport.js. Renvoie un token JWT en cas de succès.

### GET /api/documents

Récupère la liste des documents académiques indexés. Requiert une authentification.

### POST /api/documents

Ajoute un nouveau document académique. Requiert une authentification.

Le corps de la requête doit contenir les détails du document:

```json
{
  "title": "Example article",
  "content": "Text of the academic document",
  "type": "article" 
}
```

### POST /api/checkPlagiarism

Vérifie si un document contient des passages plagiés. Requiert une authentification. 

Le corps de la requête doit contenir le document à vérifier:

```json
{
  "content": "Text of the document to check for plagiarism"
}
```

Renvoie un rapport détaillé des passages suspects.

## License

MIT

J'espère que cet exemple de readme donnera une bonne idée des fonctionnalités de l'API ! N'hésite pas à me contacter si tu as d'autres questions.