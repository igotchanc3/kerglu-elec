# Instructions pour Claude — projet kerglu-elec

## Contexte en 5 lignes
- Installation électrique **hors réseau** (PV + batterie LiFePO4) pour la chaumière de l'écolieu de Kergludaouen (Riec-sur-Bélon, SCIC Résiliens).
- Production/stockage dans une **armoire de production** (bâtiment « brocante »), liaison R2V 3G6 vers le futur tableau divisionnaire de la chaumière.
- Chauffage, ECS et cuisson au bois : les besoins électriques sont modestes.
- **Toit en chaume = risque incendie** : toute décision DC est évaluée sous l'angle arc/incendie (peu de connexions, câbles préfabriqués, MC4 de même marque).
- Responsable élec : Polar (étudiant ingé génie civil/énergie, pas électricien certifié). Interventions sur site pendant des chantiers participatifs ponctuels.

Détails : `docs/contexte.md`, `docs/materiel.md`, `docs/apprentissages.md`.

## Où est quoi
- Valeurs techniques (références, calibres, sections) → **`docs/materiel.md`** uniquement.
- Réglages, séquences, relevés SOC → `docs/exploitation.md`.
- Ce qui n'est pas confirmé → `docs/a-verifier.md`.
- Historique → `docs/journal.md` (une ligne datée par décision/intervention, plus récente en haut).
- Schémas → `schemas/*.drawio` (conventions dans `schemas/README.md`).

## Règles pour Claude
1. **Ne jamais inventer une valeur** (calibre, section, référence). Si elle manque : l'écrire « ? » sur le schéma et l'ajouter à `docs/a-verifier.md`.
2. Un schéma doit reprendre **à l'identique** les valeurs de `docs/materiel.md`. Si tu modifies l'un, vérifie l'autre.
3. Après chaque session de travail : ajouter une ligne dans `docs/journal.md`. Polar a tendance à ne pas documenter en temps réel — rappelle-le-lui si besoin.
4. Fichiers `.drawio` : XML non compressé, éditable à la main ; garder des `id` lisibles (`dc_sect`, `bat`, `tabC_d1`…) pour pouvoir cibler les modifs.
5. Sécurité : signaler explicitement tout choix qui augmente le risque d'arc DC, de surcharge ou qui sort de la NF C 15-100 / guide UTE C 15-712-2 (installations PV autonomes). Ne pas valider une modif « pour faire plaisir ».
6. Réponses courtes et directes, en français.

## Commits
Messages en français, au présent : `schema: ajout départ éclairage brocante`, `docs: relevé SOC 24/10`.
