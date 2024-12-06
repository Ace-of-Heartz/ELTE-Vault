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

## Tétel
Egy $A \subset (-1,1], A \neq \emptyset$ halmazra egyenletesen konvergens egy fv. sorozat $\iff$ $\pm 1 \in A'$ 

**Általánosan**: a fv. sorozat torlódási pontjai nem elemei A'-nek $\iff$ egyenletesen konvergens a fv. sorozat $A$-n