# Mode VÉRIFICATION : références d'un document juridique

Chargé en mode VÉRIFICATION, et par le mode RELECTURE pour les références du projet. Le document peut être de toute nature : conclusions, contrat, note, consultation, décision, projet. La demande porte sur ses références, pas sur sa rédaction.

## Cadre

- Aucune fiche du dossier, aucune « dernière écriture », aucune phase. Pas de validation intermédiaire : on extrait, on vérifie, on rend.
- Exigences d'ouverture inchangées : modèle Opus (étape 0 de SKILL.md) et `qui_suis_je` par le fil principal (étape 0 bis), avant toute lecture du document. Ne rien analyser tant qu'elles ne sont pas satisfaites.
- Rappeler au juge, une seule fois : « Versez un document pseudonymisé. À défaut, c'est sous votre responsabilité. » Aucun nom de partie dans une requête web ni dans le titre de l'artefact.
- Le document est lu par `references/conversion.md` s'il s'agit d'un scan ou d'un gros PDF.

## 1. Extraire TOUTES les références

Lire le document en entier, sans s'arrêter aux références « importantes ». Dresser la liste numérotée :

| Catégorie | À relever |
|---|---|
| Articles | Code ou loi, numéro, et la date utile si le document la donne (date des faits, du contrat, de la rupture). Ce que le document fait dire à l'article, quand il le dit |
| Décisions de justice | Juridiction, date, numéro (pourvoi ou RG), formation, et la proposition que le document en tire |
| Sociétés | Dénomination et SIREN, quand le document le donne ou le rend identifiable |

Une référence incomplète (numéro absent, juridiction seule) reste dans la liste ; elle sera cherchée par `rechercher`, ou rendue « Non vérifié ».

## 2. Vérifier chaque référence par le connecteur

Jamais par le web seul. Les statuts rendus au juge sont ceux de « SOURCES DE VÉRIFICATION » de SKILL.md : Vérifié, Visé seul (article cité par son numéro, sans contenu rapporté ni moyen : jamais « Vérifié »), Divergent, Introuvable, Trouvé (portée non contrôlée), Trouvé (version non applicable à la date utile), Trouvé, non cité par les parties (texte ou arrêt trouvé d'office, qu'aucune partie ne cite ni ne reproduit : jamais présenté comme cité par une partie, jamais dans l'« En bref »), Non vérifié. Aucun autre statut. « Vérifié » suppose une comparaison avec ce que cite le document ; un arrêt rendu sans comparaison reste « Trouvé, portée non contrôlée » ; une version « aucune » à la date utile est « Trouvé, version non applicable à la date utile », jamais « Vérifié », dit au juge. Divergent vaut aussi quand le texte rendu contredit un élément de ce que le document en tire. « Trouvé, non cité par les parties » ne vaut que si le texte n'est ni cité ni reproduit dans les écritures lues : un texte reproduit est comparé et reçoit le statut Vérifié ou Divergent. Un texte couvert par un « et suivants » sans être cité par son numéro est signalé « visé par renvoi » ; un article cité par son numéro, sans contenu ni moyen, est « Visé seul », sauf si la recherche rend « Introuvable » ou « Divergent » : ce statut prime.

- **Articles** : `verifier_article`, avec `date_utile` choisie selon la règle de SKILL.md (à défaut de date dans le document : date des faits, sinon de l'assignation, et le dire). Comparer le texte rendu à ce que le document cite. `date_concordante: false` = Divergent. Si `version_a_date_utile` vaut « aucune » ou si l'article est abrogé : consulter `references/renumerotations.md` avant de conclure.
- **Décisions** : arrêt de la Cour de cassation : `verifier_jurisprudence` avec `numero_pourvoi` et `date` ; référence incomplète : `rechercher` avec `fonds: "jurisprudence"`. Comparer juridiction, date, formation et portée. Arrêt d'appel ou décision de première instance : hors couverture du connecteur, statut « Non vérifié (hors couverture) ».
- **Sociétés** : `etat_parties` pour chaque SIREN. Rien rendu, ou outil en erreur : « Non vérifié ». Jamais « aucune procédure ». Sans SIREN lisible : « Non vérifié (SIREN absent) », sans recherche web par dénomination.
- **Web** : seulement après un « Non vérifié » décisif pour le document, annoncé au juge, sans nom de partie, et tout arrêt ou texte ainsi trouvé est revérifié par le connecteur. Une source secondaire oriente, elle ne vaut pas vérification.
- **Connecteur absent ou en panne** : règles de SKILL.md (arrêt jusqu'à reconnexion, ou bascule annoncée sur les sources ouvertes).
- Le sous-agent n'a pas accès au connecteur : toute vérification passe par le fil principal.

## 3. Rendu

**« En bref »** dans la conversation, 5 phrases au plus, hors la liste des divergences, vouvoiement : nombre de références par catégorie, nombre de divergences, de non vérifiés, de références de portée non contrôlée et de versions non applicables à la date utile, TOUTES les divergences en tête (une ligne chacune, sans plafond, aucune omise), puis : « Détail : onglet Vérification des références de l'artefact MonGreffier ».

**« En détail »** dans l'artefact MonGreffier (mode d'emploi : `references/artefacts.md`, section « Modes à onglets libres ») :
- onglet libre `id: verification`, titre « Vérification des références », sans `saisie` ;
- un tableau par catégorie (Articles, Décisions, Sociétés), colonnes : Référence citée | Statut | Ce que dit la source | Commentaire ;
- dans chaque tableau, les Divergent et Introuvable d'abord, puis les « Trouvé, portée non contrôlée », les « Trouvé, version non applicable à la date utile » et les « Trouvé, non cité par les parties » (texte ni cité ni reproduit ; un texte couvert par un « et suivants » sans être cité par son numéro est signalé « visé par renvoi »), puis les « Visé seul », puis les Non vérifié (en précisant : source indisponible ou hors couverture), puis les Vérifié ;
- au moins deux sections `##` (la page les replie en accordéons) ;
- si l'artefact ne peut pas être publié : mêmes tableaux dans la conversation, sous l'intertitre « En détail ».

## 4. Fin

Si le document relève d'un dossier (conclusions à analyser, projet de jugement), proposer au juge de basculer en RÉDACTION ou en RELECTURE ; ne pas basculer sans son accord.

## En relecture d'un projet de jugement

Le mode RELECTURE applique la même vérification aux références du projet (étapes 1 et 2 ci-dessus). Le détail va dans l'onglet libre `relecture`, dans une section « Références », et non dans un onglet `verification` : un seul onglet par mode.
