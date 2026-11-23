# Cas de test — Reconnaissance vocale (Speech-to-Text)

Utiliser uniquement des enregistrements de test non sensibles et des langues prises en charge.

| ID | Scénario | Étapes | Résultat attendu |
|---|---|---|---|
| STT-001 | Phrase courte en environnement calme | Autoriser le micro, prononcer la phrase de référence | Transcription conforme au niveau attendu |
| STT-002 | Débit lent puis rapide | Répéter le texte à deux débits | Transcription exploitable dans les deux cas |
| STT-003 | Ponctuation | Dicter une phrase avec pauses et ponctuation | Ponctuation cohérente ou possibilité de correction |
| STT-004 | Silence | Démarrer puis garder le silence | Fin/absence de parole gérée clairement |
| STT-005 | Permission microphone refusée | Refuser la permission | Explication et indication pour rétablir l'accès |
| STT-006 | Microphone indisponible | Désactiver ou rendre indisponible le micro | Message explicite, pas de blocage |
| STT-007 | Environnement bruité | Utiliser un échantillon avec bruit contrôlé | Limites compréhensibles, transcription non trompeuse |
| STT-008 | Interruption d'enregistrement | Arrêter pendant la capture | État cohérent et résultat conforme au comportement attendu |
| STT-009 | Perte réseau | Couper le réseau pendant traitement | Erreur récupérable ou reprise clairement indiquée |
| STT-010 | Correction de transcription | Modifier le texte transcrit | Modifications conservées pour l'étape suivante |

## Mesure de qualité

Comparer la transcription à une référence validée. Noter les mots substitués, supprimés ou ajoutés. Si un taux d'erreur de mots (WER) est calculé, préciser la méthode de normalisation et le jeu d'échantillons ; ne pas comparer des scores issus de corpus différents.

## Fiche d'exécution

- Date / heure :
- Environnement / appareil :
- Langue / accent (description non identifiante) :
- ID du cas :
- Résultat : PASS / FAIL / BLOCKED / NOT RUN
- Transcription attendue :
- Transcription observée :
- Écarts constatés :
- Preuve anonymisée :
