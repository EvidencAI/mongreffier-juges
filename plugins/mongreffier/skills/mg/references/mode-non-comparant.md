# Mode Non-Comparant (art. 472 CPC)

## Déclencheur

Ce mode simplifié s'applique lorsque :
- Le défendeur a été régulièrement assigné
- Le défendeur n'a pas constitué avocat / n'a pas comparu
- Pas de demande reconventionnelle à traiter

## Principe directeur

**Article 472 CPC, alinéas 1 et 2** : « Si le défendeur ne comparaît pas, il est néanmoins statué sur le fond. Le juge ne fait droit à la demande que dans la mesure où il l'estime régulière, recevable et bien fondée. »

→ Le juge n'est pas lié par les demandes : il doit les vérifier.

### Aiguillage obligatoire : date d'introduction de l'instance

Le décret n° 2026-683 du 27/07/2026 (article 7) a ajouté à l'article 472 trois alinéas, en vigueur le 01/10/2026. Son article 21, 2°, b) les réserve aux **instances introduites à compter du 01/10/2026** (vérifié sur Légifrance le 12/10/2026). Ce qui compte est l'introduction de l'instance, jamais la date du jugement.

Alinéa 3, texte exact : « Lorsque l'acte introductif d'instance a été délivré à personne, le juge peut, en première instance, sauf si le demandeur s'y oppose, faire droit à la demande, dès lors qu'elle est recevable et qu'elle n'est contraire ni à l'ordre public, ni à une liberté protégée, ni à un droit fondamental. »
Alinéa 4 : « Les dispositions du troisième alinéa ne sont pas applicables lorsque le juge est tenu de motiver spécialement sa décision ou de relever un moyen d'office. »
Alinéa 5 : l'alinéa 3 ne vaut que devant les juridictions judiciaires statuant en matière civile et commerciale.

**Date retenue : la délivrance de l'assignation.** La demande en justice est formée par l'assignation (art. 54 et 750 CPC) ; en ce sens, Cass. 1re civ., 18/05/2011, n° 10-17.943 (instance introduite par la délivrance de l'assignation, en matière de divorce). Ni le décret ni sa circulaire du 29/07/2026 ne tranchent. Relever aussi la date de remise au greffe (art. 857 CPC, saisine du tribunal) : si elle tombe de l'autre côté du 01/10/2026 (délivrée avant, remise au greffe après), le signaler au juge en une ligne, la remise au greffe pouvant être soutenue comme date d'introduction.

| Assignation délivrée | Acte délivré | Régime |
|---|---|---|
| Avant le 01/10/2026 | Peu importe | Alinéas 1 et 2 seuls : contrôle complet, régularité, recevabilité **et bien-fondé sur pièces** |
| Depuis le 01/10/2026 | Autrement qu'à personne | Même contrôle complet |
| Depuis le 01/10/2026 | **À personne** | Alinéa 3 possible, dans ses termes exacts ci-dessus, sauf alinéa 4 |

**Le contrôle complet reste la règle par défaut.** L'alinéa 3 est une faculté du juge : le proposer comme option dans les points de décision, jamais le retenir à sa place, et seulement si la fiche a relevé la date de délivrance, le mode de délivrance et l'absence d'opposition du demandeur. Au moindre doute sur l'alinéa 4 (motivation spéciale exigée, moyen à relever d'office), contrôle complet.

Avant de citer l'article 472, le vérifier par `verifier_article` (`code` « CPC », `numero` « 472 ») à la date d'introduction de l'instance : une instance introduite avant le 01/10/2026 cite la version en deux alinéas.

---

## Workflow simplifié - Grille unique

```
═══════════════════════════════════════════════════════════════════
GRILLE NON-COMPARANT - Art. 472 CPC
Dossier [Demandeur] c/ [Défendeur]
═══════════════════════════════════════════════════════════════════

1. RÉGULARITÉ DE L'ASSIGNATION
   ─────────────────────────────────────────────────────────────────
   □ Date de l'assignation (délivrance) : [date]
   □ Date de saisine (remise au greffe, art. 857 CPC) : [date]
   □ Assignation délivrée depuis le 01/10/2026 : [oui / non] (remise au greffe de l'autre côté du 01/10 : le signaler)
   □ Opposition du demandeur à l'alinéa 3 de l'art. 472 : [oui / non / non dite]
   □ Délai de comparution respecté : [oui/non - calcul]
   □ Mentions obligatoires présentes : [oui/non]
   □ Mode de signification : [personne / domicile / art. 659 CPC]
   □ Si procès-verbal de recherches (art. 659 CPC) : diligences précises du commissaire de justice ; lettre recommandée envoyée au plus tard le premier jour ouvrable suivant ; lettre simple
   □ Assignation qui « annule et remplace » une précédente : laquelle fixe la date de la demande en justice (capitalisation, intérêts) ? À soumettre au juge, sans trancher
   
   → Qualification décision : [RÉPUTÉ CONTRADICTOIRE / PAR DÉFAUT]
   → Régime art. 472 : [contrôle complet / alinéa 3 possible, à proposer au juge]
   → Motivation : [cité à personne / signifié domicile + premier ressort...]

2. RECEVABILITÉ (vérifications d'office)
   ─────────────────────────────────────────────────────────────────
   □ Compétence TC : [acte de commerce / société commerciale]
   □ Défendeur personne physique (notamment entrepreneur individuel radié du RCS) : nom, prénom, date et lieu de naissance si l'acte les donne ; engagements pris pendant l'activité, nature commerciale ; si l'acte donne un SIREN (cas fréquent de l'entrepreneur individuel) : `etat_parties` comme pour toute partie ; si l'acte n'en donne aucun : hors champ du connecteur, ni web par nom, ni repli : « Non vérifié (SIREN absent) », le juge vérifie autrement
   □ Qualité à agir du demandeur : [vérifiée - motif]
   □ Intérêt à agir : [vérifié - motif]
   □ Prescription : [non acquise - délai applicable / point de départ]

3. BIEN-FONDÉ - VÉRIFICATION DES DEMANDES
   ─────────────────────────────────────────────────────────────────
   
   ┌────┬─────────────────────┬────────────┬─────────────────┬─────────┐
   │ N° │ DEMANDE             │ MONTANT    │ PIÈCES          │ VALIDÉ  │
   ├────┼─────────────────────┼────────────┼─────────────────┼─────────┤
   │ D1 │ Principal           │ [X] €      │ Facture n°...   │ □ / ✅  │
   │    │                     │            │ Contrat...      │         │
   ├────┼─────────────────────┼────────────┼─────────────────┼─────────┤
   │ D2 │ Intérêts            │ Légaux /   │ Mise en demeure │ □ / ✅  │
   │    │                     │ TX [%]     │ du [date]       │         │
   ├────┼─────────────────────┼────────────┼─────────────────┼─────────┤
   │ D3 │ Clause pénale       │ [Y] €      │ CGV art. X      │ □ / ✅  │
   │    │ (indemnité)         │            │                 │         │
   └────┴─────────────────────┴────────────┴─────────────────┴─────────┘
   
   Observations :
   • [Montant conforme à l'assignation / écart identifié ; contrôle sur pièces par le juge, sur l'original papier]
   • [Calcul des intérêts vérifié / à recalculer]
   • Chef reposant sur une pièce non vérifiable par Claude : option « écarté faute de justification » ajoutée au point de décision, jamais par défaut ; le juge tranche sur l'original papier
   • Indicateur : voir la règle spéciale QUANTUM de SKILL.md (niveaux 🟠 et 🔴, option D « Autre montant »)
   • Fait non lu, hypothèse de calcul : règle « Fait non lu » de SKILL.md (réserve `[à vérifier sur pièces : …]`)

4. ARTICLE 700 CPC
   ─────────────────────────────────────────────────────────────────
   □ Montant demandé : [Z] €
   □ Éléments d'appréciation : [simplicité/complexité dossier]
   □ Proposition retenue : [montant] €

═══════════════════════════════════════════════════════════════════
SYNTHÈSE - DÉCISIONS À RENDRE
═══════════════════════════════════════════════════════════════════

┌────┬─────────────────────┬────────────┬─────────────┐
│ N° │ CHEF                │ DEMANDÉ    │ RETENU      │
├────┼─────────────────────┼────────────┼─────────────┤
│  1 │ Principal           │ [X] €      │ [X] €       │
│  2 │ Intérêts légaux     │ Oui        │ Oui / Non   │
│  3 │ Clause pénale       │ [Y] €      │ [Y] €       │
│  4 │ Article 700         │ [Z] €      │ [montant] € │
│  5 │ Dépens              │ Défendeur  │ Défendeur   │
└────┴─────────────────────┴────────────┴─────────────┘

Si alinéa 3 possible : point de décision « Accueillir sur le fondement de l'art. 472 al. 3 (demande recevable, non contraire à l'ordre public, à une liberté protégée ni à un droit fondamental) » OU « Contrôle complet du bien-fondé » ; contrôle complet par défaut.

→ Validation requise avant rédaction
═══════════════════════════════════════════════════════════════════
```

---

## Formulations types

**Mention liminaire (après identification parties) :**
> La société [DÉFENDEUR], régulièrement assignée par acte d'huissier du [date], n'a pas constitué avocat.
>
> Personne physique : « [Prénom NOM], [né(e) le … à …], [ancien entrepreneur individuel], régulièrement assigné(e) … ».

**Motifs - structure allégée :**

```
Sur la demande en paiement :

Aux termes de l'article 472 du Code de procédure civile, si le défendeur 
ne comparaît pas, il est néanmoins statué sur le fond ; le juge ne fait 
droit à la demande que dans la mesure où il l'estime régulière, recevable 
et bien fondée.

Il ressort de la facture n°[X] en date du [date] 
(pièce n°1 du demandeur), établie conformément au contrat du [date] 
(pièce n°2), que la créance s'élève à [montant] €. Cette facture est demeurée impayée malgré mise en demeure 
du [date] (pièce n°3).

Il s'ensuit que la demande, régulière en la forme, recevable et justifiée par les pièces 
produites, sera accueillie.
```

**Variante alinéa 3 (seulement si le juge l'a retenue, instance introduite depuis le 01/10/2026) :**

```
Aux termes de l'article 472, alinéa 3, du Code de procédure civile, lorsque 
l'acte introductif d'instance a été délivré à personne, le juge peut, en 
première instance, sauf si le demandeur s'y oppose, faire droit à la demande, 
dès lors qu'elle est recevable et qu'elle n'est contraire ni à l'ordre public, 
ni à une liberté protégée, ni à un droit fondamental.

L'assignation a été délivrée à la personne de [défendeur] le [date] ; le 
demandeur ne s'y oppose pas. La demande est recevable [motif] et n'est 
contraire ni à l'ordre public, ni à une liberté protégée, ni à un droit 
fondamental.

En conséquence, il sera fait droit à la demande.
```

---

## Attention - Pas de pièces défendeur

Ne jamais faire référence à des "pièces du défendeur". Il n'y en a pas.

---

## Checklist allégée

```
═══════════════════════════════════════════════════════════════════
✓ VÉRIFICATION NON-COMPARANT
═══════════════════════════════════════════════════════════════════
□ Assignation régulière mentionnée
□ Qualification correcte (réputé contradictoire / par défaut)
□ Art. 472 CPC visé dans les motifs, dans la version applicable à la date d'introduction de l'instance
□ Si alinéa 3 : instance introduite depuis le 01/10/2026, acte à personne, première instance, pas d'opposition du demandeur, alinéa 4 écarté, choix du juge
□ Aucune thèse défendeur attribuée
□ Pas de renvoi à des pièces défendeur
□ Montants repris de l'assignation, contrôle sur pièces renvoyé au juge
□ Dispositif = demandes vérifiées (pas d'ultra petita)
═══════════════════════════════════════════════════════════════════
```
