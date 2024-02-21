# Exercice MongoDB : Manipulation et Agrégation de Données de Commandes

Cet exercice vous guidera à travers le processus d'insertion de données de commandes dans MongoDB, la réalisation d'agrégations pour analyser ces données, puis l'utilisation de jointures pour intégrer des informations depuis une collection de clients. Vous travaillerez avec deux collections : `commandes` pour les détails des commandes et `clients` pour les informations sur les clients.

## Objectif

L'objectif est de pratiquer l'insertion de données, les agrégations basiques et avancées, ainsi que les jointures entre collections dans MongoDB.

## Partie 1: Insertion des Données de Commandes

### Instructions

1. Créez une nouvelle collection nommée `commandes`.
2. Insérez les données des commandes fournies dans la collection `commandes`.

## Partie 2: Agrégations Classiques

Effectuez des opérations d'agrégation basiques sur la collection `commandes`.

### Instructions

1. Calculez le montant total des ventes.
2. Trouvez le nombre moyen de produits par commande.
3. Déterminez le montant maximum d'une commande.

## Partie 3: Jointure avec la Collection Clients

Réalisez une jointure entre les collections `commandes` et `clients` pour enrichir les données des commandes avec les informations des clients.

### Instructions

1. Utilisez l'opération `$lookup` pour joindre les collections `commandes` et `clients` sur le champ `idClient`.
2. Affichez le nom du client avec le détail de chaque commande.

## Partie 4: Agrégations Plus Complexes

Après avoir joint les collections, effectuez des agrégations plus complexes pour obtenir des insights approfondis.

### Instructions

1. Calculez le montant total des commandes par client.
2. Identifiez le produit le plus vendu.
3. Trouvez le client ayant effectué le plus grand nombre de commandes.
4. Trouvez le client ayant commandé le plus grand nombre de produits.

## Conclusion

Cet exercice vous aidera à maîtriser les techniques d'insertion de données, d'agrégation et de jointure dans MongoDB. Il vous fournira également des insights précieux sur la manipulation et l'analyse de données de ventes complexes.
