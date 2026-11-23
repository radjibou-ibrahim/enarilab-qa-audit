# Audit QA préliminaire — EnariLab

## 1. Synthèse

La première découverte d'EnariLab fait ressortir cinq domaines qui méritent une validation QA structurée : traduction, reconnaissance vocale, génération audio, performance et expérience mobile.

L'objectif de cette revue est d'aider l'équipe à réduire les risques avant une diffusion plus large, en transformant ces axes en scénarios testables et en critères d'acceptation.

## 2. Périmètre

- Compréhension et cohérence du parcours de traduction.
- Capture et transcription de la voix.
- Génération, lancement et écoute de contenus audio.
- Réactivité de l'application et comportement en cas d'attente ou d'échec.
- Adaptation de l'interface aux écrans mobiles.

## 3. Premiers risques à investiguer

### 3.1 Fiabilité des traductions
Une traduction peut être grammaticalement correcte tout en altérant le sens, le registre, les noms propres ou les expressions idiomatiques. Les contenus longs peuvent également présenter des omissions ou des inversions de sens.

**À vérifier :** fidélité au texte source, complétude, cohérence terminologique, respect de la langue cible et comportement sur les textes longs.

### 3.2 Reconnaissance vocale
La qualité de transcription peut varier selon l'accent, le débit, le bruit ambiant, la durée de l'enregistrement et la langue parlée.

**À vérifier :** exactitude, ponctuation, mots difficiles, silence, bruit, interruption, permission du microphone et retour d'erreur.

### 3.3 Génération audio
L'audio généré doit correspondre au texte attendu et être exploitable par l'utilisateur.

**À vérifier :** correspondance texte/audio, démarrage, pause/reprise, fin de lecture, qualité sonore, gestion des erreurs et possibilité de relancer une génération.

### 3.4 Performance et stabilité
Les traitements vocaux et de traduction peuvent entraîner des temps d'attente importants ou des erreurs réseau.

**À vérifier :** temps de chargement, délai de réponse, indicateurs de progression, comportement en réseau instable, prévention des soumissions multiples et récupération après échec.

### 3.5 Expérience mobile
Les parcours doivent rester compréhensibles et utilisables sur des écrans de petite taille.

**À vérifier :** débordements, lisibilité, taille des zones tactiles, clavier virtuel, orientation, défilement, affichage des états et contrôles audio.

## 4. Évaluation actuelle

| Domaine | État de l'évaluation | Suite nécessaire |
|---|---|---|
| Traduction | Axe de risque identifié | Exécuter les cas de test |
| Reconnaissance vocale | Axe de risque identifié | Tester plusieurs conditions audio |
| Génération audio | Axe de risque identifié | Tester lecture et correspondance |
| Performance | À mesurer | Collecter des mesures reproductibles |
| Mobile | À valider sur appareils | Exécuter les parcours sur mobile |

Aucun taux de réussite, niveau de sévérité ou nombre de bugs n'est attribué sans exécution documentée.

## 5. Informations à confirmer avec l'équipe

- Liste des langues et variantes linguistiques prises en charge.
- Limites de longueur des textes et des enregistrements.
- Formats audio acceptés et produits.
- Navigateurs et appareils officiellement supportés.
- Comportement attendu en cas de perte de connexion.
- Exigences de performance et volumes d'utilisation visés.

## 6. Conclusion

Les premiers axes justifient une campagne de tests fonctionnels ciblée. La prochaine étape consiste à exécuter les scénarios, collecter les résultats et distinguer les défauts reproductibles des améliorations ergonomiques ou techniques proposées.
