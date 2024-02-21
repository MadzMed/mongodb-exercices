# Exercice de Création d'une Mini Application de Commande de Sandwichs

## Objectif

Développer une mini application en ligne de commande qui permet aux utilisateurs de composer un sandwich selon leurs préférences en choisissant les ingrédients et la sauce. L'application devra ensuite enregistrer la commande dans une base de données et offrir des options pour visualiser le chiffre d'affaires total et quitter le programme.

## Fonctionnalités

1. **Menu Principal :** L'application affichera un menu principal avec les options suivantes :
   - Nouvelle commande
   - Voir le chiffre d'affaires
   - Quitter

2. **Création de Commande :**
   - L'utilisateur pourra choisir parmi une liste d'ingrédients disponibles pour composer son sandwich.
   - L'utilisateur choisira ensuite une sauce parmi les options disponibles.
   - Une fois la commande complétée, elle sera enregistrée dans une base de données.

3. **Calcul du Chiffre d'Affaires :**
   - L'application calculera et affichera le chiffre d'affaires total basé sur les commandes enregistrées.

4. **Quitter :**
   - L'option pour quitter l'application.

## Considérations Techniques

- **Langage de Programmation :** L'application peut être développée dans le langage de programmation choisi par l'étudiant (par exemple, Python, JavaScript/Node.js, etc.).
- **Base de Données :** Utiliser une base de données simple comme SQLite pour les débutants ou MongoDB pour ceux qui veulent plus de défi.
- **Interface Utilisateur :** L'interaction avec l'application se fera via le terminal ou la ligne de commande.

## Exemple de Pseudo-Code

```plaintext
Afficher le Menu Principal
Si l'utilisateur choisit "Nouvelle commande"
   Afficher les options d'ingrédients
   Laisser l'utilisateur choisir les ingrédients
   Afficher les options de sauce
   Laisser l'utilisateur choisir une sauce
   Enregistrer la commande dans la base de données
   Afficher un message de confirmation
Si l'utilisateur choisit "Voir le chiffre d'affaires"
   Calculer le total des ventes à partir des commandes enregistrées
   Afficher le chiffre d'affaires
Si l'utilisateur choisit "Quitter"
   Fermer l'application
```