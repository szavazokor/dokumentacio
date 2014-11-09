# Szavazókör

Szavazókörnek nevezem a komplett rendszert a szavazóegységekkel, a busszal, tápegységgel, tokkal-vonóval.

A szavazókört számítógépen keresztül lehet vezérelni, szavazni pedig emberenként külön-külön, dedikált szavazóegységekről párhuzamosan lehet.

## Busz
Megnevezés   |  Busz
-------------|--------------
Darabszám    |	1 / szavazókör
Fő feladat   |	Szavazóegységek tápfeszültséggel való ellátása és jelkapcsolat biztosítása
Megvalósítás |	Tíz- vagy többeres szalagkábel
Költség	     |  < 1000 Ft / db

A busz egyrészt egy tápforrás a szavazókörben lévő összes egység számára, másrészt egy CAN típusú kommunikációs busz, amin keresztül a vezérlőegység kommunikál a szavazóegységekkel szavazás előtt, és a szavazóegységek kommunikálnak a vezérlőegységgel, miután a szavazás megtörtént.

A tápellátás egy külön tápmodulon keresztül a villamos hálózatról jön, a vezérelni egy vezérlőegységen keresztül PC-ről lehet, és a szavazóegységek közvetve, csatlakozómodulokon keresztül csatlakoznak a buszra.

## Szavazóegység

Megnevezés | Szavazóegység
-----|-----
Darabszám	| annyi, amennyi a szavazók száma
Fő feladat |	A szavazók ezt nyomogatva tudnak szavazni
Megvalósítás |	Saját gyártású NYÁK, mikorkontroller, HMI
Költség |	< 2000 Ft / db

A szavazóegység az az eszköz, ami minden szavazó előtt ott van, hogy egy vagy pár gombnyomással leadhassa a szavazatát. A pontos specifikáció még nyitott kérdés, különböző bonyolultságú eszközről is lehet szó attól függően, hogy a költségek mennyire korlátozzák a fantáziánkat.

Egyéb
- Lásd az Alapszolgáltatások és a Lehetséges szolgáltatások címszó alatt.

##Tápmodul

Megnevezés | Tápmodul
---|---
Darabszám |	1 / szavazókör
Fő feladat |	Energiaellátás biztosítása
Megvalósítás |	Boltban kapható AC/DC tápegység és saját gyártású NYÁK
Költség	| < 1000 Ft / db

A tápegység modult kell a konnektorba dugni ahhoz, hogy ellássa feszültséggel a rendszert. A busz egyik végére csatlakozik, ahol a tápot és a földet adja az összes modulnak.

Egyéb
- A CAN busz egyik lezárását is ez adja.

##Csatlakozómodul

Megnevezés | Csatlakozómodul
---|---
Darabszám |	0,5 / szavazóegység
Fő feladat |	Busz meghosszabbíthatóságát biztosítja, és erre csatlakoztathatók a szavazóegységek közvetlenül.
Megvalósítás |	Saját gyártású NYÁK
Költség |	< 500 Ft / db

A csatlakozómodul két feladatot lát el. Egyrészt ráköthető két buszvég, egy aktív (feszültség alatt lévő), és egy ami a csatlakozómodulon keresztül részévé válik az aktív busznak. Másrészt a szavazóegységek is közvetlenül erre köthetőek rá, így ezen keresztül közvetlenül csatlakoznak a buszra.

Egyéb
- Hogy kevsebb csatlakozómodulra legyen szükség, egy csatlakozómodulra több, két-három szavazóegység is közvetlenül kapcsolható.
- A CAN busz másik lezárása is egy csatlakozómodul használható.
