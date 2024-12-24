# Table of Contents 
1. [[#Implicit függvény]] 
2. #X [[#Feltételes szélsőérték]]
3. #X [[#Differenciál egyenletek]]
4. #X [[#Lineáris differenciál egyenletek]]
5. #X [[#D.E.-hez kapcsolódó fogalmak, tételek]]
6. [[#Lineáris D.E. rendszerek]] 
7. #X [[#Alaprendszer/Alapmátrix]]
8. [[#Magasabb rendű lin. D.E.]] 
9. [[#Állandó együtthatós, magasabb rendű homogén lin. D.E.]]
10. #X [[#Kvázi polinom és rezgés]]
11. [[#Függvénysorozatok, függvénysorok]]
12. #X [[#Konvergens függvénysorozat tulajdonságai]]
13. #X [[#Függvénysorozatok és differenciál]]
14. [[#Trigonometrikus rendszerek + Bessel]]
15. #X [[#Egyenletesen konvergens Fourier sorok]]
16. #X [[#Fourier sorok I.]]
17. #X [[#Fourier sorok II.]]

#X ~ Azon halmazba tartozó tételek, amelyből biztosan húzva lesz az egyik tétel a kettőből
# Implicit függvény
## Implicit fv. fogalma
- $g(x,y)$
- $\{ g=0 \} := \{ \xi\in D_{g}| g(\xi) =0 \}$

## Kapcsolata a feltételes szélsőérték problémával
- Pl. Terület mérés ($g(x,y) = \dots$)
- $\{ g =0 \}$ vizsgálata, de baj!: $int \{ g =0 \} = \emptyset$ 
- Erre volt a következő ötlet:
	- $\phi(x)$ és $F(x) = f(x,\phi (x))$ bevezetése
	- **Ekkor**: $\{ g=0 \} = graf\ \phi = f|\{ g =0 \}$ vizsgálata ami megegyezik $F$ vizsgálatával, ahol $F \in D$

**Általánosan**:
- $2 \leq n\in \mathbb{N}, m = 1,\dots, n-1$
- $\emptyset \neq U \subset \mathbb{R}^n, f:U \to \mathbb{R}$
- $g = (g_{1},\dots,g_{m}) : U \to \mathbb{R}^n$
- **T.f.h**: $\{ g = 0 \}:= \{ \xi \in U: g(\xi) = 0 \} \neq \emptyset$ 
- **Ekkor**:
	- $f$-nek a $c \in \{ g = 0 \}$ helyen feltételes lokális szélső értéke van a $g = 0$ feltételre, ha: $f |\{ g = 0 \}$-nak lokális szélső értéke van $c$-ben

Az lenne jó, ha: 
- $\{  g= 0 \} \bigcap K(c) = graf\ \phi$
- **Tehát**: $\xi \in \{ g = 0 \}$ esetén: $\xi = (x,\phi(x))$, ahol $x = (\xi_{1},\dots,\xi_{n-m}) \in \mathbb{R}^{n-m}$ és $\phi(x) = (\xi_{n-m+1},\dots,\xi_{m})\in \mathbb{R}^m$
- $R^n \equiv R^{n-m} \times \mathbb{R}^m$, ahol $\xi = (x,y) \in\mathbb{R}^n, x \in \mathbb{R}^{n-m},y \in \mathbb{R}^m$
## Kapcsolata az inver függvénnyel

## Implicit fv. tétel (vázlat)
**Legyen**: (3 feltétel)
- folytonosan deriválhatóság
- 2. parc. determinánsa (a,b) ~ (Azért is kell, hogy valóban függvény legyen)
- c = (a,b) pont

**Ekkor**:
1. Környezetek létezés, és ezen beli pontokra állítás
2. $\phi$ függvény: folytonosan deriválhatóság, derivált formája 

## Inverz fv. tétel (vázlat)
**Legyen**: 
- folytonosan deriv.
- egy pont (z)
- z-ben a derivált determináns nem 0

**Ekkor**: 
- létezik a lokális inverz
- lokális inverz folytonosan deriválható
- lokális inverz deriváltja megadható

# Feltételes szélsőérték
## Szükséges feltétel (+ bizonyítás)
### Elsőrendű -||-
**Legyen**:
- $f,g$ függvények
- g ~ folytonos diff.
- f-nek c pont feltételes lok. sz. é.
- g gradiens függvényeinek c-beli helyettesítési értéke legyenek lineárisan függetlenek

**Biz**:
1. Mátrixos alak felírása (g diff.) -> g diff. fv. range = m
2. $\det A \neq_{0}$, illetve feltevés: utolsó m oszlop = A
3. Implicit fv. tétel + következményei ($\phi$ grafikon, $F$ fv.)
4. F-nek lok. sz. é. a-ban
5. F Gradiens függvény + egyenlet felírása + $\phi'$ helyettesítése
6. Végső alak
## Elégséges feltétel 



# Differenciál egyenletek 
## D.E. (rendszer) fogalma
## K.É.P. (Cauchy-feladat)
## Egzakt egyenlet
## Szeparábilis egyenlet
## Rakéta emelkedési idejének számítása

# Lineáris differenciál egyenletek
## Lineáris D.E.
## Állandók variálásának módszere
## Radioaktív bomlás felezési idejének számítása

# D.E.-hez kapcsolódó fogalmak, tételek
## Lipschitz-feltétel
## Picard-Lindelöf-féle egzisztencia-tétel (fixpont-tétel alk.)
## K.É.P. megoldásának egyertelműsége
## Unicitási tétel ($\emptyset$ biz.)

# Lineáris D.E. rendszerek
## Vizsgálatuk: Homogén/Inhomogén rendszerek

## Megoldáshalmaz szerkezete

# Alaprendszer/Alapmátrix
## Alaprendszer, alapmátrix
## Állandók variálásának módszere
## Alapmátrix előállítása állandó együtthatós, diagonalizálható mtx. esetén 
## n = 2 eset vizsgálata tetsz. állandó együtthatós mátrixra
# Magasabb rendű lin. D.E.
## Magasabb rendű lin. D.E.
## Átviteli elv 
## Megoldáshalmaz szerkezete

## Állandók variálásának módszere

# Állandó együtthatós, magasabb rendű homogén lin. D.E.
## Alaprendszerének előállítása
## Karakterisztikus polinom szerepe (biz. vázlat)

# Kvázi polinom és rezgés
## Partikuláris megoldás kvázi-polinom jobb oldal esetén (biz. vázlat)
## Csillapítás nélküli kényszerrezgés vizsgálata, rezonancia

# Függvénysorozatok, függvénysorok 
## Függvénysorozat fogalma
## Függvénysor fogalma
## Hatványsorok
## Trigonometrikus sorok
## Fourier-sorok
## Dirichlet-féle magfüggvény
## Konvergencia
## Határfüggvény/Összegfüggvény
## Egyenletes konvergencia
## Weierstrass-féle majoráns krit.
# Konvergens függvénysorozat tulajdonságai
## Folytonosság kérdése
## Riemann-integrálhatóság kérdése
## Egyenletes fv.-sorozat folytonossága
## Egyenletes fv.-sorozat integrálhatósága
## Integrálás és határátmenet felcserélhetősége
# Függvénysorozatok és differenciál
## Határfüggvény differenciálhatósága tétel
## Deriválás és határátmenet felcserélhetősége
# Trigonometrikus rendszerek + Bessel
## Trigonometrikus rendszerek ortogonalitása
## Egyenletesen konvergens trigonometrikus sor összegfüggvényének Fourier-sora
## Bessel azonosság
## Bessel egyenlőtlenség
# Egyenletesen konvergens Fourier sorok
## Egyenletesen konvergens Fourier sorok
## Trigonometrikus rendszer teljessége $C_{2\pi}$-re
# Fourier sorok I.
## Kétszer folytonosan differenciálható fv.-k Fourier sora
## $f \in C_{2\pi}, f(x):=(x-\pi)^2 \ (0 \leq x\leq 2\pi)$ függvény Fourier-sora
## $\frac{\pi^2}{6}= \sum^{\infty}_{k=1}k^{-2}$ egyenlőség
# Fourier sorok II.
## $\sum^{\infty}_{k=1}k^{-1}*\sin(kx)\ (x\in \mathbb{R})$ sor konvergenciája, összegfüggvénye
## Rezgő húr problémája