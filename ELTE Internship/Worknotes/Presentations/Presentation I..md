# Speech
## Motiváció:
A téma vezetőm által kiadott hasonlók projekteket átnéztem
- Elsősorban numerikus módszerek
- Nem-valós idejű módszerek

Ezzel ellentétben:
- Ray tracing, valós idejű 

## Szonár technológia:
A szakmai gyakorlat kezdete óta . . .
- Hogyan is működik egy szonár, milyen fajtái vannak. . .
- Passzív szonár vs. aktív szonár: 
	- Passzív szonár: környezete által kibocsátott hang feldolgozása
	- Aktív szonár: általa kibocsátott, környezete által visszavert hang feldolgozása
	- Katonai alkamazások
- Konkrétabb szonár fajták szimulálása (pl. bi-statikus szonár, stb.)


## Hang terjedése:
Rátérnék a hanghullámok terjedésére élővizekben, hiszen . . .
- elsősorban pont ezt akarjuk szimulálni alkalmazásunkkal.
- eléggé komplex témakör
### I.: 
A hang terjedésének útjában a következőt kell figyelembe venni:
- Gömb alakú terjedés - elsősorban a hanghullám kezdeti szakaszában
- Cilinder formájú terjedés - elsősorban akkor használják, amikor a hanghullám eléri a vízoszlop magasságának felét
### II.: 
Ezenkívül a hang terjedését a körülvevő médium is befolyásolja:
- hőmérséklet
- mélység
- környező víz sótartalma
- víziélőlények
A vízoszlop több rétegből épül fel:
- az ábrán található hogy a különböző rétegekben hogyan változik a hang terjedésének sebessége
=> Ez hatással van a hang maximum hatótávolságára (képek)

### III.:
Fontos: évszakonkénti változás, illetve napszakonkénti változás.
. . . ennek szimulálása is fontos a pontos eredmények érdekében

### IV.: 
A hang terjedéséből adódóan különböző jelenségeket lehet megfigyelni:
- Árnyék zóna - tengeralattjárók által preferrált mélység

### V.:
- Hangcsatornák - negatív SVP gradiens a pozitív SVP gradiens felett -> ebből adódóan egy adott mélységben használnak szonárt ennek kihasználására. 

### VI.:
- Konvergencia zónák: hanghullámok koncentrálódnak adott, szabályos intervallumú gyűrűkben a vízfelszínen, amellyel hajókat/tengerallatjárókat lehet észlelni. 
- . . . tudnak reagálni a különböző helyzetekre
## Hang visszaverődés
Ezenkívül szükséges a hang visszaverődését is megvizsgálni:
- vízfelszínről való visszaverődés
	- hullámok nagysága, sokasága
- tengerfenékről való visszaverődés
	- anyagminőség befolyásolja az elnyelt hang mennyiségét, illetve annak szétszórásának mértékét

## Sugárkövetés
Egyszerű példa megemlítése: 
- nagyjából a képen láthatókat elmagyarázni
- árnyék vetés, tükröződések, stb.

Korábban csakis offline renderingnél lehetett effektíven használni, ez azóta megváltozott az RTX API-val . . .
## RTX/DXR
- két struktúra kis magyarázata, miért segíti a sugárkövetés

## Implementáció


## Jövőre nézve...
- szonár implementálása
- kiadott irodalom feldolgozása
- kis magyarázat, hogy miért csak itt tart a projekt:
	- DirectX 12 + DXR megtanulása
	- eleinte nehézségek a fejlesztői környezet kialakulásában