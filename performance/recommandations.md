# Vérifications de performance et de résilience

## Objectif

Collecter des mesures reproductibles sur les opérations principales sans provoquer de charge excessive sur l'environnement de démonstration.

## Mesures à relever

| Opération | Mesure | Point de départ | Point de fin |
|---|---|---|---|
| Chargement initial | Temps de chargement | Navigation/actualisation | Interface utilisable |
| Traduction | Durée de traitement | Soumission | Résultat affiché |
| Reconnaissance vocale | Durée de traitement | Fin de capture | Transcription affichée |
| Génération audio | Délai avant disponibilité | Demande | Audio prêt |
| Lecture audio | Délai de démarrage | Clic lecture | Son effectivement démarré |

Ne pas fixer de seuil arbitraire : convenir des objectifs avec l'équipe produit selon les usages et les contraintes techniques.

## Scénarios de résilience

1. Réseau normal : exécuter chaque opération plusieurs fois avec les mêmes données de test.
2. Réseau lent : observer les indicateurs de progression et les délais.
3. Interruption réseau : vérifier le message d'erreur et la possibilité de reprise.
4. Requête répétée : vérifier qu'un clic répété ne crée pas d'actions multiples involontaires.
5. Session prolongée : vérifier que l'interface reste utilisable après une période d'inactivité.

## Tableau de relevé

| Date | Opération | Réseau | Tentative | Durée (s) | Résultat |
|---|---|---|---:|---:|---|
| À compléter | À compléter | À compléter | 1 | À mesurer | À compléter |

## Précautions

- Obtenir l'accord de l'équipe avant tout test de charge.
- Limiter les répétitions sur une démo publique.
- Distinguer temps réseau, temps de traitement et temps de rendu lorsque les outils le permettent.
- Indiquer l'appareil, le navigateur, la taille du contenu et le type de réseau.
- Ne pas publier de journaux contenant des textes utilisateurs ou des données sensibles.
