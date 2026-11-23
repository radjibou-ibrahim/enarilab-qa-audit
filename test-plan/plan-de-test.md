# Plan de test fonctionnel — EnariLab

## 1. Objectif

Valider les parcours de traduction, reconnaissance vocale et génération audio, puis examiner la performance et l'utilisabilité mobile.

## 2. Périmètre de test

**Inclus**
- Entrées valides et invalides.
- Langues et formats annoncés comme pris en charge.
- États de chargement, réussite et échec.
- Contrôles audio.
- Adaptation mobile et résilience réseau.

**Hors périmètre sans accord explicite**
- Tests de charge importants sur le service public.
- Tests de sécurité intrusifs, fuzzing ou scans automatisés.
- Tests impliquant des données personnelles ou des comptes tiers.

## 3. Préconditions

- Autorisation appropriée pour les tests envisagés.
- Compte de test si nécessaire.
- Navigateur et appareil identifiés.
- Langues officiellement supportées connues.
- Échantillons de texte et audio non sensibles.
- Connexion réseau documentée.

## 4. Environnements à consigner

Pour chaque exécution, noter :
- Date et heure avec fuseau.
- Appareil, système et version.
- Navigateur et version.
- Taille/orientation de l'écran.
- Type de réseau (Wi-Fi, mobile, réseau simulé).
- Compte et rôle de test, sans publier de secret.

## 5. Types de tests

- Tests fonctionnels : résultat conforme au besoin.
- Tests négatifs : saisie vide, permission refusée, langue non prise en charge.
- Tests exploratoires : parcours libre avec prise de notes.
- Tests de compatibilité : navigateurs et tailles d'écran ciblés.
- Tests de résilience : interruption réseau et reprise.
- Tests de performance légers : mesures individuelles, sans générer de trafic excessif.

## 6. Critères d'entrée

- Parcours accessible et environnement disponible.
- Exigences ou comportements attendus clarifiés.
- Données de test prêtes.
- Périmètre autorisé défini.

## 7. Critères de sortie proposés

- Tous les cas prioritaires exécutés ou leur blocage documenté.
- Chaque échec reproductible dispose d'un rapport et de preuves.
- Les résultats sont communiqués avec les limites connues.
- Les tests de confirmation et de régression sont planifiés après correction.

## 8. Statuts

- **PASS** : résultat conforme au résultat attendu.
- **FAIL** : écart reproductible entre résultat observé et attendu.
- **BLOCKED** : exécution impossible pour une raison identifiée.
- **NOT RUN** : test non exécuté.

## 9. Précautions

Respecter les conditions d'utilisation, limiter la fréquence des requêtes, ne pas tenter d'accéder à des données d'autrui et ne pas publier de captures contenant des informations personnelles, jetons ou secrets.
