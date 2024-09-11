# Theorems / Tételek
## Lineáris algebrai alapok:
- A: 
	- Def.:
		- Jordan alak
		- S.É.
		- Kar.pol.
	- Tételek:
		- 4-es S.É-ről:
			- A mtx. S.É-je <=> A kar.pol.-jának gyöke az S.É.
			- Minden S.É-hez tartozik S.V.
			- minden  S.V. v != 0 esetén c != 0-nál is v * c is S.V lesz
			- különb. S.É-hez tartozó S.V-k lineárisan függetlenek
		- 4-es S.É. és hasonlósági mtx-ok:
			- geometria mult. <= algebrai mult.
			- A és B hasonló => tr(A) == tr(B) ÉS det(A) = det(B)
			- S.V. és S.É. alakulása hasonló mtx-eknél
			- A diagonalizálható <=> alg. és geom. mult-ai egyenlőek minden S.É.-re
- B: 
	- Tételek
		- Schur tétel:
			- 4 lépés:
				- 1 és 4. lépés -> megjegyzések
				- 2.: ált. lépés
				- 3.: vég lépés
			- telj. ind.
			- Householder-transz.
		- Norm. mtx diagonalizálása:
			- <=>
			- <= : 
				- U D U* == U* D U
				- diag. mtx. és adjungáltja szorzása
			- => : 
				- 2. Lépés:
				1. ha A normális => U* A U is az
				2. példa mátrix (3x3)->as R* R = R R* kell hogy legyen -> R csakis diag lehet
## Sajátértékek becslése:
- A:
	- Def.:
		- Normával becslés
			- Előző félév
			- Mátrixnorma >= mint S.É.-k
	- Tételek:
		- Gersgorin tétel
			- adott S.É-re és hozzátartozó S.V-re
			- 1 oszlopra megnézzük
			- végtelen norma
		- Gersgorin ált. tétel (javítása diag. hasonl. trszf-val)
			- egy b_ij-re = ?
		- Ált. Gersgorin tétel:
			- diszjunkt körcsoportok
		- 5. Következmény:
			- Oszlopokkal is lehet Gersgorin kör
			- Oszlopok szerint és sorok szerinti G. körök uniójának metszete
- B: 
	- Tételek:
		- Lagrange int. öröklött hiba:
			- Lebesgue állandó
			- f és f közelítője
		- Inver. intpol:
			- gyökkeresés
			- szelő módszer, Newton módszer
## Sajátérték probléma érzékenysége:
- A:
	- Def.:
		- Kérdések:
			- A-t ismerjük, A + $\Delta$A s.é.-je és s.v-je ismeretében a hiba nagysága
			- A-t ismerjük és egy közelítő s.é., s.v.-ját -> ezek jósága mennyi (reziduális hiba)9
		- Példák:
			- Vandermonde mátrix
			- Hilber mátrix
		- Különbség: 
			- LER-nél: A kondíciószáma
			- itt: X kondíciószáma (diagonalizáló mátrixé)
	- Tételek:
		- Becslés reziudális hibával:
			- trivi. eset ha pontos a becslés
			- reziduális hiba felírása diagolizálást felhasználva
			- normákra vonatkozó háromszög egyenlőtlenség
			- vektor és mátrix normák illeszkedése
- B: 
	- Tételek:
		- Bauer-Fike-tétel:
			- trivi. eset ha pontos a becslés
			1. A + $\Delta$A-ra alkalmazzuk a hasonlósági trafót
			2. legyen (D - $\mu$*I) * (I + B) a végén
			3. determinánsokra váltsunk
			4. vegyük észre, hogy 0-val egyenlő
			5. spektrálsugár és norma közti egyenlőtlenség felhaszn.
		- Következmény:
			- S.É-k folyamatosan függenek a mátrix elemeinek változásától
			- hasonló elmondható S.V-kre is, ha a hozzájuk tartozó S.É. multiplicitása 1
## Kar. pol. meghatározására alkalmas módszerek:
- A: 
	- Determinánsal való meghatározás
	- Polinomokkal való meghatározás (interpolációsan)
	- Fagyejev - trace módszer
- B: 
	- Frobenius kar. pol.:
		- determinánsokkal (det(I*$\lambda$ - $F_n$))
		- Horner algoritmusból adódik ezután
	- Tridiagok. kar.pol-ja:
		- determinánsokkal (tetszőleges k-ra)
		- p($\lambda$)-ra
	- Tridiag mátrix előállítsa, ha szimmetrikus A:
		- n-2 Householder transzformáció
		- a_1 n-1 hosszú vektorral ^ 
		- transzponált a_1-re * H_1
		- szorzás H1 * A * H1
		- folytatás a HH trafóknak
		- k. lépésben micsoda
		- Q = H1 * H2 * ...
## Rayleigh hányados és hatványmódszer:
- A:
- 
	- Rayleigh hányados:
		- x != 0
	- 2 tétel Rayleigh hányadosról:
		- 1.: A normális lesz ekkor -> diagonalizálható
			- ezzel  Rayleigh
			- a x = v_min
			- a x = v_max 
		- 2.: 
			- reziduális hiba
			- skalárrá alakítás
			- másodfokú polinom teljes négyzetté alakítás után
- B: 
	- hatvány módszer:
		- A normális -> $\exists$ ortogonált bázisa -> ekkor ennek oszlop vektorjai az A saját vektorai  
		- 3 állítás - 3 bizonyítási szakasz
	- inverz iterációs módszer: 
		- hatvány módszer bizonyításából adódik
	- összehasonlítás:
	- shiftelés alkalmazása:
		- tétel - biz 
			- s.v-k azonosak maradnak a sajátértékekre
		- konvergencia gyorsítás
		- szélsőérték meghatározás
	- rangszám csökkentés:
		- gyakorlatról
		- + tétel
		- A szimm -> $\exists$ saját ortonormált bázisa
## Jacobi módszer
- A:
	- Jacobi módszer változatai:
		- klasszikus:
			- max elem
			- i > j; p > q;
		- ciklikus:
			- i > j
			- |$a_{ij}$| != 0
		- küszöb:
			- i > j;
			- |$a_{ij}$| > $\xi$ (= a küszöb)
	- képletek levezetése:
		- $G = Q^T * A$
			- $g_{il} = c * a_{il} - s * a_{jl}$ 
			- $g_{jl} = s * a_{il} - c * a_{jl}$
		- $B = G * Q$
			- $b_{li} = c * g_{li} - s * g_{lj}$
			- $b_{lj} = s * g_{li} + c * g_{lj}$
		- $l = 1...n$
		- $u = 2a_{ij}$
		- $v = a_{jj} - a_{ii}$
		- $w = \sqrt{u^2 + v^2}$ 
	- 3 db lemma, utolsó biz.:
		- ort. trafó
		- i.oszlopvektor norm és sorvektor norma
		- kihasználjuk, hogy csak az i. és j. sor/oszlop változik
- B:
	- Klasszikus Jacobi módszer konvergenciája:
		- 3. szakasz:
		1. megmutatjuk, hogy k és k-t lépésbeli A főátlón kívüli elemeinek összege = a absz. legnagyobb index 2x-ével (i,j)
		2. Felső becslés a $N(A^{(k)})$-ra; rekurzió kifejtése $A^k$-ra
		3. Gersgorin tétel a $R_i$-re és $a_{ii}$-re 
	- QR algo.:
		- 3. állítás
		- telj. ind.
	- LU algo.:
		- 3. állítás
		- telj. ind.
## Polinom interpoláció:
- A:
	- 
- B: 
	- Newton alak levezetése:
		- Lagrange alakból
		- $L_0(x)$ konstans
		- $L_k(x) - L_{k-1}(x)$
		- osztott differencia alt. kifejtése
		- Lagr. alappol. alt. alakja
		- azonos nevező
	- Interpoláció hibabecslése:
		- Rolle tétel
		- esetszétválasztás:
			- $x = x_i$ valamilyen i-re
			- $x \neq x_i$ tetszőleges i-re
		- $g_x(z) = f(z) - p_n(z) - \omega_n(z)/\omega_n(x)  * (f(x) - p_n(x))$
		- gyökök számlása -> n-2, majd n-1, majd .... 1 -> ekkor ezzel a gyökkel felírjuk a g-t, majd átrendezünk
## Csebisev polinom:
- A: 
	- Rekurzió: $\alpha = arccos(x)\ és\  x = cos(\alpha)$: cos additivitása
	- Főegyüttható és 1 főegyüttható Csebisev
	- Gyökök:
		- Szimm. origóra
		- n-db
		- ha n páros -> Csebisev pol. páros, ha páratlan akkor páratlan
	- Csebisev polinomok egy ortogonális polinomrendszert alkotnak
		- $1/{1-x^2}$ súlyfüggvénnyel
- B: 
	- extreminális tulajdonság:
		- INDIREKT
		- Csebisev polinomok gyökeinek száma
		- különbség polinom
		- mivel a Q és T főegyütthatója 1 -> ezért 1-el kisebb fokszámú lesz R, de ebből az adódik, hogy R a konstans0 polinom
	- interpoláció hibája \[-1,1]
		- n +1 folyt. diff.
		- Csebisev polinom (1 főegyütthatós)
		- előző tételből -> $||\omega_n||_\infty$ akkor minimális, ha ez megegyezik a fenti polinom végtelen normájával
		- ez akkor teljesül, ha a gyökei az alappontok
	- interpoláció hibája \[a,b]-n
		- mint előző
		- transzformációs függvény:
			- $(b-a)/2 * x + (a + b)/2$
	- konvergencia
		- omega felülbecslése
		- Lagrange hibaformula
		- hatvány/faktoriális
## Spline I.:
- A:
	- Spline fogalma:
		- 3 db tulajd.:
			- int. pol. alapfeladata
			- l-1 folyt. diff \[a,b]
			- $\in\ P_l$
	- 1. fokú:
		- 2 együttható
		- lineáris
		- számolgatás
		- nincs peremfeltétel
	- 2. fokú:
		- 3 együttható
		- számolgatás
		- van peremfeltétel
		- algo
			- m_1 = peremfeltétel
			- a_0
			- a_1
			- a_2
			- m_k
- B: 
	- 3. fokú:
		- Peremfeltételek:
			- Hermite:
				- $f'(b) = S'(b)$
				- $f'(a) = S'(a)$
			- Természetes:
				- $S''(a) = 0$
				- $S''(b) = 0$
			- Periodikus:
				- feltétel: 
					- \[a,b] a periódus osztója
					- f(b) = f(a)
				- $S'(a) = S'(b)$
				- $S''(a) = S''(b)$
			- Not a knot:
				- $S''' \in C\{x_1,x_{n-1}\}$
		- 4 egyenlet:
			- 1. bal oldal
			- 2. jobb oldal
			- 3. jobb oldal 1. deriv
			- 4. jobb oldal 2. deriv
		1. 4-ből $a_3$
		2. 2-ból $a_1$
		3. 3-ba behelyettesítés, majd átrendezés
			1. egyik oldalt csak a_2-k másik oldalt csak oszt. diff-ek
		- $h_k/(h_k + h_{k+1})$
	- hibabecslések:
		- lineáris, l := 1
			- 1/8
			- h = max(h_k)
		- Hermite, l := 3
			- 5/384
			- 1/24
			- 3/8
		- klasszikus peremfeltétel:
			- l := 3
			- 2-sze folytosan diff.
			- Hermite, természetes, ciklikus
			- Biz:
				- d(x) = f(x) - S(x)
				1. $S^{ii}(a)d^i(a) = S^{ii}(b) * d^i(b)$
				2. becslés felírása
				3. $<d^{ii},S^{ii}>$ = 0 megmutatása
					1. parciális int.
					2. parciális
## Spline-ok II.
## Mátrix szinguláris felbontása:
- A:
	- Szinguláris értékek:
		- $\sigma_i = \sqrt{\lambda_i * (A^* * A)}$ 
	- Szinguláris felbontás:
		1. $A^* * A$ önadjungált és pozitív szemidefinit
			- $<A^*Ax,x>$ -> $<Ax,Ax>$
		2. nem-null és null s.é.; r = rang(A); $\Sigma$ def.
		3. $A^*A$ önadjungált -> $\exists! V$, hogy $A^*A = VD^2V^*$ 
			- ekkor V a s.v-it tartlamazza oszloponként
		4. ha n = m és rang(A) = n:
			- poz. def. A
			- $V^*A^*AV = D^2$ => $D^{-1}V^*A^*AVD^{-1} = I$
			- $U= AVD^{-1}$
		5. $V = [V_1,V_2]$ 
		6. $V_1$-re külön vevés -> mint 4. csak $\Sigma$-ra
			- $U_1 = AV\Sigma^{-1}$
		7. $U_2\ elkészítése\ R^m-beli\ ortonormált\ vektorokkal\ (n-r\ db)$
			- $U = [U_1,U_2]$
		8. Ellenőrzés
			- $AV_1 = U_1\Sigma$
			- $U_2^*(AV_1) = U_2^*(U_1\Sigma) = 0$ (ortogonalitás)
			- $A*V_2 = 0*V_2 = 0$
- B: 
## Legkisebb négyzetek probléma:
- A: 
	- Def.:
		- $\Sigma^N_{i = 1}(p_n(x_i) - y_i)^2$ minimális
	- Approximációs tulajd. megoldás:
		- Írjuk fel polinom együtthatóit, majd LER-ben is
		- => klasszikusan nem oldaható meg
		- => általánosan igen, mert teljes rangú
		- túlhatározott eset:
		- $a^+$ felírása
		- szimmetrikus LER felírása
		- erre alkalmazzuk az approximációs tételt
- B: 
## Hilbert térbeli approximáció:
- A:
	- Hilbert tér
	- Hilbert térbeli approximáció 
		- H' altérből
	- + átfogalmazás
		- 2 merőleges elemből előállíthatók bármely eleme H-nak
	- Hilbert térbeli legjobban közelítő elem távolsága:
		- $||f - f'|| = d^2 = ||f||^2 -b^T*c$ 
			- ONR:
				- távolság: $||f||^2 - \Sigma^n_{i=1}(<f',g_i>)^2$ 
				- legjobban közelítő elem: $c_i = \Sigma^n_{i = 1}\ g_i * <f',g_i>$ 
			- OGR:
				- legjobban közelítő elem: $c_i = \Sigma^n_{i = 1}\ g_i * <f',g_i>/<g_i,g_i>$ 