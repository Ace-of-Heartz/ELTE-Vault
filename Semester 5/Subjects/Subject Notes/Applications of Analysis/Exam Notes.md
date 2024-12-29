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

### Másodrendű -||-
## Elégséges feltétel 

### Másodrendű -||-


# Differenciál egyenletek 
## D.E. (rendszer) fogalma
- $I \subset \mathbb{R}$
- $\Omega \subset \mathbb{R}^n$ 
- $f:I \times \Omega \to \mathbb{R}$, $f \in C$ 

**Feladat**: olyan $\phi\in I \to \Omega$, hogy:
1. $D_{\phi}$ nyílt
2. $\phi\in D$
3. $\phi'(x) = f(x,\phi(x))$ 


## K.É.P. (Cauchy-feladat)

**Ha még**: $\tau \in I$ és $\xi \in \Omega$ előre megadott, úgy hogy: $\phi(\tau) = \xi
**Akkor**:  *K.É.P.*

### K.É.P. egyértelmű megoldása
Ha $\forall \phi, \tilde{\phi}$ megoldásra: $\phi(t) = \tilde{\phi}(t),\ (\forall t \in D_{\phi} \bigcup D_{\tilde{\phi}})$
1. $M := \{ \phi|K.É.P. megoldása \}$
2. $J:= \bigcup_{\phi\in M}D_{\phi}$; $\Phi:J \to \Omega$, ahol $\Phi(x) = \phi(x)\ (\forall x \in D_{\phi},\phi\in M)$ 
3. $\Phi\in D;\ \Phi(\tau) = \xi;\ \Phi'(x) = f(x,\Phi(x))$
4. $\forall \phi\in M: \phi = \Phi|D_{\phi}$
5. $\Phi$ a teljes megoldás

## Egzakt egyenlet

**Legyen**: 
- $n= 1$
- $I,J \subset \mathbb{R}$
- $g: I \times J \to \mathbb{R}$
- $h :I \times J \to \mathbb{R} /\{ 0 \}$
- $F(x,y) = -\frac{g(x,y)}{h(x,y)}$, ahol $F : I \times J \to \mathbb{R}$; $F \in D$; $gradF = (g,h) = (\partial_{1}F,\partial_{2}F)$ 

**Ekkor**:
- $\phi$ megoldás => $\phi'(x) = -\frac{g(x,\phi(x))}{h(x,\phi(x))}$ 
- **Ötlet**: $\Phi(x) = F(x,\phi(x))$, és $x\to (x,\phi(x)) \in D$
- $\Phi(x)' = F'(x,\phi(x)) *(x\to(x,\phi(x)))$ $=$$<(g(x,\phi(x)),h(x,\phi(x))),(1,\phi'(x))>$ $=$ $g(x,\phi(x)) + h(x,\phi(x)) *\phi'(x) = 0$
- $\exists c \in \mathbb{R}: \Phi(x) = c = F(x,\phi(x))$
- $\phi(\tau) = \xi \implies c=F(\tau,\xi)$ 
- **Fordítva**:
- $F\in C^1$; $F(\tau,\xi) =0$; $\partial_{2}(F(\tau,\xi)) = h(\tau,\xi) \neq 0$   
- **Implicit fv. tétel**:
- $\exists K(\tau),K(\xi): \exists\phi:K(\tau)\to K(\xi)$
- $F(x,\phi(x)) = 0$; $\phi \in C^1$; $\phi'(x) = -\frac{\partial_{1}F(x,\phi(x))}{\partial_{2}F(x,\phi(x))} =-\frac{g(x,\phi(x))}{h(x,\phi(x))}$

**Vázlat**: 
- g, h felírása, F felírása + tulajd.
- Ha $\phi$ megoldás... (felírás)
- Ötlet: $\Phi(x)$ = $F(x,\phi(x))$ bevezetése, ill. $x \to (x,\phi (x)) \in D$ és $\Phi(x)'$ felírása
- K.É.P felírása 
- Fordítva: 
- F tulajdonságaiból => Implicit függvény tétel felírása ($\phi$, folyt. diff, deriv. fv.)
- + Tétel egyértelműségről
- + Szükséges feltétel ($\partial_{2}g = \partial_{1}h$) és ($Young-tétel$)
- + Multiplikátor módszer
- + Minden szeparábilis módszer egzakt 
## Szeparábilis egyenlet

**Legyen**:
- $n = 1$ 
- $I,J \subset \mathbb{R}$
- $g : I \to \mathbb{R}$; $h: J \to \mathbb{R} / \{ 0 \}$; $g,h \in C$
- $f(x,y) = g(x) * h(y)$

**Ekkor**: 
1. $\phi'(x) = g(x) * h(\phi(x))$
2. $\frac{\phi'(x)}{h(\phi(x))} = g(x)$
3. $G: I \to \mathbb{R}$; $H :J \to \mathbb{R}$; $G,H \in D$ 
4. $(H\ o\ \phi)' = G$
5. $(H(\phi(x)) - G(x))' = 0$; $H(\phi(x)) - G(x) \in D \implies$
6. $H(\phi(x)) -G(x) =c\in \mathbb{R}$ 
7. Ill. $D_{H'}$ nem eleme a $0$ => $H$ állandó előjelő => $H$ szigorúan monoton => $\exists H^{-1}$ 
8. $\phi(x) = H^{-1}(G(x) + c)$
9. Ill. **K.É.P.** esetén: $\phi(\tau) = \xi \implies H(\xi) -G(\tau) =c$, és ez a K.É.P. megoldása is


**Vázlat:**
- Feltételek felírása
- D.E. felírása, majd g és h szeparálása
- Primitív függvények felírása
- H függv. invertálhatóságának oka és következménye
- K.É.P. felírása H és G-vel

**Van-e megoldás? (vázlat)**
- Legyen $F(x,y) = H(y) -G(x)$ előbbi jelölésekkel
- Írjuk fel a parciális deriváltakat, illetve folytonosságukat + parc. 2 det.
- Implicit függvény tétel 
- $\phi$ folytonos diff. + deriv. fv. felírása + K.É.P felírása 
- + egyértelműség tétel

## Rakéta emelkedési idejének számítása
$m *v' =-\alpha*m -\beta*v^2$

# Lineáris differenciál egyenletek
## Lineáris D.E.

**Legyen**:
- $n = 1$
- $I \subset \mathbb{R}$ nyílt intervallum 
- $\Omega:= \mathbb{R}$ 
- $g,h : I \to \mathbb{R}$
- $f(x,y) = g(x) * y +h(x)$

**Ekkor**: $\phi:I \to \mathbb{R}$ megoldás, ha
- $\phi'(x) = g(x) * \phi(x) +h(x)$ 

**Ötlet**:
- $M_{0}:= \{ \phi:I\to \mathbb{R} |\phi \in D; \phi'(x) = g(x)*\phi(x)\}$
- $M:= \{ \phi:I\to \mathbb{R} | \phi\in D; \phi'(x) = g(x)*\phi(x) + h(x)\}$
- Van-e elemük?
**1.)** $\phi_{0}\in M_{0}$
- **Legyen**: $G:I \to \mathbb{R}$
- $\phi_{0} = e^{G(x)}$; $\phi_{0}\in D$; $\phi_{0}'(x) = e^{G(x)}*g(x) = \phi(x) *g(x) \implies \phi_{0} \in M_{0}$
- Ráadásul: $\forall c\in \mathbb{R}: c*\phi_{0}\in M_{0}$
 **2.)** $\forall\chi\in M_{0}$: $\frac{\chi}{\phi_{0}}\in M_{0}$ => $M_{0}$ szerkezete! 
**3.)** $\exists m:I\to \mathbb{R};m\in D; \psi:= m *\phi_{0} \in M$ 
**3.)** $\psi - \phi\in M_{0}$, ahol $\psi \in M$ és $\forall \phi \in M$
**4.)** $\forall \phi,\tilde{\phi}\in M: (\phi-\tilde{\phi})\in M_{0}$
**5.)** 3 + 4: $\psi -\phi \in M \iff \psi - \phi = \phi_{0} * c$ => $M$ szerkezete!

**Vázlat**:
1. Lin. D.E. felírás + halmazok
2. Homogén megoldás létezése
3. Homogén megoldások  hányadosa is homogén
4. Létezik olyan $m:I\to \mathbb{R}$, amellyel a homogén megoldást szorozva inhomogén megoldást kapunk
5. Inhomogén megoldások különbsége homogén megoldás
6. 4 + 5-ös kombináció: Inhomogén megoldások létezése! (Ismert inhomogén + homogén megoldás segítségével összes inhomogén megoldás megadása)

## Állandók variálásának módszere

Lásd fent

## Radioaktív bomlás felezési idejének számítása

- $\phi'(x) = -\alpha* \phi(x)$  
- $\phi(0) = M$
- => $\phi(x) = e^{-\alpha x} *c$ 
- +felezési idő számítása
# D.E.-hez kapcsolódó fogalmak, tételek
## Lipschitz-feltétel

$\forall Q \subset \Omega$ kompakt
$\exists L \geq_{0}:$ $\lvert \lvert f(x,u) - f(x,v) \rvert \rvert \leq L * \lvert \lvert u-v \rvert \rvert$
$(x\in I;u,v\in Q)$

## Picard-Lindelöf-féle egzisztencia-tétel (fixpont-tétel alk.)

Ha a d.e. jobb oldala eleget tesz a **Lipschitz-feltételnek**, akkor a szóban forgó d.e-re vonatkozó összes K.É.P. megoldható.

**Legyen**:
- $\delta > 0, \mu > 0$
- $I_{*}:= [\tau-\delta,\tau + \delta] \subset I$
- $K_{\mu} := \{ z \in \mathbb{R}^n | \lvert \lvert z - \xi \rvert \rvert \leq \mu \}$
- $\digamma := \{ \phi:I_{*}\to K_{\mu} | \phi \in C \}$
- Ill. metrika: $\forall \phi,\psi \in \digamma: \rho(\phi,\theta):= \max \{ \lvert \lvert  \phi(x) - \psi(x) \rvert \rvert :x \in I_{*}\}$
- $T$ a $\digamma$-n értelmezve: $T(\phi)(x) = T\phi(x):= \xi + \int^x_{\tau}f(t,\phi(t))\ dt$ 
**Ekkor**: 
1. Igaz-e, hogy $T\psi \in \digamma$? 
	1. ($T\psi\in C$ az integrál fv-ek tulajdonsága miatt)
	2. $T\psi(x) \in K_{\mu} \iff \lvert \lvert T\psi(x) - \xi \rvert \rvert \leq \mu$
	3. $\lvert \lvert T\psi(x) - \xi \rvert \rvert = \left\lvert  \left\lvert  \int^{x}_{\tau} f(t,\psi(t)) dt  \right\rvert  \right\rvert \leq \left\lvert   \int^{x}_{\tau} \lvert \lvert f(t,\psi(t)) dt \rvert \rvert  \right\rvert \leq\dots$
	4. Mivel kompakt $I_{*} \times K_{\mu}$:
	5. $\dots\leq M*|x-\tau|\leq M *\delta$ 
	6. Ha $M *\delta \leq \mu$ => OK, egyébként csökkentsük $\delta$-t
	7. $T: \digamma \to\digamma$ igaz!
2. Igaz-e, hogy $T$ kontrakció?
	1. **Lipschitz-feltétel**
	2. **Spec.:** $Q:= K_{\mu}$
	3. Kontrakció def.
	4. $\rho(T\psi,T\phi) = \max_{x} \left\lvert  \left\lvert  \int^x_{\tau} (f(t,\psi(t))) -f(t,\phi(t))\ dt  \right\rvert  \right\rvert \leq\dots$
	5. $\dots\leq \left\lvert  \int^x_{\tau} \lvert \lvert f(t,\psi(t)) -f(t,\phi(t)) \ dt \rvert \rvert  \right\rvert \leq L * \delta * \rho(\psi,\phi)$
	6. Ha $q:=L * \delta < 1$, akkor jó, egyébként csökkentsük $\delta$-t, ezzel $L$ is csökken
	7. Tehát $T: \digamma\to \digamma$ kontrakció

**+ Fixpont-tétel:**
- $\exists! \phi_{*} \in \digamma: \phi_{*} = T\phi_{*}$
- azaz: $\xi + \int^x_{\tau}f(t,\phi_{*}(t))\ dt = \phi_{*}(t)$
- és $\phi_{*}(\tau) = \xi$ feltéve, hogy $T$ kontrakció

**+ Legyen**: (*Szukcesszív approximáció*)
- $\psi_{0} \equiv \xi; \psi_{n+1}:= \xi + \int^\tau_{x}f(t,\psi_{n}(t))\ dt$
- ($T\psi_{n} =: \psi_{n+1}$) 
+ $\rho(\psi_{*},\psi_{n})\to 0$ és $\rho(\psi_{*},\psi_{n}) \leq \frac{(L*\delta)^n}{1-L*\delta}*\rho(\psi_{0},\psi_{1})$, ahol $\rho(\psi_{1},\psi_{0}) = \max_{x} \lvert \lvert \psi_{0}(x) - \psi_{1}(x) \rvert \rvert = \max_{x}  \left\lvert  \left\lvert  \int^x_{\tau} f(t,\xi)\ dt   \right\rvert  \right\rvert \leq M *\delta$
- És így, ha $\phi_{n}(x):= \psi_{n}(x)$: $max_{x}\lvert \lvert \phi_{n}(x) - \phi(x) \rvert \rvert \to 0\ (n\to \infty)$ és $\max_{x} \lvert \lvert  \phi_{n}(x) - \phi(x) \rvert \rvert \leq \frac{(L*\delta)^n}{1-L*\delta} *M * \delta$  

## K.É.P. megoldásának egyertelműsége ($\emptyset$ biz.)
## Unicitási tétel ($\emptyset$ biz.) 

 T.f.h. $\phi$ megoldás. Mivel: $x \to f(x,\phi(x))\  (x\in D_{\phi})$ folytonos
 => $\phi' \in C$ => $\phi(x) = \xi + \int^x_{\tau}\phi'(t)\ dt = \xi + \int^x_{\tau}f(t,\phi(t))\ dt$ 

**Fordítva** is igaz: K.É.P. $\iff$ "integrál egyenlet"

$\phi(x) := \psi_{*}(x)$, $(x \in I_{*})$
**Ha**:
- $\phi(x) = \xi + \int^x_{\tau}f(t,\phi(t))\ dt$, ú.h. $x \in I_{*}$
- és $\phi(\tau) = \xi$
**Akkor**:
- $\phi$ megoldása a K.É.P.-nek


# Lineáris D.E. rendszerek
## Vizsgálatuk: Homogén/Inhomogén rendszerek

**Legyen**: 
- $n \geq 2$
- $I \subset \mathbb{R}$ nyílt
- $\Omega \subset \mathbb{C}^n$ 
- $a_{ik}: I\to \mathbb{R}$ folytonosak
- $b_{i}:I\to \mathbb{R}^n$ folytonos
- és így: $A := (a_{ik}):I\to \mathbb{R}^{n\times n}$, ill. $f(x,y):= A(x) *y + b(x)$
- $M_{0}:= \{ \phi:I \to \mathbb{C}^n  | \phi\in D\ és \ \phi' = A *\phi \}$ és $M:= \{ \phi:I\to \mathbb{C}^n | \phi\in D \ és \ \phi' = A *\phi + b \}$
**Belátható:** 
-  $\forall$ K.É.P megoldható és $\forall$ teljes megoldás a teljes $I$-n van értelmezve $\phi:I\to \mathbb{C}^n$

**Tétel**: 
1. $\forall m \in \mathbb{N}$ $\phi_{1},\dots,\phi_{n}\in M_{0}: \phi_{1}\dots \phi_{n}$ lineárisan független $\iff$ $\forall \tau \in I: \phi_{1}(\tau),\phi_{2}(\tau),\dots,\phi_{m}(\tau)$ lineárisan független
2. $M_{0}$ n-dim. lineáris tér
3. $\forall \phi_{1},\dots,\phi_{m} \in M_{0}: \exists g_{1},\dots,g_{m}: I \to \mathbb{C}$ : $g_{1},\dots,g_{m} \in D$ és $\psi:= \sum^m_{k = 1}g_{k} *\phi_{k} \in M$  
4. $\phi,\tilde{\phi}\in M: \phi - \tilde{\phi} \in M_{0}$
**Biz.**: (csak végső esetben)
1. <=: Trivi; => Indirekt
2. Stuff
3. More stuff
4. Trivi

## Megoldáshalmaz szerkezete

**Tehát**: 
- $M_{0} := \{  \phi*c | c \in \mathbb{C}^n \}$
- $M := \{ \psi + \chi : \chi \in M_{0} \} = \{  \phi * g + \phi*c : c \in \mathbb{C}^n \}$
- Ilyen $A$ alapmátrix meghatározása nem lehetséges
- Ha $A$ összes komponsense konstans függvény, akkor lehetséges, de ez se szép


# Alaprendszer/Alapmátrix
## Alaprendszer, alapmátrix
## Állandók variálásának módszere

Lásd feljebb (feltétel + állítás)

**Tehát**:
- t.f.h.: $\phi_{1},\dots,\phi_{n} \in M_{0}$ bázis (*alaprendszer*)
- **Legyen**: $\Phi:= [\phi_{1},\dots,\phi_{n}] : I\to \mathbb{C}^{n\times n}$ folytonos mtx. fv. (*alapmátrix*
- **Ekkor**: $\Phi' = A * \Phi$, ha $\Phi' := [\phi_{1}',\dots,\phi_{n}']:I \to \mathbb{C}^{n\times n}$
- **Ha**: $g_{1},\dots,g_{n}:I\to \mathbb{C}$ folyt. és $g:=(g_{1},\dots, g_{n}):I\to \mathbb{C}^n$ folyt. és $\sum_{k =1}^n c_{k} * g_{k} =\Phi *g$ és $(\Phi *g)' = \Phi' *g + \Phi * g'$
- $\psi \in M \iff \psi' =A * \psi + b = A * \phi * g + b$
- $\Phi' *g + \Phi * g' = A * \phi * g + \phi * g'$, azaz $\Phi * g' = b$
- **De**: $\Phi$ oszlopai lin. függetlnek $\implies \forall x \in I : \exists (\Phi(x))^{-1} =\Phi^{-1}(x)$ és $\Phi^{-1}$ folytonos
- **Legyen**: $g'  = \Phi^{-1} * b =: (h_{1},\dots,h_{n}) \iff g'_{i} = h_{i}\ (i = 1,\dots,n)$ 

## Alapmátrix előállítása állandó együtthatós, diagonalizálható mtx. esetén 

**Legyen**:
- $\forall i, k = 1\dots n: a_{ik} \equiv a_{ik} \in \mathbb{R}$ állandó fv. és => $\phi'(x) = \phi(x) * A + b$

**Ekkor**: 
- Ha $A$ mtx. diagonalizálható => $\exists T \in \mathbb{K}^{n\times n}$, hogy $\exists T^{-1}$: 
- $T^{-1} * A * T = diag(\lambda_{1},\dots,\lambda_{n})$ 
- **Legyen**: $T = [t_{1},\dots,t_{n}]$, $t_{i} \in \mathbb{K}^n$ 
- **Ekkor**: $A * T = A * \Lambda$, azaz $A*t_{k} = \lambda_{k} * t_{k}$ ($k = 1,\dots,n$)
- **De**: Mivel $T$-nek létezik inverze (bázis is így), ezért $t_{i}$-k sajátvektorok és $\lambda_{i}$-k sajátértékek

**Állítás**:
- $\phi_{k}(x) = e^{\lambda_{k}x} *t_{k}$ alaprendszer ($x \in I, k = 1\dots n$)
- ui.: $\phi_{k}\in M_{0}$-k triviálisan, lineárisan függetlenek
- ui.: $\forall x \in I$-re $\phi_{k}(x)$-k triviálisan, lineárisan függetlenek
## n = 2 eset vizsgálata tetsz. állandó együtthatós mátrixra

$\begin{bmatrix} \alpha & \beta \\ \gamma & \delta \end{bmatrix}$ nem diagonalizálható $\iff$ $|\gamma| + |\beta| > 0$ és $A$-nak 1 darab kétszeres sajátértéke van, azaz $P(\lambda)$-nak diszkriminánsa = 0
- Azaz $(\alpha -\lambda) * (\delta-\lambda) - \beta * \gamma = \lambda^2 -\lambda(\alpha + \delta) +\alpha *\delta - \gamma *\beta$ 
- $(\alpha + \delta)^2 - 4 *\alpha *\delta + 4 \beta * \gamma = (\alpha - \delta)^2 + 4 *\beta *\gamma = 0 \implies \lambda = \frac{\alpha+\delta}{2}$

**Állítás**: $\exists t_{1},t_{2} \in \mathbb{R}^2$ lin. függetlenek, hogy $A * t_{1} = \lambda_{1} * t_{1}$ és $A * t_{2} = \lambda_{2} *t_{2}+t_{1}$
- ill.: $\phi_{1}(x):= e^{\lambda_{1}x} *t_{1}$
- $\phi_{2}(x) := e^{\lambda_{2}x}*(t_{2} +x * t_{1})$ *alaprendszer*
- **Biz**.: TODO

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

**Kvázi polinom jobb oldal**: 
- **Legyen**:
	-  $Q$ polinom, $\lambda \in \mathbb{K}$ és $c(x) = Q(x) * e^{\lambda x}$
	- $P(x) := x^n + \sum^{n-1}_{k =0} a_{k}* x^k$ ($x \in \mathbb{K}$), $a_{0},\dots,a_{n-1} \in \mathbb{R}$, $n \geq 1$  
- **Ekkor**: 
	- $\exists \psi(x) := x^r * R(x) * e^{\lambda x}$ $(x \in I)$, ahol $R$ polinom $\deg R \leq \deg Q$, $r \in \mathbb{N}$ és a $\lambda$ a $P$-nek $r$- szeres gyöke, és $\psi$ a partikuláris megoldás
	- $r = 0 \implies P(\lambda) \neq 0$; $r >0: P(\lambda) - P'(\lambda) = \dots = P^{(\lambda-1)}(\lambda) = 0$, de $P^{(\lambda)} \neq 0$
	- $\psi(x)$ ilyen választása így eleget tesz $\phi^{(n)}(x)+ \sum^{n-1}_{k=0}a_{k}*\phi^{(k)}(x) = c(x):= Q(x) * e^{\lambda x}$

**$r = 0$ eset**: 
- $\psi(x) = R(x) * e^{\lambda x}\in M \iff \psi^{(n)}(x) + \sum^{n-1}_{k=0}a_{k} *\psi^{(k)}(x)$ $=$ $\sum^n_{k=0} a_{k} *(R*e^{\lambda x})^{(k)} = \sum^n_{k =0} a_{k} * \sum^k_{j =0} {k \choose j} R^{(j)} * \lambda^{k-j}*e^{\lambda x} = Q(x) *e^{\lambda x}$
- $R$ főegyütthatója $=: \alpha \implies$
- $\alpha * \lambda^n + \sum^{n-1}_{k=0} a_{k}* \alpha * \lambda^k = \alpha * P(\lambda) = \beta$, ahol $Q$ főegyütthatója $=:\beta$ 
- Így $\alpha = \frac{\beta}{P(\lambda)}$

**Partikuláris megoldás**:
**1. eset**: $w \neq w_{0}$ => $(q*\sin(w*x))'' + w_{0}^2 * q*\sin(w*x) = \frac{F(x)}{m} = A*\sin(wx)$ 
- $\implies \exists q \in \mathbb{R}: \psi(x):= q * \sin(w * x)$ partikuláris megoldás 
- $\iff -q * w^2 * \sin(wx) + w_{0}^2 * q * \sin(wx) = \frac{F(x)}{m}= A * \sin(wx)$ ($x \in \mathbb{R}$)
- $\iff q = \frac{A}{w_{0}^2 -w^2}$
- $\iff \phi(x) = d*\sin(w_{0} +\delta) +\frac{A}{w_{0}^2 + w^2} * \sin(w*x)$ ($x \in \mathbb{R}$)
**2. eset**: $w_{0} = w$ (*rezonancia*)
- $\implies \nexists x \to q*\sin(wx)$ partikuláris megoldás
- **DE**: $\exists q\in \mathbb{R}: \psi(x):= q * x* \cos(wx)$ ($x\in \mathbb{R}$) partikuláris megoldás
- $\iff q*-2w*\sin(wx) = A * \sin(wx)$
- $\iff q = \frac{A}{-2w}$
- $\iff \phi(x) = d *\sin(wx + \delta) + q * x * \cos(wx) = d*\sin(wx +\delta) - \frac{A}{2w} *x * \cos(wx)$ 
## Csillapítás nélküli kényszerrezgés vizsgálata, rezonancia

$m * \phi'' = F - \alpha * \phi - \beta * \phi' \iff \phi'' + \frac{\alpha}{m} * \phi + \frac{\beta}{m} * \phi' = \frac{F}{m}$
ahol:
- $m$ ~ *tömeg*
- $\alpha$ ~ *visszatérítő ($\alpha>0$)*
- $\beta$ ~ *fékezés ($\beta\geq 0$)*
- $F$ ~ *külső erő*

**Nincs csillapítás** ($\beta = 0$):
- $\phi'' + w_{0}^2 * \phi = \frac{F}{m}$, ahol $w_{0} := \sqrt{ \frac{\alpha}{m} }$, a *sajátfrekvencia* 
- **Ekkor**: $P(t) = t^2 + w_{0}^2 = 0 \iff t = \pm i*w_{0}$ => *valós alaprendszer*: 
	- $x \to \cos(w_{0}*x)$
	- $x \to \sin(w_{0}*x)$
- $M_{0}$ valós értékű elemei: $c_{1} * \cos(w_{0}*x) + c_{2}*\sin(w_{0}*x) = d*\sin(w_{0}*x + \delta)$, ahol
	- $\delta$ ~ *fázisszög*
	- $d$ ~ *amplitúdó* 
- T.f.h: $\frac{F(x)}{m} = A *\sin(w*x)$ ($x \in \mathbb{R};\ w, A \in \mathbb{R}; A, w > 0$)

# Függvénysorozatok, függvénysorok 
## Függvénysorozat fogalma

$(f_{n})$ függvénysorozat, ha $\forall n \in \mathbb{N}: f_{n}$ fv.
- Mindig feltesszük, hogy $\exists D \neq \emptyset: f_{n}:D\to \mathbb{R} \ (n \in \mathbb{N})$  

## Függvénysor fogalma

**Legyen**: $F_{n}:= \sum^n_{k =0} f_{n}\ (n\in \mathbb{N})$ és $\sum(f_{n}) = (F_{n})$ *függvénysor* a $\sum(f_{n})$ $n$-edik részletösszeg fv.  

## Hatványsorok

**Legyen**:
- $a_{n} \in \mathbb{K}$ 
- $f_{n}(x) := a_{n} * (x-a)^n$ ($n \in \mathbb{N}, x\in \mathbb{K}$)

**Ekkor**: 
- $\sum(a_{n}*(x-a)^n) = \sum(f_{n})$ ~ *hatványsor*
- $F_{n}(x) = \sum^n_{k = 0}a_{k}*(x-a)^k$ ~ *polinom*
- **Cauchy-Hadamard**: $\exists! 0 \leq r \leq +\infty$ és $0 < R < +\infty$:
	- $\{ z \in \mathbb{K} : ||z -a | < r \}=:K_{r}(a) \subset D_{0} \subset \overline{K_{R}(a)} := \{  z \in \mathbb{K} : |z -a| \leq r \}$ 

## Trigonometrikus sorok

**Legyen**: 
- $\alpha_{n} \in \mathbb{R}$
- $\beta_{n} \in \mathbb{R}$
- $f_{0} \equiv \alpha_{0}$
- $f_{n}(x) := \alpha_{n} *\cos(n*x) + \beta_{n} * \sin(n*x)$ ($x\in D:=\mathbb{R}$; $1\leq n \in \mathbb{N}$)

**Ekkor**:
- $\sum (\alpha_{n} *\cos(n*x) + \beta_{n}*\sin(n*x):= \sum(f_{n})$ ~ *trigonometrikus sor*
- $F_{n}(x) = \alpha_{0} + \sum^n_{k=1} (\alpha_{k}*\cos(k*x)+ \beta_{k}*\sin(k*x))$ ($n\in \mathbb{N}$; $x \in \mathbb{R}$) ~ *trigonometrikus polinom*

## Fourier-sorok
## Dirichlet-féle magfüggvény
## Konvergencia

**T.f.h.** $x\in D$ és $(f_{n}(x)):\mathbb{N} \to \mathbb{K}$ számsorozat konvergens
**Ekkor**: 
- $(f_{n})$ fv. sor $x$-ben konvergens
## Határfüggvény/Összegfüggvény

**Legyen**: $D_{0}:= \{ x \in D: (f_{n})\ az\ x-ben\ konvergens \}$ az $(f_{n})$ *konvergencia tartománya*

**Hasonlóan** függvénysor esetén is 

**Ha**: $D_{0} \neq \emptyset$, **akkor** $f:D_{0} \to \mathbb{K}$, $f(x):= \lim_{ n \to \infty }f_{n}(x)$ ($x \in D_{0}$), ahol $f$ a $f_{n}$ *határfüggvénye*

**T.f.h.**: $D_{0} \neq \emptyset, x\in D_{0} \implies (F_{n}(x))$ konvergens, azaz $\left( \sum^n_{k =0} f_{k}(x) \right)$ konvergens
**Tehát**: 
- $\sum(f_{n}(x))$ számsor konvergens és 
- $\sum^{\infty}_{k=0}f_{k}(x)$ sorösszeg a határértéke (*összegfv*.)
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