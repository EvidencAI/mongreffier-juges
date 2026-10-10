# Table des renumérotations (Code civil 2016, Code de commerce 2019)

À quoi sert cette table : retrouver le texte qu'un ancien numéro d'article désignait avant une réforme, et le ou les numéros qui le portent depuis. Le skill la lit à la demande, quand `version_a_date_utile` vaut « aucune » ou quand l'article rendu est abrogé (voir SKILL.md, section SOURCES DE VÉRIFICATION).

**L'ancien et le nouveau numéro peuvent désigner deux articles différents ; se fier à la date utile (voir SKILL.md).** Exemple prouvé : l'ancien 1315 (preuve des obligations) et le nouveau 1315 (exceptions du débiteur solidaire) n'ont rien en commun. Un contrat conclu avant le 01/10/2016 relève de l'ancien texte.

Chaque ligne a été vérifiée le 10/10/2026 dans la source primaire (connecteur local, version dont la fin est la date de la réforme, puis version nouvelle). Les identifiants LEGIARTI désignent la version utile. Un article encore modifié depuis la réforme a d'autres versions : passer par `date_utile`.

## Code civil : ordonnance 2016-131 du 10 février 2016 (en vigueur le 01/10/2016)

| Ancien numéro | Nouveau(x) numéro(s) | Objet | Id ancien | Id(s) nouveau(x) | Vérifié le |
|---|---|---|---|---|---|
| 1134 | 1103 (al. 1), 1193 (al. 2), 1104 (al. 3) | Force obligatoire du contrat, modification par consentement mutuel, bonne foi | LEGIARTI000006436298 | LEGIARTI000032040777 (1103), LEGIARTI000032041314 (1193), LEGIARTI000032040772 (1104) | 2026-10-10 |
| 1135 | 1194 | Suites du contrat (équité, usage, loi) | LEGIARTI000006436307 | LEGIARTI000032041309 | 2026-10-10 |
| 1147 | 1231-1 | Dommages et intérêts pour inexécution ou retard | LEGIARTI000006436401 | LEGIARTI000032010123 | 2026-10-10 |
| 1148 | 1218 (al. 1) | Force majeure, cas fortuit | LEGIARTI000006436410 | LEGIARTI000032041431 | 2026-10-10 |
| 1152 | 1231-5 | Clause pénale | LEGIARTI000006436388 | LEGIARTI000032010131 | 2026-10-10 |
| 1153 | 1231-6 et 1344-1 | Intérêts moratoires, point de départ (mise en demeure), préjudice distinct | LEGIARTI000006436390 | LEGIARTI000032010133 (1231-6), LEGIARTI000032035273 (1344-1) | 2026-10-10 |
| 1154 | 1343-2 | Anatocisme (intérêts des intérêts) | LEGIARTI000006436422 | LEGIARTI000032035261 | 2026-10-10 |
| 1315 | 1353 | Charge de la preuve | LEGIARTI000006437767 | LEGIARTI000032042341 | 2026-10-10 |
| 1382 | 1240 | Responsabilité pour faute | LEGIARTI000006438819 | LEGIARTI000032041571 | 2026-10-10 |
| 1383 | 1241 | Responsabilité pour négligence ou imprudence | LEGIARTI000006438829 | LEGIARTI000032041565 | 2026-10-10 |
| 1384 | 1242 (al. 1) | Responsabilité du fait d'autrui et des choses | LEGIARTI000006438840 | LEGIARTI000032041559 | 2026-10-10 |

Notes :
- 1134 est scindé en trois articles. L'alinéa de départ de chaque article se lit dans le texte rendu.
- 1153 : le rattachement alinéa par alinéa entre les deux nouveaux articles n'est pas établi ici ; lire les deux.
- 1242 : l'id indiqué est la version du 01/10/2016 au 24/06/2025. Une version plus récente existe depuis le 25/06/2025 (LEGIARTI000051786000).
- 1384 : les alinéas suivants de l'ancien article n'ont pas été rapprochés un à un.
- 1148 : correspondance partielle. L'ancien 1148 est la conséquence de la force majeure (pas de dommages et intérêts) ; le nouveau 1218 en donne la définition et le régime.

## Code de commerce : ordonnance 2019-359 du 24 avril 2019 (en vigueur le 26/04/2019)

| Ancien numéro | Nouveau(x) numéro(s) | Objet | Id ancien | Id(s) nouveau(x) | Vérifié le |
|---|---|---|---|---|---|
| L.442-6 (I, 1° et 2°) | L.442-1 (I, 1° et 2°) | Avantage sans contrepartie, déséquilibre significatif (pratiques restrictives) | LEGIARTI000033612862 | LEGIARTI000038414278 | 2026-10-10 |
| L.442-6 (I, 5°) | L.442-1 (II) | Rupture brutale d'une relation commerciale établie | LEGIARTI000033612862 | LEGIARTI000038414278 | 2026-10-10 |
| L.441-6 | L.441-1 (CGV) et L.441-10 (délais de paiement, pénalités de retard) | Conditions générales de vente, délais de règlement | LEGIARTI000037556544 | LEGIARTI000038414469 (L.441-1), LEGIARTI000038414392 (L.441-10) | 2026-10-10 |

Pièges de numéro réutilisé :
- Le L.442-6 actuel (depuis le 26/04/2019) n'est plus l'ancien : il punit le prix de revente imposé (LEGIARTI000038414237).
- Le L.441-6 actuel n'est plus l'ancien : il prévoit l'amende administrative pour manquement aux L.441-3 à L.441-5 (LEGIARTI000038414424).
- L.441-10 est rendu en état ABROGE_DIFF (fin 01/01/2027) : une version postérieure existe. Passer par `date_utile`.

## Lignes retirées ou non rapprochées

- Code de commerce, 3°, 4°, 6° à 13° de l'ancien L.442-6, I (autres pratiques restrictives) : texte ancien rendu, mais le nouveau numéro n'a pas été prouvé par le texte. Ne pas deviner : chercher par `rechercher` du connecteur.
- Code de commerce, L.442-6 hors alinéa I (nullité des clauses, action en justice) : texte ancien rendu, mais le nouveau numéro n'a pas été prouvé par le texte. Ne pas deviner : chercher par `rechercher` du connecteur.
- Code de commerce, L.441-6 vers L.441-9 (factures) : rapprochement non prouvé, non retenu.
- Aucune ligne demandée n'a été retirée pour texte ancien non rendu : les treize anciens numéros ont été rendus par la source.
