# Table of Contents

# Gráfok megadott fokszámokkal

## Gráfok létezése
**Feltételek:**

| Gráf (Multigráf)           | Egyszerű gráf                                                                          | Páros gráf                                                                                                                 |
| -------------------------- | -------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------- |
| $\sum^n_{i=1} d_{i}$ páros | $\forall k=1\dots n:$ $(\sum^k_{i=1}d_{i}) - k(k-1) \leq \sum^n_{i=k+1} \min(d_{i},k)$ | $\sum^n_{i=1} a_{i} = \sum^n_{i=1}b_{i}$ <br>és<br>$\forall k=1,\dots,n: \sum^k_{i=1}a_{i} \leq \sum^n_{i=1}\min(b_{i},k)$ |

| Fa                           | Digráf                                                                                                                                                                |
| ---------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| $\sum^n_{i=1}d_{i} = 2(n-1)$ | $\sum^n_{i=1} \delta_{i}=\sum^n_{i=1} \rho_{i}$<br>és<br>$\forall k =1\dots n:\sum^k_{i=1}\delta_{i}=\sum^k_{i=1} \min(\rho_{i},k-1) + \sum^n_{i=k+1}min(\rho_{i},k)$ |
|                              |                                                                                                                                                                       |

### Multigráf

**Algo.**: 
1. Páros sok páratlan fokú csúcs van, ezeket kössük össze egymással úgy, hogy csakis páros hiányú csúcsok maradjanak
2. Ekkor mindegyik csúcshoz a hiány értékének felének darabnyi hurokélt rendelünk
### Egyszerű gráf

**Algo.**: 
1. Minden csúcs rendelkezzen hiány értékkel
3. Minden lépésben a legnagyobb hiányú elemet válasszuk ki, és kössük össze alkalmas mennyiségű legnagyobb hiányú elemmel
4. Szomszédok fokszámát csökkentsük


### Páros gráf

**Algo.**:
1. A és B pontok felvétele élek nélkül
3. B-beli csúcsokhoz legyen hiány érték, ez kezdetben a fokszám
4. Minden lépésben A csúcsainak kiválasztása és összekötése B alkalmas mennyiségű legnagyobb hiányú csúcsaival
5. Szomszédok csökkentése


### Fa

**Algo.**:
- **Lépés**: Csúcsok kiterjesztése, megnevezése, és szomszédos csúcsok felvétele a gráfba
- **Helyesség indoklása**: 
	- Körmentesség
	- Csúcsok száma megfelelő


### Digráf

**Fontos**: 
- $\rho$ ~ be
- $\delta$ ~ ki 

**Algo.**: 
1. Csúcsokhoz hiány érték (be fok) felvétele
2. Legnagyobb hiányú csúcs kiválasztás és összekötése alkalmas mennyiségű legnagyobb kifokú csúccsal
3. Hiányok csökkentéseű

## Kapcsolat 0-1 mátrixokkal
- **Szomszédsági mátrix**
	- **Alapfeladat átfogalmazása mátrixokra**
- **Páros szomszédsági mátrix**
	- **Feladat átfogalmazása mátrixokra**
	- **Irányított gráfok** esete max. 1 hurokéllel ($n =m$ eset)

# Párosítások páros gráfokban


## Kőnig tétel

**Legyen**: 
- $G=(A,B;E)$ páros gráf

**Ekkor**:
- $\nu(G) = \tau(G)$, ahol 
	- $\nu(G)$ ~ legnagyobb párosítás elemszáma
	- $\tau(G)$ ~ legkisebb lefogó ponthalmaz mérete
 

**Vázlat**: (($\nu \leq \tau$) trivi); $\tau \geq \nu$ most:
1. Legyen $M$ egy párosítás, átalakítjuk a páros gráfot irányított gráffá: $M$-beli élek B -> A, egyébként A -> B
2. Legyen $R_{a}$ és $R_{b}$ a két A és B-nek olyan részhalmaza, amelyet $M$ nem fog le. Legyen $Z$ az $R_{a}$-ból elérhető csúcsokat tartalmazó halmaz (utak)
3. Megvizsgáljuk $R_{b} \bigcap Z$-t: *diszjunkt* eset és *nem*-*diszjunkt* eset!
	1. *Nem-diszjunkt*: Ekkor van $R_{a}$-ből $R_{b}$-be alternáló út ($P$)
		1. Vegyük $M' := P - M$ (szimmetrikus diff.)
		2. Ekkor $M'$-nek több éle van, mint $M$-nek
		3. $M'$ párosításhoz megint előállítjuk az előző irányított segédgráfot
	2. *Diszjunkt*: 
		1. Ekkor $Z \bigcap A$ és $B-Z$ között nem megy él (**indoklás**)
		2. $L=\left( B \bigcap Z \right) \bigcup(A-Z)$ lefogó ponthalmaz ekkor (**indoklás**)
		3. **Indoklás =>** $|L| \leq |M|$
## Javító utas algoritmus - Magyar algoritmus


### Futásidő

**Egy fázis** ($R_{b} \bigcap Z$ meghatározása, $Z$ keresése, élek átirányítása.): $O(n)$ $\times$ **Minden fázisban 1-el több él**: $O(m)$
**Összesen**: $O(nm)$

## Hall tétele páros gráfokra

**Legyen**:
- $G=(A,B;E)$ páros gráf

**Ekkor**:
- $\exists A$-t lefedő párosítás $\iff$ *Hall-feltétel* teljesül $\forall X \subseteq A$-ra 


**Vázlat**: 
- $\rightarrow$: Ha **Hall-feltétel** nem teljesül, akkor már erre a nem teljesülő részhalmazra sem létezik párosítás
- $\leftarrow$:
	1. Minimális lefogó ponthalmazból kiindulunk
	2. Belátjuk, hogy $|A| \leq |L|$ : Hall feltétel $A-L$-re + $N(X)$ felsőbecslése + $|A|$ felírása, amivel az egyenlőség teljesül

## Kőnig tétele páros gráfokra

**Legyen**:
- $G=(A,B;E)$ páros gráf
- $\lvert A \rvert = \lvert  B \rvert$
- $r > 0$ a fokszáma az összes csúcsának (azaz $r$ reguláris gráf)

**Ekkor**:
- $\exists$ teljes párosítás $G$-re

**Vázlat**:
- Megmutatjuk, hogy reguláris gráf esetén teljesül a *Hall-feltétel*
- $X$-ből összesen kilépő élek száma
- $B$ minden csúcsába max hány él léphet be?

# Súlyozott párosítások

**Legyen**: 
- $G=(A,B;E)$ páros gráf, illetve $c:E\to \mathbb{R}$ súlyfv.
- Egy párosítás súlya megegyezik a benne található élek súlyának összegével

**Legyen**:
- $\nu_{c}(G)$ ~ max. súlyú párosítás értéke
- $\nu_{c}'(G)$ ~ max. súlyú teljes párosítás értéke

## Súlyozott lefogás

$\pi:V\to \mathbb{R}$ fv. súlyozott lefogás, ha:
- $\forall uv \in E: \pi(u) + \pi(v) \geq c(uv)$
- ahol $c:E \to \mathbb{R}$ súly fv.

$\pi$ súlyozott lefogás összértéke: $\pi(V) = \sum_{v \in V}\pi(v)$, ahol $V = A \bigcup B$

## Egerváry tétel

**Legyen**:
- $G=(A,B;E)$ teljes párosítással rendelkező gráf
- $c:E \to \mathbb{R}^+ \bigcup \{ 0 \}$

**Ekkor**:
+ maximális súlyú teljes párosítás értéke egyenlő a minimális összegű súlyozott lefogással, azaz $\pi(V) = \nu_{c}'(G)$
+ **Ha**: $c$ egészértékű => optimális súlyozott lefogás is választható annak
+ **Ha**: $G$ teljes páros gráf => optimális súlyozott lefogás választható nemnegatívnak

## Maximális súlyozott párosítás és súlyozott lefogás kapcsolata

**Legyen**: 
- $G = (A,B;E)$
- $c: E\to \mathbb{R}^+\ \bigcup\ \{ 0 \}$

**Ekkor**:
- A párosítások max. $\nu$ súlya egyenlő a nemnegatív súlyozott lefogások min. $\pi^+(G)$ súlyával
- Amennyiben $c$ egészértékű, $\pi$ is választható annak


# Stabil párosítások

## Blokkoló pár

**Legyen**:
- $f\in F, l \in L$ 

**Ekkor**: 
$f$ és $l$ blokkoló pár $\iff l >_{f} M(f)$ és $f >_{l} M(l)$ 

## Gale Shapley algoritmus (Házassági probléma)

**Algoritmus váza**:
**Kezdet**: mindenki pár nélkül 
**Lépések**: (2) 
1. Leány kérés páratlan esetén (preferencia sorrend)
2. Lány lépése:
	1. Elfogadja, ha páratlan
	2. Elfogadja, ha jobban preferálja, mint a párját
	3. Elutasítja, ha kevésbé preferálja, mint a párját


### Stabil párosítás + Garantált terminálás 

**Vázlat**: $(f,l) \notin M$ esetén
1. $l >_{f}M(f)$ eset
2. $M(f) >_{f} l$ eset


**Futási idő**:  $O(|F| * |L|)$ 

### Fiú optimális

**Vázlat**: 
1. *Indirekt*: nem fiú optimális $M$ párosítás **Gale**-**Shapley** által
2. $f$ ~ első visszautasított fiú
3. $f$-et visszautasító $l$-nek mostani párja $f'$. 
4. $f'$-nek nincs jobb párja, különben őt előbb utasították volna el
5. Vegyünk egy másik $M'$ párosítást, ahol $(f,l)$ páros
6. Ekkor $f'$-nek biztosan rosszabb a partnere, tehát $(f',l)$ blokkoló pár $M'$-ben => **Ellentmondás**
 

### Lány optimális 

Nem.

### Magányos farkas tétel

**Vázlat**: 
1. *Indirekt*: $f_{1}$ magányos $M$-ben, de $l_{1}$ párja $M'$-ben
2. **Ekkor**: $l_{1}$-nek van párja $M$-ben ($f_{2}$) és őt preferálja $f_{1}$ helyett, különben *blokkoló pár*
3. **Ekkor**: $f_{2}$-nek van párja $M'$-ben ($l_{2}$) és őt preferálja $l_{1}$ helyett, különben *blokkoló pár*
4. Ezt folytatva végtelen láncot kapunk => **Ellentmondás** 

## Gale-Shapley algoritmus (Felvételi feladat)

**Algoritmus váza**:
**Lépések**:
1. Hallgató jelentkezik szakra (preferencia sorrend)
2. Szak elfogadja $q(s)$ hallgatóig, utána a $q(s)$ legjobbat megtartja
**Terminálás**:
- Minden hallgató talál magának szakot **vagy** végig ér a saját listáján

### Stabil hozzárendelés + felvételizők számukra legjobb helyre kerülnek

### Feladat visszavezetése stabil párosításokra (*Konstrukció*)

**Vázlat**:
1. $i=1,\dots,q(s):(s,i)$ csúcs, mindegyik $s$ preferenciáit örökli
2. $h$ hallgató preferenciái:
	1. $(s,i) <_{h} (s',i')$ ha $s <_{h}s'$ , vagy $s = s'$ és $i' < i$

### "Vidéki főiskola" tétel (Nem biz.)

**Vázlat**:
- $q(s)$ ~ kar határlétszáma
- **Legyen**:
	-  $\mu,\nu$ két *stabil hozzárendelés*
	- $\nu$-ben valamely $s$ szak nem tudta feltölteni a keretét: $|\nu(s)| \leq q(s)$
- **Ekkor**:
	- Semelyik másik *stabil hozzárendelés*ben sem tudta
	- Ugyanazokat veszik fel mindig az adott szakra: $\nu(s) =\mu(s)$ 

# Folyamok

## Hálózat
- $(D,s,t,g)$ ahol:
	- $D$ irányított gráf
	- $s$ forrás ~ feltehető, hogy nincs bemenő él
	- $t$ nyelő ~ feltehető, hogy nincs kimenő él
	- $g: E \to \mathbb{R}^+ \bigcup\ \{ 0,\infty  \}$

**Illetve**:
- ha $D=(V,E);f:E \to \mathbb{R}; v \in V; Y \subset V$
- akkor: 
	- $\delta_{f}(v) = \sum_{e\in E_{ki}(v)}f(e)$ ~ $v$-ből kilép élek összértéke
	- $\rho_{f}(v) = \sum_{e\in E_{be}(v)}f(e)$ ~ $v$-be belépő élek összértéke
	- $\delta_{f}(Y) = \sum_{e \in E_{ki}(Y)} f(e)$ ~ $Y$-ből kilépő élek összértéke
	- $\rho_{f}(Y) = \sum_{e\in E_{be}(Y)}f(e)$ ~ $Y$-ba belépő élek összértéke

## Folyam
- $f:E(G)\to \mathbb{R}$, ha:
	- *megmaradási törvény*
	- *megengedett folyam*

## Vágás

**Legyen**:
- $D=(V,E)$ digráf

**Ekkor**:
- *Vágás*: $\nu =\{ S,T \}$ ~ $V$-t két diszjunkt halmazra bontja
	- $\nu$ egy $s-t$ vágás, ha $s \in S$ és $t \in T$ 
- $E(\nu)$ ~ vágás élhalmaza (él két végpontja a vágás két különb. oldalára esik)
- $E^+(\nu)$ ~ $S$-ből  $T$-be vezető élek
- $E^-(\nu)$ ~ $T-ből$ $S$-be vezető élek


## Lemma

**Legyen**: 
- $f$ tetsz. folyam

**Ekkor**: 
- $e(f) = \rho_{f}(t) - \delta_{f}(s)$
- Tetsz. $\nu=\{ S,T \}$ $s-t$ vágásra:
	- $e(f) = \delta_{f}(S) - \rho_{f}(S) = \rho_{f}(T) - \delta_{f}(T)$

## Vágás kapacitása

**Legyen**:
- $f$ tetsz. folyam
- $\nu =\{ S,T \}$ egy $s-t$ vágás

**Ekkor**: $e(f) \leq \sum_{e\in E^+(\nu)}g(e)=: g(\nu)$ ~ vágási kapacitás

## MFMC
**Legyen**:
- $H= (D,s,t,g)$ hálózat

**Ekkor**:
- $\max_{f\ folyam} e(f) = \min_{\nu(s-t)\ vágás} g(\nu)$ 

**Vázlat**:
- $e(f) \leq g(\nu)$ ~ vágás kapacitásából adódóan
- $e(f) \geq g(\nu)$:
	1. Legyen $D_{f}=(V,E_{f})$ segédgráf
	2. Tegyük bele az $E$-beli éleket úgy hogy a javító utak feltételei teljesüljenek
	3. $D_{f}$-ben keresünk utat $s$-ből $t$-be:
		1. Ha van -> javító út -> javítsunk -> új folyam és segédgráf (rekurzíó)
		2. Ha nincs -> $S:=$ $s$-ből elérhető csúcsok halmaza és $e \in E(s)$ 
		3. Ekkor két eset: $e$ kilép $s$-ből, vagy belép $s$-be:
			1. $e$ kilép $s$-ből => $e$ telített (nem került bele $E_{f}$-be)
			2. $e$ belép $s$-be => $f(e) = 0$ ($e$ megfordítottja nem került bele $E_{f}$-be)
		4. $\nu(S,V-S)$ vágásra $g(\nu) = e(f)$

## Ford-Fulkerson algoritmus (F.F.)

**Vázlat**:
1. $f\equiv 0$ folyam kiindulás
2. $D_{f}$ elkészítése fenti módon
3. Útkeresés $D_{f}$-ben $s$-ből $t$-be
4. **Ha találunk**: út mentén javítunk
5. **Ha nem találunk**: leáll az algoritmus

**Futásidő**: 
- $O(|V|*|E|)$, ha a növelő utas algoritmusban mindig a legrövidebb utat használjuk ($g$ tetsz. kapacitás fv.)
- Ha viszont: ez nem teljesül és . . .
	- $g$ **egész**: futásidő véges (folyam érték $\forall$ javítással min. 1-el nő)
	- $g$ **racionális**: visszavezethető egész esetre
	- de *nem* polinomiális 
	- illetve, létezik $H=(D,s,t,g)$, hogy $F.F.$ sosem áll le

## Edmonds-Karp algoritmus

- Amikor speciális módon választjuk meg a javító utat: Pl. a legrövidebb utat használjuk az F.F. algoritmusban
- Ekkor a futásidő: $O(nm^2)$ ~ egy növelés $O(m)$ lépés * lépések száma $O(nm)$

# Folyam algoritmusok

**Vázlat**:

**Legyen**:
- $g$ értékei binárisban ~ t.f.h. $\max$ M jegyet használnak
- $g_{i}$ = kapacitás első $i$ darab számjegye 

**Ekkor**:
1. $f\equiv 0$-ból való kiindulás
2. $g_{1}$-re nézve $f$-ből indulva max folyam keresése
3. **Indukciós feltevés**: t.f.h. $g_{i}$-re $f_{i}$ a max folyam. **Ekkor**:
	1. $f_{i} \leq g_{i} \implies 2f_{i} \leq 2g_{i}$ és $2g_{i} \leq g_{i+1}$
	2. **Világos**: $2f_{i}$ megengedett folyam $g_{i+1}$-re
	3. $2f_{i}$ max folyam $2g_{i}$-re is
	4. $g_{i+1}$ legfeljebb 1-el tér el $2g_{i}$-től (ha $g_{i+1}$. bit 0 akkor egyenlőek)
	5. Minimális vágás $g_{i+1}$-re max. $|E|$-vel nagyobb mint $g_{i}$-re
	6. $|E|$ lépés alatt megtaláljuk $f_{i+1}$-et

**Így**:
- $M*|E|$ ~ növelés szükséges
- $M*|E|^2$ ~ **futásidő**

# Folyamok alkalmazásai

## Maximális párosítás keresése folyammal

**Legyen**: 
- $G=(A,B;E)$ páros gráf

**Cél**:
- $D=(V',E')$ digráf elkészítése

**Lépések**:
1. $s$ és $t$ felvétele 
2. $A$-beli és $s$, illetve $B$-beli és $t$ csúcsok összekötése
3. Páros gráf éleit $A$-ból átirányítjuk $B$-be
4. $g \equiv 1$ kapacitás fv. => egészértékű
5. Maximális folyamot keresünk $s$-ből $t$-be: $g$ egészértékű => $\exists$ folyam $\{ 0,1 \}$ értékekkel
6. *Maximális folyamérték* megegyezik a *maximális párosítás méretével*

## Több forrás és nyelő

**Vázlat**:
- $D=(V,E)$ digráf, $g$ kapacitás fv., $S=\{ s_{1},\dots,s_{k} \} \subset V$ források, $T=\{ t_{1},\dots,t_{l} \} \subset V$ nyelők
- **Feladat**: folyamérték maximalizálás
- $D'$ digráft megkonstruálása, ahol:
	- Új $s'$ és $t'$ csúcs, többi nyelő és forrás csúccsal összekötve
	- Továbbá új kapacitás fv.: *régi éleken* nincs változás, *új éleken* $\infty$ lesz
- Maximális folyam keresése $(D',s',t',g')$-n

## Csúcskapacitások

**Vázlat**:
- $\tilde{g}:V \to \mathbb{R}^+_{0}$ csúcs kapacitás, ú.h. $\delta_{f}(v) \leq \tilde{g}(v)$ ($\forall v \in V - \{  s,t \}$)
- $D'=(V',E')$ gráf készítése Menger-tételben használt pontszéthúzással
- új kapacitás
- $(D',s',t'',g')$ hálózatban maximális folyam keresése

# Gráfok színezései

## Csúcsszínezés

### Reguláris gráf

**Állítás**: $\chi(G) \leq \Delta(G) + 1$, ha $G$ reguláris gráf

**Biz.**: (vázlat)
1. Összefüggő gráf feltételezése
2. Algoritmus (konstruktív biz.)
	1. Csúcsok sorrendben állítása tetszőleges módon
	2. Elsővel kezdve: csúcsok színezése olyan színnel, amilyenre a szomszédjait még nem színeztük
	3. Ekkor mivel $\Delta(G)$ a max. fokszám és $\Delta(G) +1$ színt használtunk => Lesz szabad szín


### Nem-reguláris gráf

**Állítás**: $\chi(G) \leq \Delta(G)$, ahol $G$ nem-reguláris gráf

**Biz.**: (vázlat) Algoritmussal (konstruktív biz.):
1. **Legyen**: $v \in V$, ú.h. $v$-nek kisebb a foka mint $\Delta(G)$
2. Állítsuk sorrendben $V$-beli csúcsokat $v$-től vett távolságuk alapján, amelyet (Pl. BFS)
	1. $v$ utolsó csúcs
	2. **csökkenő sorrend**
3. Mohó színezés sorrendben

**Algoritmus helyessége**:
1. Sorrend: $\forall u\in V\setminus \{ v \}$ lesz olyan szomszédja, amely sorrendben mögötte van
2. Tehát lesz olyan szín, amelyet még nem használtunk fel a szomszédjainak kiszínezésére
3. Tovébbá $v$ foka kisebb mint $\Delta(G)$, így ő is kiszínezhető 

## Élszínezés

### Trivi.

$\chi'(G) \geq \Delta(G)$

### Kőnig élszínezési tétel 

**Állítás**: $\chi'(G) = \Delta$, ahol $G$ $\Delta$ reguláris páros gráf

**Biz**: (vázlat)
1. Kiindulás $G$ és $i=1$-ből
2. Rekurzívan, amíg lehet: 
	1. Teljes párosítás keresése
	2. Eddig nem használt színnel színezése a párosítás éleinek
	3. Párosítás éleinek törlése
	4. *Kőnig-tétel reg. páros gráfokra*: Lesz mindig teljes párosítás, és az új gráf is reguláris marad
3. Az élekhez rendelt színek pont egy $\Delta$ színezést adnak meg

### Páros gráfok élszínezése

**Állítás**: $\chi'(G) = \Delta(G)$, ha $G$ páros gráf

**Biz.**: (vázlat)
1. Reguláris gráffá való kiegészítés
2. Visszavezetés Kőnigre
3. Hozzávett élek és csúcsok törlése

### Vízing tétel

**Állítás**: $\chi'(G) \leq \Delta(G) + 1$, ha $G$ egyszerű gráf

## Ramsey-tételkör

### Teljes gráf éleinek 2 színezése

**Def.:**
- $R(k,l)$, ahol $k,l \in \mathbb{Z}^+$
- $R(k,l)$ azon legkisebb szám, amelyre : $\forall n\geq R(k,l)$ esetén az *$n$ pontú teljes gráf* éleit két színnel színezve van a gráfban egyszínű $K_{k}$ vagy $K_{l}$

### Egyszínű háromszög n=5 esetén

Kiszínezhető úgy, hogy nem lesz: Pentagram belső élei 1 szín, külső élei másik szín

### Egyszínű háromszög n=6 esetén

**Vázlat**:
1. Egy csúcs ($v_{1}$) 5 él lép ki, ezekből 3 egyszínű legalább (most **piros**)
2. $v_{2},v_{3},v_{4}$ legyen ezen élek végpontjai
	1. Ha $v_{2},v_{3},v_{4}$ között meg piros él, akkor $v_{1}$-el  kiegészítve van **piros** háromszög
	2. Ha $v_{2},v_{3},v_{4}$ között nem megy piros él, akkor kék háromszöget alkotnak

# Gráfok ábrázolása

## Szomszédsági mátrix
- $A(G)=(a_{ij})$, ahol:
	- $a_{ij} = 0$, ha $i\neq j$ és $v_{i},v_{j}$ nem szomszédok 
	- $a_{ij} = k$, ha $i\neq j$ és $v_{i},v_{j}$ között $k$ db. él fut
	- $a_{ij} = l$, ha $i=j$ és $l$ db. hurokél tartozik $v_{i}$-hez

- $D$ digráf esetén . . .
- Irányítatlan eset: szimmetrikus mátrix

## Illeszkedési mátrix
- $B(D) = (b_{ij})$, ahol $D=(V,E)$ digráf
	- $b_{ij} = 0$, ha $v_{i}$ nem illeszkedik $e_{j}$-re
	- $b_{ij} = 1$, ha $v_{i}$ kezdőpontja $e_{j}$-nek
	- $b_{ij} = -1$, ha $v_{i}$ végpontja $e_{j}$-nek

- Irányítatlan esetben (-1) helyett 1
- Hurokélek: (-1)



## k-hosszú utak meghatározása

**Állítás**: $A(G)^k = (m_{ij})$-re $m_{ij}$ a $v_{i}$-ből $v_{j}$-be vezető $k$ hosszú élsorozatok száma

**Biz.**: (vázlat)
- Teljes indukcóval
1. $k=1$-re nyilván teljesül (szomszédsági mtx. def)
2. T.f.h. $k$-ra teljesül: $k+1$-re ekkor: $A(G)^{k+1} = n_{ij}$, ahol $n_{ij} = \sum^{|V|}_{l =1}m_{il}*a_{lj}$ (mátrix szorzás szabályai)
3. Továbbá $v_{i}$-ből $v_{j}$-be vezető $k+1$ hosszú utak felbontható $k$ és 1 hosszú utakra ($v_{l}$)
4. Továbbá $k$ hosszú utak száma $v_{i}-v_{l}$ között $m_{il}$, és 1 hosszú utak száma $v_{l}-v_{j}$ között $a_{lj}$
5. Ezek összeadásával $l =1\dots|V|$-re pont $n_{ij}$-t kapjuk


## Cayley-tétele

**Állítás**: $\{ 1,\dots,n \}$ csúcsokon $n^{n-2}$ különböző fa adható meg, ahol számít a csúcsok címkéje


# Síkgráfok

## Euler formula

Ha a gráf síkgráf: $v + l = e +2$ 

## Síkbarajzolható gráfok 5 színnel színezhetők

**Állítás**: bármely síkgráf csúcsai kiszínezhetők 5 színnel

**Biz.**: (vázlat) + (indirekt)
- Legyen $G$ minimális és **ellenpélda**: nem színezhető ki 5 színnel
1. **Euler-formula** + gráfok egyszerűsége (többszörös és hurokélt el lehet hagyni)
2. $|V|\geq 3$ esetén: $3\lvert V \rvert - 6 \geq \lvert E \rvert$ => $\exists u  \in V: d(u) \leq 5$
3. $G-u$ kiszínezhető 5 színnel a minimalitás miatt
4. **Ha** $d(u) \leq 4$: van olyan szín, amit szomszédaira nem használtunk fel => $u$ színezhető ezzel a színnel, így **ellentmondás**
5. $G$ síkgráf => nem tartalmaz feszített $K_{5}$-t => $\exists v,w$, hogy $uv,uw \in E$, de $vw \notin E$
6. Húzzuk össze $u,v,w$-t egy ponttá és legyen az új gráf $G'$ 
7. Színezzük $G'$-t 5 színnel
8. $G'$ színezését alkalmazzuk $G$-re => $u,w,v$ egyszínű, ez nem jó!
9. $u$ szomszédai színezésére legfeljebb 4 színt használtunk, u színezhető 5. színnel => **ellentmondás**

## Gráfok színezése 5 színnel

**Algo.**:
1. $\forall$ 5 csúcsú gráf színezhető 5 színnel
2. Legyen G gráf, amit ki akarunk színezni, keressünk benne legfeljebb 5 csúcsú fokot
3. **Ha** $deg(u) \leq 4$:
	1. $u$-t töröljük
	2. $G'$-re algoritmust futtatjuk
	3. $G'$ színezése után $u$ színe legyen a szomszédaitól különböző
4. **Ha** $deg(v) =5$:
	1. Van $u$-nak két olyan szomszédja, amelyek nincsenek összekötve.
	2. Húzzuk össze a három csúcsot
	3. Algoritmus futtatása a kapott $G''$ gráfon
	4. Húzzuk szét az új csúcsot a három csúcsra
	5. Színezzük $u$-t olyan színűre, amilyenre egyik szomszédját sem színeztük

## Duális gráf

**Legyen**: $G$ síkgráf

**Ekkor**: $G$ *duálisa* $G^*$ gráf, ha:
- $\forall G$-beli élek megfeleltünk egy  $G^*$-beli élt
- ha két tartomány több élen is szomszédos: *többszörös él*
- ha él mindkét oldalán ugyanaz a tartomány: *hurokél*
- $G^*$ csúcsai $G$ tartományai, két csúcsot összekötünk, ha $G$-ben él választja el a két tartományt egymástól

## Ötszíntétel

**Állítás**:
- Bármely síkbarajzolható gráf tartományai kiszínezhetőek 5 színnel, ú.h az **élszomszédos tartományok** színe különböző.

**Biz.**:
- Alkalmazzuk az 1. állítást a gráf duálisára

## Négyszíntétel
- Bármely síkbarajzolható gráf tartományai kiszínezhetőek 4 színnel, ú.h az élszomszédos tartományok színe különböző.

## Felosztott gráf
**Feloszott $K_{5}$ gráf**: előállnak $K_{5}$-ből az élei többször felosztásával

(hasonló $K_{3,3}$)-ra

## Peterson-gráf nem síkbarajzolható

**Biz.**: Tartalmaz $K_{3,3}$-t

![[Pasted image 20250112173554.png]]
## Kuratowski tétel

**Állítás**: $G=(V,E)$ gráf síkbarajzolható $\iff$ nem tartalmaz *felosztott* $K_{3,3}$-t és nem tartalmaz felosztott $K_{5}$-t


# Approximációk

## Approximáció

$A$ polinom idejű algoritmus $\alpha$ approximáció, ha $\forall I$ inputra $A(I) \leq \alpha *OPT(I)$

## Approximáció csúcsfedésre

Azaz lefogó ponthalmaz keresése!

**Lépések**: (vázlat)
- Kezdetben üres csúcshalmaz ($U= \emptyset$) és élek halmaza ($F=E$)
- Amíg F nem üres:
	1. $vw \in F$-re: $U= U + \{ v,w \}$
	2. Töröljük azon éleket $F$-ből, amelyek vagy $v$-t vagy $w$-t tartalmazzák

**Világos**:
- futás során $F$-ben tároljuk a még nem fedett éleket
- futás végén $F= \emptyset$

**Továbbá**: az algoritmus *2-approximáció*: (vázlat)
1. $U$-ba páronként vesszük csúcsokat => Párosítást adnak meg a párok
2. Ez a párosítás tartalmazásra nézve maximális, de nem feltétlen a legn﻿agyobb méretű
3. **Legyen**: $O$ optimális csúcsfedés
4. Ekkor ha $M$ párosítás, akkor $2\lvert O \rvert\geq \lvert M \rvert$, mert $O$ az $M$ minden élének legalább egyik csúcsát lefedi
5. $U$ egy párosítás csúcshalmazra => $2\lvert O \rvert\geq \lvert U \rvert$

## Approx. súlyozott csúcsfedésre

**Feladat**: 
- $G=(V,E)$ gráf 
- $c:V \to \mathbb{R}^+$ súly fv.
- Olyan $U$ keresése, amelyre $U$ lefogó ponthalmaz és $c(U)$ minimális
- **Ha** $c\equiv 1$ => $U$ minimális lefogó ponthalmaz

NP-teljes!

**Algo.**:
1. $F = E$ és $U= \emptyset$ kezdetben
2. Amíg $F$ nem üres:
	1. Legyen $uv \in F$, ú.h. $c(u) \leq c(v)$
	2. Ekkor $U = U + \{ u \}$, és $c(v) = c(v) - c(u)$
	3. $F$-ből töröljük az összes olyan élt, amelynek végpontja $u$

Ez egyben egy *2-approximáció* is! (nem biz)

## TSP (Utazó ügynök probléma)

**Legyen**: adott $n$ csúcsból álló teljes gráf élsúlyokkal.
**Cél**: Minimális súlyú Hamilton-kör megtalálása

Összes lehetséges bejárás: $n!$
Asszimetrikus verzió

**Metrikus változat**: $d(uw) + d(wv) \geq d(uv)\ \ (\forall u,v,w \in V)$
**Euklideszi-síkra** beágyazott verzió is *NP-teljes*

## TSP nem approximálhatóság

**Állítás**: TSP nem $\alpha$-approximálható semmilyen $\alpha$-ra sem

**Biz.**: (vázlat)
1. Van-e Hamilton-kör kérdés NP-teljes => visszavezetjük erre a problémára
2. Ha $\exists k$-approx. a TSP-re, akkor tudunk tetszőleges gráfra *Hamilton-kört* keresni
3. Kiindulunk tetsz. gráfból
4. Készítsük el a $G'=(V,E')$ teljes gráfot $w$ súly fv.-el, ú.h.:
	1. $w(e) = 1$, ha $e \in E$
	2. $w(e) = L$, ha $e \not\in E$ és $L > k*\lvert V \rvert$
5. Futassuk a TSP algot $G'$-n és $w$-n
6. Az eredmény $t$:
	1. Ha $t \leq k*n \implies$ gráfban **van** Hamilton kör
	2. Ha $t \geq L \implies$ gráfban **nincs** Hamilton kör

## Metrikus TSP

$c(uv) + c(vw) \geq c(uw)$ ($u,v,w \in V$)

## 2-approx. algoritmus metrikus TSP-re

**Algo.**:
1. Minimális feszítő fa keresés, ez legyen $F$
2. $F$-éleit duplázzuk meg, ekkor *Euler-kört* kapunk
3. Járjuk be a gráf csúcsait az Euler-kör mentén
4. Ha egy csúcsában már voltunk, akkor azt ugorjuk át
5. Ekkor *Hamilton-kört* kapunk

**Állítás**: A kapott *Hamilton-kör* 2 approx. a metrikus TSP-re
**Biz.**: 
1. Mivel $c$ metrikus, így csúcsok átugrásával nem nő a súly
2. Legyen $C_{out}$ az algo. által adott bejárás és $C_{opt}$ az optimális bejárás
3. Ekkor $c(C_{out}) \leq 2c(F)\leq 2c(C_{opt})$ lesz.


# Véletlen gráfok

## Vizsgált tulajdonságok

- Legnagyobb komponens mérete
- Fokszámeloszlás
- Átlagos úthossz
- Klaszterezettség

## Klaszterezettség

Egy csúcs szomszédai milyen gyakran vannak összekötve:
$C_{i} = \frac{|\{ v_{j}v_{k}\in E |\ v_{j},v_{k} \in N_{i} \}|}{|\{ v_{j}v_{k}|v_{j},v_{k}\in V \}|}$
ahol:
- $N_{i} = \{ v_{j}:v_{i}v_{j} \in E \}$

## Fokszám eloszlás

$p_{k} = P(\deg(v) = k)$

## Erdős-Rényi gráf

### Erdős-Rényi konstr.

1. $G(n,m)$ gráf $n$ csúcs
2. Véletlenszerűen kiválasztunk $m$ darab csúcsot és éleket húzunk közéjük

### Gilbert konstr.

1. $G(n,p)$ gráf $n$ csúcs
2. Minden lehetséges élt egymástól függetlenül $p$ valószínűséggel húzunk be

### Tulajd.

- **Legnagyobb komponens mérete**: 
	- $np < 1$: $O(\log n)$-nél szinte biztosan nincs nagyobb méretű komponens
	- $np = 1$: Maximális komponens mérete $\approx n^{2/3}$
	- $np > 1$: $\exists c$ konstans ú.h. $c*n$ méretű komponens létezik, illetve a többi komponens $\log n$-es méretű
- **Fokszám eloszlás**:
	- $p_{k} = {n-1 \choose k}*p^k*(1-p^{n-1-k})$ 
- **Átlagos úthossz**:
	- $\log n$
- **Klaszterezettség**:
	- $\frac{1}{n}$

### Valós modellel való kapcsolat

**Valós gráfokat rosszul jellemzi**:
- Kicsi laszterezettség
- Csúcsszám eloszlás *Poisson-hoz* tart, valóságban skálafüggetlen ($p_{k} = k^{-\gamma}$, $\gamma$ tetsz.)

**Probabilisztikus módszerben hasznos**:
- Ha egy tulajdonság minden gráfra teljesül => Véletlen gráfra is teljesül 1 valószínűséggel

## Watts Strogatz gráf

### Konstr.

**Legyen**: 
- $n$ csúcs, $V=\{ v_{1},\dots,v_{n} \}$, $K$ átlagos fokszám $n \gg K \gg \log n$
- $1\geq p \geq 0$

**Ekkor**:
- $\forall v_{i}$-t összekötjük $K$ db. szomszédjával
- $\forall v_{i}$ és $i<j \leq i + \frac{K}{2}\ mod\ n$-re: $v_{i}v_{j}$-t $p$ valószínűséggel kicseréljük véletlen $v_{i}v_{l}$ élre
- Hurok és többszörös éleket kerüljük

### Tulajd.

- $p=0$: Szabályos gyűrű gráf
- $p=1$: Erdős-Rényi gráf
- $0<p< 1$: 
	- **Átl. úthossz**: $< \log n$
	- "Kis világ tulajd." ~ **Lokálisan klaszterezett**: $\frac{3(K-2)}{4(K-1)}*(1-p)^3$
	- **Fokszámeloszlás**: $f(k,K) = min\left( k-\frac{K}{2},K/2 \right)$
		- $p_{k}= \sum^{f(k,K)}_{i=0} {\frac{K}{2} \choose i}(1-p)^i *p^{\frac{K}{2}-n}* \frac{\left( p* \frac{K}{2} \right)^{k- \frac{K}{2}-i}}{\left( k-\frac{K}{2}-i \right)!}$


## Barabás-Albert gráf

### Konstr.

**Paraméter**: $m$ és $n>m$

1. **Kiind.**: összefüggő gráf $n$ darab csúccsal: $V=\{ v_{1},\dots,v_{n} \}$
2. $\forall$ lépésben: 
	1. Új csúcs hozzáadása
	2. $m$ darab csúcs kiválasztása az eddigi csúcsok fokszámaival arányosan. Ezzel összekötjük a csúcsot
	3. $\frac{\deg(v_{i})}{\sum_{j}\deg(v_{j})}$ = Annak valószínűsége, hogy a $v_{i}$ össze lesz kötve az új csúccsal

### Tulajd.

- Növekedés és preferenciális kapcsolódás
- **Fokszámeloszlás**: $p_{k} \approx k^{-\gamma}$, $\gamma \in \mathbb{R}^+$ értékekre
- **Átl. úthossz**: $\frac{\log n}{\log(\log n)}$
- **Klaszterezettség**: $c \approx n^{-1}$

### Kritika

- klaszterezettség kicsi
- korai nagyfokú csúcsok fogják dominálni a struktúrát, későn jövőknek nincs esélye
- **így sok jelenségre nem jó**

### Bianconi-Barabás modell

- **Fitness-tulajdonság bevezetése**: valószínűségi eloszlásból választjuk ki, egy csúcsra állandó
- Új csúcsot a fokszámok és a fitness tulajdonság alapján kötjük össze

## Galton-Watson modell

- populáció létszámát generációnként modellezzük
- populáció egyede véletlenszámú utódot hoz lére
- utódok száma minden egyed esetén független a többi egyedtől és a generációtól

### Populáció kihalásának jellemzése

- $n$. generáció létszáma: $Z_{n}$
- $n+1.$ generációt az $n.$ generáció utódai alkotják
- **Kezdetben**: $Z_{0} = 1$
- **Ha** $Z_{n} = 0$ **akkor** a populáció kihalt és $Z_{k} = 0$ ($\forall k >n$)
- Szaporodás: $X$ valószínűségi változó alapján
- $\mu = E(Z)$
- $\mu^n = E(Z_{n})$ ~ a populáció várható értéke minden lépésben $\mu$ szeresére változik

**Állítások**: (nem biz.)
- Ha $\mu < 1$, akkor kihal a populáció
- Ha $\mu=1$:
	- Ha $p(X=1) = 1 \implies$ a populáció életben marad és $Z_{n} = 1$ ($\forall n \in \mathbb{N}$)
	- Ha $p(X = 1) < 1 \implies$ a populáció kihal (1 valószínűséggel)
- Ha $\mu > 1$:
	- Pozitív valószínűséggel nem hal ki a populáció
	- Azaz, **ha** $\mu = 1 + \epsilon$ és $VAR(X) = \sigma$, **akkor** a *túlélés valószínűsége*: $\approx 2 \frac{\epsilon}{\sigma^2}$ 