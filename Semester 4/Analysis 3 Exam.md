# Definíciók:
## Torlódási pont
- halmazok torlódási pontjainak halmaza
## Belső pont
- halmazok belső pontjainak halmaza
## Lineáris korlátos lekézpések:
- absztrakt (2 N.T. között)
- korlátos
- homogén + additív
- ezen függvények tere
- egy ilyen függvény korlátjainak tere
## Mátrixnormák:
- $f_A$ fv. ahol $f_A(x) = A*x$
- Ekkor ő lineáris, és korlátos 
- Korlátos, mert -> megmutatjuk $\infty$ normára, hogy az
## Differenciálhatóság:
- $\exists$L $\in$ L(X,Y)ött)
- korlátos
- homogén + additív
- ezen függvények tere
- egy ilyen függvény korlátjainak tere
​￼￼￼Mátrixnormák:
- ￼￼ fv. ahol ￼￼
- Ekkor ő lineáris, és korlátos 
- Korlátos, mert -> megmutatjuk ￼￼ normára, hogy az
​￼￼￼Differenciálhatóság:
- ￼￼L ￼￼ L(X,Y)
- ￼￼ ￼￼ X -> Y, lim ￼￼ = 0, ha h -> 0
- f(a + h) - f(a) = L(h) + ￼￼(h) * ￼￼ 
- $\exists \eta$ $\in$ X -> Y, lim $\eta$ = 0, ha h -> 0
- f(a + h) - f(a) = L(h) + $\eta$(h) * $||h||$ 
## Többváltozós fv. Riemann integrálása:
- Alsó közelítő összeg
- Felső közelítő összeg
- Osztás intervallum
- 6 db tulajd.
## Integrál alkalmazások:
- Felszín/felület:
	- vektoriális szorzat
	- integrál közelítő összeg
- Fluxus:
- Tömeg:
	- $\rho$ - sűrűség
- Nyomaték:
	- $\rho$ - sűrűség
	- r:= egyenes és pont távolsága
- súlypont:
	- $\rho$ - sűrűség
	- minden koordinátát külön-külön

## Egyenletes konvergencia

## Pontonkénti konvergencia

## Konvergencia def.

## Konvergencia ekv. def. környezetekkel

# Tételek / Theorems
## A zárt <=> A' $\subset$ A:
- indirekt
-  => :
	- A zárt -> X/A nyílt
	- $\exists$ x $\in$ A', hogy x $\notin$ A => x $\in$ X/A
	- x belső pont -> létezik környezete, ahol mindegyik pont $\in$ X/A-ban
	- viszont torlódási pont is => ellentmondás a def. alapján

## z torlódási pont <=> $K_r(z)\ \cap\ A\   végtelen$:
- <= Trivi. (ha végtelen akkor nem csak z az eleme)
- => :
	- INDIREKT
	- legyen véges ekkor
	- keressük meg a környezetben a legközelebbi elem és z távolságát
	- ekkor vegyünk egy ennél kisebb sugárral egy környezetet -> ellentmondás
## Konvergencia: $\alpha$ egyértelműsége:
- tfh.: létezik egy ilyen $\beta$ határérték
- mondjuk ki erre is a definíciót
- majd $\rho$($\alpha$,$\beta$)-t felül és alul becsüljük 0-val -> közrefogási elv
## $\forall z$ esetén $\rho$($x_n$,z) -> $\rho$($\alpha$,z), ha $x_n \to  \alpha$:
- felülbecslés és átrendezéssel
- nullsorozatok alkalmazása
## A zárt <=> minden A-beli konvergens sorozat A-beli elemhez konvergál:
- <=> 
- => : 
	- INDIREKT
	- X/A nyílt -> belső pont def.
	- konvergencia ekv. def. környezetekkel
- <= : 
	- INDIREKT
	- X/A sem nyílt
	- 1/n sugarú körny. 
	- $\exists$y $\in$ A $\cap$ K(b) -> minden 1/n sugarú körny. igaz lesz
	- $\rho (y_n,b) < 1/n$, de 1/n -> 0 és y_n A beli -> b-hez konvergál, ami nem A-beli
	- így ellentmondás
## Vektorsorozatok konvergenciája:
- <=>
- $(\mathbb K^s,\rho_p)$ 
- fel lehet tenni, hogy p = $\infty$ (p-ad metrika ekvivalencia)
- => ha max-ra igaz,minden i-re igaz
- <= vegyük a maximum küszöbindexet -> ekkor maxra is igaz
## Bolzano-Weierstrass tétel:
- koordináta sorozatok konvergenciája és ennek implikációja
- konvergens sorozat részsorozata is konvergens
- 3 indexsorozat
## $(C[a,b],\rho_\infty)$ teljes M.T.
- Kiind.: egy az M.T.-n Cauchy sorozatból
1. Pontonként konvergens
2. Fontos rész: | fn(x) - f(x) | = lim m -> inf ( |fn(x) - fm(x)| ) 
3. f $\in$ C[a,b] <- fn $\in$ C[a,b]
4. felülbecslés -> valóban konvergens
5. fontos részre visszautalás -> mihez is konvergál

## Létezik minimuma $K_f$-nek:
- INDIREKT
- infinum def. 
- infinum + r-ra is még igaz, hogy kisebb mint valamilyen ||f(x)|| (r > 0) -> ilyen r létezik, mert x nem lehet 0 ekkor (különbön trivi az állítás)
## Set theory 
- Nyílt halmazok uniója
	- végtelen mennyiségű halmazokra is
	- indexelő halmaz
	1. : elemek B_i-ből  
	2. : B_i nyílt -> létezik körny.
	3. : körny részh. B_i és B_i részh. unió
- Nyílt halmazok metszete
	- csak véges indexelő halmaz
	1. elem metszetből
	2. ennek részh. van minden B_i-vel
	3. minimum R -> körny. min R sugárral részh. minden B_i-nek, azaz metszetnek is
- Zárt halmazok uniója
	- De Morgan
	- csak megmutatjuk a komplementerre, hogy nyílt, mert akkor az unió valóban zár
- Zárt halmazok metszete
	- De Morgan
	- csak megmutatjuk a komplementerre, hogy nyílt, mert akkor a metszet valóban zárt

## Fv. deriválthatósága a-ban <=> Fv. i-edik koord. fv-e deriválhatósága a-ban
- <=> 
- => $\eta$ fv. limesze 0 h -> 0-ban => minden koord. fv-re is igaz lesz
-    ekkor def. szerint differenciálhatóság
- <= $\eta_i$ fv. limesze 0 h -> 0-ban => konstruálható egy olyan $\eta$ amire ez is igaz lesz

## Banach-féle fixponttétel
- Banach-féle fixponttétel
	- teljes MT-kre
	- 5 lépés:
	1. Telj. indukció -> minden $\rho$(x_n,x_n+1) <= $\rho$(x_0,x_1) * q
	2. megmutatjuk, hogy Cauchy krit. teljesül -> q^n / (1-q) * $\rho$(x_0,x_1) felül becsléssel
		- Mivel teljesül, és teljes az M.T. -> konvergenes is
	3. A határértéke fixpont
	4. A fixpont egyértelmű
	5. Hibabecslés megadása (lim segítségével)
## Lok. szélső érték tételek (3 db):
### Lok. sz.é. elsőrendű szüks. feltétele: 

- irányt menti parc. deriváltakkal
- F : R -> R fv-vel
- valós, 1 változós fv. az azonos tétel meg van -> F-re alkalmazzuk
- F (-r,r)-en
### Lok. sz.é. elégséges feltétele:
- maximum és minimum esetén hasonlóan -> elég 1, de másikra is érdemes kitérni
- >= a becsléseknél
- m/2 + éta(h) > 0 megmutatása
- a + h eleme Df-nek (belső pontból adódóan )
### Lok. sz.é. másodrendű szüks. feltétele:
- 2. eset: max és min -> elég egyik, másik hasonlóan
- belső pont és lok. sz.é. kihasználása
- INDIREKT
## Young tétel:
- Delta függvény
- Fí függvény
- (-r,r) intervallum
- grad_delta_1_f(a)
- Lagrange k.é.t.
- ugyanez u := v esetre is -> jobb oldali limeszek megegyeznek
## Összetett fv. diff.:

- a $\in$ int $D_g$ esetén a int D_f o g is teljsül
- f és g diff.-ból kiindulva, megmutatjuk a f o g-t is
## Kvadratikus alak folyt.:
- Q(x) folyt.:
	- rengeteg felső becslés
	- kihozzuk a folytonosság definíciójára 
	- az a lényeg, hogy Q-kból kiindulunk, és egy vektornormával fejezzük be a becslést, ami 0-hoz tart
## Differenciálhatóság parciális deriváltakból adódóan egyéb feltételekkel:
- feltételek: összes, kivéve egy parciális derivált létezik egy a középpontú környezet minden elemén, illetve folytonosak a-ban ILLETVE egy parciális derivált csak létezik-ban.
- Lagrange k.é.t. a folytonosokra
- a 'csak' létező-re: létezik éta is 
- 3 pont -> A B és C -> A és B között csak x, B és C között csak y koordináta változik
$$ a \in int\ D_f, \ \ r > 0,\ \ \forall x\ \in D_f \ \ ,  \exists \delta_if(x) $$
## F Paraméteres int.:
### f folytonos (f : U x \[a,b]) -> F paraméteres integrál létezik:
- Kiind: f folytonos
1. f_x is folytonos tetsz. x-re \[a,b]-n
- az hogy f_x folytonos egy gyengébb tulajd., mint hogy f folytonos
- kompakt halmaz és folytonos fv. -> Riemann int.

### f folytonos -> F folytonos:
- Kiind: F(x) - F(y) = 
- keresünk egy kompakt halmazt
- Heine tétel
- Norma átírása

## Riemann integrál kiszámítása:
- Felsőbecslések
- m = I_\*(f_x)
- 2 felosztás alkalmazása

# Megjegyzések / Notes
- Környezetek nyílt halmazok ( x < r )
- $( C[a,b],\rho_\infty)$-n egyenletes konvergenciáról beszélünk  
	