# Gestion Recettes API

Cette API permet de gérer des recettes et des catégories, en allant de leur création, lecture, mise à jour et suppression.

## Prérequis

- Node.js (version 14 ou supérieure)
- MySQL (ou un autre système de gestion de base de données compatible)
- Postman (pour tester l'API)
- Docker (v.4.30 ou supérieure)

## Installation

1. **Clonez le dépôt** :

```bash
    git clone https://github.com/Aichetou-Gaye/gestion-recette-backEnd.git
```

2.  **Acceder au dossier du projet**

```bash
  cd gestion-recette-backEnd
```

3. **Installez les dépendances**

```bash
   npm install
```

4. **Utilisation**

- Remplacer d'abord les informations de votre base de données dans:

[.env.sample](.env.sample)

- Pour démarrer le projet:

```bash
   npm start
```

- Importer la collection dans postman pour effectuer des tests :
  [postman_collection.json](postman_collection.json)

## Endpoints API

### Endpoints Recettes

**Récupérer toutes les recettes**

- URL : /recipes
- Méthode : GET
- Réponse:

```
[
  {
    "id": 1,
    "titre": "Recette 1",
    "ingredients": "Ingrédients de la recette 1",
    "type": "type 1"
  },
  {
    "id": 2,
    "titre": "Recette 2",
    "ingredients": "Ingrédients de la recette 2",
     "type": "type 2"
  },
]
```

**Récupérer une recette**

- URL : /recipes/:id
- Méthode : GET
- Réponse: 
```
[
  {
    "id": 1,
    "titre": "Recette",
    "ingredients": "Ingrédients de la recette",
    "type": "type"
  },
]
```

**Créer une nouvelle recette**

- URL : /recipes
- Méthode : POST

```
{
    "titre": "Nouvelle Recette",
    "ingredients": "Ingrédients de la recette",
    "type": "Plat principal"
    "categorie_id": 1
}
```

- Réponse: `"Added successfully"`;

  **Mettre à jour une recette**

- URL : /recipes/:id
- Méthode : PUT

```
{
   "titre": "Recette Modifiée",
   "ingredients": "Ingrédients de la recette modifiée",
   "type": "type modifiée",
   "categorie_id": 1
  }
```

- Réponse: `"Updated successfully"`

  **Supprimer une recette**

- URL : /recipes/:id
- Méthode : DELETE
- Réponse: `"Deleted successfully"`

### Endpoints Catégories

**Récupérer toutes les categories**

- URL : /categories
- Méthode : GET
- Réponse: 
```
[
  {
    "id": 1,
    "titre": "categorie 1",
    "ingredients": "Ingrédients de la categorie 1",
    "type": "type 1"
  },
  {
    "id": 2,
    "titre": "categorie 2",
    "ingredients": "Ingrédients de la categorie 2",
     "type": "type 2"
  },
]
```

**Récupérer une catégorie**

- URL : /categories/:id
- Méthode : GET
- Réponse: 
```
[
  {
    "id": 1,
    "titre": "categorie",
    "ingredients": "Ingrédients de la categorie",
    "type": "type"
  },
]
```

**Créer une nouvelle categorie**

- URL : /categories
- Méthode : POST

```
{
    "nom": "Nouvelle categorie"
}
```

- Réponse: `"Added successfully"`;

  **Mettre à jour une categorie**

- URL : /categories/:id
- Méthode : PUT

```
{
   "nom": "categorie Modifiée"
  }
```

- Réponse: `"Updated successfully"`

  **Supprimer une categorie**

- URL : /categories/:id
- Méthode : DELETE
- Réponse: `"Deleted successfully"`

### Tests unitaires

```bash
npm test
```

### ESlint : correction de code

```bash
npm run lint
```

### Prettier: format de code

```bash
npm run format
```

## Docker

### Builder l'image docker

```bash
docker compose up --build
```

### Connexion à Mysql

- Sur la ligne de commande executez pour utiliser mysql :

```bash
docker exec -it gestion_recette bash
```

```bash
mysql -u root -p
```

- Importez la collection dans Postman pour communiquez via l'URL:
  [postman_collection.json](postman_collection.json)

## Auteurs

[Aichetou Gaye](https://github.com/Aichetou-Gaye)

[Mohamed Bankolé](https://github.com/medbankole97)
