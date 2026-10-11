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
- Limite BMS 100 A ≈ ~1 800 W AC en continu (24 V × 100 A × 0,9). Résistance du lave-linge = au taquet → usage opportuniste en journée ensoleillée.
- Irradiation PVGIS décembre (Bretagne, plan incliné) ≈ 1 kWh/m²/j.

## Outils
- **VictronConnect** (Bluetooth, accès direct au SmartShunt).
- **GX Remote Console** : Wi-Fi local de l'EasySolar, navigateur sur IP locale, sans internet.
- **VRM** : cloud, internet requis. Carte SD dans le GX = log CSV continu, téléversable après coup (utile pour le 1er hiver).
- **VEConfigure** : Windows + MK3-USB.
