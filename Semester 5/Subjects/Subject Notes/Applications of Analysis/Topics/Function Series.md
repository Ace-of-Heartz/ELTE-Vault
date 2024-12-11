# Függvény sorozatok
**Legyen**:
- $f_{n}(x)$ fv. sorozat ($n \in \mathbb{N}^+$, $x \in \mathbb{R}$) 
- $f(x) = \lim_{ n \to \infty } f_{n}(x)$ 

**Konvergencia halmaz megállapítása**: ($KH(f_{n}) = D_{0}$)
- Azon pontok, ahol a fv. sorozat konvergál

## Egyenletes konvergencia vizsgálata
1. $\forall \epsilon > 0\ \exists N\in \mathbb{N}\ \forall n \in \mathbb{N} n > N$ és $\forall x\in D_{0}: |f_{n}(x) -f(x)| <\epsilon$ 
2. **Legyen:** $\epsilon$ fix, $x \in D_{0}$
3. Adjunk olyan $n$-et, amelyre teljesül, hogy $n > \frac{1}{\epsilon}$ (vagy annak valamilyen fv.-e)
4. **Tehát**: $\forall \epsilon > 0\ \exists\ N:= [\frac{1}{\epsilon}]+1\in \mathbb{N}\  \forall n \in \mathbb{N}: n>N$ és $\forall x\in D_{0}$=> $|f_{n}(x) - f(x)| \leq \frac{1}{n} < \frac{1}{N} < \epsilon$, azaz a *konvergencia egyenletes*
Ált. ezt a legbővebb $D_{0}$ halmazt kell meghatároznunk

## Egyenletes konvergencia cáfolása

## Tétel
Egy $A \subset (-1,1], A \neq \emptyset$ halmazra egyenletesen konvergens egy fv. sorozat $\iff$ $\pm 1 \in A'$ 

**Általánosan**: a $A'$-nek ($A$ torlódási pontjainak halmazának) van olyan eleme, ahol $f$ nem folytonos $\iff$ *nem* egyenletesen konvergens a fv. sorozat $A$-n

## Állítás
Ha $\sum_{n=0} (f_{n})$ egyenletesen konverges egy $A \subseteq D_{0}$ $\implies$ $(f_{n})\to 0 \equiv f; (n\to \infty)$ egyenletesen konvergál 

**Azaz**: mutassuk meg, hogy az $f$ nem egyenletesen konvergál, ekkor $\sum_{n=0}(f_{n})$ sem egyenletesen konvergens