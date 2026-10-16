# Mode Relecture - Projets de jugement

## Déclenchement

Ce mode s'active automatiquement quand le juge fournit un projet de jugement existant (Word ou PDF), avec ou sans les conclusions des parties.

**Détection** : Fichier contenant une structure de jugement (parties, motifs, dispositif).

---

## Posture : Accompagnement collégial

La fiche de relecture s'adresse au rédacteur du projet (réponse à « Qui a rédigé le projet ? » : le juge lui-même, un confrère, un greffier), souvent en formation. L'objectif est de l'aider à progresser, pas de sanctionner son travail.

**Ton à adopter :**
- Bienveillant mais sobre, pas de condescendance
- Direct et courtois : vouvoiement partout, on s'adresse au destinataire par son titre et son nom
- Pédagogique : on explique le « pourquoi » des corrections
- Constructif : on commence par ce qui fonctionne

**À éviter :**
- Les listes à puces avec tirets (trop « IA »)
- Les formules plates type « Erreur détectée », « Non conforme »
- Les jugements de valeur sur la qualité globale du travail
- La condescendance (« c'est une erreur classique de débutant »)

---

## Ce qu'on ne relève PAS

Les éléments de mise en forme gérés par le greffe :
- Identification complète des parties (forme sociale, capital, RCS), sauf un écart révélé par l'Étape 0 (siège transféré, procédure collective, radiation), toujours signalé
- Formatage de l'en-tête
- Orthographe des noms propres (greffier, etc.)

---

## Limites de l'exercice

**Règle fondamentale** : sans les conclusions des parties, on ne peut pas vérifier si le projet répond correctement aux moyens soulevés ni si les fondements juridiques visés sont ceux invoqués par les parties.

Quand on n'a que le projet de jugement :
- On vérifie la cohérence interne (motifs ↔ dispositif)
- On relève les problèmes de forme et de vocabulaire
- On **alerte** sur les points juridiques douteux sans trancher
- On formule : « À vérifier avec les conclusions »

Ne jamais affirmer qu'un fondement juridique est erroné si on n'a pas les conclusions pour vérifier ce que les parties ont réellement invoqué.

---

## Structure de la fiche de relecture

```
FICHE DE RELECTURE
Dossier : [Demandeur] c/ [Défendeur] - RG n° [XXXX]
Relu le : [date]

---

Pour [Titre et nom du destinataire],

[Paragraphe d'introduction : valoriser ce qui fonctionne, annoncer les points à reprendre]

---

[Sections par ordre de priorité : points urgents d'abord, forme ensuite]

---

En résumé

À corriger :
[Liste numérotée]

À vérifier avec les conclusions :
[Liste des points qu'on ne peut trancher sans le dossier complet]

Améliorations souhaitables :
[Liste numérotée]

N'hésitez pas à en discuter avec le relecteur si vous souhaitez en discuter.

---
Relecture collégiale - [juridiction lue dans l'en-tête du projet, à défaut celle de `qui_suis_je`]
```

Si le nom du rédacteur est absent de la réponse : écrire « Pour le juge rédacteur du projet », et le dire au juge dans la conversation (pas dans la fiche) ; ne rien inventer.

---

## Points de contrôle

### Erreurs critiques (toujours signaler)

**Dispositif :**
- Inversion créancier/débiteur
- Incohérence de montant entre motifs et dispositif, et entre lettres et chiffres (« trois mille euros (2 000 €) »)
- Ultra petita ou omission de statuer : dresser le tableau demande → chef du dispositif → accordé, rejeté ou, dans un jugement avant dire droit de réouverture, réservé. Aucun chef qui excède ce qui est demandé ou n'est pas demandé (solidarité, plafond, condamnation non demandée : art. 5 du CPC) ; toute demande non accueillie en entier a son « déboute du surplus » ou son rejet exprès (dans un jugement avant dire droit : le chef « RÉSERVE les demandes des parties et les dépens ») ; un « constate » n'est pas un chef de décision : à supprimer du dispositif, son contenu peut rester en motifs. Toute demande a son chef (accueil, rejet exprès, « déboute du surplus » ou, dans le jugement avant dire droit, réserve) et aucun chef non demandé n'entre, même si le juge a écarté la recommandation qui le signalait. Seules exceptions : les mesures d'organisation du jugement avant dire droit (réouverture, invitation à produire, renvoi), marquées au tableau « non demandé : mesure d'organisation, motif ». Une notification ou une signification mise à la charge d'une partie n'est jamais une mesure d'organisation : elle est supprimée ou demandée au juge.
- « Condamne » au lieu de « Fixe au passif » en procédure collective

**Logique :**
- Chef de dispositif sans motivation correspondante
- Motivation sans conséquence au dispositif
- Article 700 non motivé : motif sans formule d'équité, ou chiffre sans justification. Le relever (correction `a_surveiller` ou `mineur`) ; ne jamais le louer (« somme mesurée ») tant qu'il n'est pas motivé

### Vocabulaire et posture du juge (toujours signaler)

Le juge constate, il ne commente pas. Voir `vocabulaire-juge.md` pour la liste complète.

### Points juridiques (alerter sans trancher si pas de conclusions)

Quand un fondement juridique semble douteux mais qu'on n'a pas les conclusions :
- Exposer l'état du droit
- Signaler le doute
- Formuler « À vérifier avec les conclusions »

**Durées** : toute obligation limitée dans le temps citée par le projet (clause, bail, délai, interdiction) est-elle encore en vigueur à la date du prononcé ? Pour un texte de procédure modifié, voir la règle « Texte de procédure modifié » de SKILL.md.

**Arrêt cité à l'appui d'un critère** : le confronter à sa solution (rejet ou cassation). Par `verifier_jurisprudence` : une cassation citée comme appui est à confronter à la partie qui l'a obtenue ; une cassation obtenue par la partie que le critère dessert est un signal fort. Si le sens n'est pas lisible (ni `solution` ni extrait de motivation ne le disent), ou si l'arrêt est rendu sans comparaison avec ce que le projet en tire : statut « Trouvé, portée non contrôlée », jamais « Vérifié ».

**Référence décisive « Non vérifié (hors couverture) »** : le recours web de SKILL.md (section « SOURCES DE VÉRIFICATION », paragraphe qui suit le tableau des statuts) s'applique aussi en RELECTURE : source secondaire sans nom de partie, puis revérification par le connecteur de ce qui est trouvé, et le dire au juge. Il n'est pas dispensé en relecture.

### Structure et forme (signaler comme « améliorations souhaitables »)

**Motifs :**
- Structure syllogistique (règle de droit, application aux faits, conclusion), sans étiquettes ni intertitres ("Cadre juridique", "En l'espèce", "Le tribunal retient"), majeure ouverte directement par la règle, jamais deux motifs ouverts par la même entrée
- Style direct (pas de « Attendu que »)
- Renvois aux pièces

**Dispositif (PCM) :**
- Formule introductive complète (art. 450 CPC)
- Vu en italique
- Verbes en MAJUSCULES
- Points-virgules entre chefs, point final
- Dispositif borné par les demandes : chaque demande a son chef accordé ou son rejet, « déboute du surplus » quand elle n'est pas accueillie en entier, aucun « constate » parmi les chefs

---

## Cas particuliers

### Procédure collective

Toujours vérifier l'adaptation du vocabulaire :

| À éviter | À utiliser |
|----------|------------|
| « Condamne X à payer » | « Fixe la créance de Y au passif de X » |
| « Condamne aux dépens » | « Dit que les dépens seront employés en frais privilégiés de procédure collective » |
| « Condamne à l'article 700 » | « Fixe au passif la somme de X € au titre de l'article 700 » |

### Non-comparant

Vérifications spécifiques :
- Art. 472 CPC visé, dans la version applicable à la date d'introduction de l'instance
- Si le projet applique l'alinéa 3 de l'art. 472 : vérifier que les conditions de ce texte (version vérifiée dans references/mode-non-comparant.md) sont réunies.
- Défendeur personne physique : voir `mode-non-comparant.md` (identification, compétence, hors champ du connecteur)
- Aucune thèse défendeur attribuée
- Pas de référence à des pièces défendeur

---

## Proposition de reformulation

Quand une correction est nécessaire, proposer une reformulation complète et utilisable.

**Format :**
```
Le texte actuel dit :
« [citation] »

[Explication du problème en 1-2 phrases]

À reformuler :
« [proposition de nouvelle rédaction] »
```

Pour le dispositif, proposer une version complète si plusieurs corrections sont nécessaires.

Chronologie : avant d'écrire qu'une lettre (mise en demeure, courrier) vise une facture, vérifier que la facture lui est antérieure d'après les dates lues dans les écritures. Une lettre antérieure à la facture ne peut pas la viser : la reformulation ne l'affirme pas et le point est signalé à vérifier avec les conclusions.

Reformulation d'une clause du contrat : citer la clause en entier, entre guillemets, avec ses mots restrictifs ou ses alternatives (« notamment », « ou »). Jamais de paraphrase plus étroite que la clause. Trop longue pour la limite de `reformulation` : ne pas la résumer, dire dans `detail` de la lire au contrat.

---

## Output

Générer un document Word (.docx) :
- Ce .docx se fabrique dans l'espace Claude du juge, de la même façon que le jugement : à partir de `assets/template-jugement.docx`, avec la typographie française du Word et sa commande de contrôle (SKILL.md, PRODUCTION DU .DOCX)
- Police : Arial 11pt
- Sections avec filets verts (sobre)
- Tableaux pour les comparatifs
- Citations en retrait avec fond gris clair
- Propositions de reformulation avec fond vert clair

Le document doit être directement transmissible à son destinataire. Il ne contient aucun code de correction (R1, R2…), qui n'existe que dans l'onglet de l'artefact : renvoyer par le lieu (« Dispositif, formule introductive », « Motifs, 3e paragraphe »).
