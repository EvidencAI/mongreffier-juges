# Structure du jugement

## Table des matières
1. Structure générale
2. Format des motifs
3. Format du dispositif (PCM)
4. Checklist validation
5. Erreurs interdites

---

## 1. Structure générale

| Section | Obligatoire | Contenu |
|---------|-------------|---------|
| EN-TÊTE | ✅ | Tribunal, type jugement, RG, date audience, composition du délibéré (président, assesseurs), greffier |
| PARTIES | ✅ | Dénomination, forme, capital, RCS, siège, activité, représentation |
| FAITS | ✅ | Chronologie + renvois pièces |
| ÉLÉMENTS DE PROCÉDURE | ✅ | Assignation, ordonnances. Clôture : "C'est en l'état..." |
| PRÉTENTIONS | ✅ | Reprise VERBATIM des conclusions. Aucune analyse. |
| MOTIFS | ✅ | Format syllogistique STRICT (voir §2) |
| PAR CES MOTIFS | ✅ | Format PCM STRICT (voir §3) |

**Important** : Ne pas utiliser "Exposé du litige". Séparer en FAITS + ÉLÉMENTS DE PROCÉDURE.

---

## 2. Format des motifs

Pour **CHAQUE** chef de prétention :

```
Sur [intitulé du chef] :

[Majeure : la règle citée, ouverte directement par elle : "Aux termes de l'article X…"]

[Mineure : application aux faits + renvois pièces, entrée variée : "Il ressort de la pièce n° 3 du demandeur…", "En l'occurrence,", "Or,"]

[Conclusion : une phrase ouverte par un mot de liaison varié ("Dès lors,", "Il s'ensuit que", "En conséquence,", "Le tribunal en déduit que") - position validée en Phase 2]
```

**Règles :**
- Jamais de texte libre sans cette structure
- Toujours citer les pièces : `(pièce n°X du demandeur/défendeur)`
- Pas de "Attendu que"
- Style direct

---

## 3. Format du dispositif (PCM)

### 3.1 Formule introductive

```
[Juridiction de la fiche du dossier], après en avoir délibéré 
conformément à la loi, statuant par jugement [contradictoire / réputé 
contradictoire / par défaut] et en [premier / dernier] ressort, prononcé 
publiquement par mise à disposition au greffe, les parties ayant été 
préalablement avisées dans les conditions prévues au deuxième alinéa 
de l'article 450 du Code de procédure civile ;
```

→ **Point-virgule** à la fin (pas virgule, pas point)

### 3.2 Visa des textes

```
*Vu* les articles [X] du Code civil, [Y] du Code de procédure civile ;
```

→ *Vu* en **italique**
→ **Point-virgule** à la fin

### 3.3 Chefs de dispositif

```
DÉBOUTE la société X de ses demandes ;
CONDAMNE la société Y à payer... ;
CONDAMNE la société Y aux dépens.
```

| Élément | Règle |
|---------|-------|
| Verbes | **MAJUSCULES** : DÉBOUTE, CONDAMNE, DIT, ORDONNE, REJETTE, DÉCLARE |
| Séparateurs | **Point-virgule** après chaque chef |
| Dernier chef | **Point final** (pas point-virgule) |
| Exécution provisoire | **SILENCE** (de droit), ni dans les motifs ni dans le dispositif. Mentionner seulement si demande d'écartement. |

---

## 4. Checklist validation

Avant de générer le .docx, **vérifier** :

```
✅ Structure syllogistique : règle de droit, application aux faits, conclusion ouverte par un mot de liaison (sans étiquette ni intertitre : ni "Cadre juridique", ni "En l'espèce", ni "Le tribunal retient"), jamais deux motifs consécutifs ouverts par la même entrée
✅ Renvois aux pièces présents dans chaque application aux faits
✅ Sections : FAITS + ÉLÉMENTS DE PROCÉDURE (pas "Exposé du litige")
✅ PCM : formule art. 450 complète + point-virgule
✅ PCM : Vu en italique
✅ PCM : verbes MAJUSCULES
✅ PCM : points-virgules entre chefs, point final au dernier
✅ Pas de mention exécution provisoire, ni dans les motifs ni dans le dispositif (sauf écartement demandé)
✅ Tous les chefs de demande traités (pas d'omission de statuer) : toute demande non accueillie en entier a son « déboute du surplus » ou son rejet
✅ Cohérence montants entre motifs et dispositif
```

→ **Si une ligne ne peut être cochée, CORRIGER avant génération.**

---

## 5. Erreurs interdites

| ❌ INTERDIT | ✅ CORRECT |
|-------------|-----------|
| "Exposé du litige" | "FAITS" + "ÉLÉMENTS DE PROCÉDURE" |
| Motifs en texte libre | Structure : règle de droit → application aux faits → conclusion (sans étiquettes) |
| Intertitres "Cadre juridique :" et "En l'espèce :" en tête de paragraphe | Ouvrir la majeure directement par la règle : "Aux termes de l'article…" ; varier la mineure : "Il ressort de la pièce n° 3…", "En l'occurrence,", "Or," |
| Pas de renvoi aux pièces | "(pièce n°X du demandeur)" systématique |
| "Vu" en romain | *Vu* en italique |
| Verbes minuscules | VERBES MAJUSCULES |
| Point après chaque chef | Point-virgule (sauf dernier) |
| Mention exécution provisoire, motifs ou dispositif | Silence (sauf écartement demandé) |
| "Attendu que" | Style direct |

---

## Qualification de la décision (art. 473 CPC)

Qualification (art. 473 et 474 CPC) : lire les articles par `verifier_article` et en tirer la qualification ; le motif cite le texte lu.

**Ressort** : seuil de l'art. R.721-6 C. com., lu par `verifier_article`, appliqué au total des demandes.
