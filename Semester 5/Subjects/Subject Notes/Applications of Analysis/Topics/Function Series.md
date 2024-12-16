# Függvénysorozatok

**Legyen**:
- $f_{n}(x)$ fv. sorozat ($n \in \mathbb{N}^+$, $x \in \mathbb{R}$) 
- $f(x) = \lim_{ n \to \infty } f_{n}(x)$ 

**Konvergencia halmaz megállapítása**: ($KH(f_{n}) = D_{0}$)
- Azon pontok, ahol a fv. sorozat konvergál

## Egyenletes konvergencia vizsgálata
1. $\forall \epsilon > 0\ \exists N\in \mathbb{N}\ \forall n \in \mathbb{N} n > N$ és $\forall x\in D_{0}: |f_{n}(x) -f(x)| <\epsilon$ 
2. **Legyen:** $\epsilon$ fix, $x \in D_{0}$
3. Adjunk egy olyan csak $n$-től függő becslést, amely eleget tesz annak, hogy $< \epsilon$, ez most legyen $g(n)$
5. **Ekkor**: $\forall \epsilon > 0\ \exists\ N:= [g(n)]+1\in \mathbb{N}\  \forall n \in \mathbb{N}: n>N$ és $\forall x\in D_{0}$=> $|f_{n}(x) - f(x)| \leq \frac{1}{n} < \frac{1}{N} < \epsilon$, azaz a *konvergencia egyenletes*
Ált. ezt a legbővebb $D_{0}$ halmazt kell meghatároznunk.

## Egyenletes konvergencia cáfolása

### Tétellel
Egy $A \subset (-1,1], A \neq \emptyset$ halmazra egyenletesen konvergens egy fv. sorozat $\iff$ $\pm 1 \in A'$.

**Általánosan**: a $A'$-nek ($A$ torlódási pontjainak halmazának) van olyan eleme, ahol $f$ nem folytonos $\iff$ *nem* egyenletesen konvergens a fv. sorozat $A$-n.
### Definícióval
Először megsejtük, hogy valóban nem igaz az egyenletes konvergencia most.
**Majd**:
- $\exists \epsilon >0,\ \forall N \in \mathbb{N},\ \exists n \in \mathbb{N}$ és $\exists x \in H: |f_{n}(x) -f(x)|\geq \epsilon$ 
- Keressünk egy olyan $\epsilon$-t, amire igaz lesz a fenti.
- Adjunk meg egy $n:=N+1$-et
- Adjunk meg egy $x_{n}$ a $H$-ból, amelyre igaz lesz, hogy $|f_{n}(x)-f(x)|\geq \epsilon$

### Egyéb
Ha $\exists x \in D_{0}$, hogy $\forall n: f_{n} \in C\{ x \}$, de $f\notin C\{ x \}$, akkor a konvergencia **nem** egyenletes 

## Integrál számítás
**Legyen**:
- $f_{n}$ fv. sorozat
- $f_{n} \in D([a,b])$
- $f_{n}(x)$ egyenletesen konvergens
- $f = \lim_{ n \to \infty } f_{n}$

**Ekkor**:
- $\lim_{ n \to \infty }\int^b_{a} f_{n} = \int^b_{a}\lim_{ n \to \infty } f$
- Feladatnál meg kell mutatnunk, hogy $f_{n}$ valóban egyenletesen konvergens

# Függvénysorok

## Egyenletes konvergencia cáfolása

**Legyen**: 
- $\sum_{n=0}f_{n}(x)$ 

### Tétellel
Egy $A \subset (-1,1], A \neq \emptyset$ halmazra egyenletesen konvergens egy fv. sorozat $\iff$ $\pm 1 \in A'$ 

**Általánosan**: a $A'$-nek ($A$ torlódási pontjainak halmazának) van olyan eleme, ahol $f$ nem folytonos $\iff$ *nem* egyenletesen konvergens a fv. sorozat $A$-n

### Állítással
Ha $\sum_{n=0} (f_{n})$ egyenletesen konverges egy $A \subseteq D_{0}$ $\implies$ $(f_{n})\to 0 \equiv f; (n\to \infty)$ egyenletesen konvergál 

**Azaz**: mutassuk meg, hogy az $f$ nem egyenletesen konvergál, ekkor $\sum_{n=0}(f_{n})$ sem egyenletesen konvergens (ld. [[#Egyenletes konvergencia cáfolása]])

### Egyéb
Ha $\exists x \in D_{0}$, hogy $\forall n: f_{n} \in C\{ x \}$, de $f\notin C\{ x \}$, akkor a konvergencia **nem** egyenletes 