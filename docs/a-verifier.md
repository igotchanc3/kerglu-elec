# À vérifier / questions ouvertes

## Écarts entre l'inventaire d'août et la fiche Notion d'octobre
- [ ] **Fusible MEGA 125 A (+ porte-fusible Victron) et coupe-batterie Victron 275 A** : achetés (facture FA008830), absents de la fiche « Suivi ». Sont-ils installés ? Ordre côté + : batterie → MEGA → coupe-batterie → onduleur ?
- [ ] **Parafoudre DC** : fiche = Citel DS 600/51 ; inventaire d'août mentionnait aussi un DEHN type 2 DC. Lequel est posé ?
- [ ] **Bâtiment** : la fiche parle de « brocante » ; les anciennes notes de « bâtiment ardoise ». Même bâtiment ? (Indice : les fixations panneaux achetées sont des crochets pour ardoise.)

## Factures (ajoutées le 11/10/2026)
- [ ] Pas de facture pour la **batterie Redodo** ni l'**Unicable 6151 BR** : achetés ailleurs / par quelqu'un d'autre ? Ajouter les PDF à `commandes/` si possible.
- [ ] Fournisseur de la facture **FA44810771** (câbles batterie) : nom non lisible dans le PDF.
- [ ] **Câbles batterie** : 5 câbles 50 mm² (dont 4 avec une cosse M10). Relever lequel va où (batterie, MEGA, coupe-batterie, SmartShunt, onduleur).
- [ ] **Kits IZIPV IZIASEK01 ×4** : utilisés pour quoi (en plus des kits ESI2 et des agrafes Rayvolt) ?
- [ ] **Parafoudre DEHN 952179** : un seul acheté, mais prévu à la fois dans le coffret AC (départ chaumière) et dans le tableau chaumière. En racheter un, ou un seul suffit-il (distance armoire–tableau ≈ 20 m) ?
- [ ] **2 coffrets IDE 12 modules** achetés : confirmer = 1 coffret DC + 1 coffret AC.
- [ ] **R2V 3G6** : 25 m + 50 m achetés. Lequel sert à quoi, et combien en reste-t-il ?

## Coffret AC
- [ ] « Entrée R2V 3G6 » : liaison onduleur → coffret AC, ou départ vers la chaumière ? (Le départ chaumière reste à tirer d'après les prochaines étapes.)
- [ ] Le départ chaumière (disj. 25 A + parafoudre DEHN) est-il **en aval du différentiel 40 A/30 mA** ou en direct ? Si en direct, prévoir la protection différentielle en tête du tableau chaumière (sélectivité à réfléchir).
- [ ] Circuits 20 A et 10 A de la brocante : qu'alimentent-ils ? Sections associées ?

## Mise en service
- [ ] Profil LiFePO4 VEConfigure : valeurs à recouper avec la fiche technique Redodo.
- [ ] Câble VE.Direct SmartShunt → EasySolar à commander.
- [ ] Interface de suivi du SOC depuis la chaumière : Remote Console en Wi-Fi local suffit-il à 15-20 m ? Sinon Cat6 dans la tranchée.
