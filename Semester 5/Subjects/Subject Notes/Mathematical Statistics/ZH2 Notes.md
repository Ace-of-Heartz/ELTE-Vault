Minták szórása: $\frac{\sigma}{\sqrt{ n }}$ 
**Elsőfajú hiba** ~ ennek valószínűsége megegyezik a harang görbe kritikus tartományba eső részének nagyságával
^ Ezen valószínűség az ú.n. *szignifikanciaszint*. Jelölése: $\alpha$ í
- Meghatározható!

**Másodfajú hiba** ~ Ennek valószínűsége az új eloszlás alapján leírt valószínűsége annak, hogy a *nem* kritikus tartományban vagyunk (azaz ennek a tartománynak az új eloszlás szerinti nagysága)
^ Jelölése: $\beta$ 
- Nem meghatározható igazán

**Fontos** (*Mateking*): 
- Kétoldali próbánál mindig a felső %-hoz való **kritikus értéket** keressük -> ennek (-)-szerese lesz az alsó **kritikus érték**

**Egyéb fontos (konziról)**:
- "Különbség" ~ Kétoldali becslés
- "Kisebb/nagyobb-e" ~ egyoldali becslés
- 1 - pt(...) akkor kell, ha nem pl. a felső határtól jobbra levő részt vizsgáljuk (lásd órai példák + füzet)
# Próbák:

| Egymintás         |         |
| ----------------- | ------- |
| Ismert szórás     | u-próba |
| Ismeretlen szórás | t-próba |
 
# Konfidencia intervallum
$P\left( \bar{\xi} - u_{1-\frac{\alpha}{2}} * \frac{\sigma}{\sqrt{ n }} <m< \bar{\xi} + u_{1-\frac{\alpha}{2}} * \frac{\sigma}{\sqrt{ n }} \right) = 1-\alpha$
**R-ben**: 
- Ismert szórás esetén
```
Also_hatar<-mean(minta)-sigma/sqrt(n)*qnorm(1-alpha/2)
Felso_hatar<-mean(minta)+sigma/sqrt(n)*qnorm(1-alpha/2)
```
- Ismeretlen szórás esetén:
```
Also_hatar<-mean(minta)-sd(minta)/sqrt(n)*qt(1-alpha/2, n-1)
Felso_hatar<-mean(minta)+sd(minta)/sqrt(n)*qt(1-alpha/2, n-1)
```

Mert hogy $\dots$
$T_{1}(x) = \bar{x} - \theta^{-1}\left( 1-\frac{\alpha}{2} \right) *\sqrt{ \frac{\sigma^2}{n} }$
$T_{2}(x)=\bar{x} + \theta^{-1}\left( 1-\frac{\alpha}{2} \right)*\sqrt{ \frac{\sigma^2}{n} }$

# Relatív gyakoriság (vagy más milyen param. becslése)
1. **Torzítatlanság vizsgálata**: $\mathbb{E}(\hat{p}) = p$
2. **Minimális variancia**:
	1. $\hat{p}$ varianciájának kiszámítása $\mathbb{D}^2(\dots)$ 
	2. Fisher-féle információelmélet szerint a Bernoulli-eloszlás esetén egy torzítatlan becslés minimális varianciája. ($\dots= \frac{1}{n *I(p)}$ teljesül-e?)

# Fischer információ
$I_{n}(\theta) = \mathbb{E}\left( \left[ \frac{\partial l}{\partial \theta} \right]^2 \right) = -\mathbb{E}\left( \frac{\partial^2 l}{\partial \theta^2} \right)$ <- utolsó csak technikai feltételek mellett teljesül
**Fontos**: $I_{n}(\theta)$ csak pozitív lehet