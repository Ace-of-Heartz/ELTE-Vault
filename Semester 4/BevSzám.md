
# Témakörök:
## Eldöntési problémák:
Algoritmikusan értve!
### Reguláris G ($G_3$):
#### Eldönthető:
- Ugyazon nyelvet generálja G és G', ú.h. $L(G), L(G') \in L_3$
- G bővebb vagy egyenlő nyelvet generál-e mint G'
- adott T* szót generálja-e
- üres nyelvet generál-e
### Környezetfüggetlen G ($G_2$):
#### Eldönthető:
- végtelen nyelvet generál-e
- üres nyelvet generál-e
- adott T* szót generálja-e
#### Eldönthetetlen:
Ha $G_1\ és\ G_2 \in L_2$:
- $L(G_1) \cap L(G_2) =^? \varnothing$ 
- $L(G_1)=^?L(G_2)$ 
- $L(G_1) =^? \Gamma^*$ valamely $\Gamma$-ra
- $L(G_1) \subseteq^? L(G_2)$
### Hossz-nemcsökkentő G:
#### Eldönthető:
- adott T* szót generálja-e
### Turing gép (TG):
#### Eldönthető:

#### Eldönthetetlen:
- üres nyelvet ismeri-e fel; $P = \{\varnothing\}$
- véges nyelvet ismeri-e fel; $P = \{L | L\ véges\}$
- környezetfüggetlen nyelvet ismer-e fel; $P = \{L|L \in L_2\}$
- elfogadja-e az üres szót; $P = \{L \in RE|\epsilon \in L\}$
### Ítéletkalkulus:
#### Eldönthető:
- formula kielégíthető-e
- formula kielégíthetetlen-e
- formula tautológia-e
- 2 formula tautologikusan ekv.-e
- véges formulahalmaz tautologikus következménye-e egy formulának
### Elsőrendű logika:
#### Eldönthetetlen:
- formula kielégíthető-e
- formula kielégíthetetlen-e
- formula logikai következménye-e egy formulahalmaznak
## Zártságok:
### $L_i$-re (i = 0,1,2,3):
#### Zárt:
- reguláris műveletek:
	- unió
	- konkatenáció
	- iteratív zárt
### Reguláris L ($L_3$):
#### Zárt:
- komplementer
- metszet
- különbség
- szimmetria
### Környezetfüggetlen L ($L_2$):
#### Nem zárt:
- metszet
- szimmetrikus differencia
- különbség
- komplementer
### R:
#### Zárt:
- komplementer
### RE:
#### Nem zárt:
- komplementer
## Időkorlát átírás:
### k-szalagos:
- lineáris időigényű $f(n)$ időkorlátos k-szalagos TG => $O((f(n))^2)$ időkorlátos 1 szalagos TG 
### NTG:
- $f(n)$ időkorlátos NTG => $2^{O(f(n))}$ időkorlátos TG
## Normálformák:
### 3-típúsú G normálforma:
P-beli szabályok alakjai (2 db):
- $A \rightarrow \epsilon$; $A \in N$
- $A \rightarrow xB$; $A,B \in N, x \in T$ 
### Redukált grammatika ($L_2$):
- Csak aktív NT-t tartalmaz
- Csak elérhető NT-t tartalmaz
### Chomsky féle NF ($L_2$):
P-beli szabályok alakjai (3 db):
- $S \rightarrow \epsilon$, de KES nem sérülhet 
- $A \rightarrow x$; $A \in N, x \in T$
- $A \rightarrow BC$; $A,B,C \in N$
### Kuroda NF:
P-beli szabályok alakjai (5 db):
- $S \rightarrow \epsilon$, de A KES nem sérülhet 
- $A \rightarrow x$; $A \in N,x \in T$
- $A \rightarrow BC$; $A,B,C \in N$
- $AB \rightarrow AC$; $A,B,C \in N$
- $BA \rightarrow CA$; $A,B,C \in N$

### 0-típúsú NF:
P-beli szabályok alakjai (7 db):
- $S \rightarrow \epsilon$, de a KES nem sérülhet 
- $A \rightarrow x;\ A \in N, x \in T$ 
- $A \rightarrow B;\ A,B \in N$
- $A \rightarrow BC;\ A,B,C \in N$
- $AB \rightarrow B; A,B \in N$
- $AB \rightarrow AC;\ A,B,C \in N$
- $BA \rightarrow CA; A,B,C \in N$
## Algoritmusok:
### Aktív NT-k meghatározása ($L_2$):
- $A_1 := \{X | X => u \in P \ és\ u \in T^* ,X \in N\}$
- $A_{i+1} := A_i\cup\{x|x => u\in P\ és\ u \in (T \cup A_i)^*  \}$
### Elérhető NT-k meghatározása ($L_2$):
- $R_1 := \{S\}$
- $R_{i+1} := \{Y | X => uYv \in P \ és\ X \in R_i\ és\ u,v \in (N \cup T)^*\}$
### CYK:
- 1 <= i <= j <= n
- $H_{i,i} := \{A_i|B_i \to t_i\}$
- $H_{i,j}:=\{A_k|B_k \in \cup^{j-1}_{h=1}H_{i,h}H_{h+1,j} \}$ (i < j)
- $u \in L(G)$ <=> $S \in H_{1,n}$ 
## Nulladrendű logika:
### Ítéletváltozók (Var):
- előre rögzített,végtelen $Var = \{x_1,x_2,...\}$ halmaz
### Ítéletlogikai formulák (Form):
- A legszűkebb halmaz, melyre:
	- $x \in Var$ => $x \in Form$ 
	- $\phi \in Form$ => $\neg \phi \in Form$ 
	- $\alpha,\beta \in Form$ => $\alpha \circ \beta \in Form$ ahol $\circ \in \{\land,\implies,\lor\}$
### Igazságérték:
- $I: Var -> \{i,h\}$
### Ítélettábla:
- $2^n \times (n + 1)$
- első n db oszlop: ítéletváltozók
- n+1. oszlop: formula
- $2^n$ sor: az összes lehetséges interpretáció
Fontosabb fogalmak:
- kielégít
- kielégíthető formula
- kielégíthetetlen formula
- tautológia
- tautologikus következmény
- tautologikusan ekvivalens
## Elsőrendű logika: 
Szimbólum ábécék:
- Pred - predikátum szimb. ábécé
- Ind  - individuumváltozók megszámlálhatóan véges halmaza
- Func - függvény szimb. ábécé
- Cnst - konstans szimb. ábécé
### Term:
Azon legszűkebb halmaz, amelyre: 
- ha $x \in Ind$ => $x \in Term$
- ha $c \in Cnst => c \in Term$
- ha $f \in Func$ és $t_1,t_2,...t_{ar(f)} \in Term$ => $f(t_1,t_2,...,t_{ar(f)}) \in Term$
### Form:
Azon legszűkebb halmaz, amelyre: 
- ha $p \in Pred$ és $t_1,t_2,...,t_{ar(p)} \in Term$ => $p(t_1,t_2,...,t_{ar(p)}) \in Form$ 
- ha $\phi \in Form$ => $\neg \phi \in Form$ 
- ha $\phi,\psi \in Form$ => $\phi \circ \psi \in Form; \circ \in \{\land,\lor,\implies\}$ 
- ha $\phi \in Form$ => $\forall x \phi \in Form$ és $\exists x \phi \in Form$
### Szimbólum interpretáció:
$<U,I^{Func},I^{Ind},I^{Cnst}>$ rendezett négyes:
### Változóleképzés:
I interpretáció és $K$ változóleképzés esetén: 
- ha $x \in Ind$ => $|x|^{I,K} = K(x)$
- ha $c \in Cnst$ => $|c|^{I,K} = c^I$ 
- ha $f(t_1,t_2,...,t_{ar(f)}) = i$ <=> 

Fontosabb fogalmak:
- formula kielégíthető
- formula kielégíthetetlen
- logikailag érvényes/igaz
- logikailag ekv.
- formula halmaz kielégíthető
- formula halmaz logikai következménye
## Tárigény:
- det. TG:
	- tárigény
	- tárkorlátos
- NTG:
	- tárigény
	- tárkorlátos
## Spec. Halmazok:
- *RE*:
	- $\{L|\exists M\ TG: L(M)=L\}$
	- nem zárt a komplementerre
- *R*:
	- $\{L|\exists M\ TG:L(M) = L\ és\ eldönthető\}$
	-  zárt a komplementerre
- $L_h$ 
	- $\{<M,w>|M\ megáll\ w\ bemeneten\}$
	- $\in RE$
	- $\notin R$
- $L_u$
	- $\{<M,w>|w\in L(M)\}$
	- univerzális nyelv
	- $\notin R$
	- $\subseteq L_h$ 
- $L_P$ 
	- $\{<M>|L(M)\in P\}$
	- Rice tétel
- $L_{PMP}$
	- $\{<D>|D-nek\ létezik\ megoldása\}$
	- D = dominóhalmaza
	- $\in RE$
	- $\notin R$
- $L_{ECF}$
	- $\{<G>|G\ egyértelmű\ CF\ grammatika\}$
	- $\notin R$
- $ValidityPred$
	- $\{<\phi>|\phi\ logikailag\ igaz\}$
	- $\notin R$
- **$L_1$** 
	- $\subset R$
- $Time(f(n))$
	- $\{L |L\ eldönthető\ O(f(n))\ időkorlátos\ del.\ TG-vel\}$
- $NTime(f(n))$
	- $\{L|L\ eldönthető\ O(f(n))\ időkorltáos\ NTG-vel\}$
- $P$
	- $= \cup_{k>=1}Time(n^k)$ 
- NP
	- $= \cup_{k>=1}NTime(n^k)$
	- $P \subseteq NP$   
- $SAT$
	- $\{<\phi>|\phi\ kielégíthető\ nulladrendű\ KNF\}$
	- NP-teljes
- $kSAT$
	- ${<\phi>| \phi\ kielégíthető\ nulladrendű\ kKNF}$
	- 3SAT NP-teljes
	- 2SAT $\in$ P 
- $HornSAT$
	- $\{<\phi>|\phi\ kielégítő\ Horn\ formula \}$
	- $\in P$ 
- $kSzínezés$
	- $\{<G>|G\ k-színezhető\}$
	- 3Színezés NP-teljes
	- 2Színezés $\in$ P
- $Klikk$
	- $\{<G,k>|G-nek\ van\ k-méretű\ klikkje\}$
	- NP-teljes
- $LefogóPonthalmaz$
	- $\{<G,k>|G-nek\ létezik\ k-méretű\ lefogó\ ponthalmaza\}$
	- NP-teljes
- $FüggetlenPonthalmaz$
	- NP-teljes
- $HipergráfLefogóPonthalmaz$
	- $\{<S,k>|S\ hipergráfnak\ létezik\ k-elemű\ S-et\ lefogó\ ponthalmaza\}$
	- NP-teljes
- $HÚ$
	- $\{<G,s,t>|G\ irányított\ gráfnak\ létezik\ s-ből\ t-be\ H-út\}$
	- NP-teljes
- $IHÚ$
	- $\{<G,s,t>|G\ irányítatlan\ gráfnak\ létezik\ s-ből\ t-be\ H-út\}$
	- NP-teljes
- $IHK$
	- $\{<G>|G\ irányítatlan\ gráfnak\ létezik\ H-köre\}$
	- NP-teljes
- $Elér$
	- $\{<G,s,t>|G\ irányítatlan\ gráfban\ \exists\ s-ből\ t-be\ út\}$
	- $\in Space(log^2(n))$
	- $\in Time(n^2)$ 
- $Space(f(n))$
	- $\{L|L-t\ felismeri\ egy\ O(f(n))\ tárkorlátos\ OTG\}$
- $NSpace(f(n))$:
	- $\{L|L-t\ felismeri\ egy\ O(f(n))\ tárkorlátos\ NOTG\}$ 
- $L$
	- Space(log(n))
- NL
	- NSpace(log(n))

