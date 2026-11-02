# Journal

> Plus récent en haut. Une ligne par décision ou intervention : `AAAA-MM-JJ — quoi — pourquoi (si décision)`.

## Prochaines étapes (reprises de Notion, 11/10/2026)
- [ ] Montrer à au moins une personne sur place comment éteindre/rallumer l'EasySolar (réarmement après surcharge). Voir `exploitation.md` § Gestion de la surcharge.
- [ ] Raccorder le parafoudre AC du départ 230 V (oublié le 31/10)
- [ ] Afficher une fiche de remise en route sur l'armoire
- [ ] Programmer l'onduleur (VEConfigure → PC Windows nécessaire)
- [ ] Brancher le SmartShunt à l'onduleur (commander le câble VE.Direct Victron)
- [ ] **Suivi du niveau batterie en CPL** (Remote Console) : apporter les boîtiers CPL de chez Polar (même modèle sur tout le réseau, appairés avant le départ) et tester GX ↔ atelier puis GX ↔ chaumière. Branchés en direct sur la prise (pas de multiprise filtrée). Voir `a-verifier.md` § Mise en service.
- [ ] Petit réseau d'éclairage (et prises ?) dans la brocante, au moins pour éclairer l'armoire en maintenance
- [ ] Tirer le 3G6 de l'armoire jusqu'au tableau divisionnaire de la chaumière
- [ ] Dimensionner les éléments d'éclairage, proposer des références à faire valider par Mymy pour la déco
- [ ] Acheter des cache-dents pour le peigne HX³ du tableau chaumière (dents libres à protéger, IP2X) — avant mise sous tension

## Entrées
- 2026-11-02 — Décision surcharge révisée : **pas de limiteur**, on laisse les protections de l'onduleur (coupure + réarmement manuel après 3 surcharges) et du BMS, et on observe aux chantiers 2027. Pourquoi : usure estimée ~6 €/an contre 100-200 € de matériel ; le GX de l'EasySolar n'a pas de relais ; un disjoncteur DC batterie risquerait de casser le MPPT. Node-RED gardé en réserve. Détail dans `exploitation.md`.
- 2026-11-02 — Décision suivi SOC à distance : CPL sur le réseau 230 V de l'onduleur plutôt qu'un câble Ethernet en tranchée. Pourquoi : affichage à l'atelier **et** à la chaumière (lieux d'usage éloignés), boîtiers déjà possédés (2 modèles, 3-4 ex. chacun), rien à acheter. Limites connues : l'affichage tombe si l'onduleur ou le futur limiteur coupe le 230 V ; ~2-4 W par boîtier en continu.
- 2026-11-01 — Départ fin de chantier d'octobre : installation entièrement coupée (sectionneur PV → EasySolar → sectionneur batterie), batterie laissée à ~90 % (pas de décharge vers 50-60 %, écart jugé négligeable sur quelques mois). Tour de vérif de l'installation : rien d'anormal. Peu d'usage prévu avant printemps/été 2027.
- 2026-11-01 — Décision surcharge : le seuil de surcharge de l'EasySolar n'est pas réglable (vérifié doc Victron) et le C25 de départ ne limite pas la puissance → limiteur à mettre en place au prochain retour (relais GX + contacteur auto-maintien + réarmement accessible). Pourquoi : protéger la batterie (100 A continu) d'un usage partagé où personne ne voit la puissance totale.
- 2026-10-31 — Test de dépassement : ~2 900 W / ~115 A sans coupure, seulement une alarme Overload sur le GX.
- 2026-10-31 — Test de charge : ~2 300 W AC = ~92 A batterie, arrêté là. Limite = BMS 100 A. Le MK3 branché sur le VE.Bus empêchait le GX de lire l'onduleur (Output absent de l'afficheur) : à débrancher après chaque usage.
- 2026-10-31 — MPPT passé en préconfiguration Smart Lithium (LiFePO4) depuis le téléphone : 28,4 / 27,0 V, coupure basse température 5 °C.
- 2026-10-31 — Profil LiFePO4 appliqué sur l'EasySolar (partie VE.Bus, via VictronConnect Mac + MK3, mdp `ZZZ`) : détail dans `exploitation.md`. Câble VE.Direct SmartShunt posé. Reste : MPPT (réglages séparés, via Bluetooth) et choix du SmartShunt comme moniteur batterie dans le GX.
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
