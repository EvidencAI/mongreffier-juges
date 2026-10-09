# Mode Relecture - Projets de jugement

## Déclenchement

Ce mode s'active automatiquement quand le juge fournit un projet de jugement existant (Word ou PDF), avec ou sans les conclusions des parties.

**Détection** : Fichier contenant une structure de jugement (parties, motifs, dispositif).

---

## Posture : Accompagnement collégial

La fiche de relecture s'adresse à un confrère juge, souvent en formation. L'objectif est de l'aider à progresser, pas de sanctionner son travail.

**Ton à adopter :**
- Bienveillant mais sobre, pas de condescendance
- Direct et amical : on tutoie, on s'adresse par prénom
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
- Identification complète des parties (forme sociale, capital, RCS)
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

Pour [Prénom],

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

N'hésite pas si tu veux qu'on en discute.

---
Relecture collégiale - [juridiction de la fiche du dossier]
```

---

## Points de contrôle

### Erreurs critiques (toujours signaler)

**Dispositif :**
- Inversion créancier/débiteur
- Incohérence de montant entre motifs et dispositif
- Ultra petita ou omission de statuer
- « Condamne » au lieu de « Fixe au passif » en procédure collective

**Logique :**
- Chef de dispositif sans motivation correspondante
- Motivation sans conséquence au dispositif

### Vocabulaire et posture du juge (toujours signaler)

Le juge constate, il ne commente pas. Voir `vocabulaire-juge.md` pour la liste complète.

### Points juridiques (alerter sans trancher si pas de conclusions)

Quand un fondement juridique semble douteux mais qu'on n'a pas les conclusions :
- Exposer l'état du droit
- Signaler le doute
- Formuler « À vérifier avec les conclusions »

### Structure et forme (signaler comme « améliorations souhaitables »)

**Motifs :**
- Structure syllogistique (règle de droit, application aux faits, Le tribunal retient), sans intertitres "Cadre juridique" ni "En l'espèce"
- Style direct (pas de « Attendu que »)
- Renvois aux pièces

**Dispositif (PCM) :**
- Formule introductive complète (art. 450 CPC)
- Vu en italique
- Verbes en MAJUSCULES
- Points-virgules entre chefs, point final

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
- Art. 472 CPC visé
- Qualification correcte (réputé contradictoire / défaut selon art. 473)
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

---

## Output

Générer un document Word (.docx) :
- Ce .docx se fabrique dans l'espace Claude du juge, de la même façon que le jugement : à partir de `assets/template-jugement.docx`
- Police : Arial 11pt
- Sections avec filets verts (sobre)
- Tableaux pour les comparatifs
- Citations en retrait avec fond gris clair
- Propositions de reformulation avec fond vert clair

Le document doit être directement transmissible au confrère.
