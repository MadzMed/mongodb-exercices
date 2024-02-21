# Exercice Avancé sur la Base de Données Pokémon GO

Cet exercice propose une série de tâches pour explorer les fonctionnalités avancées de MongoDB, en utilisant la collection Pokémon GO. Les étapes couvrent l'ajout de données, l'agrégation de statistiques, et l'analyse de documents.

## Étape 1: Ajout de Statistiques Aléatoires

Votre première tâche consiste à enrichir chaque document Pokémon avec des statistiques d'attaque et de défense générées aléatoirement.

### Instructions

- Parcourez chaque document de la collection `pokemonGO`.
- Générez des statistiques aléatoires pour l'attaque et la défense (valeurs entre 1 et 100).
- Mettez à jour chaque Pokémon avec ces nouvelles statistiques sous un objet `stats`.

## Étape 2: Agrégation des Statistiques HP et CP

Effectuez une analyse détaillée des Points de Vie (HP) et des Points de Combat (CP) des Pokémon.

### Instructions

- Calculez la moyenne des HP et des CP pour l'ensemble des Pokémon.
- Calculez la moyenne des HP et des CP par type.
- Déterminez le Pokémon ayant le HP et le CP les plus élevés.

## Étape 3: Lecture de Données sur les Documents

Exécutez des requêtes pour extraire des informations ciblées de votre collection.

### Instructions

- Identifiez tous les Pokémon avec plus de 50 d'attaques.
- Sélectionnez les Pokémon avec un CP supérieur à la moyenne des CP.

## Étape 4: Agrégation des Statistiques par Type

Analysez les statistiques d'attaque et de défense, en les regroupant par type de Pokémon.

### Instructions

- Calculez la moyenne des statistiques d'attaque et de défense pour chaque Pokémon.
- Comparez les statistiques moyennes d'attaque et de défense de chaque Pokémon groupé par type.

Cet exercice met en lumière la puissance des opérations CRUD, des fonctions d'agrégation et des requêtes sur documents imbriqués dans MongoDB. Il offre une occasion d'appliquer ces concepts à un ensemble de données ludique et engageant.
