# Pièces du dossier : conclusions seulement

Ce fichier dit quoi faire de chaque pièce que le juge verse. Le skill travaille sur les **conclusions des parties** (et l'assignation quand le défendeur ne comparaît pas). Il ne lit **jamais** les pièces annexes, même versées : elles saturent l'analyse et le fil n'arrive plus à terminer. Le juge les garde en papier ; la liste des vérifications sur pièces lui dit quoi y regarder.

## 1. Avant le dépôt

Dire au juge, mot pour mot :

« Versez uniquement les conclusions des parties, et l'assignation si le défendeur ne comparaît pas. Ne versez pas les pièces annexes : je ne les lis pas, elles saturent l'analyse. Gardez-les en papier, je vous dirai quoi y vérifier. »

## 2. Trier chaque pièce reçue, à la première page

| Première page | Classement |
|---|---|
| Titre « Conclusions » (en réponse, récapitulatives, n° 2…), « Assignation », « Dires », « Requête » ; nom ou cachet d'avocat ; adresse au tribunal ; dispositif « Par ces motifs » | Conclusions : à lire |
| Projet de jugement à relire (mode relecture : seul le projet du juge est lu) | À lire, hors règle des annexes |
| Pièce numérotée, facture, devis, contrat, courrier, courriel imprimé, mise en demeure, extrait Kbis, relevé, constat, photo, jugement ou ordonnance antérieurs | Annexe : ne pas lire |
| Doute | Une question au juge, en une ligne ; ne pas lire pour trancher |

- Le classement d'un fichier se décide sur sa première page, même s'il n'est pas encore lu ; la règle suivante dit où s'arrêter dans un fichier classé conclusions. Un bordereau de pièces fait partie des conclusions ; il se lit, les pièces qu'il liste non.
- Un fichier qui enchaîne conclusions puis pièces : arrêter la lecture à la première page qui n'est plus des conclusions (page « Pièce n° », facture après le bordereau) et dire « pages X à Y : annexes, non lues ». Vaut aussi pour des conclusions déjà visibles dans la conversation.
- Plusieurs versions des conclusions d'une même partie : retenir la plus récente et dire laquelle.

## 3. Annexe reçue malgré tout

Écrire au juge : « <nom du fichier> : pièce annexe, non lue. Je n'en tiens pas compte ; la liste des vérifications sur pièces vous dira quoi y regarder. »

- Si elle n'est qu'un fichier : ne pas l'ouvrir.
- Si son contenu est déjà visible dans la conversation (certaines interfaces lisent d'office les petits PDF) : ne s'en servir pour rien, ni chiffre, ni date, ni fait.
- Le SIREN d'une partie absent des conclusions et de l'assignation : le demander au juge en une ligne (il le lit sur le Kbis papier), jamais le tirer d'une annexe.

Puis poursuivre.

## 4. Conclusions : selon ce qui est arrivé

| Situation | Conduite |
|---|---|
| Contenu déjà visible dans la conversation | Travailler dessus directement. Ne pas reconvertir : le coût est déjà payé. Section 5 pour chaque valeur relevée sur une page scannée |
| Simple fichier, et l'environnement permet des sous-agents | Un sous-agent par PDF, sur le modèle Sonnet si le choix existe, 4 en parallèle au plus, tranches de 20 pages. Lui donner le chemin du fichier, la section 5 et la règle d'arrêt de la section 2 (s'arrêter à la première page qui n'est plus des conclusions et rendre « pages X à Y : annexes, non lues »). Il rend le seul Markdown, jamais d'image ni de résumé. S'il ne trouve pas le fichier : ligne suivante |
| Simple fichier, sans sous-agent | Le fil principal lit par tranches de 20 pages et garde par tranche une note brève (parties, demandes chiffrées, moyens, dates, pièces citées), qui conserve chaque `[?]` |

Sans sous-agent, ou si un sous-agent ne trouve pas le fichier : repli unique décrit dans SKILL.md, « Économie du contexte ».

Un PDF texte se lit normalement : la section 5 ne vaut que pour les pages scannées.

## 5. Transcrire une page scannée

- En tête de chaque page scannée : `<!-- page N lue par OCR -->` (N : page du PDF, pas la pagination de l'avocat).
- Transcription fidèle : ne pas résumer, ne pas corriger, ne pas compléter. Retirer seulement les en-têtes et pieds de page répétés.
- Montant, date, nom propre, dénomination, numéro (SIREN, RG, IBAN) dont un seul caractère est douteux : `[?]` juste après la valeur entière, par exemple `2 083,22 € [?]` ; `[?]` seul si rien n'est lisible.
- Ne jamais normaliser selon la vraisemblance : un SIREN qui n'a pas 9 chiffres, un code postal étrange se recopient tels quels, avec `[?]`.
- Montants recopiés caractère par caractère, sans recalcul ni arrondi. Un total qui ne correspond pas à ses lignes se recopie tel quel avec `[?]`.
- Mention manuscrite : `[manuscrit]` devant. Caractère barré, surchargé ou sous un tampon : `[?]`.
- Page vide : `<!-- page N blanche -->`. Page illisible : `<!-- page N illisible -->`. Jamais de texte inventé.
- Tableaux en tableaux Markdown.
- Rien d'autre que la transcription. Une observation (incohérence de l'original, phrase coupée) va dans un commentaire `<!-- … -->`.

Une valeur marquée `[?]` n'est jamais écrite comme certaine dans la suite ; une page blanche ou illisible est signalée au juge, son contenu n'est jamais supposé (voir « Lectures incertaines » dans SKILL.md).
