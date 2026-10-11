# kerglu-elec

Installation électrique autonome (PV + batterie, hors réseau) de la chaumière de Kergludaouen (Riec-sur-Bélon), lieu porté par la SCIC Résiliens.

Ce repo est **la source de vérité** du projet élec : contexte, matériel, décisions, journal et schémas. Il sert de mémoire commune entre :
- **Claude Code** (sur ton ordi, dans VS Code) : édition des schémas `.drawio`, mise à jour des docs ;
- **Claude chat** (projet « kerglu » sur claude.ai) : discussions, réflexion, relecture ;
- **toi** et toute personne du collectif qui reprendra l'install.

## Structure

```
CLAUDE.md                   Instructions lues automatiquement par Claude Code
docs/
  contexte.md               Le lieu, l'objectif, les contraintes (chaume = sécurité incendie)
  materiel.md               Inventaire du matériel installé / sur site
  commandes.md              Achats : fournisseurs, factures, quantités, prix
  missions.md               Les 5 missions (M1 à M5) et dépendances entre corps d'état
  apprentissages.md         Ce qu'on a appris (Victron, LiFePO4, DC, terre, bilan énergie)
  exploitation.md           Séquences d'arrêt / remise en route, réglages, relevés SOC
  a-verifier.md             Points ouverts et incertitudes à lever sur site
  journal.md                Journal daté des décisions et interventions
commandes/                  Factures PDF
schemas/
  README.md                 Conventions de dessin
  synoptique.drawio         Vue d'ensemble PV → ardoise → chaumière
  exports/                  PNG exportés (pour Notion / impression dans les coffrets)
```

## Règles de fonctionnement

1. **Toute décision ou intervention** → une ligne datée dans `docs/journal.md`.
2. **Toute valeur technique** (calibre, section, réglage) vit à **un seul endroit** (`materiel.md` ou `exploitation.md`) ; les schémas doivent la reprendre à l'identique.
3. Quand un schéma change → réexporter le PNG dans `schemas/exports/`.
4. Ce qui n'est pas confirmé sur site reste dans `docs/a-verifier.md` jusqu'à vérification.
