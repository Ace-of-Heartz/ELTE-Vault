Értem, így fogom írni a jelöléseket:

Legyen $X_1, X_2, \ldots, X_n$ i.i.d. $\text{Bernoulli}(p)$ eloszlású, vagyis minden $X_i$ valószínűsége $P(X_i = 1) = p$, ahol $0 \leq p \leq 1$. A relatív gyakoriság, mint a $p$ paraméter becslése, az alábbi módon definiált:

p^=1n∑i=1nXi.\hat{p} = \frac{1}{n} \sum_{i=1}^n X_i.

Meg kell mutatni, hogy $\hat{p}$ hatásos becslése $p$-nek. Ehhez két tulajdonságot kell ellenőriznünk:

1. **Torzítatlanság:** $\mathbb{E}[\hat{p}] = p$,
2. **Minimális variancia:** A becslés varianciája minimális az összes torzítatlan becslés között.

### 1. Torzítatlanság

Számoljuk ki $\hat{p}$ várható értékét:

E[p^]=E[1n∑i=1nXi]=1n∑i=1nE[Xi].\mathbb{E}[\hat{p}] = \mathbb{E}\left[\frac{1}{n} \sum_{i=1}^n X_i \right] = \frac{1}{n} \sum_{i=1}^n \mathbb{E}[X_i].

Mivel az $X_i$-k i.i.d.-k és $\mathbb{E}[X_i] = p$, ezért:

E[p^]=1n⋅n⋅p=p.\mathbb{E}[\hat{p}] = \frac{1}{n} \cdot n \cdot p = p.

Tehát $\hat{p}$ torzítatlan becslése $p$-nek.

---

### 2. Minimális variancia

Számoljuk ki $\hat{p}$ varianciáját:

Var(p^)=Var(1n∑i=1nXi)=1n2∑i=1nVar(Xi).\text{Var}(\hat{p}) = \text{Var}\left(\frac{1}{n} \sum_{i=1}^n X_i \right) = \frac{1}{n^2} \sum_{i=1}^n \text{Var}(X_i).

Mivel az $X_i$-k i.i.d.-k, $\text{Var}(X_i) = p(1-p)$, így:

Var(p^)=1n2⋅n⋅p(1−p)=p(1−p)n.\text{Var}(\hat{p}) = \frac{1}{n^2} \cdot n \cdot p(1-p) = \frac{p(1-p)}{n}.

Fisher-féle információelmélet szerint a Bernoulli-eloszlás esetén egy torzítatlan becslés minimális varianciája:

1n⋅I(p),\frac{1}{n \cdot I(p)},

ahol $I(p)$ a Fisher-információ, és Bernoulli-eloszlás esetén $I(p) = \frac{1}{p(1-p)}$. Így a minimális variancia:

1n⋅1p(1−p)=p(1−p)n.\frac{1}{n \cdot \frac{1}{p(1-p)}} = \frac{p(1-p)}{n}.

Mivel $\hat{p}$ varianciája pontosan megegyezik ezzel az értékkel, $\hat{p}$ eléri a Cramér–Rao határt, és így minimális varianciájú.

---

### Következtetés

A relatív gyakoriság, $\hat{p}$, hatásos becslése $p$-nek, mert torzítatlan és minimális varianciájú az összes torzítatlan becslés között.