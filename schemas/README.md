# Conventions des schémas

## Outil
- Fichiers `.drawio` (XML non compressé), édités dans VS Code avec l'extension **Draw.io Integration** (`hediet.vscode-drawio`) ou sur app.diagrams.net.
- Symboles : bibliothèque draw.io « Electrical » (IEC) pour les unifilaires ; blocs simples pour le synoptique.

## Couleurs
| Élément | Couleur |
|---|---|
| DC + | rouge `#b85450` |
| DC − | noir `#333333` |
| AC (phase/neutre) | bleu `#6c8ebf` |
| PE / terre | vert pointillé `#2d7600` |
| Élément à vérifier | contour orange pointillé + « ? » |

## Schémas prévus
- [x] `synoptique.drawio` — vue d'ensemble
- [ ] `unifilaire-armoire.drawio` — DC + AC de l'armoire de production
- [ ] `unifilaire-chaumiere.drawio` — tableau divisionnaire chaumière

## Exports
Après chaque modif : exporter en PNG dans `exports/` (même nom de fichier) pour Notion et pour impression plastifiée dans les coffrets.
