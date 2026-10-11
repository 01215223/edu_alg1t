# Algebra – Zestaw 3 – rozwiązania

> **Założenia i konwencje.** Jednostka urojona: $j$, gdzie $j^2 = -1$. Moduł i sprzężenie:
> $\lvert z\rvert$ oraz $\overline{z}$; część rzeczywista i urojona: $\text{Re } z$, $\text{Im } z$.
> Argument główny podajemy w przedziale $(-\pi, \pi]$; kąty pierwiastków, gdy jest to wygodniejsze,
> podajemy w $[0, 2\pi)$. Wszystkie wyniki są dokładne — ułamki dziesiętne występują wyłącznie
> jako dodatkowa ilustracja przybliżonych wartości.
>
> **Uwaga o liczbie pierwiastków.** Pytanie „ile jest różnych pierwiastków rzeczywistych, a ile
> zespolonych” rozumiemy tak: ile różnych liczb rzeczywistych oraz ile różnych liczb nierzeczywistych
> (o niezerowej części urojonej) występuje wśród pierwiastków. Każda liczba rzeczywista jest zarazem
> zespoloną, dlatego podajemy również łączną liczbę różnych pierwiastków. Krotności wypisujemy osobno
> przy każdym pierwiastku.

---

## Zadanie 1

Dla każdego wielomianu wyznaczamy pełny rozkład na czynniki, listę różnych pierwiastków wraz
z krotnościami, liczbę pierwiastków rzeczywistych i nierzeczywistych oraz współrzędne punktów,
które należy zaznaczyć na płaszczyźnie zespolonej.

### 1.1

* **Wielomian:** $w(z) = z^{17} + z^{12} - z^7 - z^2$.
* **Krok 1 — wyłączenie wspólnego czynnika $z^2$:**

  $$w(z) = z^2\left(z^{15} + z^{10} - z^5 - 1\right)$$

* **Krok 2 — podstawienie $t = z^5$ i rozkład na czynniki:**

  $$t^3 + t^2 - t - 1 = t^2(t + 1) - (t + 1) = (t + 1)\left(t^2 - 1\right) = (t + 1)^2(t - 1)$$

* **Krok 3 — powrót do zmiennej $z$:**

  $$w(z) = z^2\left(z^5 + 1\right)^2\left(z^5 - 1\right)$$

  $$\boxed{w(z) = z^2\left(z^5 + 1\right)^2\left(z^5 - 1\right)}$$

* **Pierwiastki i krotności.** Z ostatniego rozkładu:

  * $z = 0$ (z czynnika $z^2$) — krotność $2$;
  * pierwiastki $z^5 = 1$ — krotność $1$ każdy;
  * pierwiastki $z^5 = -1$ (z czynnika $\left(z^5 + 1\right)^2$) — krotność $2$ każdy.

  Wszystkie niezerowe pierwiastki mają moduł $1$ i spełniają jedno z równań $z^5 = 1$ lub
  $z^5 = -1$, czyli są to dokładnie pierwiastki dziesiątego stopnia z jedynki:
  $\zeta_k^5 = (-1)^k$, więc $k$ parzyste odpowiada równaniu $z^5 = 1$, a $k$ nieparzyste —
  równaniu $z^5 = -1$:

  $$\zeta_k = \cos\frac{k\pi}{5} + j\sin\frac{k\pi}{5}, \qquad k = 0, 1, \ldots, 9$$

  Współrzędne na płaszczyźnie (kąt $\varphi_k = \frac{k\pi}{5}$, wartości dokładne przez
  $\cos 36^\circ = \frac{1 + \sqrt5}{4}$ oraz $\cos 72^\circ = \frac{\sqrt5 - 1}{4}$):

| Pierwiastek $z$ | Kąt $\varphi_k$ | Krotność | $(\text{Re } z, \text{Im } z)$ |
| :--- | :---: | :---: | :--- |
| $0$ | — | $2$ | $(0, 0)$ — środek układu |
| $1$ | $0$ | $1$ | $(1, 0)$ |
| $\zeta_1$ | $\frac{\pi}{5}$ | $2$ | $\left(\frac{1 + \sqrt5}{4}, \frac{\sqrt{10 - 2\sqrt5}}{4}\right)$ |
| $\zeta_2$ | $\frac{2\pi}{5}$ | $1$ | $\left(\frac{\sqrt5 - 1}{4}, \frac{\sqrt{10 + 2\sqrt5}}{4}\right)$ |
| $\zeta_3$ | $\frac{3\pi}{5}$ | $2$ | $\left(-\frac{\sqrt5 - 1}{4}, \frac{\sqrt{10 + 2\sqrt5}}{4}\right)$ |
| $\zeta_4$ | $\frac{4\pi}{5}$ | $1$ | $\left(-\frac{1 + \sqrt5}{4}, \frac{\sqrt{10 - 2\sqrt5}}{4}\right)$ |
| $-1$ | $\pi$ | $2$ | $(-1, 0)$ |
| $\zeta_6$ | $\frac{6\pi}{5}$ | $1$ | $\left(-\frac{1 + \sqrt5}{4}, -\frac{\sqrt{10 - 2\sqrt5}}{4}\right)$ |
| $\zeta_7$ | $\frac{7\pi}{5}$ | $2$ | $\left(-\frac{\sqrt5 - 1}{4}, -\frac{\sqrt{10 + 2\sqrt5}}{4}\right)$ |
| $\zeta_8$ | $\frac{8\pi}{5}$ | $1$ | $\left(\frac{\sqrt5 - 1}{4}, -\frac{\sqrt{10 + 2\sqrt5}}{4}\right)$ |
| $\zeta_9$ | $\frac{9\pi}{5}$ | $2$ | $\left(\frac{1 + \sqrt5}{4}, -\frac{\sqrt{10 - 2\sqrt5}}{4}\right)$ |

* **Liczby pierwiastków:** różnych pierwiastków jest $11$ (kąt $k\pi/5$ dla $k = 0, \ldots, 9$
  oraz $z = 0$). Wśród nich:

  * różnych pierwiastków **rzeczywistych**: $3$, mianowicie $-1$, $0$, $1$;
  * różnych pierwiastków **nierzeczywistych** (zespolonych o niezerowej części urojonej): $8$
    (po cztery z równań $z^5 - 1 = 0$ i $z^5 + 1 = 0$);
  * łącznie różnych pierwiastków zespolonych: $11$.

* **Opis położenia:** dziesięć pierwiastków niezerowych to wierzchołki dziesięciokąta foremnego
  wpisanego w okrąg jednostkowy, rozmieszczone co $\frac{\pi}{5}$; krotność $1$ mają wierzchołki
  o kątach $0$, $\frac{2\pi}{5}$, $\frac{4\pi}{5}$, $\frac{6\pi}{5}$, $\frac{8\pi}{5}$,
  a krotność $2$ — o kątach $\frac{\pi}{5}$, $\frac{3\pi}{5}$, $\pi$, $\frac{7\pi}{5}$,
  $\frac{9\pi}{5}$. Dodatkowo pierwiastkiem jest środek układu (krotność $2$).

* **Szkic** (poglądowy, nie w skali; $+$ — pierwiastek $z = 0$):

  ```text
                       Im
                       ^
                       |
            k=3 *      |      * k=2
                 `.    |    .'
         k=4 *     `.  |  .'     * k=1
                     .|.
         k=5 * - - - (+) - - - - * k=0
                     `|`
         k=6 *     .' | `.     * k=9
                 .'    |    `.
            k=7 *      |      * k=8
                       |
     +  srodek: pierwiastek z = 0 (krotnosc 2)
     *  krotnosc 1: katy 0, 72, 144, 216, 288 stopni  (k parzyste)
     *  krotnosc 2: katy 36, 108, 180, 252, 324 stopni (k nieparzyste)
  ```

* **Sprawdzenie.** Suma krotności: $2 + 5 \cdot 1 + 5 \cdot 2 = 17$ — tyle, ile wynosi
  stopień wielomianu. Dla kontroli wartość $w(2) = 2^{17} + 2^{12} - 2^7 - 2^2 = 135036$ zgadza się
  z wartością rozkładu: $2^2 \cdot 33^2 \cdot 31 = 135036$.

* **Wynik:**

  $$
  \boxed{w(z) = z^2\left(z^5 + 1\right)^2\left(z^5 - 1\right); \quad
  \text{rzeczywiste: } -1, 0, 1\ (3); \quad \text{nierzeczywiste: } 8}
  $$

### 1.2

* **Wielomian:** $w(z) = z^9 + 4z^6 + 4z^3$.
* **Krok 1 — wyłączenie $z^3$ i podstawienie $t = z^3$:**

  $$w(z) = z^3\left(z^6 + 4z^3 + 4\right), \qquad t^2 + 4t + 4 = (t + 2)^2$$

* **Krok 2 — rozkład:**

  $$\boxed{w(z) = z^3\left(z^3 + 2\right)^2}$$

* **Pierwiastki i krotności:**

  * $z = 0$ (z czynnika $z^3$) — krotność $3$;
  * pierwiastki $z^3 = -2$, czyli $z_k = \sqrt[3]{2}\left(\cos\frac{\pi + 2k\pi}{3} + j\sin\frac{\pi + 2k\pi}{3}\right)$
    dla $k = 0, 1, 2$ (z czynnika $\left(z^3 + 2\right)^2$) — krotność $2$ każdy.

  Wartości dokładne:

  $$
  z_0 = \frac{\sqrt[3]{2}}{2} + j\frac{\sqrt3\sqrt[3]{2}}{2}, \qquad
  z_1 = -\sqrt[3]{2}, \qquad
  z_2 = \frac{\sqrt[3]{2}}{2} - j\frac{\sqrt3\sqrt[3]{2}}{2}
  $$

* **Tabela współrzędnych** (promień okręgu $r = \sqrt[3]{2} \approx 1{,}26$):

| Pierwiastek $z$ | Kąt | Krotność | $(\text{Re } z, \text{Im } z)$ |
| :--- | :---: | :---: | :--- |
| $0$ | — | $3$ | $(0, 0)$ — środek układu |
| $-\sqrt[3]{2}$ | $\pi$ | $2$ | $(-\sqrt[3]{2}, 0)$ |
| $\frac{\sqrt[3]{2}}{2}\left(1 + j\sqrt3\right)$ | $\frac{\pi}{3}$ | $2$ | $\left(\frac{\sqrt[3]{2}}{2}, \frac{\sqrt3\sqrt[3]{2}}{2}\right)$ |
| $\frac{\sqrt[3]{2}}{2}\left(1 - j\sqrt3\right)$ | $\frac{5\pi}{3}$ | $2$ | $\left(\frac{\sqrt[3]{2}}{2}, -\frac{\sqrt3\sqrt[3]{2}}{2}\right)$ |

* **Liczby pierwiastków:** różnych pierwiastków jest $4$;

  * różnych pierwiastków **rzeczywistych**: $2$, mianowicie $0$ oraz $-\sqrt[3]{2}$;
  * różnych pierwiastków **nierzeczywistych**: $2$ (zespolone sprzężone
    $\frac{\sqrt[3]{2}}{2} \pm j\frac{\sqrt3\sqrt[3]{2}}{2}$);
  * łącznie różnych pierwiastków zespolonych: $4$.

* **Opis położenia:** trzy pierwiastki niezerowe tworzą wierzchołki trójkąta równobocznego
  wpisanego w okrąg o promieniu $\sqrt[3]{2}$, o kątach $\frac{\pi}{3}$, $\pi$, $\frac{5\pi}{3}$;
  dodatkowo pierwiastkiem jest środek układu (krotność $3$).

* **Szkic** (poglądowy, nie w skali):

  ```text
                       Im
                       ^
                       |            * k=0  (kat pi/3)
                       |          .'
                       |        .'
   k=1 *---------------(+)-------------------> Re
     (kat pi)          |  `.          (+): pierwiastek z = 0, krotnosc 3
                       |    `.
                       |      `.
                       |        `.
                       |          * k=2  (kat 5pi/3)
  ```

* **Sprawdzenie.** Suma krotności: $3 + 3 \cdot 2 = 9$ — tyle, ile stopień wielomianu.
  Dodatkowo $w(1) = 1 + 4 + 4 = 9$ oraz $z^3\left(z^3 + 2\right)^2$ dla $z = 1$ daje $1 \cdot 9 = 9$.

* **Wynik:**

  $$
  \boxed{w(z) = z^3\left(z^3 + 2\right)^2; \quad
  \text{rzeczywiste: } 0, -\sqrt[3]{2}\ (2); \quad \text{nierzeczywiste: } 2}
  $$

### 1.3

* **Wielomian:** $w(z) = z^7 - jz$.
* **Krok 1 — wyłączenie $z$:**

  $$w(z) = z\left(z^6 - j\right)$$

* **Krok 2 — pierwiastki szóstego stopnia z $j$.** Ponieważ $j = \cos\frac{\pi}{2} + j\sin\frac{\pi}{2}$
  oraz $\lvert j\rvert = 1$, ze wzoru Moivre'a dla pierwiastków:

  $$
  z_k = \cos\left(\frac{\pi/2 + 2k\pi}{6}\right) + j\sin\left(\frac{\pi/2 + 2k\pi}{6}\right)
  = \cos\left(\frac{\pi}{12} + \frac{k\pi}{3}\right) + j\sin\left(\frac{\pi}{12} + \frac{k\pi}{3}\right),
  \qquad k = 0, 1, \ldots, 5
  $$

  Kąty te to $\frac{\pi}{12}$ ($15^\circ$), $\frac{5\pi}{12}$ ($75^\circ$), $\frac{3\pi}{4}$
  ($135^\circ$), $\frac{13\pi}{12}$ ($195^\circ$), $\frac{17\pi}{12}$ ($255^\circ$),
  $\frac{7\pi}{4}$ ($315^\circ$) — jest to sześciokąt foremny obrócony o $\frac{\pi}{12}$.
  Są to jednocześnie pierwiastki $24$. stopnia z jedynki o wskaźnikach $m \equiv 1 \pmod 4$.

* **Krok 3 — rozkład:**

  $$
  \boxed{w(z) = z\left(z^6 - j\right), \qquad \text{zatem } w'(z_k) = 6j \ne 0
  \text{ — wszystkie pierwiastki są jednokrotne}}
  $$

* **Wartości dokładne** (wzory na $\cos 15^\circ = \frac{\sqrt6 + \sqrt2}{4}$,
  $\sin 15^\circ = \frac{\sqrt6 - \sqrt2}{4}$):

| Pierwiastek $z$ | Kąt | Krotność | $(\text{Re } z, \text{Im } z)$ |
| :--- | :---: | :---: | :--- |
| $0$ | — | $1$ | $(0, 0)$ — środek układu |
| $\frac{\sqrt6 + \sqrt2}{4} + j\frac{\sqrt6 - \sqrt2}{4}$ | $\frac{\pi}{12}$ | $1$ | $\left(\frac{\sqrt6 + \sqrt2}{4}, \frac{\sqrt6 - \sqrt2}{4}\right)$ |
| $\frac{\sqrt6 - \sqrt2}{4} + j\frac{\sqrt6 + \sqrt2}{4}$ | $\frac{5\pi}{12}$ | $1$ | $\left(\frac{\sqrt6 - \sqrt2}{4}, \frac{\sqrt6 + \sqrt2}{4}\right)$ |
| $-\frac{\sqrt2}{2} + j\frac{\sqrt2}{2}$ | $\frac{3\pi}{4}$ | $1$ | $\left(-\frac{\sqrt2}{2}, \frac{\sqrt2}{2}\right)$ |
| $-\frac{\sqrt6 + \sqrt2}{4} - j\frac{\sqrt6 - \sqrt2}{4}$ | $\frac{13\pi}{12}$ | $1$ | $\left(-\frac{\sqrt6 + \sqrt2}{4}, -\frac{\sqrt6 - \sqrt2}{4}\right)$ |
| $-\frac{\sqrt6 - \sqrt2}{4} - j\frac{\sqrt6 + \sqrt2}{4}$ | $\frac{17\pi}{12}$ | $1$ | $\left(-\frac{\sqrt6 - \sqrt2}{4}, -\frac{\sqrt6 + \sqrt2}{4}\right)$ |
| $\frac{\sqrt2}{2} - j\frac{\sqrt2}{2}$ | $\frac{7\pi}{4}$ | $1$ | $\left(\frac{\sqrt2}{2}, -\frac{\sqrt2}{2}\right)$ |

* **Liczby pierwiastków:** różnych pierwiastków jest $7$;

  * różnych pierwiastków **rzeczywistych**: $1$, mianowicie $z = 0$;
  * różnych pierwiastków **nierzeczywistych**: $6$ (wszystkie pierwiastki $z^6 = j$, położone
    na okręgu jednostkowym w kątach innych niż $0$ i $\pi$);
  * łącznie różnych pierwiastków zespolonych: $7$.

* **Opis położenia:** sześć pierwiastków niezerowych to wierzchołki sześciokąta foremnego wpisanego
  w okrąg jednostkowy, o kątach $\frac{\pi}{12} + \frac{k\pi}{3}$; dodatkowo pierwiastkiem jest
  środek układu (krotność $1$).

* **Szkic** (poglądowy, nie w skali):

  ```text
                       Im
                       ^
                k=2 *  |  * k=1
                     `. | .'
                       `|'
     k=3 *--------------(+)-------------* k=0
                       .|.
                     .' | `.
                k=4 *  |  * k=5
     (+): pierwiastek z = 0 (krotnosc 1)
     *  : katy 15, 75, 135, 195, 255, 315 stopni
  ```

* **Sprawdzenie.** Liczba $z_0 = \frac{\sqrt6 + \sqrt2}{4} + j\frac{\sqrt6 - \sqrt2}{4}$ ma postać
  trygonometryczną $z_0 = \cos\frac{\pi}{12} + j\sin\frac{\pi}{12}$, więc
  $z_0^6 = \cos\frac{\pi}{2} + j\sin\frac{\pi}{2} = j$; analogicznie dla pozostałych pierwiastków.
  Suma krotności $1 + 6 \cdot 1 = 7$ równa się stopniowi wielomianu; dla kontroli
  $w(1) = 1 - j$ oraz $z\left(z^6 - j\right)$ dla $z = 1$ daje $1 - j$.

* **Wynik:**

  $$
  \boxed{w(z) = z\left(z^6 - j\right); \quad
  \text{rzeczywiste: } 0\ (1); \quad \text{nierzeczywiste: } 6}
  $$

### Zestawienie liczb pierwiastków (zadanie 1)

| Podpunkt | Różnych pierwiastków łącznie | Rzeczywistych | Nierzeczywistych |
| :---: | :---: | :---: | :---: |
| 1.1 | $11$ | $3$ | $8$ |
| 1.2 | $4$ | $2$ | $2$ |
| 1.3 | $7$ | $1$ | $6$ |

---

## Zadanie 2

* **Dane:** $w(z) = z^4 + 2z^3 + 2z^2 + 10z + 25$ oraz $z_0 = 1 + 2j$ — pierwiastek tego wielomianu.
* **Krok 1 — sprawdzenie danej liczby $z_0$:**

  $$
  z_0^2 = (1 + 2j)^2 = -3 + 4j, \qquad z_0^3 = (-3 + 4j)(1 + 2j) = -11 - 2j, \qquad
  z_0^4 = z_0^3 \cdot z_0 = (-11 - 2j)(1 + 2j) = -7 - 24j
  $$

  $$w(z_0) = (-7 - 24j) + 2(-11 - 2j) + 2(-3 + 4j) + 10(1 + 2j) + 25 = 0 + 0j$$

* **Krok 2 — drugi pierwiastek z pary sprzężonej.** Wielomian ma współczynniki rzeczywiste, więc
  razem z $z_0 = 1 + 2j$ jego pierwiastkiem jest również $\overline{z_0} = 1 - 2j$. Para ta daje
  czynnik rzeczywisty:

  $$\left(z - (1 + 2j)\right)\left(z - (1 - 2j)\right) = (z - 1)^2 + 4 = z^2 - 2z + 5$$

* **Krok 3 — dzielenie wielomianu.** Szukamy ilorazu $z^2 + az + b$:

  $$z^4 + 2z^3 + 2z^2 + 10z + 25 = \left(z^2 - 2z + 5\right)\left(z^2 + az + b\right)$$

  Porównanie współczynników przy kolejnych potęgach:

  * $z^3$: $a - 2 = 2$, więc $a = 4$;
  * $z^2$: $b - 2a + 5 = 2$, więc $b = 2 + 8 - 5 = 5$;
  * $z^1$: $5a - 2b = 20 - 10 = 10$ oraz $z^0$: $5b = 25$ — oba warunki są spełnione.

  Zatem

  $$w(z) = \left(z^2 - 2z + 5\right)\left(z^2 + 4z + 5\right)$$

* **Krok 4 — pierwiastki trójmianu $z^2 + 4z + 5$:**

  $$z^2 + 4z + 5 = (z + 2)^2 + 1 = 0 \quad\Longrightarrow\quad z = -2 \pm j$$

* **Sprawdzenie.** Suma wszystkich pierwiastków: $(1 + 2j) + (1 - 2j) + (-2 + j) + (-2 - j) = -2$,
  co zgadza się ze współczynnikiem przy $z^3$ (suma pierwiastków $= -2$). Iloczyn wszystkich
  pierwiastków: $5 \cdot 5 = 25$, co zgadza się ze stałą $25$.

* **Wynik:**

  $$
  \boxed{\text{pozostałe pierwiastki: } z \in \left\{-2 - j,\ -2 + j,\ 1 - 2j\right\}}
  $$

  Pełny zbiór pierwiastków wielomianu, razem z danym $z_0 = 1 + 2j$, to
  $\left\{1 + 2j,\ 1 - 2j,\ -2 + j,\ -2 - j\right\}$.

---

## Zadanie 3

### 3.1

* **Wielomian:** $w(z) = z^4 + 6z^2 + 25$.
* **Krok 1 — podstawienie $u = z^2$:**

  $$u^2 + 6u + 25 = 0, \qquad \Delta = 36 - 100 = -64, \qquad \sqrt{\Delta} = 8j$$

  $$u = \frac{-6 \pm 8j}{2} = -3 \pm 4j$$

* **Krok 2 — pierwiastki kwadratowe liczb $-3 \pm 4j$.** Ponieważ

  $$(1 + 2j)^2 = 1 + 4j - 4 = -3 + 4j, \qquad (1 - 2j)^2 = 1 - 4j - 4 = -3 - 4j,$$

  więc $z^2 = (1 + 2j)^2$ albo $z^2 = (1 - 2j)^2$, skąd:

  $$z \in \left\{1 + 2j,\ -1 - 2j,\ 1 - 2j,\ -1 + 2j\right\}$$

* **Rozkład na czynniki liniowe:**

  $$\boxed{w(z) = \left(z - 1 - 2j\right)\left(z + 1 + 2j\right)\left(z - 1 + 2j\right)\left(z + 1 - 2j\right)}$$

* **Sprawdzenie.** Iloczyn par sprzężonych daje rozkład nad $\mathbb{R}$:

  $$
  \left(z^2 - 2z + 5\right)\left(z^2 + 2z + 5\right) = \left(z^2 + 5\right)^2 - 4z^2
  = z^4 + 10z^2 + 25 - 4z^2 = z^4 + 6z^2 + 25
  $$

### 3.2

* **Wielomian:** $w(z) = z^4 - (3 + 2j)^4$.
* **Krok 1 — różnica kwadratów:**

  $$
  w(z) = \left(z^2 - (3 + 2j)^2\right)\left(z^2 + (3 + 2j)^2\right)
  = \left(z^2 - (3 + 2j)^2\right)\left(z^2 - \left(j(3 + 2j)\right)^2\right)
  $$

  bo $-1 = j^2$, czyli $+(3 + 2j)^2 = -\left(j(3 + 2j)\right)^2$.

* **Krok 2 — pierwiastki.** Z pierwszego czynnika $z = \pm(3 + 2j)$, z drugiego
  $z = \pm j(3 + 2j) = \pm(-2 + 3j)$:

  $$z \in \left\{3 + 2j,\ -3 - 2j,\ -2 + 3j,\ 2 - 3j\right\}$$

* **Rozkład na czynniki liniowe:**

  $$\boxed{w(z) = \left(z - 3 - 2j\right)\left(z + 3 + 2j\right)\left(z + 2 - 3j\right)\left(z - 2 + 3j\right)}$$

* **Sprawdzenie.** $(3 + 2j)^2 = 5 + 12j$, więc $(3 + 2j)^4 = (5 + 12j)^2 = -119 + 120j$.
  Z drugiej strony iloczyn dwóch par sprzężonych daje

  $$
  \left(z^2 - 5 - 12j\right)\left(z^2 + 5 + 12j\right) = z^4 - (5 + 12j)^2 = z^4 + 119 - 120j,
  $$

  czyli dokładnie $z^4 - (3 + 2j)^4$ — zgodnie z wyjściowym wielomianem.

### 3.3

* **Wielomian:** $w(z) = (1 + j\sqrt3)z^4 + 8$.
* **Krok 1 — wyznaczenie $z^4$:**

  $$
  (1 + j\sqrt3)z^4 = -8 \quad\Longrightarrow\quad
  z^4 = \frac{-8}{1 + j\sqrt3} = \frac{-8\left(1 - j\sqrt3\right)}{\left(1 + j\sqrt3\right)\left(1 - j\sqrt3\right)}
  = \frac{-8 + 8j\sqrt3}{4} = -2 + 2\sqrt3 j
  $$

  Ponieważ $1 + j\sqrt3 = 2\left(\cos\frac{\pi}{3} + j\sin\frac{\pi}{3}\right)$ oraz
  $-2 + 2\sqrt3 j = 4\left(\cos\frac{2\pi}{3} + j\sin\frac{2\pi}{3}\right)$, cztery pierwiastki
  mają moduł $\sqrt2$ i kąty $\frac{\pi}{6} + \frac{k\pi}{2}$:

  $$
  z_k = \sqrt2\left(\cos\left(\frac{\pi}{6} + \frac{k\pi}{2}\right)
  + j\sin\left(\frac{\pi}{6} + \frac{k\pi}{2}\right)\right), \qquad k = 0, 1, 2, 3
  $$

* **Krok 2 — wartości algebraiczne:**

  $$
  z_0 = \frac{\sqrt6}{2} + j\frac{\sqrt2}{2}, \qquad
  z_1 = -\frac{\sqrt2}{2} + j\frac{\sqrt6}{2}, \qquad
  z_2 = -\frac{\sqrt6}{2} - j\frac{\sqrt2}{2}, \qquad
  z_3 = \frac{\sqrt2}{2} - j\frac{\sqrt6}{2}
  $$

* **Rozkład na czynniki liniowe** (współczynnik wiodący $1 + j\sqrt3$ pozostaje przed iloczynem):

  $$
  \boxed{(1 + j\sqrt3)z^4 + 8 = (1 + j\sqrt3)
  \left(z - \frac{\sqrt6}{2} - \frac{\sqrt2}{2}j\right)
  \left(z + \frac{\sqrt2}{2} - \frac{\sqrt6}{2}j\right)
  \left(z + \frac{\sqrt6}{2} + \frac{\sqrt2}{2}j\right)
  \left(z - \frac{\sqrt2}{2} + \frac{\sqrt6}{2}j\right)}
  $$

* **Sprawdzenie.** Dla $z_0 = \sqrt2\left(\cos\frac{\pi}{6} + j\sin\frac{\pi}{6}\right)$:
  $z_0^4 = 4\left(\cos\frac{2\pi}{3} + j\sin\frac{2\pi}{3}\right) = -2 + 2\sqrt3 j$, a stąd

  $$
  (1 + j\sqrt3)z_0^4 = 2 \cdot 4\left(\cos\left(\frac{\pi}{3} + \frac{2\pi}{3}\right)
  + j\sin\left(\frac{\pi}{3} + \frac{2\pi}{3}\right)\right) = 8(-1) = -8
  $$

  czyli $w(z_0) = 0$; analogicznie dla $z_1$, $z_2$, $z_3$ (ich kąty różnią się o wielokrotność
  $\frac{\pi}{2}$).

---

## Zadanie 4

Podajemy ogólną postać rozkładu na ułamki proste nad $\mathbb{R}$, bez wyznaczania współczynników.
Przypominamy regułę: każdemu czynnikowi liniowemu $(x - a)^m$ odpowiada suma
$\frac{A_1}{x - a} + \ldots + \frac{A_m}{(x - a)^m}$, a każdemu czynnikowi kwadratowemu
nierozkładalnemu $(x^2 + px + q)^m$ — suma
$\frac{B_1x + C_1}{x^2 + px + q} + \ldots + \frac{B_mx + C_m}{(x^2 + px + q)^m}$.

### 4.1

* **Dane:** $\dfrac{2x^2 - 7x}{(x - 3)^3(x^2 + 4)^2}$; stopień licznika $2$ < stopień mianownika $5$,
  więc rozkład nie zawiera części wielomianowej.
* **Czynniki mianownika:** $(x - 3)^3$ oraz $(x^2 + 4)^2$; trójmian $x^2 + 4$ jest nierozkładalny
  nad $\mathbb{R}$ ($\Delta = -16 < 0$).
* **Ogólna postać rozkładu:**

  $$
  \boxed{\frac{2x^2 - 7x}{(x - 3)^3(x^2 + 4)^2}
  = \frac{A}{x - 3} + \frac{B}{(x - 3)^2} + \frac{C}{(x - 3)^3}
  + \frac{Dx + E}{x^2 + 4} + \frac{Fx + G}{(x^2 + 4)^2}}
  $$

  gdzie $A, B, C, D, E, F, G \in \mathbb{R}$.

### 4.2

* **Dane:** $\dfrac{3x^4 - 2}{x^4 - 2x^3 + 2x - 1}$; stopnie licznika i mianownika są równe ($4$),
  więc najpierw wydzielamy część wielomianową.
* **Krok 1 — dzielenie:**

  $$3x^4 - 2 = 3\left(x^4 - 2x^3 + 2x - 1\right) + \left(6x^3 - 6x + 1\right)$$

  $$\frac{3x^4 - 2}{x^4 - 2x^3 + 2x - 1} = 3 + \frac{6x^3 - 6x + 1}{x^4 - 2x^3 + 2x - 1}$$

* **Krok 2 — rozkład mianownika na czynniki:**

  $$
  x^4 - 2x^3 + 2x - 1 = (x - 1)\left(x^3 - x^2 - x + 1\right)
  = (x - 1)(x - 1)\left(x^2 - 1\right) = (x - 1)^3(x + 1)
  $$

* **Ogólna postać rozkładu:**

  $$
  \boxed{\frac{3x^4 - 2}{x^4 - 2x^3 + 2x - 1}
  = 3 + \frac{A}{x - 1} + \frac{B}{(x - 1)^2} + \frac{C}{(x - 1)^3} + \frac{D}{x + 1}}
  $$

  gdzie $A, B, C, D \in \mathbb{R}$.

### 4.3

* **Dane:** $\dfrac{5x^3}{(x^4 + 4)^2}$; stopień licznika $3$ < stopień mianownika $8$, brak części
  wielomianowej.
* **Krok 1 — rozkład $x^4 + 4$ na czynniki nierozkładalne nad $\mathbb{R}$** (tożsamość
  Sophie Germain: $x^4 + 4 = \left(x^2 + 2\right)^2 - 4x^2$):

  $$
  x^4 + 4 = \left(x^2 + 2 - 2x\right)\left(x^2 + 2 + 2x\right)
  = \left(x^2 - 2x + 2\right)\left(x^2 + 2x + 2\right)
  $$

  Oba trójmiany są nierozkładalne nad $\mathbb{R}$ (odpowiednio $\Delta = -4$ i $\Delta = -4$),
  zatem

  $$\left(x^4 + 4\right)^2 = \left(x^2 - 2x + 2\right)^2\left(x^2 + 2x + 2\right)^2$$

* **Ogólna postać rozkładu:**

  $$
  \boxed{\frac{5x^3}{(x^4 + 4)^2}
  = \frac{Ax + B}{x^2 - 2x + 2} + \frac{Cx + D}{\left(x^2 - 2x + 2\right)^2}
  + \frac{Ex + F}{x^2 + 2x + 2} + \frac{Gx + H}{\left(x^2 + 2x + 2\right)^2}}
  $$

  gdzie $A, B, C, D, E, F, G, H \in \mathbb{R}$.

* **Uwaga.** Bez rozkładania $x^4 + 4$ na iloczyn dwóch trójmianów (tj. traktując $x^4 + 4$ jako
  jeden czynnik stopnia $4$) dałoby się zapisać krótszą postać

  $$
  \frac{ax^3 + bx^2 + cx + d}{x^4 + 4} + \frac{ex^3 + fx^2 + gx + h}{(x^4 + 4)^2},
  $$

  która również opisuje każdą funkcję wymierną o mianowniku $(x^4 + 4)^2$, ale nie jest rozkładem
  względem czynników nierozkładalnych nad $\mathbb{R}$. Kanoniczna postać rozkładu nad
  $\mathbb{R}$ to postać podana w ramce.

---

## Zadanie 5

Korzystamy z tej samej reguły co w zadaniu 4 oraz z wzoru na współczynniki przy czynnikach
liniowych jednokrotnych (dla mianownika $g$ o pierwiastkach jednokrotnych $a_i$):
$A_i = \frac{f(a_i)}{g'(a_i)}$ — analogicznie jak we wskazówce do zadań 7 dla liczb zespolonych.

### 5.1

* **Dane:** $f(x) = 4x - 10$, $g(x) = (x - 1)(x - 2)(x - 3)$ — trzy pierwiastki jednokrotne.
* **Krok 1 — współczynniki ze wzoru $A_i = \frac{f(a_i)}{g'(a_i)}$:**

  $$
  A = \frac{f(1)}{(1 - 2)(1 - 3)} = \frac{-6}{2} = -3, \qquad
  B = \frac{f(2)}{(2 - 1)(2 - 3)} = \frac{-2}{-1} = 2, \qquad
  C = \frac{f(3)}{(3 - 1)(3 - 2)} = \frac{2}{2} = 1
  $$

* **Rozkład:**

  $$\boxed{\frac{4x - 10}{(x - 1)(x - 2)(x - 3)} = \frac{-3}{x - 1} + \frac{2}{x - 2} + \frac{1}{x - 3}}$$

* **Sprawdzenie.** Dla $x = 0$: lewa strona $= \frac{-10}{-6} = \frac53$,
  prawa strona $= \frac{-3}{-1} + \frac{2}{-2} + \frac{1}{-3} = 3 - 1 - \frac13 = \frac53$.

### 5.2

* **Dane:** $\dfrac{8}{x^2 - 4x + 2}$.
* **Krok 1 — pierwiastki mianownika:** $\Delta = 16 - 8 = 8$,
  $x_{1,2} = \frac{4 \pm 2\sqrt2}{2} = 2 \pm \sqrt2$.
* **Krok 2 — współczynniki** (tu $g'(x) = 2x - 4 = 2\left(x - 2\right)$):

  $$
  A = \frac{8}{2\left(\left(2 + \sqrt2\right) - 2\right)} = \frac{8}{2\sqrt2} = 2\sqrt2, \qquad
  B = \frac{8}{2\left(\left(2 - \sqrt2\right) - 2\right)} = \frac{8}{-2\sqrt2} = -2\sqrt2
  $$

* **Rozkład:**

  $$
  \boxed{\frac{8}{x^2 - 4x + 2}
  = \frac{2\sqrt2}{x - 2 - \sqrt2} - \frac{2\sqrt2}{x - 2 + \sqrt2}}
  $$

* **Sprawdzenie.** Dla $x = 0$: lewa strona $= 4$; prawa strona
  $= \frac{2\sqrt2}{-\left(2 + \sqrt2\right)} + \frac{2\sqrt2}{2 - \sqrt2} = \left(2 - 2\sqrt2\right) + \left(2 + 2\sqrt2\right) = 4$.

### 5.3

* **Dane:** $\dfrac{x^2 - 3x + 6}{x^4 - 5x^2 + 4}$.
* **Krok 1 — rozkład mianownika:**

  $$x^4 - 5x^2 + 4 = \left(x^2 - 1\right)\left(x^2 - 4\right) = (x - 1)(x + 1)(x - 2)(x + 2)$$

  Cztery pierwiastki jednokrotne: $-2$, $-1$, $1$, $2$.
* **Krok 2 — współczynniki ze wzoru $A_i = \frac{f(a_i)}{g'(a_i)}$, gdzie
  $g'(x) = 4x^3 - 10x$:**

  $$
  A_1 = \frac{f(1)}{g'(1)} = \frac{4}{-6} = -\frac23, \qquad
  A_2 = \frac{f(-1)}{g'(-1)} = \frac{10}{6} = \frac53,
  $$

  $$
  A_3 = \frac{f(2)}{g'(2)} = \frac{4}{12} = \frac13, \qquad
  A_4 = \frac{f(-2)}{g'(-2)} = \frac{16}{-12} = -\frac43
  $$

* **Rozkład:**

  $$
  \boxed{\frac{x^2 - 3x + 6}{x^4 - 5x^2 + 4}
  = -\frac{2}{3(x - 1)} + \frac{5}{3(x + 1)} + \frac{1}{3(x - 2)} - \frac{4}{3(x + 2)}}
  $$

* **Sprawdzenie.** Dla $x = 0$: lewa strona $= \frac{6}{4} = \frac32$; prawa strona
  $= \frac23 + \frac53 - \frac16 - \frac23 = \frac{10}{6} - \frac{1}{6} = \frac32$.

### 5.4

* **Dane:** $\dfrac{2x^3 + 5x^2 + 3x + 1}{x^2\left(x^2 + 1\right)^2}$; stopień licznika $3$ <
  stopień mianownika $6$.
* **Krok 1 — postać rozkładu** ($x^2 + 1$ jest nierozkładalny nad $\mathbb{R}$):

  $$
  \frac{2x^3 + 5x^2 + 3x + 1}{x^2\left(x^2 + 1\right)^2}
  = \frac{A}{x} + \frac{B}{x^2} + \frac{Cx + D}{x^2 + 1} + \frac{Ex + F}{\left(x^2 + 1\right)^2}
  $$

* **Krok 2 — mnożenie przez mianownik:**

  $$
  2x^3 + 5x^2 + 3x + 1 = Ax\left(x^2 + 1\right)^2 + B\left(x^2 + 1\right)^2
  + (Cx + D)x^2\left(x^2 + 1\right) + (Ex + F)x^2
  $$

  Po rozwinięciu prawej strony i porównaniu współczynników:

  $$
  \begin{aligned}
  x^5:&\quad A + C = 0 \\
  x^4:&\quad B + D = 0 \\
  x^3:&\quad 2A + C + E = 2 \\
  x^2:&\quad 2B + D + F = 5 \\
  x^1:&\quad A = 3 \\
  x^0:&\quad B = 1
  \end{aligned}
  $$

  Rozwiązanie układu: $A = 3$, $B = 1$, $C = -3$, $D = -1$,
  $E = 2 - 2A - C = -1$, $F = 5 - 2B - D = 4$.

* **Rozkład:**

  $$
  \boxed{\frac{2x^3 + 5x^2 + 3x + 1}{x^2\left(x^2 + 1\right)^2}
  = \frac{3}{x} + \frac{1}{x^2} - \frac{3x + 1}{x^2 + 1} - \frac{x - 4}{\left(x^2 + 1\right)^2}}
  $$

* **Sprawdzenie.** Dla $x = 1$: lewa strona $= \frac{11}{4}$; prawa strona
  $= 3 + 1 - \frac{4}{2} - \frac{-3}{4} = 4 - 2 + \frac34 = \frac{11}{4}$.

---

## Zadanie 6

Podajemy ogólną postać rozkładu na ułamki proste nad $\mathbb{C}$, bez wyznaczania współczynników.
Nad ciałem $\mathbb{C}$ każdy wielomian rozkłada się na czynniki liniowe: każdemu czynnikowi
$(z - z_0)^m$ odpowiada suma $\frac{A_1}{z - z_0} + \ldots + \frac{A_m}{(z - z_0)^m}$,
gdzie $A_i \in \mathbb{C}$.

### 6.1

* **Dane:** $\dfrac{4z + 3j}{z^2 - 2jz + 3}$; stopień licznika $1$ < stopień mianownika $2$.
* **Krok 1 — pierwiastki mianownika:**

  $$
  \Delta = (2j)^2 - 4 \cdot 1 \cdot 3 = -4 - 12 = -16, \qquad \sqrt{\Delta} = 4j, \qquad
  z = \frac{2j \pm 4j}{2} \in \{3j,\ -j\}
  $$

  $$z^2 - 2jz + 3 = (z - 3j)(z + j)$$

* **Ogólna postać rozkładu:**

  $$
  \boxed{\frac{4z + 3j}{z^2 - 2jz + 3} = \frac{A}{z - 3j} + \frac{B}{z + j},
  \qquad A, B \in \mathbb{C}}
  $$

  (wartości $A$, $B$ pozostają do wyznaczenia — zgodnie z poleceniem ich nie liczymy).

### 6.2

* **Dane:** $\dfrac{z^4 + 3z - 2}{z^2\left(z^2 + 9\right)(z + 3j)^2}$.
* **Krok 1 — rozkład mianownika nad $\mathbb{C}$:**

  $$
  z^2 + 9 = (z - 3j)(z + 3j) \quad\Longrightarrow\quad
  z^2\left(z^2 + 9\right)(z + 3j)^2 = z^2(z - 3j)(z + 3j)^3
  $$

  Pierwiastki mianownika: $z = 0$ (krotność $2$), $z = 3j$ (krotność $1$), $z = -3j$
  (krotność $3$). Stopień mianownika $2 + 1 + 3 = 6$, stopień licznika $4 < 6$, brak części
  wielomianowej.

* **Ogólna postać rozkładu:**

  $$
  \boxed{\frac{z^4 + 3z - 2}{z^2\left(z^2 + 9\right)(z + 3j)^2}
  = \frac{A}{z} + \frac{B}{z^2} + \frac{C}{z - 3j} + \frac{D}{z + 3j}
  + \frac{E}{(z + 3j)^2} + \frac{F}{(z + 3j)^3}}
  $$

  gdzie $A, B, C, D, E, F \in \mathbb{C}$.

### 6.3

* **Dane:** $\dfrac{z^7 + z^2}{\left(z^4 + 4\right)^2}$; stopień licznika $7$ < stopień mianownika
  $8$, brak części wielomianowej.
* **Krok 1 — pierwiastki $z^4 + 4$ nad $\mathbb{C}$.** Rozwiązujemy równanie

  $$
  z^4 = -4 = 4\left(\cos\pi + j\sin\pi\right)
  $$

  Cztery pierwiastki mają moduł $\sqrt2$ oraz kąty $\frac{\pi}{4} + \frac{k\pi}{2}$:

  $$
  z_k = \sqrt2\left(\cos\left(\frac{\pi}{4} + \frac{k\pi}{2}\right)
  + j\sin\left(\frac{\pi}{4} + \frac{k\pi}{2}\right)\right), \qquad k = 0, 1, 2, 3
  $$

  czyli $z \in \left\{1 + j,\ -1 + j,\ -1 - j,\ 1 - j\right\}$ i każdy pierwiastek ma krotność $2$:

  $$\left(z^4 + 4\right)^2 = (z - 1 - j)^2(z + 1 - j)^2(z + 1 + j)^2(z - 1 + j)^2$$

* **Ogólna postać rozkładu:**

  $$
  \boxed{\frac{z^7 + z^2}{\left(z^4 + 4\right)^2}
  = \frac{A}{z - 1 - j} + \frac{B}{(z - 1 - j)^2} + \frac{C}{z + 1 - j} + \frac{D}{(z + 1 - j)^2}
  + \frac{E}{z + 1 + j} + \frac{F}{(z + 1 + j)^2} + \frac{G}{z - 1 + j} + \frac{H}{(z - 1 + j)^2}}
  $$

  gdzie $A, B, C, D, E, F, G, H \in \mathbb{C}$.

---

## Zadanie 7

Korzystamy ze wskazówki: jeżeli $g(z) = \left(z - z_1\right) \cdot \ldots \cdot \left(z - z_n\right)$,
gdzie $z_1, \ldots, z_n$ są różnymi liczbami zespolonymi, to współczynniki rozkładu

$$\frac{f(z)}{g(z)} = \frac{a_1}{z - z_1} + \ldots + \frac{a_n}{z - z_n}$$

wyrażają się wzorami $a_i = \frac{f(z_i)}{g'(z_i)}$ dla $i = 1, \ldots, n$.

### 7.1

* **Dane:** $f(z) = 4z^2 + 1$, $g(z) = z^4 - 1$; pierwiastki: $z_1 = 1$, $z_2 = j$, $z_3 = -1$,
  $z_4 = -j$ (wszystkie jednokrotne, bo $g'(z) = 4z^3$ nie ma wspólnych pierwiastków z $g$).
* **Krok 1 — wartości $g'(z_i) = 4z_i^3$:**

  $$g'(1) = 4, \qquad g'(j) = 4j^3 = -4j, \qquad g'(-1) = -4, \qquad g'(-j) = 4(-j)^3 = 4j$$

* **Krok 2 — współczynniki $a_i = \frac{f(z_i)}{g'(z_i)}$:**

  $$
  a_1 = \frac{4 \cdot 1^2 + 1}{4} = \frac54, \qquad
  a_2 = \frac{4j^2 + 1}{-4j} = \frac{-3}{-4j} = \frac{3}{4j} = -\frac34 j,
  $$

  $$
  a_3 = \frac{4(-1)^2 + 1}{-4} = -\frac54, \qquad
  a_4 = \frac{4(-j)^2 + 1}{4j} = \frac{-3}{4j} = \frac34 j
  $$

  Przy przekształceniach użyto $\frac{1}{j} = -j$: na przykład
  $\frac{3}{4j} = \frac{3}{4j} \cdot \frac{-j}{-j} = -\frac34 j$.

* **Rozkład:**

  $$
  \boxed{\frac{4z^2 + 1}{z^4 - 1}
  = \frac{5}{4(z - 1)} - \frac{3j}{4(z - j)} - \frac{5}{4(z + 1)} + \frac{3j}{4(z + j)}}
  $$

* **Sprawdzenie.** Dla $z = 2$: lewa strona $= \frac{17}{15} \approx 1{,}1333$;
  prawa strona:

  $$
  \frac{5}{4} + \frac{-3j}{4(2 - j)} - \frac{5}{12} + \frac{3j}{4(2 + j)}
  = \frac54 - \frac{5}{12} + \frac{-3j(2 + j) + 3j(2 - j)}{20}
  = \frac{10}{12} + \frac{6}{20} = \frac{17}{15}
  $$

  Dodatkowo suma współczynników $\sum a_i = \frac54 - \frac{3j}{4} - \frac54 + \frac{3j}{4} = 0$,
  co jest zgodne z tym, że $\frac{f(z)}{g(z)} \sim \frac{4}{z^2}$ przy $z \to \infty$.

### 7.2

* **Dane:** $f(z) = z^{2020}$, $g(z) = z^{2021} + 1$; stopień licznika $2020$ < stopień mianownika
  $2021$, brak części wielomianowej.
* **Krok 1 — pierwiastki mianownika.** Są to pierwiastki $2021$. stopnia z liczby $-1$:

  $$z_k = \cos\frac{(2k + 1)\pi}{2021} + j\sin\frac{(2k + 1)\pi}{2021}, \qquad k = 0, 1, \ldots, 2020$$

  Wszystkie są jednokrotne: $g'(z) = 2021z^{2020}$ oraz $g'(z_k) = 2021z_k^{2020} \ne 0$,
  bo $\lvert z_k\rvert = 1$; ponadto $z_k \ne 0$.
* **Krok 2 — współczynniki ze wzoru $a_k = \frac{f(z_k)}{g'(z_k)}$:**

  $$a_k = \frac{z_k^{2020}}{2021z_k^{2020}} = \frac{1}{2021}, \qquad k = 0, 1, \ldots, 2020$$

  Wszystkie współczynniki są więc jednakowe.
* **Rozkład:**

  $$
  \boxed{\frac{z^{2020}}{z^{2021} + 1} = \frac{1}{2021}\sum_{k=0}^{2020}
  \frac{1}{z - z_k}, \qquad
  z_k = \cos\frac{(2k + 1)\pi}{2021} + j\sin\frac{(2k + 1)\pi}{2021}}
  $$

* **Sprawdzenie.** Suma współczynników $\sum_{k=0}^{2020} a_k = \frac{2021}{2021} = 1$, co jest
  zgodne z zachowaniem funkcji przy $z \to \infty$: $\frac{z^{2020}}{z^{2021} + 1} \sim \frac{1}{z}$.
  Dla $k = 0$ kontrola bezpośrednia: $z_0 = \cos\frac{\pi}{2021} + j\sin\frac{\pi}{2021}$ oraz
  $z_0^{2021} = \cos\pi + j\sin\pi = -1$, czyli $z_0$ jest pierwiastkiem mianownika i $z_0 \ne 0$.

---

## Podsumowanie wyników

| Podpunkt | Wynik |
| :--- | :--- |
| 1.1 | $w(z) = z^2\left(z^5 + 1\right)^2\left(z^5 - 1\right)$; $11$ różnych pierwiastków: $0$ (krotność $2$), $\zeta_k = \cos\frac{k\pi}{5} + j\sin\frac{k\pi}{5}$ (krotność $1$ dla $k$ parzystych, $2$ dla $k$ nieparzystych); rzeczywiste: $-1, 0, 1$ ($3$); nierzeczywiste: $8$ |
| 1.2 | $w(z) = z^3\left(z^3 + 2\right)^2$; $4$ różne pierwiastki: $0$ (krotność $3$), $\sqrt[3]{2}\left(\cos\frac{\pi}{3} + j\sin\frac{\pi}{3}\right)$, $-\sqrt[3]{2}$, $\sqrt[3]{2}\left(\cos\frac{5\pi}{3} + j\sin\frac{5\pi}{3}\right)$ (krotność $2$ każdy); rzeczywiste: $0, -\sqrt[3]{2}$ ($2$); nierzeczywiste: $2$ |
| 1.3 | $w(z) = z\left(z^6 - j\right)$; $7$ różnych pierwiastków jednokrotnych: $0$ oraz $\cos\left(\frac{\pi}{12} + \frac{k\pi}{3}\right) + j\sin\left(\frac{\pi}{12} + \frac{k\pi}{3}\right)$, $k = 0, \ldots, 5$; rzeczywiste: $0$ ($1$); nierzeczywiste: $6$ |
| 2 | Pozostałe pierwiastki: $1 - 2j$, $-2 + j$, $-2 - j$ |
| 3.1 | $w(z) = \left(z - 1 - 2j\right)\left(z + 1 + 2j\right)\left(z - 1 + 2j\right)\left(z + 1 - 2j\right)$ |
| 3.2 | $w(z) = \left(z - 3 - 2j\right)\left(z + 3 + 2j\right)\left(z + 2 - 3j\right)\left(z - 2 + 3j\right)$ |
| 3.3 | $w(z) = (1 + j\sqrt3)\left(z - \frac{\sqrt6}{2} - \frac{\sqrt2}{2}j\right)\left(z + \frac{\sqrt2}{2} - \frac{\sqrt6}{2}j\right)\left(z + \frac{\sqrt6}{2} + \frac{\sqrt2}{2}j\right)\left(z - \frac{\sqrt2}{2} + \frac{\sqrt6}{2}j\right)$ |
| 4.1 | $\frac{A}{x - 3} + \frac{B}{(x - 3)^2} + \frac{C}{(x - 3)^3} + \frac{Dx + E}{x^2 + 4} + \frac{Fx + G}{(x^2 + 4)^2}$ |
| 4.2 | $3 + \frac{A}{x - 1} + \frac{B}{(x - 1)^2} + \frac{C}{(x - 1)^3} + \frac{D}{x + 1}$, bo $x^4 - 2x^3 + 2x - 1 = (x - 1)^3(x + 1)$ |
| 4.3 | $\frac{Ax + B}{x^2 - 2x + 2} + \frac{Cx + D}{(x^2 - 2x + 2)^2} + \frac{Ex + F}{x^2 + 2x + 2} + \frac{Gx + H}{(x^2 + 2x + 2)^2}$, bo $x^4 + 4 = (x^2 - 2x + 2)(x^2 + 2x + 2)$ |
| 5.1 | $\frac{-3}{x - 1} + \frac{2}{x - 2} + \frac{1}{x - 3}$ |
| 5.2 | $\frac{2\sqrt2}{x - 2 - \sqrt2} - \frac{2\sqrt2}{x - 2 + \sqrt2}$ |
| 5.3 | $-\frac{2}{3(x - 1)} + \frac{5}{3(x + 1)} + \frac{1}{3(x - 2)} - \frac{4}{3(x + 2)}$ |
| 5.4 | $\frac{3}{x} + \frac{1}{x^2} - \frac{3x + 1}{x^2 + 1} - \frac{x - 4}{(x^2 + 1)^2}$ |
| 6.1 | $\frac{A}{z - 3j} + \frac{B}{z + j}$, $A, B \in \mathbb{C}$ |
| 6.2 | $\frac{A}{z} + \frac{B}{z^2} + \frac{C}{z - 3j} + \frac{D}{z + 3j} + \frac{E}{(z + 3j)^2} + \frac{F}{(z + 3j)^3}$, współczynniki zespolone |
| 6.3 | ośmiowyrazowa suma nad biegunami $1 + j$, $-1 + j$, $-1 - j$, $1 - j$ (po dwa wyrażenia na biegun), współczynniki zespolone |
| 7.1 | $\frac{5}{4(z - 1)} - \frac{3j}{4(z - j)} - \frac{5}{4(z + 1)} + \frac{3j}{4(z + j)}$ |
| 7.2 | $\frac{1}{2021}\sum_{k=0}^{2020} \frac{1}{z - z_k}$, gdzie $z_k = \cos\frac{(2k + 1)\pi}{2021} + j\sin\frac{(2k + 1)\pi}{2021}$ |
