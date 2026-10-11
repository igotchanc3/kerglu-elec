# Matériel — référence unique des valeurs techniques

> Sources : fiche Notion « Suivi » (11/10/2026) + factures de `commandes/` (détail des achats et prix : `commandes.md`).
> Les lignes marquées ⚠️ sont à confirmer sur site (voir `a-verifier.md`).

## Production PV (toiture brocante)
| Élément | Référence / valeur |
|---|---|
| Panneaux | 2× Trina Vertex S+ 500 Wc biverre/bifacial, **en série** — par panneau : Voc 40,1 V, Vmpp 33,3 V, Isc 15,86 A, Impp 15,03 A ; Voc string à froid ≈ 100 V |
| Fixation (toiture ardoise) | Novotegra : 6 crochets ardoise, 2 rails alu 2,40 m, 4 cales d'extrémité 30-42 C noir, 2 cales centrales 30-42 C noir, 4 caches fin de rail C47 |
| Liaison panneaux → coffret DC | Unicable 6151 BR, 15 m, 6 mm², MC4 ⚠️ pas de facture |
| Terre panneaux | H07V-K 6 mm² V/J (25 m) — agrafes Rayvolt IZIRV03 ×7 (câble/panneaux) — kits ESI2 ESI2ASEK02 ×4 (câble/rails) |
| | Kits IZIPV IZIASEK01 ×4 (T-bolt) ⚠️ usage à préciser |

## Coffret DC PV
| Élément | Référence / valeur |
|---|---|
| Coffret | IDE CDN12PT/RR, 12 modules, IP65 |
| Sectionneur | Sectionneur solaire 600 Vdc / 25 A |
| Parafoudre DC | Citel DS 600/51, type 2 (facture : « Parafoudre DC 600/51 », marque non indiquée) |
| Terre coffret | PE 10 mm² (H07V-R rigide V/J) → répartiteur de terre |

## Armoire de production
| Élément | Référence / valeur |
|---|---|
| Onduleur-chargeur | Victron EasySolar-II GX 24/3000/70-32 (MPPT 250/70 + GX intégrés) — [manuel](https://www.victronenergy.com/upload/documents/EasySolar-II_GX/11230-EasySolar-II_GX-pdf-fr.pdf) |
| Câbles PV → onduleur | Câble solaire 6 mm² (3 m rouge + 3 m noir), cosses M6 |
| Terre onduleur | PE 6 mm², cosse M6 |
| Batterie | Redodo LiFePO4 24 V 100 Ah, BMS 100 A, protection charge basse température ⚠️ pas de facture |
| Câbles batterie | 50 mm² extra souple, sur mesure : 30 cm M8–M8 rouge · 30 cm M8–M10 rouge · 30 cm M8–M10 noir · 50 cm M8–M10 rouge · 50 cm M8–M10 noir ⚠️ affectation de chaque câble à relever |
| Fusible batterie | Fusible MEGA 125 A + porte-fusible Victron MEGA ⚠️ acheté, pose à confirmer |
| Sectionneur batterie | Victron coupe-batterie 275 A ⚠️ acheté, pose à confirmer |
| Shunt | Victron SmartShunt 300 A / 50 mV (IP65) — **pas encore raccordé** à l'onduleur (câble VE.Direct à commander) |
| Interface | Victron MK3-USB-C (pour VEConfigure) |

## Coffret AC (armoire)
| Élément | Référence / valeur |
|---|---|
| Coffret | IDE CDN12PT/RR, 12 modules, IP65 ⚠️ (2 achetés : 1 coffret DC + 1 coffret AC ?) |
| Câble | R2V 3G6 ⚠️ rôle « entrée » à préciser |
| **Circuit brocante** | Interrupteur différentiel Legrand DX³ 2P 40 A 30 mA type A (LEG411617) |
| | Disjoncteur DNX³ 1P+N 20 A courbe C (LEG406784) |
| | Disjoncteur DNX³ 1P+N 10 A courbe C (LEG406782) |
| | Prise modulaire 2P+T 16 A (LEG004280) |
| **Départ chaumière** | Disjoncteur DNX³ 1P+N 25 A courbe C (LEG406776) |
| | Parafoudre DEHN type 2 15 kA 230 V débrochable (952179) |

## Mise à la terre
| Élément | Référence / valeur |
|---|---|
| Prise de terre | Kit starter 123elec PACKTERRE01 : 1 piquet 1 m + tresse cuivre 25 mm² |
| Barrette de coupure | Tresse 25 mm² ↔ PE 16 mm² |
| Répartiteur | Batilec Q832, 35 mm², 5 départs, alimenté en PE 16 mm² |
| Départs du répartiteur | PE 6 mm² panneaux + rails · PE 6 mm² onduleur · PE 10 mm² coffret DC · PE 10 mm² bornier de terre (coffret AC) · 1 libre |

## Chaumière (à réaliser)
| Élément | Référence / valeur |
|---|---|
| Liaison | R2V 3G6 armoire → tableau divisionnaire (PE inclus, pas de 2e piquet) |
| Tableau | IDE CDN18PT/RR 18 modules IP65 — différentiel 40 A/30 mA type A, ~6 disjoncteurs, peigne HX³, parafoudre DEHN AC 15 kA (composants sur site) ⚠️ un seul DEHN acheté |
| Hauteurs de pose | Prises : axe 25 cm · interrupteurs : 110 cm |

## Stock (acheté, d'après les factures)
Bilan des achats d'appareillage, pour savoir ce qui reste dispo pour la chaumière. « Posé » = d'après les sections ci-dessus.

| Article | Acheté | Posé (coffret AC) | Reste |
|---|---|---|---|
| Interrupteur diff. DX³ 2P 40 A 30 mA type A (LEG411617) | 2 | 1 | 1 |
| DNX³ 1P+N C25 (LEG406776) | 1 | 1 | 0 |
| DNX³ 1P+N C20 (LEG406784) | 4 | 1 | 3 |
| DNX³ 1P+N C16 (LEG406783) | 1 | 0 | 1 |
| DNX³ 1P+N C10 (LEG406782) | 5 | 1 | 4 |
| Peigne 13 appareils 1P+N (LEG404926) | 3 | ? | ? |
| Prise modulaire 2P+T 16 A (LEG004280) | 2 | 1 | 1 |
| Parafoudre DEHN 952179 | 1 | 1 | 0 |
| Coffret IDE 18 modules (CDN18PT/RR) | 1 | 0 | 1 |
| R2V 3G6 | 25 m + 50 m | ? | ? |
| Wago 221-615 (5 × 6 mm²) | 15 | ? | ? |
| Presse-étoupes | 5 × M25 Batilec, 5 × M20 Batilec, 5 × M20 Schneider Mureva | ? | ? |
| H07V-R 10 mm² V/J | 7 m | ? | ? |
