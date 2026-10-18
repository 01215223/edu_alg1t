# Algebra – Zestaw 2 – rozwiązania

> **Założenia i konwencje.** Jednostka urojona: $j$, gdzie $j^2 = -1$. Argument główny podajemy
> w przedziale $(-\pi, \pi]$; przy wyznaczaniu pierwiastków kąty wygodnie jest podawać
> w $[0, 2\pi)$. Zapis trygonometryczny: $r(\cos\varphi + j\sin\varphi)$. Wypisujemy wszystkie
> pierwiastki. Wszystkie wyniki są dokładne; przybliżenia dziesiętne występują tylko tam, gdzie
> wymaga tego polecenie (zadanie 1.5 — argument „z kalkulatora”) albo w tabelach pomocniczych.
>
> **Uwaga organizacyjna.** Plik jest samodzielnym, pełnym rozwiązaniem zestawu 2; w repozytorium
> istnieje także plik `zestaw2-odpowiedzi.md` z wcześniejszą wersją odpowiedzi.

---

## Zadanie 1 — potęgi i pierwiastki liczb zespolonych

### 1.1

* **Dane:** $\dfrac{(-2 + 2\sqrt3 j)^{21}}{(2 - 2j)^{26}}$.
* **Krok 1 — postać trygonometryczna obu podstaw:**

  $$
  -2 + 2\sqrt3 j = 4\left(\cos\frac{2\pi}{3} + j\sin\frac{2\pi}{3}\right), \qquad
  2 - 2j = 2\sqrt2\left(\cos\left(-\frac{\pi}{4}\right) + j\sin\left(-\frac{\pi}{4}\right)\right)
  $$

  bo $\lvert -2 + 2\sqrt3 j\rvert = \sqrt{4 + 12} = 4$, $\lvert 2 - 2j\rvert = 2\sqrt2$.

* **Krok 2 — wzór Moivre'a dla licznika i mianownika:**

  $$
  (-2 + 2\sqrt3 j)^{21} = 4^{21}\left(\cos 14\pi + j\sin 14\pi\right) = 4^{21},
  $$

  $$
  (2 - 2j)^{26} = (2\sqrt2)^{26}\left(\cos\left(-\frac{13\pi}{2}\right)
  + j\sin\left(-\frac{13\pi}{2}\right)\right) = 2^{39} \cdot (-j)
  $$

* **Krok 3 — iloraz (moduł i argument):**

  $$
  \frac{4^{21}}{(2\sqrt2)^{26}} = \frac{2^{42}}{2^{39}} = 8, \qquad
  14\pi + \frac{13\pi}{2} = \frac{41\pi}{2} \equiv \frac{\pi}{2} \pmod{2\pi}
  $$

* **Wynik:**

  $$
  \boxed{\frac{(-2 + 2\sqrt3 j)^{21}}{(2 - 2j)^{26}}
  = 8\left(\cos\frac{\pi}{2} + j\sin\frac{\pi}{2}\right) = 8j}
  $$

* **Sprawdzenie (rachunek niezależny).** Licznik jest rzeczywisty, bo kąt $14\pi$ jest parzystą
  wielokrotnością $\pi$; mianownik ma argument $-\frac{13\pi}{2} \equiv -\frac{\pi}{2}$, czyli
  wartość $-j$. Zatem

  $$
  \frac{2^{42}}{2^{39}(-j)} = \frac{8}{-j} = \frac{8j}{-j^2} = 8j
  $$

### 1.2

* **Dane:** $\left(\dfrac{2j - 4}{j + 3}\right)^{101}$.
* **Krok 1 — uproszczenie podstawy** (mnożymy licznik i mianownik przez sprzężenie mianownika):

  $$
  \frac{2j - 4}{j + 3} = \frac{(-4 + 2j)(3 - j)}{(3 + j)(3 - j)}
  = \frac{-12 + 4j + 6j - 2j^2}{10} = \frac{-10 + 10j}{10} = -1 + j
  $$

* **Krok 2 — postać trygonometryczna:** $\lvert -1 + j\rvert = \sqrt2$, argument $\frac{3\pi}{4}$,
  więc

  $$
  (-1 + j)^{101} = (\sqrt2)^{101}\left(\cos\frac{303\pi}{4} + j\sin\frac{303\pi}{4}\right)
  $$

* **Krok 3 — redukcja:** $(\sqrt2)^{101} = 2^{101/2} = 2^{50}\sqrt2$ oraz
  $\frac{303\pi}{4} = 76\pi - \frac{\pi}{4} \equiv -\frac{\pi}{4} \pmod{2\pi}$, więc

  $$
  (-1 + j)^{101} = 2^{50}\sqrt2\left(\frac{\sqrt2}{2} - j\frac{\sqrt2}{2}\right)
  = 2^{50}(1 - j)
  $$

* **Wynik:**

  $$
  \boxed{\left(\frac{2j - 4}{j + 3}\right)^{101} = 2^{50}(1 - j)
  = 1125899906842624 - 1125899906842624j}
  $$

* **Sprawdzenie (rachunek niezależny).** $(-1 + j)^2 = -2j$, więc

  $$
  (-1 + j)^{101} = \left((-1 + j)^2\right)^{50}(-1 + j) = (-2j)^{50}(-1 + j)
  = 2^{50} j^{50}(-1 + j) = -2^{50}(-1 + j) = 2^{50}(1 - j)
  $$

  bo $j^{50} = (j^2)^{25} = -1$.

### 1.3

* **Dane:** $\sqrt{7 - 24j}$.
* **Krok 1 — moduł:** $\lvert 7 - 24j\rvert = \sqrt{49 + 576} = \sqrt{625} = 25$.
* **Krok 2 — pierwiastek metodą algebraiczną.** Szukamy $a, b \in \mathbb{R}$ takich, że
  $(a + bj)^2 = a^2 - b^2 + 2abj = 7 - 24j$. Porównując części rzeczywiste, urojone i moduły:

  $$
  a^2 - b^2 = 7, \qquad 2ab = -24, \qquad a^2 + b^2 = 25
  $$

  Dodając pierwsze i trzecie równanie: $2a^2 = 32$, czyli $a^2 = 16$ i $b^2 = 9$; z warunku
  $ab = -12 < 0$ liczby $a$ i $b$ mają przeciwne znaki, więc $a = 4$, $b = -3$.

* **Wynik:**

  $$
  \boxed{\sqrt{7 - 24j} = \pm(4 - 3j)}
  $$

* **Sprawdzenie.** $(4 - 3j)^2 = 16 - 24j + 9j^2 = 7 - 24j$ — zgadza się.

### 1.4

* **Dane:** $\sqrt[4]{3j - \sqrt3}$, czyli pierwiastki czwartego stopnia z $-\sqrt3 + 3j$.
* **Krok 1 — moduł i argument:**

  $$
  r = \lvert -\sqrt3 + 3j\rvert = \sqrt{3 + 9} = \sqrt{12} = 2\sqrt3, \qquad
  \cos\varphi = \frac{-\sqrt3}{2\sqrt3} = -\frac12, \quad \sin\varphi = \frac{3}{2\sqrt3}
  = \frac{\sqrt3}{2} \implies \varphi = \frac{2\pi}{3}
  $$

* **Krok 2 — moduł i kąty pierwiastków:**

  $$
  \rho = \sqrt[4]{2\sqrt3} = \sqrt[4]{\sqrt{12}} = \sqrt[8]{12} \approx 1{,}3643, \qquad
  \varphi_k = \frac{\frac{2\pi}{3} + 2k\pi}{4} = \frac{\pi}{6} + \frac{k\pi}{2},
  \quad k = 0, 1, 2, 3
  $$

* **Wynik:**

  $$
  \boxed{z_k = \sqrt[8]{12}\left(\cos\left(\frac{\pi}{6} + \frac{k\pi}{2}\right)
  + j\sin\left(\frac{\pi}{6} + \frac{k\pi}{2}\right)\right), \qquad k = 0, 1, 2, 3}
  $$

| $k$ | Kąt | Wartość dokładna | Przybliżenie |
| :---: | :---: | :--- | :--- |
| $0$ | $\frac{\pi}{6} = 30^\circ$ | $\frac{\sqrt3\sqrt[8]{12}}{2} + j\frac{\sqrt[8]{12}}{2}$ | $1{,}1815 + 0{,}6821j$ |
| $1$ | $\frac{2\pi}{3} = 120^\circ$ | $-\frac{\sqrt[8]{12}}{2} + j\frac{\sqrt3\sqrt[8]{12}}{2}$ | $-0{,}6821 + 1{,}1815j$ |
| $2$ | $\frac{7\pi}{6} = 210^\circ$ | $-\frac{\sqrt3\sqrt[8]{12}}{2} - j\frac{\sqrt[8]{12}}{2}$ | $-1{,}1815 - 0{,}6821j$ |
| $3$ | $\frac{5\pi}{3} = 300^\circ$ | $\frac{\sqrt[8]{12}}{2} - j\frac{\sqrt3\sqrt[8]{12}}{2}$ | $0{,}6821 - 1{,}1815j$ |

* **Sprawdzenie.** Dla $k = 0$ moduł spełnia $\lvert z_0\rvert^4 = \sqrt{12} = 2\sqrt3$, a kąt
  wynosi $4 \cdot \frac{\pi}{6} = \frac{2\pi}{3}$, więc

  $$
  z_0^4 = 2\sqrt3\left(\cos\frac{2\pi}{3} + j\sin\frac{2\pi}{3}\right)
  = 2\sqrt3\left(-\frac12 + j\frac{\sqrt3}{2}\right) = -\sqrt3 + 3j
  $$

  Suma czterech pierwiastków wynosi $0$, co zgadza się z brakiem wyrazu $z^3$ w równaniu
  $z^4 + \sqrt3 - 3j = 0$.

### 1.5

* **Dane:** $\sqrt[3]{-4 + 3j}$.
* **Krok 1 — moduł i argument** (argument z kalkulatora, zgodnie z poleceniem):

  $$
  r = \sqrt{16 + 9} = 5, \qquad
  \alpha = \pi - \arctan\frac34 \approx \pi - 0{,}6435011 = 2{,}4980915\ \text{rad}
  \approx 143{,}1301^\circ
  $$

* **Krok 2 — moduł i kąty pierwiastków:**

  $$
  \rho = \sqrt[3]{5} \approx 1{,}709976, \qquad
  \varphi_k = \frac{\alpha + 2k\pi}{3}, \qquad k = 0, 1, 2
  $$

* **Wynik:**

  $$
  \boxed{z_k = \sqrt[3]{5}\left(\cos\frac{\alpha + 2k\pi}{3} + j\sin\frac{\alpha + 2k\pi}{3}\right),
  \qquad k = 0, 1, 2, \qquad \alpha = \pi - \arctan\frac34 \approx 2{,}4980915\ \text{rad}}
  $$

| $k$ | Kąt $\varphi_k$ [rad] | Kąt $[\ ^\circ]$ | Wartość przybliżona |
| :---: | :---: | :---: | :--- |
| $0$ | $0{,}8326972$ | $47{,}7100^\circ$ | $1{,}1506 + 1{,}2650j$ |
| $1$ | $2{,}927092$ | $167{,}7100^\circ$ | $-1{,}6708 + 0{,}3640j$ |
| $2$ | $5{,}021487$ | $287{,}7100^\circ$ | $0{,}5202 - 1{,}6289j$ |

* **Sprawdzenie.** Suma pierwiastków: $z_0 + z_1 + z_2 = 0$ (brak wyrazu $z^2$ w równaniu
  $z^3 + 4 - 3j = 0$), a moduł każdego pierwiastka wynosi $\sqrt[3]{5}$; podniesienie $z_0$
  do trzeciej potęgi daje kąt $3 \cdot 0{,}8326972 = 2{,}4980915 = \alpha$ i moduł $5$, czyli
  liczbę $-4 + 3j$.

### 1.6

* **Dane:** $\sqrt[5]{(1 - j\sqrt3)(2j - 2)}$.
* **Krok 1 — iloczyn w postaci algebraicznej:**

  $$
  (1 - \sqrt3 j)(2j - 2) = 2j - 2 - 2\sqrt3 j^2 + 2\sqrt3 j
  = (2\sqrt3 - 2) + (2 + 2\sqrt3)j
  $$

* **Krok 2 — moduł i argument iloczynu:**

  $$
  r = \sqrt{(2\sqrt3 - 2)^2 + (2 + 2\sqrt3)^2} = \sqrt{32} = 4\sqrt2 = 2^{5/2}
  $$

  Argument: $\tan\varphi = \frac{2 + 2\sqrt3}{2\sqrt3 - 2} = 2 + \sqrt3$, a ponieważ
  $\tan 75^\circ = 2 + \sqrt3$ i obie współrzędne są dodatnie, $\varphi = \frac{5\pi}{12}$.
  (Ten sam wynik daje rachunek w postaci trygonometrycznej: $1 - \sqrt3 j = 2e^{-j\pi/3}$,
  $2j - 2 = 2\sqrt2 e^{j3\pi/4}$, więc iloczyn to $4\sqrt2 e^{j5\pi/12}$.)

* **Krok 3 — moduł i kąty pierwiastków:**

  $$
  \rho = \sqrt[5]{2^{5/2}} = \sqrt2, \qquad
  \varphi_k = \frac{\frac{5\pi}{12} + 2k\pi}{5} = \frac{\pi}{12} + \frac{2k\pi}{5},
  \qquad k = 0, 1, 2, 3, 4
  $$

* **Wynik:**

  $$
  \boxed{z_k = \sqrt2\left(\cos\left(\frac{\pi}{12} + \frac{2k\pi}{5}\right)
  + j\sin\left(\frac{\pi}{12} + \frac{2k\pi}{5}\right)\right), \qquad k = 0, 1, 2, 3, 4}
  $$

| $k$ | Kąt | Wartość dokładna | Przybliżenie |
| :---: | :---: | :--- | :--- |
| $0$ | $\frac{\pi}{12} = 15^\circ$ | $\frac{\sqrt3 + 1}{2} + j\frac{\sqrt3 - 1}{2}$ | $1{,}3660 + 0{,}3660j$ |
| $1$ | $\frac{29\pi}{60} = 87^\circ$ | $\sqrt2\left(\cos\frac{29\pi}{60} + j\sin\frac{29\pi}{60}\right)$ | $0{,}0740 + 1{,}4123j$ |
| $2$ | $\frac{53\pi}{60} = 159^\circ$ | $\sqrt2\left(\cos\frac{53\pi}{60} + j\sin\frac{53\pi}{60}\right)$ | $-1{,}3203 + 0{,}5068j$ |
| $3$ | $\frac{77\pi}{60} = 231^\circ$ | $\sqrt2\left(\cos\frac{77\pi}{60} + j\sin\frac{77\pi}{60}\right)$ | $-0{,}8900 - 1{,}0991j$ |
| $4$ | $\frac{101\pi}{60} = 303^\circ$ | $\sqrt2\left(\cos\frac{101\pi}{60} + j\sin\frac{101\pi}{60}\right)$ | $0{,}7702 - 1{,}1861j$ |

* **Sprawdzenie.** Dla $k = 0$ otrzymujemy

  $$
  z_0^5 = (\sqrt2)^5\left(\cos 75^\circ + j\sin 75^\circ\right)
  = 4\sqrt2\left(\frac{\sqrt6 - \sqrt2}{4} + j\frac{\sqrt6 + \sqrt2}{4}\right)
  = (2\sqrt3 - 2) + (2 + 2\sqrt3)j
  $$

  czyli dokładnie liczbę spod pierwiastka. Suma pięciu pierwiastków wynosi $0$, co zgadza się
  z brakiem wyrazu $z^4$ w równaniu $z^5 - (2\sqrt3 - 2) - (2 + 2\sqrt3)j = 0$.

---

## Zadanie 2 — wzór Moivre'a: $\sin 4x$ i $\cos 4x$

* **Krok 1 — wzór Moivre'a dla $n = 4$:**

  $$
  (\cos x + j\sin x)^4 = \cos 4x + j\sin 4x
  $$

* **Krok 2 — rozwinięcie dwumianem Newtona lewej strony:**

  $$
  (\cos x + j\sin x)^4 = \cos^4 x + 4j\cos^3 x \sin x + 6j^2\cos^2 x \sin^2 x
  + 4j^3\cos x \sin^3 x + j^4\sin^4 x
  $$

* **Krok 3 — użycie $j^2 = -1$, $j^3 = -j$, $j^4 = 1$ i rozdzielenie części:**

  $$
  (\cos x + j\sin x)^4
  = \left(\cos^4 x - 6\cos^2 x \sin^2 x + \sin^4 x\right)
  + j\left(4\cos^3 x \sin x - 4\cos x \sin^3 x\right)
  $$

* **Krok 4 — porównanie części rzeczywistych i urojonych:**

  $$
  \boxed{\cos 4x = \cos^4 x - 6\cos^2 x \sin^2 x + \sin^4 x}
  $$

  $$
  \boxed{\sin 4x = 4\cos^3 x \sin x - 4\cos x \sin^3 x
  = 4\sin x \cos x \left(\cos^2 x - \sin^2 x\right) = 2\sin 2x \cos 2x}
  $$

* **Postacie alternatywne** (po podstawieniu $\sin^2 x = 1 - \cos^2 x$ albo
  $\cos^2 x = 1 - \sin^2 x$):

  $$
  \cos 4x = 8\cos^4 x - 8\cos^2 x + 1 = 8\sin^4 x - 8\sin^2 x + 1
  $$

* **Sprawdzenie.** Dla $x = \frac{\pi}{4}$: $\cos 4x = \cos\pi = -1$, a wzór daje
  $\frac14 - 6 \cdot \frac12 \cdot \frac12 + \frac14 = -1$; $\sin 4x = \sin\pi = 0$, a wzór daje
  $4 \cdot \frac{1}{2\sqrt2} \cdot \frac{1}{\sqrt2} \cdot 0 = 0$.

---

## Zadanie 3 — równania w zbiorze liczb zespolonych

### 3.1

* **Dane:** $(z^4 - 16)(z^2 - 4j + 3) = 0$.
* **Krok 1 — pierwszy czynnik:**

  $$
  z^4 = 16 = 16(\cos 0 + j\sin 0) \implies z_k = 2\left(\cos\frac{k\pi}{2}
  + j\sin\frac{k\pi}{2}\right), \quad k = 0, 1, 2, 3 \implies z \in \{2, 2j, -2, -2j\}
  $$

* **Krok 2 — drugi czynnik:** $z^2 = 4j - 3 = -3 + 4j$. Moduł tej liczby wynosi $5$; szukamy
  $a, b \in \mathbb{R}$ takich, że $(a + bj)^2 = -3 + 4j$, czyli

  $$
  a^2 - b^2 = -3, \qquad a^2 + b^2 = 5, \qquad 2ab = 4
  $$

  Stąd $a^2 = 1$, $b^2 = 4$, a z warunku $ab = 2 > 0$ obie liczby są dodatnie: $a = 1$, $b = 2$,
  zatem

  $$
  z = \pm(1 + 2j)
  $$

* **Wynik:**

  $$
  \boxed{z \in \{2, -2, 2j, -2j, 1 + 2j, -1 - 2j\}}
  $$

* **Szkic zbioru rozwiązań** (sześć punktów):

| Punkt | $\text{Re } z$ | $\text{Im } z$ |
| :---: | :---: | :---: |
| $A$ | $2$ | $0$ |
| $B$ | $-2$ | $0$ |
| $C$ | $0$ | $2$ |
| $D$ | $0$ | $-2$ |
| $E$ | $1$ | $2$ |
| $F$ | $-1$ | $-2$ |

```text
                  Im
                  ^
          (0, 2)  |  *  (1, 2)
             *    |
                  |
   *--------------+--------------*-----> Re
 (-2, 0)        (0, 0)         (2, 0)
                  |
   (-1, -2) *     *  (0, -2)
```

* **Sprawdzenie.** $(1 + 2j)^2 - 4j + 3 = -3 + 4j - 4j + 3 = 0$ oraz
  $(\pm 2)^4 - 16 = 0$, $(\pm 2j)^4 - 16 = 16 - 16 = 0$.

### 3.2

* **Dane:** $\lvert z\rvert^2 + z = 7 - j$.
* **Krok 1 — podstawienie $z = x + jy$, $x, y \in \mathbb{R}$** (wtedy $\lvert z\rvert^2 = x^2 + y^2$):

  $$
  x^2 + y^2 + x + jy = 7 - j
  $$

* **Krok 2 — porównanie części urojonych i rzeczywistych:**

  $$
  y = -1, \qquad x^2 + 1 + x = 7 \iff x^2 + x - 6 = 0 \iff (x + 3)(x - 2) = 0
  $$

  czyli $x = 2$ albo $x = -3$.

* **Wynik:**

  $$
  \boxed{z = 2 - j \quad \text{lub} \quad z = -3 - j}
  $$

* **Szkic zbioru rozwiązań** (dwa punkty na prostej $y = -1$):

```text
                  Im
                  ^
                  |
   ---------------+---------------------------> Re
                  |
  (-3, -1) *      |      * (2, -1)
                  |
```

* **Sprawdzenie.** $\lvert 2 - j\rvert^2 + 2 - j = 5 + 2 - j = 7 - j$;
  $\lvert -3 - j\rvert^2 - 3 - j = 10 - 3 - j = 7 - j$.

### 3.3

* **Dane:** $z^4 \lvert z\rvert = -8\overline{z}^{\,2}$.
* **Krok 1 — porównanie modułów obu stron** (z warunku $\lvert \overline z\rvert = \lvert z\rvert$):

  $$
  \lvert z\rvert^5 = 8\lvert z\rvert^2 \iff \lvert z\rvert^2\left(\lvert z\rvert^3 - 8\right) = 0
  \iff \lvert z\rvert = 0 \quad \text{lub} \quad \lvert z\rvert = 2
  $$

* **Krok 2 — przypadek $z = 0$:** $0 = 0$, więc $z = 0$ jest rozwiązaniem.
* **Krok 3 — przypadek $\lvert z\rvert = 2$.** Niech $z = 2(\cos\varphi + j\sin\varphi)$; wtedy
  $\overline{z}^{\,2} = 4(\cos 2\varphi - j\sin 2\varphi)$ i równanie przyjmuje postać

  $$
  32(\cos 4\varphi + j\sin 4\varphi) = -32(\cos 2\varphi - j\sin 2\varphi)
  $$

  czyli $e^{4j\varphi} = -e^{-2j\varphi}$, a stąd $e^{6j\varphi} = -1 = e^{j\pi}$:

  $$
  6\varphi = \pi + 2k\pi \implies \varphi = \frac{\pi}{6} + \frac{k\pi}{3}, \qquad k = 0, 1, \ldots, 5
  $$

* **Wynik:**

  $$
  \boxed{z = 0 \quad \text{oraz} \quad
  z_k = 2\left(\cos\left(\frac{\pi}{6} + \frac{k\pi}{3}\right)
  + j\sin\left(\frac{\pi}{6} + \frac{k\pi}{3}\right)\right), \quad k = 0, 1, \ldots, 5}
  $$

| $k$ | Kąt | Rozwiązanie |
| :---: | :---: | :--- |
| $0$ | $30^\circ$ | $\sqrt3 + j$ |
| $1$ | $90^\circ$ | $2j$ |
| $2$ | $150^\circ$ | $-\sqrt3 + j$ |
| $3$ | $210^\circ$ | $-\sqrt3 - j$ |
| $4$ | $270^\circ$ | $-2j$ |
| $5$ | $330^\circ$ | $\sqrt3 - j$ |

* **Szkic zbioru rozwiązań** (siedem punktów: środek układu i sześciokąt foremny na okręgu
  o promieniu $2$):

```text
                  Im
                  ^
      (-√3, 1) *  |  * (0, 2)  *  (√3, 1)
                  \  |  /
                   \ | /
   ------------------+--------------------> Re
                   / | \        (0, 0)
                  /  |  \
     (-√3,-1) *      *      * (√3,-1)
                     (0,-2)
```

* **Sprawdzenie.** Dla $z = \sqrt3 + j$: $z^2 = 2 + 2\sqrt3 j$, $z^4 = -8 + 8\sqrt3 j$,
  $\lvert z\rvert = 2$, więc lewa strona $= -16 + 16\sqrt3 j$; prawa strona
  $= -8(\sqrt3 - j)^2 = -8(2 - 2\sqrt3 j) = -16 + 16\sqrt3 j$ — zgadza się.

### 3.4

* **Dane:** $z^2 - z = \dfrac{2j - 14}{j + 3}$.
* **Krok 1 — uproszczenie prawej strony:**

  $$
  \frac{2j - 14}{j + 3} = \frac{(-14 + 2j)(3 - j)}{(3 + j)(3 - j)}
  = \frac{-42 + 14j + 6j - 2j^2}{10} = \frac{-40 + 20j}{10} = -4 + 2j
  $$

* **Krok 2 — równanie kwadratowe i wyróżnik:**

  $$
  z^2 - z + 4 - 2j = 0, \qquad \Delta = 1 - 4(4 - 2j) = -15 + 8j
  $$

* **Krok 3 — pierwiastek z wyróżnika.** Szukamy $(a + bj)^2 = -15 + 8j$; moduł $\Delta$ wynosi
  $17$, więc $a^2 + b^2 = 17$, $a^2 - b^2 = -15$, $2ab = 8$: stąd $a^2 = 1$, $b^2 = 16$, $ab > 0$,
  czyli $a = 1$, $b = 4$ i $\sqrt{\Delta} = \pm(1 + 4j)$.

* **Krok 4 — wzory na pierwiastki:**

  $$
  z = \frac{1 \pm (1 + 4j)}{2} \implies z_1 = \frac{2 + 4j}{2} = 1 + 2j, \qquad
  z_2 = \frac{-4j}{2} = -2j
  $$

* **Wynik:**

  $$
  \boxed{z = 1 + 2j \quad \text{lub} \quad z = -2j}
  $$

* **Szkic zbioru rozwiązań** (dwa punkty):

```text
                  Im
                  ^
          (1, 2)  |
             *    |
                  |
   ---------------+---------------------> Re
                  |
                  *  (0, -2)
```

* **Sprawdzenie.** $(1 + 2j)^2 - (1 + 2j) = -3 + 4j - 1 - 2j = -4 + 2j$;
  $(-2j)^2 + 2j = -4 + 2j$ — oba wyniki równe prawej stronie.

### 3.5

* **Dane:** $(z - j)^4 = (\sqrt3 + j)^6$.
* **Krok 1 — prawa strona:** $\sqrt3 + j = 2\left(\cos\frac{\pi}{6} + j\sin\frac{\pi}{6}\right)$,
  więc

  $$
  (\sqrt3 + j)^6 = 2^6(\cos\pi + j\sin\pi) = -64
  $$

* **Krok 2 — podstawienie $w = z - j$:** $w^4 = -64 = 64(\cos\pi + j\sin\pi)$, zatem

  $$
  w_k = \sqrt[4]{64}\left(\cos\frac{\pi + 2k\pi}{4} + j\sin\frac{\pi + 2k\pi}{4}\right)
  = 2\sqrt2\left(\cos\left(\frac{\pi}{4} + \frac{k\pi}{2}\right)
  + j\sin\left(\frac{\pi}{4} + \frac{k\pi}{2}\right)\right), \quad k = 0, 1, 2, 3
  $$

  czyli $w \in \{2 + 2j, -2 + 2j, -2 - 2j, 2 - 2j\}$.

* **Krok 3 — powrót do $z = w + j$:**

  $$
  z \in \{2 + 3j, -2 + 3j, -2 - j, 2 - j\}
  $$

* **Wynik:**

  $$
  \boxed{z \in \{2 + 3j, -2 + 3j, -2 - j, 2 - j\}}
  $$

* **Szkic zbioru rozwiązań** (kwadrat o boku $4$ i środku w punkcie $j$):

```text
                  Im
                  ^
     (-2, 3) *--------------* (2, 3)
              |      *      |
              |   (0, 1)    |
   -----------+-------------+-------------> Re
              |             |
    (-2,-1) *---------------*  (2, -1)
```

* **Sprawdzenie.** Dla $z = 2 + 3j$: $w = 2 + 2j$, $w^2 = 8j$, $w^4 = -64$ — zgadza się
  z prawą stroną.

### 3.6

* **Dane:** $z^4 = -\overline{z}^{\,4}$.
* **Krok 1 — porównanie modułów:** $\lvert z\rvert^4 = \lvert z\rvert^4$ — równość zachodzi
  dla każdego $z$, więc moduł nie jest ograniczony; decyduje argument.
* **Krok 2 — postać trygonometryczna.** Niech $z = r(\cos\varphi + j\sin\varphi)$, $r \ge 0$;
  wtedy $\overline{z}^{\,4} = r^4(\cos 4\varphi - j\sin 4\varphi)$ i równanie ma postać

  $$
  r^4(\cos 4\varphi + j\sin 4\varphi) = -r^4(\cos 4\varphi - j\sin 4\varphi)
  $$

* **Krok 3 — przypadek $r = 0$:** $z = 0$ spełnia równanie ($0 = 0$).
* **Krok 4 — przypadek $r > 0$:** dzielimy przez $r^4$ i otrzymujemy
  $e^{4j\varphi} = -e^{-4j\varphi}$, czyli $e^{8j\varphi} = -1 = e^{j\pi}$:

  $$
  8\varphi = \pi + 2k\pi \implies \varphi = \frac{(2k + 1)\pi}{8}, \qquad k = 0, 1, \ldots, 7
  $$

* **Wynik:**

  $$
  \boxed{z = t\left(\cos\frac{(2k + 1)\pi}{8} + j\sin\frac{(2k + 1)\pi}{8}\right),
  \qquad t \ge 0, \quad k = 0, 1, \ldots, 7}
  $$

  Zbiór rozwiązań to osiem półprostych wychodzących z początku układu (wspólny koniec
  $z = 0$ należy do zbioru), rozłożonych co $45^\circ$.

| $k$ | Kąt $\varphi_k$ | Kąt $[\ ^\circ]$ |
| :---: | :---: | :---: |
| $0$ | $\frac{\pi}{8}$ | $22{,}5^\circ$ |
| $1$ | $\frac{3\pi}{8}$ | $67{,}5^\circ$ |
| $2$ | $\frac{5\pi}{8}$ | $112{,}5^\circ$ |
| $3$ | $\frac{7\pi}{8}$ | $157{,}5^\circ$ |
| $4$ | $\frac{9\pi}{8}$ | $202{,}5^\circ$ |
| $5$ | $\frac{11\pi}{8}$ | $247{,}5^\circ$ |
| $6$ | $\frac{13\pi}{8}$ | $292{,}5^\circ$ |
| $7$ | $\frac{15\pi}{8}$ | $337{,}5^\circ$ |

* **Szkic zbioru rozwiązań** (osiem półprostych; szkic poglądowy, dokładne kąty w tabeli):

```text
                    Im
                    ^
               *    |    *
                 \  |  /
                  \ | /
   ------*---------\|/---------*---------> Re
                    O
                  / | \
                 /  |  \
               *    |    *
```

* **Brzegi.** Każda półprosta jest domknięta (zawiera punkt $z = 0$) i nieograniczona;
  na szkicu rysujemy je linią ciągłą.
* **Sprawdzenie.** Dla $\varphi = \frac{\pi}{8}$ i dowolnego $t > 0$:
  $z^4 = t^4 e^{j\pi/2} = t^4 j$ oraz $-\overline{z}^{\,4} = -t^4 e^{-j\pi/2} = t^4 j$ — równość
  zachodzi; analogicznie dla pozostałych $k$ (warunek $8\varphi \equiv \pi \pmod{2\pi}$).

---

## Zadanie 4 — trójkąt równoboczny o danym wierzchołku i środku

### 4.1

* **Dane:** wierzchołek $A = 5 - 2j$, środek $S = 1 + 2j$ (w trójkącie równobocznym środek
  ciężkości pokrywa się ze środkiem okręgu opisanego).
* **Krok 1 — promień okręgu opisanego:**

  $$
  A - S = 4 - 4j, \qquad R = \lvert A - S\rvert = \sqrt{16 + 16} = 4\sqrt2
  $$

* **Krok 2 — pozostałe wierzchołki przez obrót o $\pm\frac{2\pi}{3}$ wokół $S$.** Kąty środkowe
  w trójkącie równobocznym wynoszą $\frac{2\pi}{3}$, więc

  $$
  B = S + (A - S)\omega, \qquad C = S + (A - S)\overline{\omega}, \qquad
  \omega = e^{j2\pi/3} = -\frac12 + j\frac{\sqrt3}{2}
  $$

* **Krok 3 — obliczenie $B$:**

  $$
  (4 - 4j)\omega = (4 - 4j)\left(-\frac12 + j\frac{\sqrt3}{2}\right)
  = -2 + 2\sqrt3 j + 2j + 2\sqrt3 = (2\sqrt3 - 2) + (2\sqrt3 + 2)j
  $$

  $$
  B = (1 + 2j) + (2\sqrt3 - 2) + (2\sqrt3 + 2)j = (2\sqrt3 - 1) + (2\sqrt3 + 4)j
  $$

* **Krok 4 — obliczenie $C$:**

  $$
  (4 - 4j)\overline{\omega} = (4 - 4j)\left(-\frac12 - j\frac{\sqrt3}{2}\right)
  = (-2 - 2\sqrt3) + (2 - 2\sqrt3)j
  $$

  $$
  C = (1 + 2j) + (-2 - 2\sqrt3) + (2 - 2\sqrt3)j = (-1 - 2\sqrt3) + (4 - 2\sqrt3)j
  $$

* **Wynik:**

  $$
  \boxed{B = (2\sqrt3 - 1) + (2\sqrt3 + 4)j, \qquad
  C = (-1 - 2\sqrt3) + (4 - 2\sqrt3)j}
  $$

| Wierzchołek | Wartość dokładna | Przybliżenie |
| :---: | :--- | :--- |
| $A$ | $5 - 2j$ | $5{,}0000 - 2{,}0000j$ |
| $B$ | $(2\sqrt3 - 1) + (2\sqrt3 + 4)j$ | $2{,}4641 + 7{,}4641j$ |
| $C$ | $(-1 - 2\sqrt3) + (4 - 2\sqrt3)j$ | $-4{,}4641 + 0{,}5359j$ |
| $S$ | $1 + 2j$ | $1{,}0000 + 2{,}0000j$ |

* **Szkic** (rozmieszczenie poglądowe):

```text
                  Im
                  ^
                  |      * B (2,46; 7,46)
                  |
   * C (-4,46; 0,54)   * S (1, 2)
                  |
   ---------------+---------------------> Re
                  |
                  |            * A (5, -2)
```

* **Sprawdzenie.** Środek ciężkości: $\frac{A + B + C}{3} = \frac{3 + 6j}{3} = 1 + 2j = S$.
  Długości boków:

  $$
  \lvert A - B\rvert = \lvert B - C\rvert = \lvert C - A\rvert = 4\sqrt6 \approx 9{,}7980
  $$

  co jest zgodne ze wzorem $a = R\sqrt3 = 4\sqrt2 \cdot \sqrt3$ dla trójkąta równobocznego.

---

## Zadanie 5 — wartości zespolonych funkcji trygonometrycznych

* **Definicje** (wynikające z definicji przez funkcję wykładniczą): dla $t \in \mathbb{R}$

  $$
  \cos(jt) = \cosh t, \qquad \sin(jt) = j\sinh t
  $$

### 5.1 — $\cos(j\pi - \pi)$

* **Krok 1 — wzór na cosinus różnicy:**

  $$
  \cos(j\pi - \pi) = \cos(j\pi)\cos\pi + \sin(j\pi)\sin\pi
  = \cosh\pi \cdot (-1) + j\sinh\pi \cdot 0
  $$

* **Wynik:**

  $$
  \boxed{\cos(j\pi - \pi) = -\cosh\pi = -\frac{e^{\pi} + e^{-\pi}}{2} \approx -11{,}5920}
  $$

* **Sprawdzenie (z definicji wykładniczej):**

  $$
  \cos(j\pi - \pi) = \frac{e^{j(j\pi - \pi)} + e^{-j(j\pi - \pi)}}{2}
  = \frac{e^{-\pi}e^{j\pi} + e^{\pi}e^{-j\pi}}{2} = \frac{-e^{-\pi} - e^{\pi}}{2} = -\cosh\pi
  $$

### 5.2 — $\sin\left(\frac{\pi}{2} + 7j\right)$

* **Krok 1 — wzór na sinus sumy:**

  $$
  \sin\left(\frac{\pi}{2} + 7j\right)
  = \sin\frac{\pi}{2}\cos(7j) + \cos\frac{\pi}{2}\sin(7j)
  = 1 \cdot \cosh 7 + 0 \cdot j\sinh 7
  $$

* **Wynik:**

  $$
  \boxed{\sin\left(\frac{\pi}{2} + 7j\right) = \cosh 7 = \frac{e^{7} + e^{-7}}{2}
  \approx 548{,}3170}
  $$

* **Sprawdzenie (z definicji wykładniczej):**

  $$
  \sin\left(\frac{\pi}{2} + 7j\right)
  = \frac{e^{j(\pi/2 + 7j)} - e^{-j(\pi/2 + 7j)}}{2j}
  = \frac{e^{-7}e^{j\pi/2} - e^{7}e^{-j\pi/2}}{2j}
  = \frac{je^{-7} + je^{7}}{2j} = \frac{e^{7} + e^{-7}}{2} = \cosh 7
  $$

---

## Podsumowanie wyników

| Podpunkt | Wynik |
| :--- | :--- |
| 1.1 | $8j$ |
| 1.2 | $2^{50}(1 - j) = 1125899906842624(1 - j)$ |
| 1.3 | $\pm(4 - 3j)$ |
| 1.4 | $z_k = \sqrt[8]{12}\left(\cos\left(\frac{\pi}{6} + \frac{k\pi}{2}\right) + j\sin\left(\frac{\pi}{6} + \frac{k\pi}{2}\right)\right)$, $k = 0, 1, 2, 3$ |
| 1.5 | $z_k = \sqrt[3]{5}\left(\cos\frac{\alpha + 2k\pi}{3} + j\sin\frac{\alpha + 2k\pi}{3}\right)$, $k = 0, 1, 2$, gdzie $\alpha \approx 2{,}4981$ rad |
| 1.6 | $z_k = \sqrt2\left(\cos\left(\frac{\pi}{12} + \frac{2k\pi}{5}\right) + j\sin\left(\frac{\pi}{12} + \frac{2k\pi}{5}\right)\right)$, $k = 0, \ldots, 4$ |
| 2 | $\cos 4x = \cos^4 x - 6\cos^2 x \sin^2 x + \sin^4 x$; $\sin 4x = 4\cos^3 x \sin x - 4\cos x \sin^3 x$ |
| 3.1 | $z \in \{2, -2, 2j, -2j, 1 + 2j, -1 - 2j\}$ |
| 3.2 | $z = 2 - j$ lub $z = -3 - j$ |
| 3.3 | $z = 0$ oraz $z_k = 2\left(\cos\left(\frac{\pi}{6} + \frac{k\pi}{3}\right) + j\sin\left(\frac{\pi}{6} + \frac{k\pi}{3}\right)\right)$, $k = 0, \ldots, 5$ |
| 3.4 | $z = 1 + 2j$ lub $z = -2j$ |
| 3.5 | $z \in \{2 + 3j, -2 + 3j, -2 - j, 2 - j\}$ |
| 3.6 | osiem półprostych $z = t e^{j(2k+1)\pi/8}$, $t \ge 0$, $k = 0, \ldots, 7$ |
| 4.1 | $B = (2\sqrt3 - 1) + (2\sqrt3 + 4)j$, $C = (-1 - 2\sqrt3) + (4 - 2\sqrt3)j$ |
| 5 | $\cos(j\pi - \pi) = -\cosh\pi \approx -11{,}5920$; $\sin\left(\frac{\pi}{2} + 7j\right) = \cosh 7 \approx 548{,}3170$ |
