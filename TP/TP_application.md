# Création d'une application pour un Système de Sondage avec MongoDB

## Objectif

L'objectif de cet exercice est de développer une application pour un système de sondage. L'application permettra la création de sondages, la gestion des questions, et la collecte des réponses. MongoDB servira de système de stockage pour les sondages et les réponses.

## Exigences Fonctionnelles

1. **Création de Sondage :**
   - L'application doit permettre la création d'un sondage.
   - Chaque sondage doit avoir un nom unique.
   - Un sondage doit contenir une liste de questions.
   - Chaque question aura un intitulé, un type (ouverte, choix multiple, etc.), et potentiellement des réponses prédéfinies si c'est un QCM.

2. **Modification de Sondage :**
   - Le créateur doit pouvoir modifier le sondage, y compris les questions et les réponses prédéfinies.

3. **Suppression de Sondage :**
   - Le créateur peut supprimer un sondage.

4. **Mise à jour de Sondage :**
   - L'application doit permettre la mise à jour des informations du sondage et des questions.

5. **Répondre aux Sondages :**
   - Les utilisateurs peuvent répondre aux questions des sondages.
   - Les réponses seront stockées dans une collection MongoDB avec une référence unique au sondage.

6. **Consultation des Sondages :**
   - Tous les utilisateurs peuvent consulter la liste des sondages publiés.

## Exemple de Structure de Données

### Collection `sondages`

```json
{
  "_id": ObjectId("5f3a3c1c1234567890123456"),
  "nom": "Sondage Préférences Alimentaires",
  "createur": ObjectId("5f3a3c1b1234567890123456"),
  "questions": [
    {
      "_id": ObjectId("5f3a3c1d1234567890123456"),
      "intitule": "Quel est votre plat préféré ?",
      "type": "ouverte"
    },
    {
      "_id": ObjectId("5f3a3c1e1234567890123456"),
      "intitule": "Quels types de cuisine préférez-vous ?",
      "type": "qcm",
      "reponses": ["Italienne", "Chinoise", "Mexicaine", "Indienne"]
    }
  ]
}
```

### Collection `reponses`

```json
{
  "sondage_id": ObjectId("5f3a3c1c1234567890123456"),
  "utilisateur_id": ObjectId("5f3a3c1d1234567890123456"),
  "reponses": [
    {
      "question_id": ObjectId("5f3a3c1d1234567890123456"),
      "reponse": "Pizza"
    },
    {
      "question_id": ObjectId("5f3a3e1f1234567890123456"),
      "reponse": ["Italienne", "Indienne"]
    }
  ]
}
```

## Consignes pour l'Exercice

### Modélisation des Données :

- Définissez la structure des documents pour les collections sondages et reponses.
- Assurez-vous que les sondages peuvent être facilement mis à jour et que les réponses peuvent être associées de manière unique à la fois au sondage et à l'utilisateur.

### Développement de l'Application:

- Le framework est libre, vous utiliserez le langage de programmation de votre choix ainsi que le framework qui vous convient le plus
- Une documentation vous est demandée sur le projet.

### Stockage et Récupération des Données :

- Utilisez MongoDB pour stocker les sondages et les réponses.
Assurez-vous de gérer correctement les identifiants uniques et les références entre les collections.

### Sécurité et Permissions :

- Mettez en place une authentification pour identifier les créateurs de sondages et les utilisateurs répondant aux sondages.
- Assurez-vous que seuls les créateurs puissent modifier ou supprimer leurs sondages.

## Livrable

- le github du projet.
- Un script pour initialiser la base de données avec des données de test.
