# 📰 Blog Symfony - Projet Web

## 🚀 Fonctionnalités

- Authentification sécurisée (login / logout)
- Rôles utilisateurs :
  - `ROLE_ADMIN` : accès complet, gestion des articles, utilisateurs, etc.
  - `ROLE_USER` : peut consulter les articles et son profil
  - `ROLE_BANNED` : accès limité, redirigé vers une page d'avertissement
- CRUD complet pour les entités :
  - Article
  - Catégorie
  - Langue
  - Commentaire (si activé)
- Filtrage des articles par catégorie
- Affichage dynamique des articles récents en page d’accueil
- Protection des routes selon le rôle
- Affichage du prénom/nom de l'utilisateur connecté
- Slug pour les URLs des articles

---

## 👤 Utilisateurs de test

| Email                | Mot de passe | Rôles           | Accès                                         |
|---------------------|--------------|------------------|-----------------------------------------------|
| `admin@example.com` | `admin123`   | `ROLE_ADMIN`     | Admin, gestion des articles, dashboard        |
| `user@example.com`  | `user123`    | `ROLE_USER`      | Profil, lecture d’articles                    |
| `banned@example.com`| `banned123`  | `ROLE_BANNED`    | Redirigé vers la page `/banned`               |

---

## 🗺️ Routes principales

| Route                       | Description                               | Accès              |
|----------------------------|-------------------------------------------|---------------------|
| `/`                        | Page d’accueil (liste des articles)       | Publique            |
| `/blog/{slug}`             | Voir un article spécifique                | Publique            |
| `/article`                 | Liste des articles (back-office)          | `ROLE_ADMIN`        |
| `/article/new`             | Créer un article                          | `ROLE_ADMIN`        |
| `/article/{id}`            | Voir un article (admin)                   | `ROLE_ADMIN`        |
| `/article/{id}/edit`       | Éditer un article                         | `ROLE_ADMIN`        |
| `/categorie`               | Gestion des catégories                    | `ROLE_ADMIN`        |
| `/langue`                  | Gestion des langues                       | `ROLE_ADMIN`        |
| `/login`                   | Page de connexion                         | Tous                |
| `/logout`                  | Déconnexion                               | Connecté uniquement |
| `/profile`                 | Profil de l’utilisateur                   | `ROLE_USER` / `ADMIN` |
| `/banned`                  | Page affichée pour un utilisateur banni  | `ROLE_BANNED`       |
| `/admin`                   | Dashboard admin (exemple)                 | `ROLE_ADMIN`        |

---
