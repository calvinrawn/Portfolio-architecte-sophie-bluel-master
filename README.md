# Portfolio de Sophie Bluel | Développement Frontend & Backend

Ce projet consistait à développer le portfolio dynamique d'une architecte d'intérieur, avec une interface d'administration permettant de gérer les projets présentés en temps réel. L'objectif était de créer une application full-stack fonctionnelle, connectant un frontend statique à une API backend sécurisée par authentification.

## 🛠️ Missions réalisées

* **Développement Frontend** : Intégration HTML/CSS/JS d'une page portfolio dynamique, avec filtrage des projets par catégorie.
* **Connexion API** : Implémentation des appels `fetch` vers le backend pour récupérer et afficher les travaux (works) et catégories depuis la base de données.
* **Authentification** : Mise en place d'un système de connexion (login) sécurisé avec gestion de token, débloquant un mode édition pour l'utilisateur connecté.
* **Mode édition** : Ajout d'une modale permettant d'ajouter ou de supprimer des projets directement depuis l'interface, avec upload d'image.

## 🚀 Compétences techniques

* **JavaScript** : Manipulation du DOM, requêtes asynchrones (fetch/API REST), gestion d'événements.
* **Backend** : Node.js / Express, base de données SQLite (Sequelize).
* **Authentification** : Gestion de token JWT et de sessions utilisateur.
* **Outils** : Live Server, Swagger (documentation API).

---

## ⚙️ Installation et lancement du projet

Le projet est composé de deux parties indépendantes à lancer séparément : le **backend** (API + base de données) et le **frontend** (interface visuelle). Il est recommandé d'ouvrir chaque dossier dans une fenêtre VSCode distincte pour éviter toute confusion.

### Prérequis

* [Node.js](https://nodejs.org/) installé (version LTS recommandée)
* L'extension **Live Server** installée dans VSCode

Vérifier l'installation de Node.js dans un terminal :
```bash
node -v
npm -v
```

### 1. Lancer le backend

Dans un terminal, se placer dans le dossier `Backend` du projet :

```bash
cd chemin/vers/Backend
npm install
npm start
```

Si le lancement fonctionne, le terminal doit afficher :
```
Listening on port 5678
db is ready
```

### 2. Lancer le frontend

Le frontend est un site statique, il ne se lance **pas** avec `npm start` mais directement via l'extension **Live Server** :

1. Ouvrir le dossier `Frontend` dans VSCode.
2. Clic droit sur le fichier `index.html` → **"Open with Live Server"**.
3. Le site s'ouvre automatiquement dans le navigateur.

⚠️ **Point de vigilance (CORS)** : le port utilisé par Live Server doit correspondre à celui autorisé par le backend. Le port est configurable dans le fichier `.vscode/settings.json` du frontend :

```jsonc
{
    "liveServer.settings.port": 5501
}
```

Si une erreur CORS apparaît dans la console du navigateur (F12), vérifier que le port déclaré ici correspond à celui autorisé dans le code du backend (fichier `app.js` ou équivalent).

### 3. Utilisation

Une fois le frontend et le backend lancés simultanément, se connecter avec le compte de test ci-dessus pour accéder au mode édition (ajout/suppression de projets, upload d'images).