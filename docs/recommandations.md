# Pistes d'amélioration QA — EnariLab

Ces propositions découlent des premiers axes d'attention identifiés pendant la découverte du produit. Elles constituent des recommandations à discuter avec l'équipe et non des constats de défauts déjà confirmés.

## P1 — Fiabilité des traductions

**Risques à couvrir**
- Perte ou modification du sens.
- Omission de phrases ou de segments.
- Traduction incohérente des termes récurrents.
- Mauvaise gestion des textes longs, caractères spéciaux et ponctuation.

**Recommandations**
1. Constituer un jeu de textes de référence validés par des locuteurs compétents pour chaque paire de langues prioritaire.
2. Tester des textes courts, longs, techniques, conversationnels et contenant des expressions idiomatiques.
3. Vérifier la conservation des noms propres, nombres, dates, citations et éléments de mise en forme.
4. Afficher clairement la langue source et la langue cible et permettre à l'utilisateur de les corriger avant traitement.
5. Prévoir un message explicite en cas de langue non reconnue, de texte vide ou de traitement échoué.
6. Éviter de présenter une traduction incertaine comme certaine ; permettre à l'utilisateur de signaler une traduction problématique.

**Critères d'acceptation proposés**
- Le contenu retourné correspond à la langue cible choisie.
- Aucun segment du texte source n'est omis sans indication.
- Les noms, nombres et éléments critiques sont conservés conformément au résultat de référence.
- Les erreurs sont signalées sans effacer silencieusement la saisie.

## P1 — Reconnaissance vocale (Speech-to-Text)

**Risques à couvrir**
- Transcription inexacte selon l'accent, le débit ou le bruit.
- Microphone non autorisé ou indisponible.
- Enregistrement bloqué, interrompu ou vide.

**Recommandations**
1. Tester chaque langue prise en charge avec plusieurs locuteurs et niveaux de débit.
2. Constituer des échantillons de référence avec transcription attendue.
3. Couvrir les environnements silencieux et bruyants, les silences et les enregistrements courts/longs.
4. Afficher distinctement les états : prêt, enregistrement, traitement, terminé et échec.
5. Demander la permission du microphone au moment utile et expliquer comment la réactiver.
6. Permettre de relire et corriger la transcription avant de la réutiliser.
7. Prévoir une récupération claire en cas de coupure réseau ou d'interruption.

**Critères d'acceptation proposés**
- L'utilisateur sait quand l'enregistrement est actif.
- Une permission refusée produit une explication et une alternative.
- Le texte transcrit peut être vérifié et corrigé.
- Un échec ne provoque ni blocage permanent ni perte silencieuse du contenu.

## P1 — Génération audio (Text-to-Speech)

**Risques à couvrir**
- Audio absent, incomplet ou interrompu.
- Prononciation incorrecte ou voix/langue inattendue.
- Commandes de lecture peu compréhensibles.

**Recommandations**
1. Vérifier la correspondance entre texte soumis et contenu prononcé.
2. Tester ponctuation, nombres, abréviations, noms propres et textes multilingues.
3. Rendre visibles les états de génération et de lecture.
4. Fournir des commandes accessibles de lecture, pause, reprise et relance.
5. Gérer explicitement les erreurs de génération et les fichiers audio indisponibles.
6. Vérifier le comportement lorsque l'utilisateur quitte la page ou change d'onglet, selon le comportement attendu du produit.

**Critères d'acceptation proposés**
- L'audio correspond au texte et à la langue demandés.
- Les commandes réagissent une seule fois à chaque action utilisateur.
- L'utilisateur reçoit un retour en cas d'échec et peut réessayer.

## P2 — Expérience utilisateur mobile

**Recommandations**
1. Vérifier l'absence de défilement horizontal non souhaité.
2. Garantir la lisibilité des libellés, résultats et messages d'erreur.
3. Prévoir des zones tactiles suffisamment grandes et espacées.
4. Vérifier que le clavier virtuel ne masque pas le champ actif ni le bouton principal.
5. Contrôler les parcours en portrait et en paysage.
6. Conserver les saisies en cas d'erreur récupérable, lorsque cela est possible.
7. Rendre les états de chargement, succès et échec immédiatement compréhensibles.

## P2 — Performance et résilience

**Recommandations**
1. Mesurer séparément le chargement initial, la traduction, la transcription et la génération audio.
2. Définir avec l'équipe des objectifs de temps de réponse réalistes par opération.
3. Afficher un indicateur de progression pour les traitements longs.
4. Empêcher les soumissions répétées involontaires.
5. Tester les réseaux lents, les pertes de connexion et les délais dépassés.
6. Vérifier la récupération après échec sans perte de données saisies.
7. Surveiller les erreurs côté client et serveur avec des journaux qui excluent les contenus personnels.

## Ordre de mise en œuvre suggéré

1. Stabiliser et valider les parcours principaux (traduction, transcription, génération audio).
2. Améliorer la gestion des erreurs et la récupération.
3. Vérifier l'utilisabilité mobile.
4. Mesurer les performances sur des conditions réseau représentatives.
5. Mettre en place une non-régression à chaque évolution.

## Limite

Les priorités P1/P2 sont des priorités de couverture QA proposées. Elles ne constituent pas une classification de bugs observés.
