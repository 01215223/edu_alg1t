# Algebra – Zestaw 2 – rozwiązania

> **Założenia i konwencje.** Jednostka urojona: $j$, gdzie $j^2=-1$. Argument główny podajemy w przedziale $(-\pi,\pi]$; przy wyznaczaniu pierwiastków kąty można podawać w $[0,2\pi)$. Zapis trygonometryczny ma postać $r(\cos\varphi+j\sin\varphi)$. Wypisujemy wszystkie pierwiastki. Wyniki są dokładne, z wyjątkiem przybliżeń argumentów wymaganych w zadaniu 1.5.

---

## Zadanie 1

### 1.1

Moduły i argumenty podstawy licznika oraz podstawy mianownika są równe:

$$
-2+2\sqrt{3}j=4\left(\cos\frac{2\pi}{3}+j\sin\frac{2\pi}{3}\right),\qquad
2-2j=2\sqrt{2}\left(\cos\left(-\frac{\pi}{4}\right)+j\sin\left(-\frac{\pi}{4}\right)\right).
$$

Ze wzoru Moivre'a:

$$
\frac{(-2+2\sqrt{3}j)^{21}}{(2-2j)^{26}}
=\frac{4^{21}}{(2\sqrt{2})^{26}}
\left(\cos\left(21\cdot\frac{2\pi}{3}+\frac{26\pi}{4}\right)+j\sin\left(21\cdot\frac{2\pi}{3}+\frac{26\pi}{4}\right)\right).
$$

Moduł ilorazu oraz jego argument upraszczają się następująco:

$$
\frac{4^{21}}{(2\sqrt{2})^{26}}=\frac{2^{42}}{2^{39}}=8,\qquad
21\cdot\frac{2\pi}{3}+\frac{26\pi}{4}=\frac{41\pi}{2}\equiv\frac{\pi}{2}\pmod{2\pi}.
$$

Zatem

$$
\boxed{\frac{(-2+2\sqrt{3}j)^{21}}{(2-2j)^{26}}=8\left(\cos\frac{\pi}{2}+j\sin\frac{\pi}{2}\right)=8j}
$$

### 1.2

Najpierw upraszczamy podstawę potęgi, mnożąc licznik i mianownik przez sprzężenie mianownika:

$$
\frac{2j-4}{j+3}=\frac{(-4+2j)(3-j)}{(3+j)(3-j)}=\frac{-10+10j}{10}=-1+j.
$$

Liczba $-1+j$ ma moduł $\sqrt{2}$ i argument $3\pi/4$. Stąd

$$
(-1+j)^{101}=2^{101/2}\left(\cos\frac{303\pi}{4}+j\sin\frac{303\pi}{4}\right)
=2^{50}\sqrt{2}\left(\cos\frac{7\pi}{4}+j\sin\frac{7\pi}{4}\right).
$$

Ponieważ $\cos(7\pi/4)=\sqrt{2}/2$ i $\sin(7\pi/4)=-\sqrt{2}/2$, otrzymujemy

$$
\boxed{\left(\frac{2j-4}{j+3}\right)^{101}=2^{50}(1-j)}
$$

### 1.3

Niech $q=7-24j$. Wtedy

$$
|q|=\sqrt{7^2+(-24)^2}=25,\qquad \arg(q)=-\arctan\frac{24}{7}.
$$

Ze wzoru na pierwiastki kwadratowe:

$$
u_k=5\left(\cos\frac{-\arctan(24/7)+2\pi k}{2}+j\sin\frac{-\arctan(24/7)+2\pi k}{2}\right),\qquad k\in\{0,1\}.
$$

Aby zapisać pierwiastki algebraicznie, niech $u=a+bj$ będzie jednym z nich. Porównanie części rzeczywistych i urojonych w równaniu $u^2=7-24j$ daje

$$
a^2-b^2=7,\qquad 2ab=-24,\qquad a^2+b^2=25.
$$

Z dwóch równań dotyczących kwadratów wynika $a^2=16$ i $b^2=9$; warunek $2ab=-24$ ustala przeciwne znaki $a$ i $b$. Zatem

$$
\boxed{u=\pm(4-3j)}
$$

Sprawdzenie: $(4-3j)^2=(-4+3j)^2=7-24j$. Są to dwa punkty o współrzędnych $(4,-3)$ i $(-4,3)$; oba pierwiastki mają moduł $5$.

### 1.4

Niech $w=3j-\sqrt{3}=-\sqrt{3}+3j$. Wtedy

$$
|w|=2\sqrt{3},\qquad \arg(w)=\frac{2\pi}{3}.
$$

Wszystkie cztery pierwiastki mają moduł $\rho=\sqrt[4]{2\sqrt{3}}$ i argumenty $\frac{\pi}{6}+\frac{k\pi}{2}$ dla $k=0,1,2,3$.

| $k$ | Argument pierwiastka | Pierwiastek w postaci algebraicznej |
| :---: | :---: | :--- |
| $0$ | $\frac{\pi}{6}$ | $\rho\left(\frac{\sqrt{3}}{2}+\frac{1}{2}j\right)$ |
| $1$ | $\frac{2\pi}{3}$ | $\rho\left(-\frac{1}{2}+\frac{\sqrt{3}}{2}j\right)$ |
| $2$ | $\frac{7\pi}{6}$ | $\rho\left(-\frac{\sqrt{3}}{2}-\frac{1}{2}j\right)$ |
| $3$ | $\frac{5\pi}{3}$ | $\rho\left(\frac{1}{2}-\frac{\sqrt{3}}{2}j\right)$ |

Zatem

$$
\boxed{w_k=\rho\left(\cos\left(\frac{\pi}{6}+\frac{k\pi}{2}\right)+j\sin\left(\frac{\pi}{6}+\frac{k\pi}{2}\right)\right),\qquad k=0,1,2,3}
$$

Pierwiastki leżą na okręgu o środku $0$ i promieniu $\rho$. Podniesienie ogólnego pierwiastka do czwartej potęgi odtwarza liczbę podpierwiastkową:

$$
w_k^4=2\sqrt{3}\left(\cos\left(\frac{2\pi}{3}+2\pi k\right)+j\sin\left(\frac{2\pi}{3}+2\pi k\right)\right)=-\sqrt{3}+3j.
$$

### 1.5

Niech $w=-4+3j$. Jego moduł wynosi $5$, a argument leży w II ćwiartce:

$$
|w|=5,\qquad \theta=\arg(w)=\pi-\arctan\frac{3}{4}\approx 2{,}4981\ \text{rad}.
$$

Przybliżenie argumentu obliczono kalkulatorem i podano do czterech miejsc po przecinku. Pierwiastki sześcienne mają moduł $\sqrt[3]{5}$ oraz argumenty $\alpha_k=(\theta+2\pi k)/3$.

| $k$ | Argument dokładny $\alpha_k$ | Przybliżenie $\alpha_k$ w radianach |
| :---: | :---: | :---: |
| $0$ | $\frac{\pi-\arctan(3/4)}{3}$ | $0{,}8327$ |
| $1$ | $\frac{\pi-\arctan(3/4)+2\pi}{3}$ | $2{,}9271$ |
| $2$ | $\frac{\pi-\arctan(3/4)+4\pi}{3}$ | $5{,}0215$ |

Wszystkie rozwiązania to

$$
\boxed{w_k=\sqrt[3]{5}\left(\cos\alpha_k+j\sin\alpha_k\right),\qquad k=0,1,2}
$$

Sprawdzenie przez podniesienie do trzeciej potęgi:

$$
w_k^3=5\left(\cos(\theta+2\pi k)+j\sin(\theta+2\pi k)\right)=5(\cos\theta+j\sin\theta)=-4+3j.
$$

Pierwiastki są trzema wierzchołkami trójkąta równobocznego na okręgu o środku $0$ i promieniu $\sqrt[3]{5}$.

### 1.6

Najpierw obliczamy iloczyn pod pierwiastkiem:

$$
(1-j\sqrt{3})(2j-2)=(1-j\sqrt{3})(-2+2j)=2(\sqrt{3}-1)+2(\sqrt{3}+1)j.
$$

Postać trygonometryczna czynników daje równoważnie

$$
1-j\sqrt{3}=2\left(\cos\left(-\frac{\pi}{3}\right)+j\sin\left(-\frac{\pi}{3}\right)\right),\qquad
-2+2j=2\sqrt{2}\left(\cos\frac{3\pi}{4}+j\sin\frac{3\pi}{4}\right).
$$

Iloczyn ma więc moduł $4\sqrt{2}$ i argument $5\pi/12$. Pięć pierwiastków ma moduł $\rho=\sqrt[5]{4\sqrt{2}}$.

| $k$ | Argument pierwiastka | Pierwiastek |
| :---: | :---: | :--- |
| $0$ | $\frac{5\pi}{60}$ | $\rho\left(\cos\frac{5\pi}{60}+j\sin\frac{5\pi}{60}\right)$ |
| $1$ | $\frac{29\pi}{60}$ | $\rho\left(\cos\frac{29\pi}{60}+j\sin\frac{29\pi}{60}\right)$ |
| $2$ | $\frac{53\pi}{60}$ | $\rho\left(\cos\frac{53\pi}{60}+j\sin\frac{53\pi}{60}\right)$ |
| $3$ | $\frac{77\pi}{60}$ | $\rho\left(\cos\frac{77\pi}{60}+j\sin\frac{77\pi}{60}\right)$ |
| $4$ | $\frac{101\pi}{60}$ | $\rho\left(\cos\frac{101\pi}{60}+j\sin\frac{101\pi}{60}\right)$ |

Zatem

$$
\boxed{z_k=\rho\left(\cos\left(\frac{5\pi}{60}+\frac{2\pi k}{5}\right)+j\sin\left(\frac{5\pi}{60}+\frac{2\pi k}{5}\right)\right),\qquad k=0,1,2,3,4}
$$

Są to wierzchołki foremnego pięciokąta na okręgu o środku $0$ i promieniu $\rho$. Podniesienie pierwiastka do piątej potęgi daje

$$
z_k^5=4\sqrt{2}\left(\cos\left(\frac{5\pi}{12}+2\pi k\right)+j\sin\left(\frac{5\pi}{12}+2\pi k\right)\right)=2(\sqrt{3}-1)+2(\sqrt{3}+1)j.
$$

---

## Zadanie 2

Oznaczmy $c=\cos x$ i $s=\sin x$. Ze wzoru Moivre'a oraz dwumianu Newtona:

$$
(c+js)^4=c^4+4jc^3s+6j^2c^2s^2+4j^3cs^3+j^4s^4.
$$

Korzystamy z równości $j^2=-1$, $j^3=-j$ i $j^4=1$ oraz porównujemy części rzeczywistą i urojoną z $\cos 4x+j\sin 4x$:

$$
\cos 4x=c^4-6c^2s^2+s^4,\qquad \sin 4x=4c^3s-4cs^3.
$$

Po powrocie do zapisu przez sinus i cosinus:

$$
\boxed{\cos 4x=\cos^4x-6\cos^2x\sin^2x+\sin^4x,\qquad
\sin 4x=4\sin x\cos x\left(\cos^2x-\sin^2x\right)}
$$

Równoważnie, używając $\cos^2x+\sin^2x=1$, można zapisać $\cos 4x=1-8\sin^2x\cos^2x$ oraz $\sin 4x=4\sin x\cos x(1-2\sin^2x)$.

---

## Zadanie 3

W równaniach rozwiązujemy w zbiorze $\mathbb{C}$. Dla każdego skończonego zbioru rozwiązań podano współrzędne punktów i ich położenie, co pozwala odtworzyć szkic na płaszczyźnie zespolonej.

### 3.1

Iloczyn jest równy zeru wtedy i tylko wtedy, gdy co najmniej jeden czynnik jest równy zeru. Z pierwszego czynnika:

$$
z^4=16\quad\Longrightarrow\quad z=2\left(\cos\frac{k\pi}{2}+j\sin\frac{k\pi}{2}\right),\qquad k=0,1,2,3,
$$

czyli $z\in\{2,2j,-2,-2j\}$. Z drugiego czynnika:

$$
z^2=4j-3=-3+4j=(1+2j)^2,
$$

więc $z=1+2j$ albo $z=-1-2j$. Niech $\alpha=\arctan 2$. Pełny zbiór rozwiązań przedstawia tabela.

| Rozwiązanie $z$ | Współrzędne $(\text{Re}(z),\text{Im }z)$ | Postać trygonometryczna, kąt w $[0,2\pi)$ |
| :--- | :---: | :--- |
| $2$ | $(2,0)$ | $2(\cos 0+j\sin 0)$ |
| $2j$ | $(0,2)$ | $2(\cos\frac{\pi}{2}+j\sin\frac{\pi}{2})$ |
| $-2$ | $(-2,0)$ | $2(\cos\pi+j\sin\pi)$ |
| $-2j$ | $(0,-2)$ | $2(\cos\frac{3\pi}{2}+j\sin\frac{3\pi}{2})$ |
| $1+2j$ | $(1,2)$ | $\sqrt{5}(\cos\alpha+j\sin\alpha)$ |
| $-1-2j$ | $(-1,-2)$ | $\sqrt{5}(\cos(\alpha+\pi)+j\sin(\alpha+\pi))$ |

Zbiór składa się z czterech punktów na okręgu o promieniu $2$ na osiach oraz dwóch punktów antypodycznych o promieniu $\sqrt{5}$ i kątach $\alpha$ oraz $\alpha+\pi$.

$$
\boxed{\{2,2j,-2,-2j,1+2j,-1-2j\}}
$$

### 3.2

Niech $z=x+jy$, gdzie $x,y\in\mathbb{R}$. Wtedy

$$
|z|^2+z=x^2+y^2+x+jy=7-j.
$$

Porównanie części urojonych daje $y=-1$. Części rzeczywiste spełniają zatem

$$
x^2+x+1=7\quad\Longleftrightarrow\quad (x-2)(x+3)=0,
$$

więc $x=2$ albo $x=-3$. Otrzymujemy

| Rozwiązanie $z$ | Współrzędne | Moduł i argument główny |
| :--- | :---: | :--- |
| $2-j$ | $(2,-1)$ | $\sqrt{5}$, $-\arctan\frac{1}{2}$ |
| $-3-j$ | $(-3,-1)$ | $\sqrt{10}$, $-\pi+\arctan\frac{1}{3}$ |

W postaci trygonometrycznej są to

$$
2-j=\sqrt{5}\left(\cos\left(-\arctan\frac{1}{2}\right)+j\sin\left(-\arctan\frac{1}{2}\right)\right),
$$

$$
-3-j=\sqrt{10}\left(\cos\left(-\pi+\arctan\frac{1}{3}\right)+j\sin\left(-\pi+\arctan\frac{1}{3}\right)\right).
$$

Sprawdzenie przez podstawienie:

$$
|2-j|^2+(2-j)=5+2-j=7-j,\qquad |-3-j|^2+(-3-j)=10-3-j=7-j.
$$

Geometrycznie są to przecięcia prostej $y=-1$ z okręgiem

$$
\left(x+\frac{1}{2}\right)^2+y^2=\frac{29}{4},
$$

a więc dwa punkty zaznaczone w tabeli. Zatem

$$
\boxed{z\in\{2-j,-3-j\}}
$$

### 3.3

Liczba $z=0$ spełnia równanie. Dla $z\ne0$ zapisujemy $z=r(\cos\theta+j\sin\theta)$, gdzie $r>0$. Wtedy $\overline{z}=r(\cos\theta-j\sin\theta)$, a porównanie modułów i argumentów w równaniu daje

$$
r^5=8r^2\quad\Longrightarrow\quad r=2,
$$

$$
4\theta\equiv\pi-2\theta\pmod{2\pi}\quad\Longrightarrow\quad \theta=\frac{\pi}{6}+\frac{k\pi}{3},\qquad k=0,1,2,3,4,5.
$$

Rozwiązania niezerowe to

| Kąt $\theta$ | Rozwiązanie $z$ | Współrzędne |
| :---: | :--- | :---: |
| $\frac{\pi}{6}$ | $\sqrt{3}+j$ | $(\sqrt{3},1)$ |
| $\frac{\pi}{2}$ | $2j$ | $(0,2)$ |
| $\frac{5\pi}{6}$ | $-\sqrt{3}+j$ | $(-\sqrt{3},1)$ |
| $\frac{7\pi}{6}$ | $-\sqrt{3}-j$ | $(-\sqrt{3},-1)$ |
| $\frac{3\pi}{2}$ | $-2j$ | $(0,-2)$ |
| $\frac{11\pi}{6}$ | $\sqrt{3}-j$ | $(\sqrt{3},-1)$ |

Każdy z tych sześciu punktów ma postać trygonometryczną $2(\cos\theta+j\sin\theta)$ dla odpowiedniego kąta z tabeli. Szkic to wierzchołki regularnego sześciokąta na okręgu o środku $0$ i promieniu $2$, wraz z początkiem układu.

$$
\boxed{\{0\}\cup\left\{2\left(\cos\left(\frac{\pi}{6}+\frac{k\pi}{3}\right)+j\sin\left(\frac{\pi}{6}+\frac{k\pi}{3}\right)\right):k=0,1,2,3,4,5\right\}}
$$

### 3.4

Najpierw upraszczamy prawą stronę równania:

$$
\frac{2j-14}{j+3}=\frac{(-14+2j)(3-j)}{(3+j)(3-j)}=\frac{-40+20j}{10}=-4+2j.
$$

Równanie przyjmuje więc postać $z^2-z+4-2j=0$. Jego wyróżnik wynosi

$$
\Delta=1-4(4-2j)=-15+8j=(1+4j)^2.
$$

Stąd

$$
z=\frac{1\pm(1+4j)}{2},
$$

czyli otrzymujemy dwa rozwiązania:

| Rozwiązanie $z$ | Współrzędne | Postać trygonometryczna |
| :--- | :---: | :--- |
| $1+2j$ | $(1,2)$ | $\sqrt{5}(\cos(\arctan 2)+j\sin(\arctan 2))$ |
| $-2j$ | $(0,-2)$ | $2(\cos(-\frac{\pi}{2})+j\sin(-\frac{\pi}{2}))$ |

Sprawdzenie: $(1+2j)^2-(1+2j)=-4+2j$ oraz $(-2j)^2-(-2j)=-4+2j$. Na szkicu zaznaczamy punkty $(1,2)$ i $(0,-2)$. Zatem

$$
\boxed{z\in\{1+2j,-2j\}}
$$

### 3.5

Liczba $\sqrt{3}+j$ ma moduł $2$ i argument $\pi/6$, zatem

$$
(\sqrt{3}+j)^6=2^6\left(\cos\pi+j\sin\pi\right)=-64.
$$

Równanie jest równoważne $(z-j)^4=-64$. Cztery pierwiastki prawej strony mają moduł $2\sqrt{2}$ i argumenty $\pi/4+k\pi/2$, dla $k=0,1,2,3$. Po dodaniu $j$ otrzymujemy:

| $k$ | $z-j$ | Rozwiązanie $z$ | Współrzędne |
| :---: | :---: | :--- | :---: |
| $0$ | $2+2j$ | $2+3j$ | $(2,3)$ |
| $1$ | $-2+2j$ | $-2+3j$ | $(-2,3)$ |
| $2$ | $-2-2j$ | $-2-j$ | $(-2,-1)$ |
| $3$ | $2-2j$ | $2-j$ | $(2,-1)$ |

W postaci trygonometrycznej względem początku układu:

| Rozwiązanie $z$ | Postać trygonometryczna |
| :--- | :--- |
| $2+3j$ | $\sqrt{13}(\cos(\arctan\frac{3}{2})+j\sin(\arctan\frac{3}{2}))$ |
| $-2+3j$ | $\sqrt{13}(\cos(\pi-\arctan\frac{3}{2})+j\sin(\pi-\arctan\frac{3}{2}))$ |
| $-2-j$ | $\sqrt{5}(\cos(-\pi+\arctan\frac{1}{2})+j\sin(-\pi+\arctan\frac{1}{2}))$ |
| $2-j$ | $\sqrt{5}(\cos(-\arctan\frac{1}{2})+j\sin(-\arctan\frac{1}{2}))$ |

Są to wierzchołki kwadratu o środku $j$ (współrzędne $(0,1)$) i promieniu okręgu opisanego $2\sqrt{2}$.

$$
\boxed{z\in\{2+3j,-2+3j,-2-j,2-j\}}
$$

### 3.6

Dla $z=0$ równanie jest spełnione. Dla $z=r(\cos\theta+j\sin\theta)$, gdzie $r>0$, porównanie argumentów po obu stronach daje

$$
4\theta\equiv\pi-4\theta\pmod{2\pi}\quad\Longrightarrow\quad
\theta=\frac{\pi}{8}+\frac{k\pi}{4},\qquad k=0,1,\ldots,7.
$$

Moduł $r$ może być dowolną liczbą dodatnią. Zatem w postaci trygonometrycznej zbiór rozwiązań składa się z początku układu oraz ośmiu półprostych:

$$
z=r\left(\cos\left(\frac{\pi}{8}+\frac{k\pi}{4}\right)+j\sin\left(\frac{\pi}{8}+\frac{k\pi}{4}\right)\right),\qquad r>0,\quad k=0,1,\ldots,7.
$$

Równoważny zapis kartezjański otrzymujemy z $z^4+\overline{z}^{4}=0$. Dla $z=x+jy$:

$$
x^4-6x^2y^2+y^4
=\left(y^2-(3-2\sqrt{2})x^2\right)\left(y^2-(3+2\sqrt{2})x^2\right)=0.
$$

Ponieważ $3-2\sqrt{2}=(\sqrt{2}-1)^2$ oraz $3+2\sqrt{2}=(\sqrt{2}+1)^2$, otrzymujemy cztery proste przechodzące przez początek:

| Kąt kierunkowy prostej w $[0,\pi)$ | Równanie prostej |
| :---: | :--- |
| $\frac{\pi}{8}$ | $y=(\sqrt{2}-1)x$ |
| $\frac{3\pi}{8}$ | $y=(\sqrt{2}+1)x$ |
| $\frac{5\pi}{8}$ | $y=-(\sqrt{2}+1)x$ |
| $\frac{7\pi}{8}$ | $y=-(\sqrt{2}-1)x$ |

Każda z tych prostych zawiera punkt $z=0$, a poza nim wszystkie jej punkty spełniają równanie. Ostatecznie

$$
\boxed{\left\{0\right\}\cup\left\{r\left(\cos\left(\frac{\pi}{8}+\frac{k\pi}{4}\right)+j\sin\left(\frac{\pi}{8}+\frac{k\pi}{4}\right)\right):r>0,\ k=0,1,\ldots,7\right\}}
$$

---

## Zadanie 4

### 4.1

Środek trójkąta równobocznego to zarazem jego środek ciężkości i środek okręgu opisanego. Oznaczmy go przez $C=1+2j$. Wektor od środka do danego wierzchołka $P=5-2j$ wynosi

$$
P-C=(5-2j)-(1+2j)=4-4j,
$$

więc promień okręgu opisanego jest równy $R=|4-4j|=4\sqrt{2}$, a kąt początkowy $\alpha_0=-\pi/4$. Trzy kąty wierzchołków mają postać $\alpha_k=-\pi/4+2\pi k/3$, dla $k=0,1,2$.

Obracając wektor $4-4j$ o $\pm 2\pi/3$, otrzymujemy

$$
(4-4j)\left(-\frac{1}{2}+j\frac{\sqrt{3}}{2}\right)=(-2+2\sqrt{3})+(2+2\sqrt{3})j,
$$

$$
(4-4j)\left(-\frac{1}{2}-j\frac{\sqrt{3}}{2}\right)=(-2-2\sqrt{3})+(2-2\sqrt{3})j.
$$

Dodanie środka $C$ daje trzy wierzchołki:

| $k$ | Kąt $\alpha_k$ | Wierzchołek $z_k$ | Współrzędne |
| :---: | :---: | :--- | :---: |
| $0$ | $-\frac{\pi}{4}$ | $5-2j$ | $(5,-2)$ |
| $1$ | $\frac{5\pi}{12}$ | $2\sqrt{3}-1+(4+2\sqrt{3})j$ | $(2\sqrt{3}-1,4+2\sqrt{3})$ |
| $2$ | $-\frac{11\pi}{12}$ | $-1-2\sqrt{3}+(4-2\sqrt{3})j$ | $(-1-2\sqrt{3},4-2\sqrt{3})$ |

Zatem pozostałe wierzchołki to

$$
\boxed{2\sqrt{3}-1+(4+2\sqrt{3})j\quad\text{oraz}\quad -1-2\sqrt{3}+(4-2\sqrt{3})j}
$$

Kontrola: średnia arytmetyczna trzech wierzchołków wynosi $1+2j$, zgodnie z podanym środkiem.

---

## Zadanie 5

Dla liczb rzeczywistych $a,b$ zachodzą tożsamości

$$
\cos(a+jb)=\cos a\cosh b-j\sin a\sinh b,\qquad
\sin(a+jb)=\sin a\cosh b+j\cos a\sinh b.
$$

Stosując je do pierwszej wartości, otrzymujemy

$$
\cos(j\pi-\pi)=\cos(-\pi+j\pi)=\cos(-\pi)\cosh\pi-j\sin(-\pi)\sinh\pi=-\cosh\pi.
$$

Stąd

$$
\boxed{\cos(j\pi-\pi)=-\cosh\pi=-\frac{e^{\pi}+e^{-\pi}}{2}}
$$

Dla drugiej wartości:

$$
\sin\left(\frac{\pi}{2}+7j\right)=\sin\frac{\pi}{2}\cosh 7+j\cos\frac{\pi}{2}\sinh 7=\cosh 7.
$$

Zatem

$$
\boxed{\sin\left(\frac{\pi}{2}+7j\right)=\cosh 7=\frac{e^7+e^{-7}}{2}}
$$

---

## Podsumowanie wyników

| Podpunkt | Wynik |
| :--- | :--- |
| 1.1 | $8j$ |
| 1.2 | $2^{50}(1-j)$ |
| 1.3 | $\{4-3j,-4+3j\}$ |
| 1.4 | $\rho(\cos(\frac{\pi}{6}+\frac{k\pi}{2})+j\sin(\frac{\pi}{6}+\frac{k\pi}{2}))$, $k=0,1,2,3$, $\rho=\sqrt[4]{2\sqrt{3}}$ |
| 1.5 | $\sqrt[3]{5}(\cos\alpha_k+j\sin\alpha_k)$, $\alpha_k=(\pi-\arctan(3/4)+2\pi k)/3$, $k=0,1,2$ |
| 1.6 | $\rho(\cos(\frac{5\pi}{60}+\frac{2\pi k}{5})+j\sin(\frac{5\pi}{60}+\frac{2\pi k}{5}))$, $k=0,1,2,3,4$, $\rho=\sqrt[5]{4\sqrt{2}}$ |
| 2 | $\cos 4x=\cos^4x-6\cos^2x\sin^2x+\sin^4x$; $\sin 4x=4\sin x\cos x(\cos^2x-\sin^2x)$ |
| 3.1 | $\{2,2j,-2,-2j,1+2j,-1-2j\}$ |
| 3.2 | $\{2-j,-3-j\}$ |
| 3.3 | $\{0\}\cup\{2(\cos(\frac{\pi}{6}+\frac{k\pi}{3})+j\sin(\frac{\pi}{6}+\frac{k\pi}{3})):k=0,1,2,3,4,5\}$ |
| 3.4 | $\{1+2j,-2j\}$ |
| 3.5 | $\{2+3j,-2+3j,-2-j,2-j\}$ |
| 3.6 | $y=\pm(\sqrt{2}-1)x$ lub $y=\pm(\sqrt{2}+1)x$ |
| 4.1 | $2\sqrt{3}-1+(4+2\sqrt{3})j$ oraz $-1-2\sqrt{3}+(4-2\sqrt{3})j$ |
| 5 | $\cos(j\pi-\pi)=-\cosh\pi$; $\sin(\frac{\pi}{2}+7j)=\cosh 7$ |
