# 📘 Fiche Projet Pédagogique – Système de Journalisation Sécurisée

## 🎯 Objectifs pédagogiques
- Comprendre les concepts de journalisation (logging) dans un contexte de cybersécurité.
- Utiliser MongoDB pour stocker et structurer des logs de sécurité.
- Appliquer des techniques de protection de l'intégrité des logs (hachage, horodatage).
- Concevoir un petit système de détection d'anomalies à partir de requêtes sur les logs.

## 🧠 Compétences mobilisées
- Stockage NoSQL avec MongoDB.
- Programmation (Python, Node.js ou autre langage supporté).
- Cryptographie (SHA256, HMAC, etc.).
- Analyse de données de sécurité.
- Sécurisation des bases de données (authentification, droits d’accès).

## 🛠 Technologies recommandées
- MongoDB (avec MongoDB Atlas ou en local).
- Langage : Python (ou Node.js).
- Librairies : `pymongo`, `hashlib`, `datetime`, `flask` (optionnel pour une API).

## 📁 Structure du projet

### 1. Ingestion des logs
- Générer ou récupérer des logs (ex. : tentatives de connexions, erreurs systèmes).
- Structurer les logs au format JSON :

```json
{
  "timestamp": "2025-04-03T15:32:00Z",
  "ip": "192.168.1.12",
  "user": "admin",
  "action": "login_attempt",
  "status": "failed"
}
```

### 2. Stockage sécurisé dans MongoDB
- Connexion à MongoDB.
- Insertion des logs dans une collection.
- Ajout d’un champ `log_hash` pour garantir l’intégrité :

```json
"log_hash": "SHA256(timestamp + ip + user + action + status)"
```

- Exemple de document final inséré dans MongoDB :

```json
{
  "timestamp": "2025-04-03T15:32:00Z",
  "ip": "192.168.1.12",
  "user": "admin",
  "action": "login_attempt",
  "status": "failed",
  "log_hash": "e3b0c44298fc1c149afbf4c8996fb924..."
}
```

### 3. Interface ou API simple (optionnel)

- Créer une interface Web ou API REST pour visualiser les logs.

- Permettre des recherches :

    - Par date

    - Par utilisateur

    - Par adresse IP

    - Par action ou statut

### 4. Détection d’anomalies

- Implémenter un script d’analyse des comportements suspects :

    - IPs avec plus de 5 échecs de connexion en moins de 10 minutes.

    - Connexions depuis des plages IP inconnues.

    - Tentatives d’accès à des heures inhabituelles.

- Exemple de requête MongoDB pour détection :

```python
collection.aggregate([
  { "$match": { "status": "failed" } },
  { "$group": {
      "_id": { "ip": "$ip", "minute": { "$substr": ["$timestamp", 0, 16] } },
      "count": { "$sum": 1 }
  }},
  { "$match": { "count": { "$gt": 5 } } }
])
```

### 5. Audit et sécurité

- Configurer MongoDB avec authentification (utilisateurs et rôles).

- Restreindre les droits d’accès en lecture/écriture.

- Activer la journalisation des accès.

- Mettre en place des sauvegardes régulières de la base :

    - Utiliser mongodump pour exporter les données.

    - Documenter le processus de restauration

### ✅ Livrables attendus

- Code source du système de logging.

- Base MongoDB fonctionnelle avec données de test.

- Script de vérification de l’intégrité des logs.

- Rapport de projet :

    - Architecture choisie

    - Justification des choix techniques

    - Requêtes utilisées pour l’analyse

    - Propositions d’amélioration ou d’extension