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
## Kapcsolata az inverz függvénnyel

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

**Vázlat**:
1. A mátrix diagonalizálható és állandó együtthatós => ez mit jelent
2. T felírása oszlopvektorosan
3. T-nek van inverze => s.v. és s.é.-k meghatározása
4. **Állítás**: alaprendszer felírása (előző függetlenséget állító állítás alapján) 
## n = 2 eset vizsgálata tetsz. állandó együtthatós mátrixra

$\begin{bmatrix} \alpha & \beta \\ \gamma & \delta \end{bmatrix}$ nem diagonalizálható $\iff$ $|\gamma| + |\beta| > 0$ és $A$-nak 1 darab kétszeres sajátértéke van, azaz $P(\lambda)$-nak diszkriminánsa = 0
- Azaz $(\alpha -\lambda) * (\delta-\lambda) - \beta * \gamma = \lambda^2 -\lambda(\alpha + \delta) +\alpha *\delta - \gamma *\beta$ 
- $(\alpha + \delta)^2 - 4 *\alpha *\delta + 4 \beta * \gamma = (\alpha - \delta)^2 + 4 *\beta *\gamma = 0 \implies \lambda = \frac{\alpha+\delta}{2}$

**Állítás**: $\exists t_{1},t_{2} \in \mathbb{R}^2$ lin. függetlenek, hogy $A * t_{1} = \lambda_{1} * t_{1}$ és $A * t_{2} = \lambda_{2} *t_{2}+t_{1}$
- ill.: $\phi_{1}(x):= e^{\lambda_{1}x} *t_{1}$
- $\phi_{2}(x) := e^{\lambda_{2}x}*(t_{2} +x * t_{1})$ *alaprendszer*
- **Biz**.: TODO

**Vázlat**: 
1. Nem diagonalizálható mátrix vétele (n = 2)
2. Ez mikor nem diagonalizálható? (2 felt. < = >)
3. Lambda levezetése  és felírása
4. **Állítás** (függetlenség + alaprendszer) 
# Magasabb rendű lin. D.E.
## Magasabb rendű lin. D.E.

**Legyen**:
- $2\leq n \in \mathbb{N}$ 
- $\ I \subset \mathbb{R}$ nyílt int.
- $a_{0},\dots,a_{n-1}:I\to \mathbb{R}$ folytonos
- $c:I \to \mathbb{K}$ folytonos

**Cél**: olyan $\phi \in I\to \mathbb{K}$ fv. keresése, hogy:
- $D_{\phi}$ nyílt
- $\phi \in D^n$
- $\forall x \in D_{\phi}$: $\phi^{(n)}(x) + \sum^{n-1}_{k=0} a_{k}(x) *\phi^{(k)}(x)=c(x)$

**Ha még**:
- $\tau \in I;\ \xi_{0},\xi_{1},\dots,\xi_{n-1} \in \mathbb{K}$ és
- $\tau \in D_{\phi}; \phi^{(k)}(\tau) = \xi_{k}$, $(k =0,\dots,n-1)$: K.É.P.

## Átviteli elv 

**Legyen**: 
$$A =\begin{bmatrix}
0 & 1 & 0 & 0 & \dots & 0 & 0 \\
0 & 0 & 1 & 0 & \dots & 0 & 0  \\
\dots  \\
0 & 0 & 0 & 0 & \dots & 0 & 1  \\
-a_{0} & -a_{1} & -a_{2} & -a_{3} & \dots & -a_{n-2} & -a_{n-1} 
\end{bmatrix} : I \to \mathbb{R}^{n\times n}$$

és tekintsük a $\psi' = A * \psi + b$ lineáris d.e. rendszert, ahol $b:=(0,\dots,0,c): I \to \mathbb{K}^n$


Ekkor (**átviteli elv**):
1. Ha $\phi$ ($\phi^{(n)}(x) + \sum^{n-1}_{k=0} a_{k}(x) *\phi^{(k)}(x)=c(x)$)-beli (*magasabbrendű d.e. rendszer*), akkor: $\psi:=(\phi,\phi',\dots,\phi^{(n-1)})$  ($\psi' = A * \psi + b$)-beli (*lineáris d.e. rendszer*)
2. Ha $\psi =(\psi_{1},\dots,\psi_{n})$ ($\psi' = A * \psi + b$)-beli (*lineáris d.e. rendszer*), akkor: $\phi:= \psi_{1}$ ($\phi^{(n)}(x) + \sum^{n-1}_{k=0} a_{k}(x) *\phi^{(k)}(x)=c(x)$)-beli (*magasabbrendű d.e. rendszer*)

## Megoldáshalmaz szerkezete

**Legyen**:
- $M_{0}:= \left\{  \phi:I\to \mathbb{K}: \phi\in D^n; \ \phi^{(n)} + \sum^{n-1}_{k=0} a_{k}*\phi^{(k)} =0  \right\}$ ~ homogén m.o. halmaza
- $M:= \left\{  \phi:I\to \mathbb{K}: \phi\in D^n; \ \phi^{(n)} + \sum^{n-1}_{k=0} a_{k}*\phi^{(k)} = c  \right\}$ ~ inhomogén m.o. halmaza


**Állítás**:
1. $M_{0}$ n-dimenziós vektortér
2. $\forall \phi,\tilde{\phi} \in M: \phi-\tilde{\phi} \in M_{0}$
3. $\forall \phi_{1},\phi_{2},\dots,\phi_{n} \in M_{0}$ bázis (*alaprendszer*) $\exists g_{1},\dots,g_{n}:I\to \mathbb{K}$ differenciálható fv., hogy: $\phi := \sum^n_{k=1}g_{k}*\phi_{k} \in M$ ~ *állandók variálása* (átviteli elv + lin. d.e.r.)

- $M = \psi + M_{0}$, ahol $\psi \in M$
**Legyen**:
- $\hat{\phi_k}:=(\phi_{k},\phi_{k}',\dots,\phi_{k}^{(n-1)}):I\to \mathbb{K}^n$ ~ *alaprendszer* ($k =1,\dots,n$)
- $\Phi := [\hat{\phi}_{1},\hat{\phi}_{2},\dots,\hat{\phi}_{n}] : I\to \mathbb{K}^{n\times n}$, $g:= (g_{1},\dots,g_{n})$

=> $\psi = \Phi * g \in M \iff \Phi * g' =b = (0,0,\dots,c)$

Ill.:
- Fenti felírása mátrixos/vektoros formába
- n darab szumma, azaz:
	- $\sum^n_{k=1} \phi_{k}^{(j)}* g_{k}' =0$, $(j= 0,\dots,n-2)$
	- $\sum^n_{k=1} \phi_{k}^{(n-1)}*g_{k}' = c$

**Wronski-det.**: $W(x) := \det \Phi(x)$ ($x \in I$)

## Állandók variálásának módszere

**Lásd feljebb**

# Állandó együtthatós, magasabb rendű homogén lin. D.E.
## Alaprendszerének előállítása

**Legyen**: 
- $a_{k}\ (k = 0,\dots,n-1) \equiv a_{k} \in \mathbb{R}$ állandó
- $P(t) := t^n +\sum^{n-1}_{k=0} a_{k} * t^k$ ~ $n$-ed fokú polinom, d.e. *karakterisztikus polinomja*
- T.f.h: $\lambda \in \mathbb{K}: P(\lambda) = 0$ és $\phi(x) := e^{\lambda x} \implies T\phi(x) = \lambda^n * e^{\lambda x} + \sum^{n-1}_{k=0} a_{k}*\lambda^k * e^{\lambda x} = e^{\lambda x} * P(x) = 0$, ahol $T\phi(x) := \phi^{(n)}(x) + \sum^{n-1}_{k=0} a_{k} * \phi^{(k)}(x) = c(x)$
- **Ekkor**: $\phi\in M_{0}$, illetve => ha $\lambda$ min. 2-szeres gyök: $\phi(x) := x *e^{\lambda x} \in M_{0}$ is 
- $P(t) = \prod^s_{k = 1} (1-\lambda_{k})^{\nu_{k}}$ ~ $P(t)$ gyöktényezős alakja, ahol
	- $s\in \mathbb{N}$
	- $\lambda_{1},\dots,\lambda_{s}$ a polinom. különböző gyökei
	- $\nu_{1},\dots,\nu_{s}$ a k. gyök multiplicitása
	- és: $\phi_{jk}(x) := x^k *e^{\lambda_{j}x}$, ($x \in I;\ j = 1,\dots,s;\ k = 0,\dots,\nu_{j-1}$) 
- **Ekkor**: $\phi_{jk}$-k alaprendszert alkotnak

**Illetve**: $\phi_{jk}$-k lineárisan függetlenek, azaz:
$\sum^s_{j=1} \sum^{j-1}_{k=0} c_{jk} * x^k *e^{\lambda_{j}x}=0 \iff c_{jk} =0$, ($x\in I$, $c_{jk}\in \mathbb{K}$ együtthatók)


## Karakterisztikus polinom szerepe (biz. vázlat)

### Polinomiális függetlenség (Lemma)
$\forall R_{1},\dots,R_{k}$ polinomok esetén:
- $\sum^s_{k=1}R_{k}(x)*e^{\lambda_{k}x} =0 \iff R_{k} \equiv 0$


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
- $\alpha \in \mathbb{K}$
- $f_{n}(x) := a_{n} * (x-\alpha)^n$ ($n \in \mathbb{N}, x\in \mathbb{K}$)

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
**a)**: 
- $R_{2\pi} := \{ f:\mathbb{R}\to \mathbb{R}$: az $f\ 2\pi$ szerint periodikus és $f|[0,2\pi]\in R[0,2\pi]$$\}$  
- **Ha**: $f \in R_{2\pi}\implies \forall I \subset \mathbb{R}$ zárt, $|I| = 2\pi: f|I \in R(I)$ és $\int_{I} f = \int^{2\pi}_{0}f$, pl. $I := [-\pi,\pi]$
**b)**: 
- **Ha** $f\in R_{2\pi}$ és 
	- $a_{0}:= \frac{1}{2\pi}\int^{2\pi}_{0}f(t)\ dt$
	- $a_{n}:= \frac{1}{\pi}\int^{2\pi}_{0}f(t)* \cos(nt)\ dt$
	- $b_{n}:= \frac{1}{\pi}\int^{2\pi}_{0} f(t) * \sin(nt)\ dt$ 
- **Akkor** az $f\dots$ : 
	- **Fourier-sora**: $\sum a_{n} *\cos(nx) +b_{n}*\sin(nx) =: Sf$
	- $a_{n},b_{n}$ az $f$ *Fourier-együtthatói*
	- **n-edik Fourier részletösszege**: $S_{n}f(x):= a_{0} + \sum^n_{k=1} a_{k}*\cos(kx) + b_{k}*\sin(kx)$, $(n \in \mathbb{N}, x\in \mathbb{R})$

## Dirichlet-féle magfüggvény

$S_{n}f(x) = \frac{1}{2\pi} * \int^{2\pi}_{0} f(t)\ dt + \sum^n_{k =1}\left( \frac{1}{\pi}*\int^{2\pi}_{0}f(t)*\cos(kt)\ dt \right) *\cos(kx) + (\frac{1}{\pi}\int^{2\pi}_{0} f(t) * \sin(nt)\ dt)*\sin(kx) =\dots$
$\dots= \frac{1}{\pi} * \int^{2\pi}_{0}f(t) * \left[ \frac{1}{2} +\sum^n_{k=1} \cos(kt )*\cos (kx)+\sin(kt)*\sin(kx) \right]\ dt=\dots$ 
$\dots= \frac{1}{\pi} *\int^{2\pi}_{0}f(t) *\left[ \frac{1}{2} + \sum^n_{k=1} \cos(k*(x-t)) \right] \ dt= \frac{1}{\pi} *\int^{2\pi}_{0}f(t) * D_{n}(x-t)\ dt$
**ahol**:
- $D_{n}(z) := \frac{1}{2} + \sum^n_{k=1}\cos(k*z)$, $(n\in \mathbb{N}, z \in \mathbb{R})$ a *Dirichlet-magfüggvény*

**Ekkor**:
- $D_{n}$ $2\pi$ periodikus
- $D_{n}(0) = n +\frac{1}{2}$, ha $0<z <2\pi \implies 0< \frac{z}{2} <\pi \implies\dots$

**Legyen**: $\sin\left( \frac{z}{2} \right)\neq 0 \implies \sin \frac{z}{2}*D_{n}(z) = \frac{1}{2} * \sin\left( \frac{z}{2} \right) + \sum^n_{k=1}\cos(kz)* \sin\left( \frac{z}{2} \right) = \dots$
$\dots= \frac{\sin\left( \frac{z}{2} \right)}{2} + \frac{1}{2} *\sum^n_{k=1} \left[ \sin\left( \left( k+\frac{1}{2} \right)*z \right) - \sin\left( \left( k-\frac{1}{2} \right) *z \right) \right] =\dots$
$\dots= \frac{1}{2} * \sin\left( \left( n+\frac{1}{2} \right) * z \right)\implies D_{n}(z) = \frac{\sin\left( \left( n+\frac{1}{2} \right)*z \right)}{2*\sin\left( \frac{z}{2} \right)}$

És ekkor legyen: $\frac{\sin\left( \left( n+\frac{1}{2} \right)*z \right)}{2*\sin\left( \frac{z}{2} \right)} := n+\frac{1}{2}$, ha $z = 0$ 

$\implies S_{n}f(x) = \frac{1}{\pi} * \int^{2\pi}_{0}f(t) * \frac{\sin\left( \left( n+\frac{1}{2} \right)*(x-t) \right)}{2*\sin\left( \frac{x-t}{2} \right)}\ dt$

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

**Def**: 
- **T.f.h.**: $\emptyset \neq A \subset D;\ f : A \to \mathbb{K}; \forall \epsilon > 0 \ \exists N \in \mathbb{N}, \forall n \in \mathbb{N}, n > N, \forall x\in A: |f_{n}(x) - f(x)|< \epsilon$  
- **Ekkor**: $(f_{n})$ az $A$-n *egyenletesen konvergál $f$-hez*

**Megj**:
1. $A \subset D_{0}:$ ha $A = D_{0}$, akkor: $(f_{n})$ egyenletesen konvergens

### Spec.: Egyenletes Cauchy-krit

$A = D$ esetén: $(f_{n})$ egyenletesen konvergens $\iff$ 
- $\forall \epsilon > 0,\ \exists N \in \mathbb{N}\ \forall m,n \in \mathbb{N};\ m,n > N, \forall x \in A: |f_{m}(x) - f_{n}x()| < \epsilon$ (*egyenletes Cauchy-krit.*)

### Spec.:

$\sum(f_{n})$ egyenletesen konvergens az $A$-n, ha $(F_{n})$ egyenletesen konvergens az $A$-n, azaz:
- $\forall \epsilon > 0; \exists N \in \mathbb{N};\ \forall m,n \in \mathbb{N};\ m> n > N;\ \forall x\in A: |F_{n}(x) - F_{m}(x)| =|\sum^m_{k=n+1}f_{k}(x)|<\epsilon$

## Weierstrass-féle majoráns krit.

**T.f.h:** $(a_{n}): \mathbb{N}\to[0, +\infty)$ és $\sum^\infty_{n=0} a_{n} < +\infty$, továbbá:
- $|f_{k}(x)|\leq a_{k}$, ($k \in \mathbb{N};\ x\in A$)

**Ekkor**:
- $\sum(f_{n})$ egyenletesen konvergens az $A$-n

# Konvergens függvénysorozat tulajdonságai

**Legyen**: 
- $D \subset \mathbb{K};\ f_{n}: D\to \mathbb{K};\ n\in \mathbb{N}$ és $f_{n}$ *egyenletesen konvergens*
- $f(x):= \lim_{ n \to \infty }f_{n}(x)$; ($x\in D$) 

## Folytonosság kérdése

**Legyen**:
- $D \neq \emptyset;\ f_{n}: D\to \mathbb{K}$ ($n \in \mathbb{N}$) és t.f.h.: $D_{0} \neq \emptyset;\ f(x):= \lim_{ n \to \infty } f_{n}(x)$
**Kérdés**:
Ha, a konvergens függvénysorozat folytonos, akkor a határfüggvénye is folytonos-e?
Nem -> Még fel kell tennünk az egyenletes folytonosságot is.

**Például**:
$$f_{n}(x) =\begin{cases}
1-xn : 0 < x \leq \frac{1}{n}  \\
0 : x > \frac{1}{n}
\end{cases}$$
Ekkor
$$
f(x) = \begin{cases}
1 : x = 0 \\
0 : 0 < x \leq 1
\end{cases}
$$
és $f \notin C\{ 0 \}$
## Riemann-integrálhatóság kérdése

**Legyen**:
- $D \neq \emptyset;\ f_{n}: D\to \mathbb{K}$ ($n \in \mathbb{N}$) és t.f.h.: $D_{0} \neq \emptyset;\ f(x):= \lim_{ n \to \infty } f_{n}(x)$
**Kérdés**:
Ha, a konvergens függvénysorozat Riemann-integrálható, akkor a határfüggvénye is?
Nem -> Még fel kell tennünk az egyenletes folytonosságot is.

**Példa**:
Legyen: $(r_{n}): \mathbb{N}\to[0,1]$ ~ racionális számok sorozata
$$f_{n}(x) := \begin{cases}
1: x \in \{  r_{0},\dots,r_{n} \} \\
0: különben
\end{cases}$$
és $f_{n} \in R[0,1]$ és határfüggvénye létezik:
$$
f(x) := \begin{cases}
1: x\in Q \\
0: x \notin Q
\end{cases}
$$
**Dirichlet fv.**: $\implies f \not\in R[0,1]$

**Másik példa**: 

$$
f_{n}(x) = \begin{cases}
a_{n} :\left( 0 < x < \frac{1}{n} \right) \\
0: x \in [0,1] \setminus \left( 0, \frac{1}{n} \right)
\end{cases}
$$
Ekkor: $\frac{a_{n}}{n}$ az integrálja, ill. $f \equiv 0$
Ha viszont $a_{n} := n$, akkor a kettő integrálja $[1,2]$ intervallumon: $0 \neq 1$ lesz 
## Egyenletes fv.-sorozat folytonossága

**Legyen**:
- $a \in D; \ f_{n} \in C\{ a \}, (n\in \mathbb{N})$
**Ekkor**: $f \in C \{ a \}$

**Legyen**:
- $f_{n} \in C$
**Ekkor**:
- $f \in C$ 


**Biz.**: 
1. **Legyen**: $A := D$ 
2. $f(x) - f(a)$ írjuk fel bővítve $f_{n}(x)$ és $f_{n}(a)$-val
3. Tegyünk egy felső becslést, alakítsuk át amit lehet epszilonná
4. Használjuk fel a folytonosságot, miszerint létezik olyan delta, amellyel már felül becsülhető a maradék rész epszilonnal 
5. Írjuk fel csak epszilonos felső becsléssel ($< 3 *\epsilon$)

## Egyenletes fv.-sorozat integrálhatósága

**Legyen**: 
- $-\infty <a < b < +\infty;\ D := [a,b]$
- $f_{n}:[a,b]\to \mathbb{R}$, $f_{n} \in R[a,b], (n \in \mathbb{N})$
- $f_{n}$ egyenl. konvergens, $f(x):= \lim_{ n \to \infty }f_{n}(x)$ ($x \in[a,b]$)
**Ekkor**:
- $f\in R[a, b]$ és $\int^b_{a} f= \lim_{ n \to \infty }\left( \int^b_{a} f_{n} \right)$

**Biz.**:
1. f Riemann integrálható < = > létezik megfelelő felosztás
2. Oszcillációs összeg felírás: $\omega(f,\tau) = \sum^{s-1}_{i=0} \sup\{ |f(x) - f(y)|: x_{i} \leq x,y \leq x_{i+1} \} *(x_{i+1} - x_{i}) < \epsilon$
3. Legyen i tetszőleges felosztásnak indexe, x és y a két szomszédos felosztás közti szám
4. Írjuk fel abszolút értékbeli különbségüket, és becsüljük felül $f_{n}$ segítségével
5. Használjuk fel az egyenletes konvergenciát -> így kiesik 2 tag és epszilon lesz helyette
6. **Legyen**: $O_{i}(f) = \sup\{ |f(x) - f(y)|: x_{i} \leq x,y \leq x_{i+1} \}$
7. **Ekkor**: $O_{i}f \leq 2 * \epsilon + O_{i}(f_{n})$
8. **Azaz**: $\omega(f,\tau) \leq 2*\epsilon * (b-a) + \omega(f_{n},\tau)$ 
9. De $f_{n}$ Riemann-integrálható, azaz létezik olyan $\tau$ felosztás, amellyel: $\omega(f_{n}, \tau) < \epsilon$ 
10. Tehát $w(f,\tau) < 3*\epsilon$ azaz $f$ Riemann integrálható
11. **Továbbá**: $\forall n: \left\lvert  \int^b_{a} f(x)\ dx - \int^b_{a} f_{n}(x)\ dx  \right\rvert \leq \int^b_{a}\lvert f(x) - f_{n}(x) \rvert \ dx \leq (b-a) * \epsilon$  is igaz!


## Integrálás és határátmenet felcserélhetősége

**Lásd feljebb.**

# Függvénysorozatok és differenciál
## Határfüggvény differenciálhatósága tétel

**Legyen**:
- $I \subset \mathbb{R}$ nyílt és korlátos, $f_{n} : I\to \mathbb{R}$, $f_{n} \in D$
- $(f_{n}')$ egyenletesen konvergens
**Ha**: $\exists a \in I: f_{n}(a)$ konvergens

**Akkor**: 
- $(f_{n})$ egyenletesen konvergens
- $f(x):= \lim_{ n \to \infty }f_{n}(x)$
- $f \in D$, $f(x)' = \lim_{ n \to \infty } f_{n}'(x)$, ($\forall x \in I$)  

**Biz.**:
1. Legyen m, n term. szám, $a \neq x \in I$ és induljunk ki: $f_{m}(x) - f_{n}(x)$-ből
2. $\dots = f_{m}(x) -f_{m}(a) + f_{m}(a) - f_{n}(a) + f_{n}(a) - f_{n}(x) \leq\dots$
3.  $\dots\leq \lvert (f_{m} - f_{n})(x) - (f_{m} - f_{n})(a) \rvert + \lvert f_{m}(a) - f_{n}(a)  \rvert \leq\dots$
4. $\dots =  |(f_{m} -  f_{n})'(\xi) * (x-a)| + |f_{m}(a) - f_{n}(a)| \leq\dots$
5. $\dots \leq \lvert f_{m}'(\xi) - f_{n}'(\xi) \rvert * \lvert I \rvert +\lvert f_{m}(a) - f_{n}(a) \rvert \leq \epsilon *(1 + |I|)$, mert $f_{n}'$ egyenletesen konvergens, azaz egyenletes Cauchy kritérium teljesül, illetve $a$-ban konvergens $f_{n}$, azaz a Cauchy kritérium teljesül
6. Legyen $z \in I$, és legyen $$\phi_{n}(x) = \begin{cases}
\frac{f_{n}(x) - f_{n}(z)}{x -z} : z \neq x \in I \\
f_{n}'(z): z = x
\end{cases}$$
1. Ekkor lássuk, be hogy $\phi_{n}$ folytonos ($x\neq z$-nél $f_{n}$ folytonossága + műveletek);($x = z$-nél vizsgáljuk meg a limeszt, ha x z-hez közelít)
2. **Továbbá** $\phi_{n}$ egyenletesen konvergens, mert: Lagrange k.é.t. felhasználva írjuk fel az alábbit:
3. $\frac{(f_{n}(x) - f_{m}(x))-(f_{n}(z) - f_{m}(z))}{(x-z)} = (f_{n}-f_{m})'(\xi_{nm}) = f_{n}'(\xi_{nm}) - f_{m}'(\xi_{nm})$, ahol $\xi_{nm} \in (z,x)$
4. **Így**: $$\lvert  \phi_{n}(x) - \phi_{m}(x) \rvert = \begin{cases}
\lvert f_{n}'(\xi_{nm}) - f_{m}'(\xi_{nm}) \rvert : z \neq x \in I \\
\lvert  f_{n}'(z) - f_{m}'(z) \rvert : z = x \\ 
\end{cases}$$
1. Mivel $f_{n}'$ egyenletesen konvergens, így egyenletes Cauchy-krit. is teljesül, azaz $\forall \epsilon>0, \exists N \in \mathbb{N};n,m \in \mathbb{N};n,m > N:\lvert f_{n}'(t) - f_{m}'(t) \rvert < \epsilon$
2. Emiatt $|\phi_{n}(x) - \phi_{m}(x) | < \epsilon$ is igaz, azaz teljesül rá a Cauchy-krit. => Így valóban egyenletesen konvergál
3. Azt is tudjuk, hogy $$\phi(x) := \lim_{ n \to \infty } \phi_{n}(x) = \begin{cases}
\frac{f(x) - f(z)}{x -z} : x \neq z \\
\lim_{ n \to \infty } f_{n}'(z) : x = z
\end{cases}$$
4. **Azaz**: $\lim_{ n \to \infty } f_{n}'(z) = \phi(z) = \lim_{ x \to z }\phi(x) = \lim_{ x \to z } \frac{f(x) - f(z)}{x-z}$

## Deriválás és határátmenet felcserélhetősége

**Lásd feljebb.**

A fenti tétel feltételei mellett: $(\lim_{ n \to \infty }f_{n})' = \lim_{ n \to \infty }f_{n}'$ 
Azaz a határátmenet és deriválás felcserélhető

# Trigonometrikus rendszerek + Bessel
## Trigonometrikus rendszerek ortogonalitása

**Legyen**: ($1 \leq n \in \mathbb{N}$)
- $c_{0}(x):= 1$
- $c_{n}(x):= \cos(nx)$
- $s_{n}(x):= \sin(nx)$
és $T:=\{c_{0},c_{n},s_{n} :1 \leq n \in \mathbb{N}\}$ *trigonometrikus rendszer*

**Ekkor**: *trigonometrikus rendszer ortogonalitás*
$$\forall \phi, \psi \in T : \int^{2\pi}_{0} \phi*\psi = \begin{cases}
2\pi : \phi = \psi = c_{0} \\
0: \phi \neq \psi \\
\pi : \phi = \psi \neq c_{0}
\end{cases}$$
Illetve ez elmondható bármely $2\pi$ hosszúságú korlátos és zárt $I \in \mathbb{R}$-re

## Egyenletesen konvergens trigonometrikus sor összegfüggvényének Fourier-sora

**T.f.h.**:
- $\sum(\alpha_{k} * \cos(kx) + \beta_{k}*\sin(kx))$ trigonometrikus sor egyenl. konvergens
- $f(x):= a_{0} + \sum^{\infty}_{k=1} \alpha_{k} * \cos(kx) + \beta_{k}*\sin(kx)$ ($x\in \mathbb{R}$)

**Ekkor**: $1\leq n \in \mathbb{N}$
- $a_{0} := \frac{1}{2\pi} *\int^{2\pi}_{0} f(x)\ dx$
- $a_{n}:= \frac{1}{\pi}*\int^{2\pi}_{0} f(x) *\cos(nx)\ dx$
- $b_{n}:= \frac{1}{\pi} *\int^{2\pi}_{0} f(x)*\sin(nx)\ dx$ 

## Bessel azonosság
**Legyen**:
- $n \in \mathbb{N}$; $\alpha_{0},\dots,\alpha_{n} \in \mathbb{R}$; $\beta_{0},\dots,\beta_{n} \in \mathbb{R}$ 
- $R(x):= \alpha_{0} + \sum^n_{k=1}(\alpha_{k}*\cos(kx) + b_{k}*\sin(kx))$ 
**Ekkor**:
$\int^{2\pi}_{0} (f(x)-R(x))^2\ dx = \int^{2\pi}_{0} f^2(x) \ dx - \int^{2\pi}_{0}f(x)*R(x)\ dx + \int^{2\pi}_{0}R(x) * R(x)\ dx = \dots =$
$\dots= \int^{2\pi}_{0} f_{2} - 2\left( 2\pi a_{0}\alpha_{0} + \pi \sum^n_{k=1}(a_{k}\alpha_{k} + b_{k}\beta_{k}) \right) + 2\pi \alpha_{0}^2 + \pi \sum^n_{k=1}(\alpha_{k}^2+\beta^2_{k})$

**Spec.:** (ha az együtthatók megegyeznek) (*Bessel-azonosság*)
$\int^{2\pi}_{0} (f(x)-R(x))^2\ dx = \int^{2\pi}_{0}f^2-\pi\left( 2a_{0}^2 +\sum^n_{k=1}(a_{k}^2 + b_{k}^2) \right)$ 

... és ebből jön a *Bessel egyenlőtlenség* 
## Bessel egyenlőtlenség

$\exists \min_{R} \int^{2\pi}_{0}(f-R)^2 = \int^{2\pi}_{0}f^2 - \pi * \left[ 2*a_{0}^2 + \sum^n_{k=1} (a_{k}^2 + b_{k}^2) \right]$ ($\geq 0$)

- $2a_{0}^2 + \sum^\infty_{k=1}(a_{k}^2 + b_{k}^2)\leq \frac{1}{\pi} *\int^{2\pi}_{0} f^2$ ~ *Bessel egyenlőtlenség*
-  és itt valójában $=$ van, ez pedig az ún. *Parseval-egyenlőség*

# Egyenletesen konvergens Fourier sorok
## Egyenletesen konvergens Fourier sorok

**Legyen**: 
- $f\in C_{2\pi}$
- t.f.h.: $Sf$ egyenletesen konvergens

**Ekkor**:
- $f(x) = a_{0}+\sum^{\infty}_{k=1}(a_{k}*\cos(kx)+b_{k}*\sin(kx))$
- azaz a fv. Fourier sorba fejthető

## Trigonometrikus rendszer teljessége $C_{2\pi}$-re

**1. Állítás**:
**T.f.h.**:
- $S:=\sum (\alpha_{n} * \cos(nx) + \beta_{n}*\sin(nx)$ egyenletesen konvergens
- $f(x):= \alpha_{0} + \sum^\infty_{k=1} \alpha_{k}*\cos(xk) + \beta_{k}*\sin(xk)$ $x \in \mathbb{R}$
**Ekkor**:
- $f\in C_{2\pi}:= \{ f \in R_{2\pi} | f \in C \}$
- $S=Sf$

**Biz.**:
1. Ui. $f\in C_{2\pi}$
2. Legyen $1 \leq k \in \mathbb{N}: g(x):= \sin(kx)$, így g korlátos és $S * g$ egyenletesen konvergens
3. $f(x)*g(x)$ felírása, kifejtése. Használjuk fel, hogy trigonometrikus rendszer ortogonális
4. Így: $\pi b_{k} = \int^{2\pi}_{0}f(x)*\sin(kx)\ dx =$ "tagonkénti integrál" = $\beta_{k}\pi$, azaz $\beta_{k} = b_{k}$ 
5. Hasonlóan $\alpha_{l} = a_{l}$
6. **Fordítva**: $f\in C_{2\pi};\ S:= Sf$, azaz t.f.h. $Sf$ egyenletesen konvergens
	1. Legyen $g\in C_{2\pi}$ az összefv.-e
	2. Ekkor $Sg = Sf$, azaz $g$ és $f$ Fourer-együtthatói azonosak


**2. Állítás** (*teljesség*)
**Legyen**:
- $h := f-g \in C_{2\pi}$, és t.f.h.  $h$ Fourier-együtthatói $\equiv 0$ 

**Ekkor**:
- $h \equiv 0$ 

**Biz.**:
1. 1. Ötlet: **Indirekt feltevés**: $h(0) > 1$ 
2. De: $h \in C \implies \exists 0 < \delta < \frac{\pi}{2}: h(x) >1$ ($|x|< \delta$)  
3. 2. Ötlet: $T(x) = \cos x + 1 - \cos\delta$ , ekkor $T^n$ trig. polinom minden n-re (term. szám) (*telj. ind.*)
4. és $\int^{2\pi}_{0} h*T^n = 0$ (h Fourier együtthatói 0-k)
5. 3. Ötlet: **Belátjuk** $\exists n \in \mathbb{N}: \int^{2\pi}_{0} h*T^n \neq 0$ 
6. Világos, hogy $\delta \in (0, \frac{\pi}{2})$, akkor $\cos\delta \in (0,1)$
7. Legyen $\delta < \Delta < \frac{\pi}{2}$
8. $\int^\pi_{-\pi} h*T^n = \int_{-\pi}^{-\Delta} h*T^n + \int_{-\Delta}^{-\delta}h *T^n + \int_{-\delta}^{\delta}h*T^n + \int_{\delta}^{\Delta}h*T^n + \int_{\Delta}^\pi h*T^n$
9. Adjuk alsó becslést: $2\delta - \int^{-\Delta}_{-\pi}|h *T^n| - \dots - \int^{\pi}_{\Delta}|h*T^n|$
10. Világos, hogy $\int^{-\delta}_{-\Delta} |h*T^n| + \int^{\Delta}_{\delta}|h*T^n| < 2*\lvert \lvert h \rvert \rvert_{\infty} * (\delta - \Delta)$
11. és $\int^{-\Delta}_{-\pi}|h *T^n| + \int^\pi_{\Delta}|h*T^n| \leq 2* \lvert \lvert h \rvert \rvert_{\infty} * q_{\Delta}^n  *\pi$, ahol $q_{\Delta}:= \max_{\Delta\leq x \leq \pi}|T(x)| < 1$
12. Legyen így $2*\lvert \lvert h \rvert \rvert_{\infty}*(\delta - \Delta) < \frac{\delta}{2}$ és $n\in \mathbb{N}: 2*\pi*\lvert \lvert h \rvert \rvert_{\infty} *q_{\Delta}^n < \delta$
13. Ekkor $\int^\pi_{-\pi}h*T^n \geq 2*\delta - \delta -\frac{\delta}{2}= \frac{\delta}{2} >0$, tehát valóban beláttuk
# Fourier sorok I.
## Kétszer folytonosan differenciálható fv.-k Fourier sora
## $f \in C_{2\pi}, f(x):=(x-\pi)^2 \ (0 \leq x\leq 2\pi)$ függvény Fourier-sora

**Vázlat**:
1. $b_{n},a_{n},a_{0}$ kiszámítása, függvény paritás felhasználása
2. Fourier-sor felírása
3. $Sf$ egyenletes konvergenciájának megmutatása Weierstrass-kritériummal
4. Azaz $f = Sf$-el is igaz lesz
## $\frac{\pi^2}{6}= \sum^{\infty}_{k=1}k^{-2}$ egyenlőség

**Lásd fent** + $x=0$ esetet számoljuk ki! Ez adja a fenti egyenlőséget

# Fourier sorok II.
## $\sum^{\infty}_{k=1}k^{-1}*\sin(kx)\ (x\in \mathbb{R})$ sor konvergenciája, összegfüggvénye

**Állítás**:
- $\forall 0 < \delta < \pi: \sum\left( \frac{\sin(kx)}{k} \right)$ egyenletesen konvergens a $(\delta,2\pi-\delta)$ intervallumon

**Biz.**:

1. **Cél**: Megmutatni, hogy az *egyenletes Cauchy kritérium* teljesül
2. Ehhez legyen írjuk fel: $\sin\left( \frac{x}{2} \right) *\sum^\infty_{k=m+1} \frac{\sin(kx)}{k}$
3. Világos, hogy $\delta < x < 2\pi - \delta \implies \frac{\delta}{2} < \frac{x}{2} <\pi-\frac{\delta}{2} <\pi$ illetve $\sin\left( \frac{\delta}{2} \right)\leq\sin\left( \frac{x}{2}  \right)$  
4. Trigonometrikus addíció tétel felhasználása
5. Ábel-átalakítás + Teleszkópikus összeggé alakítás
6. Kifejtés: $\frac{1}{m+1}$
7. Ekkor adjunk felső becslést: $|\sum^n_{k=m+1} \frac{\sin(kx)}{k}|\leq \frac{1}{m+1} *\frac{1}{\sin\left( \frac{x}{2} \right)}\leq \frac{1}{m+1} * \frac{1}{\sin\left( \frac{\delta}{2} \right)}$ 
8. Teljesül az *egyenletes Cauch kritérium =>* korábbi tétel alapján deriváljuk tagonként a következőt: $\frac{\pi^2}{3} + 4 *\sum^{\infty}_{k=1} \frac{\sin(xk)}{k} = (x-\pi)^2$
9. Fejtsük ki $\frac{\pi-x}{2} =\dots$ -re az egyenlőséget
10. Tehát a fűrészfog fv. Fourier-sora előállítja 
## Rezgő húr problémája

**Feladat**: két végén rögzített húr mozgása
**Matematika modell**:
- $l > 0$, $t \in \mathbb{R}$
- $u:\mathbb{R}^2 \to \mathbb{R}$, $u \in C^2$
- *Kérdés*: $u$ felírása 

**Peremfeltétel**:
- $u(0,t) = u(l,t) = 0$
- $u(x,t) = F(x) * G(t)$, ahol $F,G:\mathbb{R}\to \mathbb{R}; F,G \in C^2$ 
- $\exists q > 0: \partial_{22}u = q * \partial_{11}u \implies$ $F(x) * G''(t) = q *F''(x)*G(t)$ 
- => $\frac{G''(t)}{G(t)} = q* \frac{F''(x)}{F(x)}$, ahol világos, hogy $u \neq 0$ (különben nyugalmi helyzet)
- => **Azaz**: $\exists \lambda \in \mathbb{R}: \frac{G''(t)}{G(t)} = q* \frac{F''(x)}{F(x)} = \lambda$ 
 
**Így**: $G'' - \lambda *G = 0$ és $F''-\frac{\lambda}{q}*F =0$ 
- Állandó együtthatós, homogén diff. egyenlet

**Esetek**:
$\lambda = 0$, azaz 2. deriv. $\equiv 0$
1. $\exists a,b,c,d \in \mathbb{R}:$ $u(x,t) = (c*x +d)(a*t + b)$
2. Peremfeltételek miatt $u\equiv 0$ 

$\lambda > 0$:
1. Karakterisztikus polinom $z^2-\lambda \implies \pm \sqrt{ \lambda }$ gyökök 
2. $\exists a, b\in \mathbb{R}: G(t) = a * e^{\sqrt{ \lambda }t} + b*e^{-\sqrt{ \lambda }t}$
3. és hasonlóan: $F(x) = c *e^{\sqrt{ \frac{\lambda}{q} }x} + d*e^{-\sqrt{ \frac{\lambda}{q} }x}$ 
4. Peremfeltétel miatt $u \equiv 0$

$\lambda < 0$: 
1. Karakterisztikus polinom: $\pm i*\sqrt{ |\lambda| }$
2. Ekkor: $G(t) = a * \cos(\sqrt{ \lambda}t) + b *\sin(\sqrt{ \lambda}t)$
3. és: $F(x) = c *\cos\left( \sqrt{ \frac{\lambda}{q} }x \right) + d *\sin\left( \sqrt{ \frac{\lambda}{q} } x\right)$
4. Írjuk fel a peremfeltételeket, ekkor: $c = 0$ lesz, illetve $d \equiv 0$ SEM jó, különben $u \equiv0$
5. Ekkor világos, hogy: $\sin\left( \sqrt{ \frac{\lambda}{q} }l \right) = 0 \iff \sqrt{ \frac{\lambda}{q} }l = n\pi$
6. Azaz $\sqrt{ \lambda } = \frac{n\pi \sqrt{ q }}{l}$ 
7. Írjuk fel $u(x,t)$ a behelyettesítésekkel
8. Írjuk fel az alkalmas feltételeket, illetve következményüket
	1. $u(x,t) = \sum^\infty_{n=0} u_{n}(x,t)$ megoldás
	2. Kezdeti feltételek: $u(x,0) = f(x)$, $\partial_{2}u(x,0) = g(x)$ ($x \in [0,l]$)
	3. $f(x) = \sum^\infty_{n =0} u_{n}(x,0)$ + kifejtés ($f,g \in \mathbb{R}\to \mathbb{R}$)
	4. $g(x) = \sum^\infty_{n=0}\partial_{2}u(x,0)$ + kifejtés
	5. *n-től függő részek az ú.n. felhangok*
