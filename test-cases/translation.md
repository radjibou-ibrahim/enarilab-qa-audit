# Cas de test — Traduction

Les scénarios ci-dessous sont à exécuter uniquement pour les langues annoncées comme supportées. Compléter les résultats après exécution.

| ID | Scénario | Étapes | Résultat attendu |
|---|---|---|---|
| TR-001 | Traduction d'une phrase simple | Choisir source/cible, saisir une phrase, lancer | Traduction dans la langue cible, sens conservé |
| TR-002 | Texte vide | Soumettre sans texte | Validation explicite, aucun résultat trompeur |
| TR-003 | Texte long | Soumettre un texte long dans les limites annoncées | Traitement complet ou limite clairement signalée |
| TR-004 | Noms propres et nombres | Soumettre un texte avec noms, dates et nombres | Éléments critiques conservés |
| TR-005 | Ponctuation et caractères spéciaux | Soumettre accents, apostrophes, guillemets et ponctuation | Caractères correctement traités |
| TR-006 | Expression idiomatique | Soumettre une expression contextualisée | Sens global préservé |
| TR-007 | Langue non prise en charge | Choisir/soumettre une langue non supportée si possible | Message clair, pas de traduction présentée comme fiable |
| TR-008 | Changement de langue cible | Modifier la cible puis relancer | Résultat correspondant à la nouvelle cible |
| TR-009 | Erreur réseau | Interrompre le réseau pendant le traitement | Erreur explicite et possibilité de réessayer |
| TR-010 | Double soumission | Cliquer plusieurs fois rapidement sur lancer | Pas de traitements dupliqués involontaires |

## Fiche d'exécution

- Date / heure :
- Environnement :
- Langue source / cible :
- ID du cas :
- Résultat : PASS / FAIL / BLOCKED / NOT RUN
- Résultat observé :
- Preuve (référence anonymisée) :
- Commentaire :
