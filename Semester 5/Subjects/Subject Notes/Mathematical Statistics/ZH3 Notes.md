# Függetlenség vizsgálat
**Diszkrét eloszlasú, vagy ilyenné tehető**: *Khí-négyzet próba*
# Illeszkedés vizsgálat
**Diszkrét eloszlású**:  *Khí-négyzet próba*
**Folytonos eloszlású**: 
- Diszkretizálás révén *Khí-négyzet próba*
- Kolmogorov-Szmirnov próba
- Cramér-von Mises próba
- Anderson-Darling próba
- Shapiro-Wilk próba (normalitás vizsgálatához)
# Homogenitás vizsgálat
*Khí-négyzet próba* 

# R Summary()
- `Pr(>|t|)` oszlop: p értékek 
- `Std. Error` oszlop: becslések szórásnégyzete
- `Residual Standard Error`: hiba/reziduum szórásnégyzete
- `Estimate`: a változó egységnyi növekedése átlagosan ennyivel csökkenti a függő változót (y)
- Koefficiensek szignifikánsan különböznek 0-től $\iff$ Elvetjük a $H_{0}$-t

# 1. Feladat
1. $T(x) = \frac{L_{1}(x)}{L_{0}(x)}$
2. Nézzük meg, hogy $x$-re nézve mon. csökkenő vagy növekvő-e a fv.
3. Ha **csökkenő** => alsó kritikus érték. Ha **növekvő** => felső kritikus érték
4. $T_{krit} = F^{-1}_{[eloszlas]}(\alpha)$
5. Ha **diszkrét** => még véletlenítést kell alakalmaznunk. 

