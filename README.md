# EnariLab — Audit QA fonctionnel préliminaire

**Projet évalué :** EnariLab — démonstration accessible à l'adresse http://demo.enarilab.xyz/  
**Type de mission :** revue exploratoire et recommandations QA  
**Auteur :** Radjibou Ibrahim — Consultant QA  
**Statut :** audit préliminaire — à compléter par des tests reproductibles

## Contexte et portée

Cette documentation formalise les premiers axes d'attention relevés lors d'une découverte exploratoire de la plateforme. Les domaines retenus sont :

- fiabilité des traductions ;
- reconnaissance vocale (Speech-to-Text) ;
- génération audio / synthèse vocale (Text-to-Speech) ;
- performances et stabilité ;
- expérience utilisateur sur mobile.

**Important :** ce dépôt présente des risques à investiguer, des recommandations et une stratégie de validation. À ce stade, les axes mentionnés ne doivent pas être interprétés comme des bugs confirmés. Aucun défaut n'est déclaré reproductible sans scénario exécuté, résultat observé et preuve associée.

## Arborescence

- `docs/audit-preliminaire.md` — synthèse, périmètre et limites de l'analyse ;
- `docs/recommandations.md` — pistes d'amélioration priorisées ;
- `test-plan/plan-de-test.md` — stratégie et conditions de test ;
- `test-cases/translation.md` — scénarios de traduction ;
- `test-cases/speech-to-text.md` — scénarios de reconnaissance vocale ;
- `test-cases/text-to-speech.md` — scénarios de génération audio ;
- `bug-reports/README.md` — modèle de rapport d'anomalie ;
- `performance/recommandations.md` — contrôles de performance ;
- `evidence/README.md` — règles de collecte des preuves.

## Priorités proposées

| Priorité | Domaine | Objectif |
|---|---|---|
| P1 | Traduction | Vérifier fidélité, sens, langue et stabilité |
| P1 | Reconnaissance vocale | Vérifier transcription, langues et conditions audio |
| P1 | Génération audio | Vérifier lecture, qualité, cohérence et erreurs |
| P2 | Mobile | Vérifier lisibilité, commandes et parcours tactiles |
| P2 | Performance | Mesurer temps de réponse, chargement et stabilité |

Les priorités sont des propositions de planification QA, pas une mesure de sévérité de bugs confirmés.

## Méthode

1. Définir l'environnement, le navigateur, l'appareil et la date.
2. Exécuter les scénarios documentés dans `test-cases/`.
3. Consigner chaque résultat : Pass, Fail, Blocked ou Not Run.
4. Reproduire tout échec et joindre des preuves anonymisées.
5. Créer un rapport dans `bug-reports/` uniquement lorsqu'un défaut est observé.
6. Rejouer les tests après correction (tests de confirmation et de régression).

## Limites

Les recommandations devront être affinées après accès aux parcours complets, aux langues prises en charge, aux formats audio, aux règles métier et aux environnements techniques du produit. Les tests ne doivent pas utiliser de données personnelles ou de contenus confidentiels sans autorisation.

## Contact

**Radjibou Ibrahim** — Consultant QA  
GitHub : https://github.com/radjibou-ibrahim
