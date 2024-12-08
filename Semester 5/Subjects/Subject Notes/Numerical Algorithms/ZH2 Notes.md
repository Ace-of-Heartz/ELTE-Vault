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


# Runge-Kutta módszer konzisztencia (vázlat)