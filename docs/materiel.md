# Matériel — référence unique des valeurs techniques

> Source initiale : fiche Notion « Suivi » (kerglu_elec), état au 11/10/2026.
> Les lignes marquées ⚠️ sont à confirmer sur site (voir `a-verifier.md`).

## Production PV (toiture brocante)
| Élément | Référence / valeur |
|---|---|
| Panneaux | 2× Trina Vertex S+ 500 Wc bifacial, **en série** — par panneau : Voc 40,1 V, Vmpp 33,3 V, Isc 15,86 A, Impp 15,03 A ; Voc string à froid ≈ 100 V |
| Liaison panneaux → coffret DC | Unicable 6151 BR, 15 m, 6 mm², MC4 |
| Terre panneaux | H07V-K 6 mm² V/J — agrafes Rayvolt IZIRV03 (câble/panneaux) — kit ESI2 ESI2ASEK02 (câble/rails) |

## Coffret DC PV
| Élément | Référence / valeur |
|---|---|
| Coffret | IDE CDN12PT/RR, 12 modules, IP65 |
| Sectionneur | Sectionneur solaire 600 Vdc / 25 A |
| Parafoudre DC | Citel DS 600/51, type 2 |
| Terre coffret | PE 10 mm² → répartiteur de terre |

## Armoire de production
| Élément | Référence / valeur |
|---|---|
| Onduleur-chargeur | Victron EasySolar-II GX 24/3000/70-32 (MPPT 250/70 + GX intégrés) — [manuel](https://www.victronenergy.com/upload/documents/EasySolar-II_GX/11230-EasySolar-II_GX-pdf-fr.pdf) |
| Câbles PV → onduleur | 6 mm², cosses M6 |
| Terre onduleur | PE 6 mm², cosse M6 |
| Batterie | Redodo LiFePO4 24 V 100 Ah, BMS 100 A, protection charge basse température |
| Câbles batterie | 50 mm², cosses M8 |
| Fusible batterie | ⚠️ MEGA 125 A (présent sur site d'après inventaire d'août, emplacement à confirmer) |
| Sectionneur batterie | ⚠️ à confirmer |
| Shunt | Victron SmartShunt 300 A (IP65) — **pas encore raccordé** à l'onduleur (câble VE.Direct à commander) |
| Interface | Victron MK3-USB (pour VEConfigure) |

## Coffret AC (armoire)
| Élément | Référence / valeur |
|---|---|
| Câble | R2V 3G6 (couronne 50 m) ⚠️ rôle « entrée » à préciser |
| **Circuit brocante** | Interrupteur différentiel Legrand DX³ 2P 40 A 30 mA type A (LEG411617) |
| | Disjoncteur DNX³ 1P+N 20 A courbe C (LEG406784) |
| | Disjoncteur DNX³ 1P+N 10 A courbe C (LEG406782) |
| | Prise modulaire 2P+T 16 A (LEG004280) |
| **Départ chaumière** | Disjoncteur DNX³ 1P+N 25 A courbe C (LEG406776) |
| | Parafoudre DEHN type 2 15 kA 230 V débrochable (952179) |

## Mise à la terre
| Élément | Référence / valeur |
|---|---|
| Prise de terre | Kit starter 1 piquet 1 m + tresse cuivre 25 mm² |
| Barrette de coupure | Tresse 25 mm² ↔ PE 16 mm² |
| Répartiteur | Répartiteur de terre 35 mm², 5 départs, alimenté en PE 16 mm² |
| Départs du répartiteur | PE 6 mm² panneaux + rails · PE 6 mm² onduleur · PE 10 mm² coffret DC · PE 10 mm² bornier de terre (coffret AC) · 1 libre |

## Chaumière (à réaliser)
| Élément | Référence / valeur |
|---|---|
| Liaison | R2V 3G6 armoire → tableau divisionnaire (PE inclus, pas de 2e piquet) |
| Tableau | IDE 18 modules IP65 — différentiel 40 A/30 mA type A, ~6 disjoncteurs, peigne HX³, parafoudre DEHN AC 15 kA (composants sur site) |
| Hauteurs de pose | Prises : axe 25 cm · interrupteurs : 110 cm |
