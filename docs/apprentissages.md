# Apprentissages techniques

## Batterie et suivi du SOC
- La courbe de tension LiFePO4 est trop plate pour estimer le SOC à la tension → le **SmartShunt** (comptage coulombmétrique, VE.Direct vers le GX) est indispensable.
- Le Bluetooth du BMS Redodo ne parle qu'à l'appli Redodo, pas au GX Victron.
- **VEConfigure obligatoire avant tout fonctionnement sans surveillance** : l'EasySolar sort d'usine avec un profil plomb qui abîme le LiFePO4. Nécessite MK3-USB + Windows. VEConfigure à distance via VRM = internet nécessaire, peu fiable sur site.
- Synchro SmartShunt à 100 % seulement si tension « Charged », courant de queue et durée de détection sont réunis. Régler « Charged voltage » vers 27,6-27,8 V pour éviter les fausses synchros en fin de journée.
- Stockage longue durée : idéal ~50 % SOC, 75 % acceptable, jamais 100 %.

## Sécurité DC
- MC4 de **même marque** obligatoirement (sinon risque d'arc).
- Pas de jonction nu-à-nu en DC.
- La string est sous tension dès qu'il y a de la lumière ; ne jamais déconnecter des MC4 en charge.
- Séquence : batterie **en dernier** à la mise sous tension, **en premier** à l'isolement.
- Parafoudres en dérivation, jamais en série ; longueur totale conducteurs de raccordement + terre < 50 cm.

## Terre
- Un seul piquet au bâtiment de production ; le PE suit le R2V jusqu'à la chaumière (pas de 2e piquet → pas de différence de potentiel).
- Toutes les terres PV et parafoudres convergent vers le même répartiteur.
- PE nu au contact du bois : pas de risque en fonctionnement normal (courant négligeable, défaut coupé en ms par le différentiel).
- Les terminaisons VE.Can (RJ45) restent en place sur les deux ports VE.Can ; le SmartShunt utilise VE.Direct.

## Bilan énergétique
- Consommation à vide EasySolar ~10-15 W en continu (~300 Wh/j) : poids important en hiver.
- Puissance ≠ énergie ; un calibre de disjoncteur protège le câble, pas l'appareil.
- Limite BMS 100 A ≈ 2 300-2 400 W AC (mesuré : 2 300 W ≈ 92 A, 2 900 W ≈ 115 A). La puissance continue de l'onduleur (2 400 W à 25 °C) tombe pile à ~100 A batterie. Résistance du lave-linge = au taquet → usage opportuniste en journée ensoleillée.
- Irradiation PVGIS décembre (Bretagne, plan incliné) ≈ 1 kWh/m²/j.

## Limiter le courant batterie (étude 02/11/2026)
- Un onduleur ne peut pas « brider » une charge : il fournit ou il coupe. Pas de réglage de puissance max en sortie sur l'EasySolar.
- Le **GX intégré à l'EasySolar-II n'a pas de relais** (contrairement au Cerbo GX) : pas de « Generator start/stop » sur le courant batterie. Seul le relais programmable de la partie MultiPlus existe, piloté par Assistants (VEConfigure), qui ne voit pas le SmartShunt.
- Le **SmartShunt n'a ni relais ni alarme programmable**. Le BMV-712 a un relais, mais seulement sur tension/SOC, pas sur courant. La limite de décharge (DCL/DVCC) n'existe qu'avec une batterie communicante (CAN), pas la Redodo.
- **Ne jamais déconnecter la batterie pendant que le PV produit** (règle Victron pour le MPPT) → pas de disjoncteur/contacteur côté DC batterie comme limiteur.
- Disjoncteur thermique : ne déclenche pas à 1,13 × In (1 h), déclenche à 1,45 × In en < 1 h. Un « 100 A » ne coupe donc pas à 100 A.
- Usure LiFePO4 : s'accélère avec le courant de décharge (ordre de grandeur, sources de vulgarisation : ~6 000 cycles à 0,5C contre ~2 500 à 1C). Coût de base Redodo ≈ 0,04 €/kWh tiré (≈ 350-430 € / 4 000 cycles × 2,56 kWh).
- Node-RED (Venus OS Large) est compatible EasySolar-II GX : peut lire le SmartShunt et passer l'onduleur en « chargeur seul » (sans support officiel Victron).

## Outils
- **VictronConnect** (Bluetooth, accès direct au SmartShunt).
- **GX Remote Console** : Wi-Fi local de l'EasySolar, navigateur sur IP locale, sans internet.
- **VRM** : cloud, internet requis. Carte SD dans le GX = log CSV continu, téléversable après coup (utile pour le 1er hiver).
- **VEConfigure** : Windows + MK3-USB.
- Le MK3-USB branché sur le port VE.Bus (avec VictronConnect ouvert) bloque la lecture de l'onduleur par le GX : le débrancher après chaque session de réglage.
