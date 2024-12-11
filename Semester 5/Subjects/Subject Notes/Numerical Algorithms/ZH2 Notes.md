# K.É.P. létezése, egyértelműsége



# Numerikus módszer

# Konvergencia, p-adrendű konvergencia

# Lokális hiba 

# p-adrendű Konzisztencia

# Globális hiba 

# Stabilitás 
# Euler-módszer konzisztencia
1. Lokális hiba felírása
2. Taylor-soros kifejtés felírása
3. Végtelen norma alkalmazása konstans szorzóval való felsőbecsléshez

# Euler-módszer stabilitása
1. Módszer és lokális hiba képletének felírása és kivonása
2. Globális hibák megjelenése
3. Lipschitz-feltétel -> Abszolút értékben felírása
4. Felsőbecslések rekurzivan egészen $e_{0}$-ig
5. Ekkor $(1+h*L)^i$ felülbecsülhető $e^{i*h*L} = e^{x_{i}L}$-el, ami így $e^{x_{i}L} \leq e^{L}$, mert $x_{i} \leq 1$ 
6. Ekkor $e^L$ minden tagból kiemelhető => Meg van a becslés

# Javított Euler-módszer
1. Lokális hiba felírása
2. $k_{2}(x,y)$-t fejtsük ki sorba (szétbomlik a fv.)
3. Alkalmazzuk a fenti sorbafejtést és a $y(x_{i+1})$-re a Taylor-sorba fejtést
4. Írjuk fel a $g_{i}$-t már csak az $O(h^3)$-al 
5. Így $p=2$ 


# Runge-Kutta módszer stabilitása
**Segéd fv.:** $\phi(x,y) = \sum^s_{i=1}c_{i}*k_{i}(x,y)$
1. Lokális hiba és módszer képletének felírása
2. Globális hiba felírása ezek különbségéből
3. Ha $\phi \in Lip(2)$, akkor **Euler-módszer** stabilitásával analóg
4. $\phi$ kifejtése
5. Ha $\forall i: k_{i}\in Lip(2)$, akkor $\phi\in Lip(2)$ is teljesül
6. Teljes indukció $k_{i}$-re $i$ szerint

# Runge-Kutta módszer konzisztencia (vázlat)

# Tapasztalati lokális hiba és $(p-1)$-ed rendű módszer hibaközelítésének összefüggése
1. Írjuk fel az alábbit:
$g_{j-1}^{(p-1)} =y_{j-1}(x_{j}) -y_{j}^{(p-1)} = C^{(p-1)}*h^p + O(h^{p+1})$
$g_{j-1}^{(p)} =y_{j-1}(x_{j})-y_{j}^{(p)}= C^{(p)} *h^{p+1} + O(h^{p+2})$ 
- Ezeket *konvergencia* és *konzisztencia* kapcsolata miatt tudjuk így leírni, illetve a *konzisztencia* definíciója miatt

2. Írjuk fel a lokális hibák különbségét
$\tilde{g}_{j-1} = y_{j}^{(p)} -y_{j}^{(p-1)}=C^{(p-1)}*h^{p} + O(h^{p+1})$

# Adaptív R-K Stratégia:
1. $h < h_{min}$
2. $h_{min} \leq h < h_{j}$
3. $h_{j}\leq h <2h_{j}$
4. $2h_{j} \leq h$ 