# Journal

> Plus récent en haut. Une ligne par décision ou intervention : `AAAA-MM-JJ — quoi — pourquoi (si décision)`.

## Prochaines étapes (reprises de Notion, 11/10/2026)
- [ ] Programmer l'onduleur (VEConfigure → PC Windows nécessaire)
- [ ] Brancher le SmartShunt à l'onduleur (commander le câble VE.Direct Victron)
- [ ] Mettre en place et tester le suivi du niveau batterie depuis la chaumière
- [ ] Petit réseau d'éclairage (et prises ?) dans la brocante, au moins pour éclairer l'armoire en maintenance
- [ ] Tirer le 3G6 de l'armoire jusqu'au tableau divisionnaire de la chaumière
- [ ] Dimensionner les éléments d'éclairage, proposer des références à faire valider par Mymy pour la déco
- [ ] Acheter des cache-dents pour le peigne HX³ du tableau chaumière (dents libres à protéger, IP2X) — avant mise sous tension

## Entrées
- 2026-10-31 — Tableau chaumière : peigne HX³ laissé entier (réserve pour ajouts futurs) — dents libres à protéger par cache-dents, pas de scotch en définitif.
- 2026-10-27 — Chantier d'octobre, J2 : séchage de l'armoire DC au radiateur, alimenté directement par le solaire (bon ensoleillement). Suivi SOC toujours via l'appli Redodo (Bluetooth, sur place).
- 2026-10-26 — Chantier d'octobre, J1 : eau trouvée dans l'armoire DC, amenée par les gaines PV (annelé inox le long du toit puis IRL). Décision : point d'évacuation + remontée du tube avant l'entrée, sans monter sur le toit ; jonction annelé/IRL à reprendre plus tard. Pilotes MK3-USB + VEConfigure installés (prise en main rapide), Remote Console consultée, clé USB insérée dans le GX pour l'enregistrement des logs.
- 2026-10-11 — Fin de session schémas : `unifilaire-armoire.drawio` terminé pour l'état installé (retouches de mise en page par Polar, circuit prises brocante marqué « à réaliser » hors X1, note sur l'ordre MEGA / coupe-batterie retirée). Reste ouvert : 30 mA du départ chaumière (décision avant de tirer le câble), test N–PE, sections Q4/Q5, export PNG.
- 2026-10-11 — Unifilaire armoire : DC en 2 fils, réponses de Polar intégrées (parafoudre DC = Citel, sortie AC en R2V 3G6, Q4 = prises dont X1, Q5 = éclairage, Q6 en parallèle de Q3 par Wago). ⚠️ Départ chaumière sans 30 mA : décision à prendre avant de tirer le câble.
- 2026-10-11 — `unifilaire-armoire.drawio` refait en vrai unifilaire (symboles normalisés, jeu de barres, repères Q/F/G/U, ligne de départs) à la place de la version en blocs.
- 2026-10-11 — Schéma `unifilaire-armoire.drawio` (état installé) ; points flous marqués « ? » et ajoutés à `a-verifier.md` (régime de neutre, sortie AC, prise modulaire). Export PNG à faire (pas de draw.io CLI sur le Mac).
- 2026-10-11 — Confirmé : MEGA 125 A et coupe-batterie posés ; câbles batterie OK. Décision (prise cet été) : un seul parafoudre DEHN, dans l'armoire, pas dans le tableau chaumière.
- 2026-10-11 — Factures ajoutées (`commandes/`) : création de `docs/commandes.md`, `materiel.md` complété (réfs, stock), nouveaux points dans `a-verifier.md`.
- 2026-10-11 — Migration de la fiche Notion « Suivi » vers ce repo ; création des docs et du synoptique.
- 2026-08 — Chantier d'été : armoire de production posée et câblée, panneaux posés sur la toiture et mis à la terre.
- 2026-08-11 — Arrivée sur site, inventaire complet du matériel : tout reçu et conforme.
