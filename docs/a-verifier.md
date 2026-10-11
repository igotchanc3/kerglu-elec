# À vérifier / questions ouvertes

## Écarts entre l'inventaire d'août et la fiche Notion d'octobre
- [ ] **Fusible MEGA 125 A et coupe-batterie 275 A** : posés (confirmé par Polar le 11/10). Reste à relever l'ordre côté + (batterie → MEGA → coupe-batterie → onduleur ?) pour le schéma.
- [ ] **Bâtiment** : la fiche parle de « brocante » ; les anciennes notes de « bâtiment ardoise ». Même bâtiment ? (Indice : les fixations panneaux achetées sont des crochets pour ardoise.)

## Factures (ajoutées le 11/10/2026)
- [ ] Fournisseur de la facture **FA44810771** (câbles batterie) : nom non lisible dans le PDF.
- [ ] **Kits IZIPV IZIASEK01 ×4** : utilisés pour quoi (en plus des kits ESI2 et des agrafes Rayvolt) ?
- [ ] **2 coffrets IDE 12 modules** achetés : confirmer = 1 coffret DC + 1 coffret AC.
- [ ] **R2V 3G6** : 25 m + 50 m achetés. Lequel sert à quoi, et combien en reste-t-il ?

## Coffret AC
- [ ] ⚠️ **Départ chaumière sans 30 mA** : Q6 (C25) est en parallèle du différentiel (Wago). Le R2V enterré et le tableau chaumière (en amont de son différentiel) ne sont protégés par aucun 30 mA. Avec un onduleur comme source, le courant de court-circuit est limité, donc le C25 risque de ne pas déclencher sur défaut. **Décision à prendre avant de tirer le câble** : mettre un 30 mA sur le départ chaumière dans l'armoire (le DX³ de réserve ?), quitte à en racheter pour le tableau chaumière.
- [ ] Sections posées : Q4 (C20, prises) → 2,5 mm² minimum requis ; Q5 (C10, éclairage) → 1,5 mm² minimum. Relever ce qui est posé (marquage sur la gaine).

## Mise en service
- [ ] **Liaison N–PE en sortie de l'EasySolar** (le PE, lui, est continu) : normalement faite par le relais de terre interne en mode onduleur. Test : onduleur seul en marche, sur la prise X1 mesurer N–PE ≈ 0 V et L–PE ≈ 230 V. Si N–PE ≈ 115 V, le neutre est flottant et le 30 mA ne protège pas.
- [ ] Synoptique : un trait de terre arrive sur le coupe-batterie — volontaire ? (pas repris dans l'unifilaire)
- [ ] Profil LiFePO4 VEConfigure : valeurs à recouper avec la fiche technique Redodo.
- [ ] Câble VE.Direct SmartShunt → EasySolar à commander.
- [ ] Interface de suivi du SOC depuis la chaumière : Remote Console en Wi-Fi local suffit-il à 15-20 m ? Sinon Cat6 dans la tranchée.
