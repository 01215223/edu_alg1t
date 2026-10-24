# Algebra – Zestaw 3 – rozwiązania

> **Założenia i konwencje.** Jednostka urojona: $j$, gdzie $j^2 = -1$. Moduł i sprzężenie liczby
> zespolonej oznaczamy odpowiednio $\lvert z\rvert$ oraz $\overline{z}$, a część rzeczywistą
> i urojoną: $\text{Re}(z)$ oraz $\text{Im } z$. Argument główny przyjmujemy w przedziale
> $(-\pi, \pi]$, natomiast kąty kolejnych pierwiastków z liczby zespolonej podajemy w $[0, 2\pi)$.
> Wszystkie wyniki podajemy w postaci dokładnej.
>
> **Metodyka: podejście obliczeniowe + analiza metody „graficznej”.** Każde zadanie rozwiązujemy
> pełną, systematyczną **metodą obliczeniową** (podstawienia pomocnicze, wyróżnik $\Delta$, wzór
> Moivre'a, algebraiczny układ równań dla pierwiastka zespolonego, dzielenie wielomianów, schemat
> Hornera, metoda współczynników nieoznaczonych i układy równań liniowych, wzór residuowy
> z pochodną $a_i = \frac{f(z_i)}{g'(z_i)}$), opisując wszystkie kroki rachunkowe. Równolegle przy
> każdym podpunkcie oceniamy, **czy metoda „graficzna”** (geometria na płaszczyźnie zespolonej
> Gaussa lub wykres funkcji zmiennej rzeczywistej $y = f(x)$) **nie jest szybsza**, wskazując dokładnie,
> które kroki rysunek skraca do kilku sekund, a gdzie rachunek algebraiczny jest niezastąpiony.
>
> **Uwaga terminologiczna do zadania 1.** Pytanie „Ile jest różnych pierwiastków rzeczywistych?
> Ile zespolonych?” rozstrzygamy w obu używanych konwencjach akademickich: podajemy liczbę różnych
> pierwiastków rzeczywistych ($\in \mathbb{R}$), liczbę różnych pierwiastków nierzeczywistych
> ($\in \mathbb{C} \setminus \mathbb{R}$, potocznie nazywanych „zespolonymi”) oraz łączną liczbę
> różnych pierwiastków w $\mathbb{C}$ (zgodnie z inkluzją $\mathbb{R} \subset \mathbb{C}$).

---

## Zadanie 1

Wyznaczamy pierwiastki wielomianu metodą obliczeniową, określamy ich krotności, zliczamy różne
pierwiastki rzeczywiste i zespolone, zaznaczamy je na płaszczyźnie zespolonej oraz porównujemy
czas rachunku z metodą graficzną.

### 1.1

* **Dane:** $w(z) = z^{17} + z^{12} - z^7 - z^2$, dziedzina: $z \in \mathbb{C}$.
* **Metoda obliczeniowa — przebieg krok po kroku:**
  * **Krok 1 — wyłączenie wspólnego czynnika $z^2$ i podstawienie pomocnicze $t = z^5$:**

    $$
    w(z) = z^2\left(z^{15} + z^{10} - z^5 - 1\right)
    $$

    Dla $t = z^5$ otrzymujemy wielomian trzeciego stopnia $p(t) = t^3 + t^2 - t - 1$. Sprawdzamy
    dzielniki wyrazu wolnego ($\pm 1$): $p(1) = 0$ oraz $p(-1) = 0$, a po rozkładzie:

    $$
    t^3 + t^2 - t - 1 = t^2(t + 1) - (t + 1) = (t + 1)\left(t^2 - 1\right) = (t + 1)^2(t - 1)
    $$

    Po powrocie do zmiennej $z$:

    $$
    w(z) = z^2\left(z^5 + 1\right)^2\left(z^5 - 1\right)
    $$

  * **Krok 2 — obliczenie pierwiastków z czynników i ich krotności ze wzoru Moivre'a:**
    1. Z czynnika $z^2 = 0$ dostajemy $z = 0$ o **krotności $2$**.
    2. Z czynnika $z^5 - 1 = 0$ rozwiązujemy $z^5 = 1 = 1(\cos 0 + j\sin 0)$:

       $$
       u_m = \cos\frac{2m\pi}{5} + j\sin\frac{2m\pi}{5}, \qquad m = 0, 1, 2, 3, 4
       $$

       Każdy z pięciu pierwiastków $u_m$ ma **krotność $1$** (gdyż $\left(z^5 - 1\right)' = 5z^4 \ne 0$
       dla $z \ne 0$, a $u_m^5 = 1 \ne -1$, więc czynnik $z^5 + 1$ się w nich nie zeruje).
    3. Z czynnika $\left(z^5 + 1\right)^2 = 0$ rozwiązujemy $z^5 = -1 = 1(\cos\pi + j\sin\pi)$:

       $$
       v_m = \cos\frac{(2m + 1)\pi}{5} + j\sin\frac{(2m + 1)\pi}{5}, \qquad m = 0, 1, 2, 3, 4
       $$

       Ponieważ $z^5 + 1$ ma pięć różnych pierwiastków jednokrotnych ($\left(z^5 + 1\right)' = 5z^4 \ne 0$),
       podniesienie nawiasu do kwadratu daje każdemu $v_m$ **krotność $2$**.

    Łącząc obie rodziny w jeden zapis ($\zeta_k$ dla $k = 0, 1, \ldots, 9$, gdzie $k = 2m$ daje $u_m$,
    a $k = 2m + 1$ daje $v_m$), mamy:

    $$
    \zeta_k = \cos\frac{k\pi}{5} + j\sin\frac{k\pi}{5}, \qquad k = 0, 1, \ldots, 9
    $$

  * **Krok 3 — obliczeniowe wyprowadzenie dokładnych współrzędnych kartezjańskich:**
    Dla kąta $\alpha = \frac{2\pi}{5}$ zachodzi $3\alpha = 2\pi - 2\alpha$, więc $\cos 3\alpha = \cos 2\alpha$.
    Podstawiając $c = \cos\frac{2\pi}{5}$ do tożsamości $4c^3 - 3c = 2c^2 - 1$, otrzymujemy:

    $$
    4c^3 - 2c^2 - 3c + 1 = (c - 1)\left(4c^2 + 2c - 1\right) = 0
    $$

    Ponieważ $c = \cos\frac{2\pi}{5} \in (0, 1)$, wybieramy dodatni pierwiastek równania kwadratowego
    $4c^2 + 2c - 1 = 0$ ($\Delta = 4 + 16 = 20$):

    $$
    \cos\frac{2\pi}{5} = \frac{-2 + 2\sqrt{5}}{8} = \frac{\sqrt{5} - 1}{4}, \qquad
    \cos\frac{\pi}{5} = -\cos\frac{4\pi}{5} = \frac{\sqrt{5} + 1}{4}
    $$

    Z jedynki trygonometrycznej $\sin\varphi = \sqrt{1 - \cos^2\varphi}$ obliczamy:

    $$
    \sin\frac{\pi}{5} = \sqrt{1 - \frac{6 + 2\sqrt{5}}{16}} = \frac{\sqrt{10 - 2\sqrt{5}}}{4}, \qquad
    \sin\frac{2\pi}{5} = \sqrt{1 - \frac{6 - 2\sqrt{5}}{16}} = \frac{\sqrt{10 + 2\sqrt{5}}}{4}
    $$

    a pozostałe kąty obliczamy ze wzorów redukcyjnych dla II, III i IV ćwiartki.
  * **Krok 4 — obliczeniowe zliczenie pierwiastków rzeczywistych:**
    Pierwiastek $\zeta_k$ jest rzeczywisty wtedy i tylko wtedy, gdy $\sin\frac{k\pi}{5} = 0 \iff 5 \mid k$.
    W zbiorze $\{0, 1, \ldots, 9\}$ warunek spełniają tylko $k = 0$ ($\zeta_0 = 1$) oraz $k = 5$
    ($\zeta_5 = -1$). Doliczając $z = 0$, otrzymujemy $3$ różne pierwiastki rzeczywiste i $10 - 2 = 8$
    nierzeczywistych.

* **Czy metoda „graficzna” będzie szybsza? — TAK (zdecydowanie szybsza przy zliczaniu pierwiastków i określaniu ich położenia, po wstępnym wyłączeniu czynników):**
  * **Jak działa tu metoda graficzna:** znając równania $z = 0$, $z^5 = 1$ oraz $z^5 = -1$, bez
    rozpisywania dziesięciu kątów ze wzoru Moivre'a rysujemy okrąg jednostkowy $\lvert z\rvert = 1$,
    wpisujemy w niego **pięciokąt foremny** z wierzchołkiem w $(1, 0)$ (krotność $1$) oraz **drugi
    pięciokąt foremny** obrócony o $36^\circ$, z wierzchołkiem w $(-1, 0)$ (krotność $2$) — razem
    tworzą one **dziesięciokąt foremny** wraz ze środkiem $(0, 0)$ (krotność $2$).
  * **Co rysunek daje błyskawicznie (w 2 sekundy zamiast rachunków z Kroku 4):** okrąg przecina oś
    $\text{Re}$ wyłącznie w punktach $(-1, 0)$ i $(1, 0)$, do których należą wierzchołki obu
    pięciokątów, a na osi $\text{Re}$ leży jeszcze środek $(0, 0)$. Bez liczenia ani jednego sinusa
    odczytujemy z rysunku: **$3$ różne pierwiastki rzeczywiste** i **$8$ pierwiastków poza osią
    $\text{Re}$** (nierzeczywistych), a także widzimy, że wierzchołki obu pięciokątów się przeplatają
    (żadne dwa się nie pokrywają).
  * **Czego sam rysunek nie zastąpi:** bez rachunku algebraicznego nie otrzymamy dokładnych ułamków
    z $\sqrt{5}$ w tabeli ani krotności algebraicznej $(z^5 + 1)^2$. Najefektywniejsze jest więc
    połączenie krótkiego rozkładu z odczytem geometrycznym na okręgu.

| Pierwiastek | Kąt $\varphi_k$ | Krotność | Współrzędne $(\text{Re}(z), \text{Im } z)$ |
| :--- | :---: | :---: | :--- |
| $z = 0$ | — | $2$ | $(0, 0)$ — początek układu |
| $\zeta_0 = 1$ | $0$ | $1$ | $(1, 0)$ |
| $\zeta_1$ | $\frac{\pi}{5}$ | $2$ | $\left(\frac{\sqrt{5} + 1}{4}, \frac{\sqrt{10 - 2\sqrt{5}}}{4}\right)$ |
| $\zeta_2$ | $\frac{2\pi}{5}$ | $1$ | $\left(\frac{\sqrt{5} - 1}{4}, \frac{\sqrt{10 + 2\sqrt{5}}}{4}\right)$ |
| $\zeta_3$ | $\frac{3\pi}{5}$ | $2$ | $\left(-\frac{\sqrt{5} - 1}{4}, \frac{\sqrt{10 + 2\sqrt{5}}}{4}\right)$ |
| $\zeta_4$ | $\frac{4\pi}{5}$ | $1$ | $\left(-\frac{\sqrt{5} + 1}{4}, \frac{\sqrt{10 - 2\sqrt{5}}}{4}\right)$ |
| $\zeta_5 = -1$ | $\pi$ | $2$ | $(-1, 0)$ |
| $\zeta_6$ | $\frac{6\pi}{5}$ | $1$ | $\left(-\frac{\sqrt{5} + 1}{4}, -\frac{\sqrt{10 - 2\sqrt{5}}}{4}\right)$ |
| $\zeta_7$ | $\frac{7\pi}{5}$ | $2$ | $\left(-\frac{\sqrt{5} - 1}{4}, -\frac{\sqrt{10 + 2\sqrt{5}}}{4}\right)$ |
| $\zeta_8$ | $\frac{8\pi}{5}$ | $1$ | $\left(\frac{\sqrt{5} - 1}{4}, -\frac{\sqrt{10 + 2\sqrt{5}}}{4}\right)$ |
| $\zeta_9$ | $\frac{9\pi}{5}$ | $2$ | $\left(\frac{\sqrt{5} + 1}{4}, -\frac{\sqrt{10 - 2\sqrt{5}}}{4}\right)$ |

  ```text
                         Im
                         ^
              k=3 @      |      o k=2
                   `.    |    .'
           k=4 o     `.  |  .'     @ k=1
                       `.|.'
           k=5 @ --------@-------- o k=0 ---> Re
                       .'|`.       (srodek @: z = 0, kr. 2)
           k=6 o     .'  |  `.     @ k=9
                   .'    |    `.
              k=7 @      |      o k=8
                         |
     o : krotnosc 1  (pieciokat z^5 = 1:  k = 0, 2, 4, 6, 8)
     @ : krotnosc 2  (z = 0 oraz pieciokat z^5 = -1:  k = 1, 3, 5, 7, 9)
  ```

* **Wynik:**

  $$
  \boxed{
  \begin{aligned}
  &z = 0\ (\text{kr. } 2), \quad \zeta_k = \cos\frac{k\pi}{5} + j\sin\frac{k\pi}{5}
  \ \left(\text{kr. } 1 \text{ dla } 2 \mid k;\ \text{kr. } 2 \text{ dla } 2 \nmid k\right); \\
  &\text{różnych rzeczywistych: } 3\ (\{-1, 0, 1\}), \quad
  \text{zespolonych w } \mathbb{C}\text{: } 11\ (\text{w tym nierzeczywistych: } 8)
  \end{aligned}
  }
  $$

* **Sprawdzenie:** suma krotności $2 + 5 \cdot 1 + 5 \cdot 2 = 17 = \deg w$; ponadto
  $w(2) = 131072 + 4096 - 128 - 4 = 135036 = 2^2 \cdot 33^2 \cdot 31$.

---

### 1.2

* **Dane:** $w(z) = z^9 + 4z^6 + 4z^3$, dziedzina: $z \in \mathbb{C}$.
* **Metoda obliczeniowa — przebieg krok po kroku:**
  * **Krok 1 — wyłączenie $z^3$ i podstawienie $t = z^3$:**

    $$
    w(z) = z^3\left(z^6 + 4z^3 + 4\right)
    $$

    Dla równania kwadratowego $t^2 + 4t + 4 = 0$ obliczamy wyróżnik:

    $$
    \Delta = 4^2 - 4 \cdot 1 \cdot 4 = 16 - 16 = 0 \implies t_0 = \frac{-4}{2} = -2\ (\text{pierwiastek dwukrotny})
    $$

    Stąd $w(z) = z^3\left(z^3 + 2\right)^2$.
  * **Krok 2 — obliczenie pierwiastków ze wzoru Moivre'a:**
    1. Równanie $z^3 = 0$ daje $z = 0$.
    2. Równanie $z^3 = -2 = 2(\cos\pi + j\sin\pi)$ daje trzy pierwiastki o module $R = \sqrt[3]{2}$:

       $$
       z_k = \sqrt[3]{2}\left(\cos\frac{\pi + 2k\pi}{3} + j\sin\frac{\pi + 2k\pi}{3}\right),
       \qquad k = 0, 1, 2
       $$

       Podstawiając kolejne wartości $k$:
       * dla $k = 0$: $z_0 = \sqrt[3]{2}\left(\cos\frac{\pi}{3} + j\sin\frac{\pi}{3}\right) = \frac{\sqrt[3]{2}}{2} + j\frac{\sqrt{3}\sqrt[3]{2}}{2}$;
       * dla $k = 1$: $z_1 = \sqrt[3]{2}(\cos\pi + j\sin\pi) = -\sqrt[3]{2}$;
       * dla $k = 2$: $z_2 = \sqrt[3]{2}\left(\cos\frac{5\pi}{3} + j\sin\frac{5\pi}{3}\right) = \frac{\sqrt[3]{2}}{2} - j\frac{\sqrt{3}\sqrt[3]{2}}{2}$.
  * **Krok 3 — rachunkowe potwierdzenie krotności z pochodnych:**

    $$
    w'(z) = 9z^8 + 24z^5 + 12z^2 = 3z^2\left(z^3 + 2\right)\left(3z^3 + 2\right), \qquad
    w''(z) = 24z\left(3z^6 + 5z^3 + 1\right), \qquad
    w'''(0) = 24
    $$

    Dla $z = 0$: $w(0) = w'(0) = w''(0) = 0$ oraz $w'''(0) = 24 \ne 0$ (**krotność $3$**).
    Dla $z_k^3 = -2$: $w(z_k) = w'(z_k) = 0$ oraz $w''(z_k) = 24z_k(12 - 10 + 1) = 72z_k \ne 0$ (**krotność $2$**).

* **Czy metoda „graficzna” będzie szybsza? — TAK na etapie wyznaczania pierwiastków z $z^3 = -2$ i ich liczby:**
  * Zamiast podstawiać $k = 0, 1, 2$ do wzoru Moivre'a, zaznaczamy na ujemnej osi $\text{Re}$ oczywisty
    pierwiastek rzeczywisty $\left(-\sqrt[3]{2}, 0\right)$ i wpisujemy w okrąg o promieniu
    $R = \sqrt[3]{2}$ **trójkąt równoboczny** (obrót o $\pm 120^\circ$, czyli kąty $\pm 60^\circ$
    w I i IV ćwiartce). Z własności trójkąta $30^\circ\text{–}60^\circ\text{–}90^\circ$ od razu
    odczytujemy rzuty na osie: $\left(\frac{1}{2}R, \pm\frac{\sqrt{3}}{2}R\right)$, oraz widzimy
    z rysunku dokładnie $2$ punkty na osi $\text{Re}$ ($0$ i $-\sqrt[3]{2}$) oraz $2$ poza nią.
  * Natomiast gdybyśmy narysowali jedynie rzeczywisty wykres funkcji $y = x^9 + 4x^6 + 4x^3 = x^3(x^3 + 2)^2$,
    zobaczylibyśmy punkt przegięcia w $x = 0$ (kr. $3$) i odbicie wykresu od osi $OX$ w $x = -\sqrt[3]{2}$
    (kr. $2$), **ale wykres rzeczywisty całkowicie ukryłby dwa pierwiastki nierzeczywiste $z_0, z_2$**!
    Szybka jest więc geometria na **płaszczyźnie zespolonej**, a nie wykres funkcji rzeczywistej.

| Pierwiastek | Kąt $\varphi_k$ | Krotność | Współrzędne $(\text{Re}(z), \text{Im } z)$ |
| :--- | :---: | :---: | :--- |
| $z = 0$ | — | $3$ | $(0, 0)$ — początek układu |
| $z_0$ | $\frac{\pi}{3}$ | $2$ | $\left(\frac{\sqrt[3]{2}}{2}, \frac{\sqrt{3}\sqrt[3]{2}}{2}\right)$ |
| $z_1 = -\sqrt[3]{2}$ | $\pi$ | $2$ | $\left(-\sqrt[3]{2}, 0\right)$ |
| $z_2$ | $\frac{5\pi}{3}$ | $2$ | $\left(\frac{\sqrt[3]{2}}{2}, -\frac{\sqrt{3}\sqrt[3]{2}}{2}\right)$ |

  ```text
                         Im
                         ^
                         |          @ z0 (kat pi/3, kr. 2)
                         |        .'
                         |      .'
      z1 @---------------#---------------> Re
   (kat pi, kr. 2)       |`.    (srodek #: z = 0, kr. 3)
                         |  `.
                         |    `.
                         |      ` @ z2 (kat 5pi/3, kr. 2)
                         |
     # : krotnosc 3  (z = 0)
     @ : krotnosc 2  (wierzcholki trojkata rownobocznego na okregu |z| = 2^(1/3))
  ```

* **Wynik:**

  $$
  \boxed{
  \begin{aligned}
  &z = 0\ (\text{kr. } 3), \quad
  z \in \left\{-\sqrt[3]{2},\ \frac{\sqrt[3]{2}}{2}\left(1 + j\sqrt{3}\right),\ \frac{\sqrt[3]{2}}{2}\left(1 - j\sqrt{3}\right)\right\}\ (\text{kr. } 2 \text{ każdy}); \\
  &\text{różnych rzeczywistych: } 2, \quad
  \text{zespolonych w } \mathbb{C}\text{: } 4\ (\text{w tym nierzeczywistych: } 2)
  \end{aligned}
  }
  $$

* **Sprawdzenie:** suma krotności $3 + 3 \cdot 2 = 9 = \deg w$; $w(1) = 1 + 4 + 4 = 9 = 1^3(1 + 2)^2$.

---

### 1.3

* **Dane:** $w(z) = z^7 - jz$, dziedzina: $z \in \mathbb{C}$.
* **Metoda obliczeniowa — przebieg krok po kroku:**
  * **Krok 1 — rozkład i krotności z pochodnej:**

    $$
    w(z) = z\left(z^6 - j\right), \qquad w'(z) = 7z^6 - j
    $$

    Dla $z = 0$ mamy $w'(0) = -j \ne 0$, a dla $z^6 = j$ mamy $w'(z) = 7j - j = 6j \ne 0$, więc
    wszystkie $7$ pierwiastków ma **krotność $1$**.
  * **Krok 2 — obliczenie pierwiastków $z^6 = j$ ze wzoru Moivre'a:**
    Zapisujemy $j = 1\left(\cos\frac{\pi}{2} + j\sin\frac{\pi}{2}\right)$. Sześć pierwiastków ma
    moduł $\sqrt[6]{1} = 1$ oraz argumenty:

    $$
    \varphi_k = \frac{\frac{\pi}{2} + 2k\pi}{6} = \frac{\pi}{12} + \frac{k\pi}{3}
    = \frac{(4k + 1)\pi}{12}, \qquad k = 0, 1, 2, 3, 4, 5
    $$

  * **Krok 3 — obliczenie wartości dokładnych ze wzorów na różnicę i sumę kątów:**
    Korzystając z $\frac{\pi}{12} = \frac{\pi}{3} - \frac{\pi}{4}$ oraz $\frac{5\pi}{12} = \frac{\pi}{6} + \frac{\pi}{4}$:

    $$
    \cos\frac{\pi}{12} = \cos\frac{\pi}{3}\cos\frac{\pi}{4} + \sin\frac{\pi}{3}\sin\frac{\pi}{4}
    = \frac{1}{2}\cdot\frac{\sqrt{2}}{2} + \frac{\sqrt{3}}{2}\cdot\frac{\sqrt{2}}{2}
    = \frac{\sqrt{6} + \sqrt{2}}{4}
    $$

    $$
    \sin\frac{\pi}{12} = \sin\frac{\pi}{3}\cos\frac{\pi}{4} - \cos\frac{\pi}{3}\sin\frac{\pi}{4}
    = \frac{\sqrt{3}}{2}\cdot\frac{\sqrt{2}}{2} - \frac{1}{2}\cdot\frac{\sqrt{2}}{2}
    = \frac{\sqrt{6} - \sqrt{2}}{4}
    $$

    Ze wzorów redukcyjnych ($\cos\frac{5\pi}{12} = \sin\frac{\pi}{12}$, $\sin\frac{5\pi}{12} = \cos\frac{\pi}{12}$,
    a dla $\frac{3\pi}{4}$ wartości $\mp\frac{\sqrt{2}}{2}$) oraz relacji $\cos(\alpha + \pi) = -\cos\alpha$,
    $\sin(\alpha + \pi) = -\sin\alpha$ obliczamy wszystkie sześć punktów $z_0, \ldots, z_5$.
  * **Krok 4 — rachunkowe sprawdzenie liczby pierwiastków rzeczywistych:**
    Warunek $\sin\frac{(4k + 1)\pi}{12} = 0$ wymagałby $12 \mid (4k + 1)$, co jest sprzeczne
    (liczba nieparzysta $4k + 1$ nie dzieli się przez $12$). Zatem żaden z pierwiastków $z_0, \ldots, z_5$
    nie jest rzeczywisty; jedynym pierwiastkiem rzeczywistym jest $z = 0$.

* **Czy metoda „graficzna” będzie szybsza? — TAK do zliczenia pierwiastków rzeczywistych/zespolonych i redukcji obliczeń współrzędnych o 80%:**
  * Zaznaczając na okręgu jednostkowym pierwszy wierzchołek pod kątem $\frac{90^\circ}{6} = 15^\circ$
    i odkładając **sześciokąt foremny** co $60^\circ$ ($15^\circ, 75^\circ, 135^\circ, 195^\circ, 255^\circ, 315^\circ$),
    **w ułamku sekundy widzimy z rysunku**, że żaden wierzchołek nie leży na osi $\text{Re}$ ($0^\circ$
    ani $180^\circ$), więc jedynym pierwiastkiem rzeczywistym jest środek $(0, 0)$, a pozostałe $6$
    jest nierzeczywistych!
  * Co więcej, rysunek natychmiast pokazuje symetrię względem prostej $y = x$ ($z_1$ ma zamienione
    współrzędne względem $z_0$) oraz symetrię środkową względem $(0, 0)$ ($z_3 = -z_0$, $z_4 = -z_1$,
    $z_5 = -z_2$), a wierzchołki $z_2, z_5$ leżą wprost na przekątnej ćwiartek ($135^\circ, 315^\circ$).
    Zamiast liczyć $6$ par funkcji trygonometrycznych, wystarczy obliczyć wyłącznie $z_0$.

| Pierwiastek | Kąt $\varphi_k$ | Krotność | Współrzędne $(\text{Re}(z), \text{Im } z)$ |
| :--- | :---: | :---: | :--- |
| $z = 0$ | — | $1$ | $(0, 0)$ — początek układu |
| $z_0$ | $\frac{\pi}{12}$ | $1$ | $\left(\frac{\sqrt{6} + \sqrt{2}}{4}, \frac{\sqrt{6} - \sqrt{2}}{4}\right)$ |
| $z_1$ | $\frac{5\pi}{12}$ | $1$ | $\left(\frac{\sqrt{6} - \sqrt{2}}{4}, \frac{\sqrt{6} + \sqrt{2}}{4}\right)$ |
| $z_2$ | $\frac{3\pi}{4}$ | $1$ | $\left(-\frac{\sqrt{2}}{2}, \frac{\sqrt{2}}{2}\right)$ |
| $z_3 = -z_0$ | $\frac{13\pi}{12}$ | $1$ | $\left(-\frac{\sqrt{6} + \sqrt{2}}{4}, -\frac{\sqrt{6} - \sqrt{2}}{4}\right)$ |
| $z_4 = -z_1$ | $\frac{17\pi}{12}$ | $1$ | $\left(-\frac{\sqrt{6} - \sqrt{2}}{4}, -\frac{\sqrt{6} + \sqrt{2}}{4}\right)$ |
| $z_5 = -z_2$ | $\frac{7\pi}{4}$ | $1$ | $\left(\frac{\sqrt{2}}{2}, -\frac{\sqrt{2}}{2}\right)$ |

  ```text
                         Im
                         ^
                  z2 o   |   o z1 (75 stopni)
        (135 stopni)  `. | .'
                        `|'        o z0 (15 stopni)
       ------------------o--------'---------> Re
               .--------'|.      (srodek o: z = 0, kr. 1)
       z3 o             ' | `.
   (195 st.)           o  |   o z5 (315 stopni)
                  z4 (255 stopni)

     o : wszystkie 7 pierwiastkow ma krotnosc 1
  ```

* **Wynik:**

  $$
  \boxed{
  \begin{aligned}
  &z = 0 \quad \text{oraz} \quad
  z_k = \cos\left(\frac{\pi}{12} + \frac{k\pi}{3}\right) + j\sin\left(\frac{\pi}{12} + \frac{k\pi}{3}\right)
  \ (k = 0, \ldots, 5), \ \text{wszystkie kr. } 1; \\
  &\text{różnych rzeczywistych: } 1\ (\{0\}), \quad
  \text{zespolonych w } \mathbb{C}\text{: } 7\ (\text{w tym nierzeczywistych: } 6)
  \end{aligned}
  }
  $$

* **Sprawdzenie:** $z_2^6 = \left(-\frac{\sqrt{2}}{2} + j\frac{\sqrt{2}}{2}\right)^6 = (-j)^3 = j$,
  a suma krotności wynosi $1 + 6 \cdot 1 = 7 = \deg w$.

---

## Zadanie 2

* **Dane:** $w(z) = z^4 + 2z^3 + 2z^2 + 10z + 25$ oraz dany pierwiastek $z_0 = 1 + 2j$.
* **Metoda obliczeniowa (sprzężenie + pisemne dzielenie wielomianów + wyróżnik $\Delta$):**
  * **Krok 1 — rachunkowe sprawdzenie $w(z_0) = 0$ i wyznaczenie czynnika kwadratowego:**
    Obliczamy kolejne potęgi $z_0 = 1 + 2j$:

    $$
    z_0^2 = 1 + 4j + 4j^2 = -3 + 4j, \qquad
    z_0^3 = (-3 + 4j)(1 + 2j) = -11 - 2j, \qquad
    z_0^4 = (-11 - 2j)(1 + 2j) = -7 - 24j
    $$

    Podstawiamy do $w(z_0)$:

    $$
    w(1 + 2j) = (-7 - 24j) + 2(-11 - 2j) + 2(-3 + 4j) + 10(1 + 2j) + 25
    = (-7 - 22 - 6 + 10 + 25) + j(-24 - 4 + 8 + 20) = 0
    $$

    Ponieważ wielomian $w$ ma współczynniki rzeczywiste, drugim pierwiastkiem jest sprzężenie
    $z_1 = \overline{z_0} = 1 - 2j$. Wymnażamy odpowiadający tej parze trójmian rzeczywisty:

    $$
    \left(z - (1 + 2j)\right)\left(z - (1 - 2j)\right)
    = (z - 1)^2 - (2j)^2 = z^2 - 2z + 1 + 4 = z^2 - 2z + 5
    $$

  * **Krok 2 — dzielenie wielomianu $w(z)$ przez $z^2 - 2z + 5$ krok po kroku:**
    1. Pierwszy składnik ilorazu: $\frac{z^4}{z^2} = z^2$. Odejmujemy $z^2\left(z^2 - 2z + 5\right) = z^4 - 2z^3 + 5z^2$:

       $$
       \left(z^4 + 2z^3 + 2z^2 + 10z + 25\right) - \left(z^4 - 2z^3 + 5z^2\right)
       = 4z^3 - 3z^2 + 10z + 25
       $$

    2. Drugi składnik ilorazu: $\frac{4z^3}{z^2} = 4z$. Odejmujemy $4z\left(z^2 - 2z + 5\right) = 4z^3 - 8z^2 + 20z$:

       $$
       \left(4z^3 - 3z^2 + 10z + 25\right) - \left(4z^3 - 8z^2 + 20z\right)
       = 5z^2 - 10z + 25
       $$

    3. Trzeci składnik ilorazu: $\frac{5z^2}{z^2} = 5$. Odejmujemy $5\left(z^2 - 2z + 5\right) = 5z^2 - 10z + 25$,
       otrzymując resztę $0$ oraz iloraz $q(z) = z^2 + 4z + 5$.
  * **Krok 3 — obliczenie pierwiastków trójmianu $z^2 + 4z + 5 = 0$ z wyróżnika $\Delta$:**

    $$
    \Delta = 4^2 - 4 \cdot 1 \cdot 5 = 16 - 20 = -4 = (2j)^2
    $$

    $$
    z_{2,3} = \frac{-4 \pm 2j}{2} = -2 \pm j
    $$

* **Czy metoda „graficzna” będzie szybsza? — Wykres rzeczywisty NIE działa wcale, natomiast konstrukcja geometryczna na płaszczyźnie Gaussa JEST szybsza niż dzielenie wielomianów!**
  * **Pułapka wykresu rzeczywistego $y = w(x)$:** dla każdego $x \in \mathbb{R}$ zachodzi
    $w(x) = \left[(x - 1)^2 + 4\right]\left[(x + 2)^2 + 1\right] \ge 4 \cdot 1 = 4 > 0$. Wykres funkcji
    rzeczywistej wisi w całości powyżej osi $OX$ i nie ma ani jednego przecięcia z osią — z wykresu
    rzeczywistego nie odczytamy żadnego pierwiastka!
  * **Szybka metoda geometryczna na płaszczyźnie zespolonej Gaussa:**
    1. Odbijamy punkt $z_0 = (1, 2)$ względem osi $\text{Re}$ i od razu mamy $z_1 = (1, -2)$
       (środek tej pary leży w punkcie $S_1 = (1, 0)$, a jej odległość od początku układu wynosi
       $r_1 = \sqrt{1^2 + 2^2} = \sqrt{5}$).
    2. Środek ciężkości (średnia arytmetyczna) wszystkich czterech pierwiastków leży w punkcie
       $\left(-\frac{a_3}{4}, 0\right) = \left(-\frac{2}{4}, 0\right) = \left(-\frac{1}{2}, 0\right)$.
       Aby średnia środków $S_1 = (1, 0)$ i $S_2 = (x_2, 0)$ dała $-\frac{1}{2}$, środek drugiej
       pary sprzężonej musi leżeć na prostej pionowej $x_2 = -2$!
    3. Ponieważ iloczyn kwadratów odległości par od $(0, 0)$ jest równy wyrazowi wolnemu $a_0 = 25$,
       mamy $r_1^2 \cdot r_2^2 = 25 \implies 5 \cdot r_2^2 = 25 \implies r_2 = \sqrt{5}$ — **wszystkie
       cztery pierwiastki leżą na tym samym okręgu $x^2 + y^2 = 5$**! Przecięcie okręgu
       $x^2 + y^2 = 5$ z pionową prostą $x = -2$ odczytujemy z kratki: $(-2, 1)$ oraz $(-2, -1)$,
       czyli $-2 \pm j$, bez wykonywania pisemnego dzielenia wielomianów!

* **Wynik:**

  $$
  \boxed{\text{Pozostałe pierwiastki: } z_1 = 1 - 2j, \quad z_2 = -2 + j, \quad z_3 = -2 - j}
  $$

* **Sprawdzenie:** suma pierwiastków $(1 + 2j) + (1 - 2j) + (-2 + j) + (-2 - j) = -2 = -a_3$, iloczyn
  $\left(1^2 + 2^2\right)\left((-2)^2 + 1^2\right) = 5 \cdot 5 = 25 = a_0$.

---

## Zadanie 3

Rozkładamy każdy wielomian na czynniki liniowe metodą obliczeniową i oceniamy przydatność metody graficznej.

### 3.1

* **Dane:** $w(z) = z^4 + 6z^2 + 25$.
* **Metoda obliczeniowa (równanie dwukwadratowe + algebraiczny układ równań na pierwiastek zespolony):**
  * **Krok 1 — podstawienie $t = z^2$ i wyróżnik $\Delta$:**

    $$
    t^2 + 6t + 25 = 0, \qquad \Delta = 6^2 - 4 \cdot 1 \cdot 25 = 36 - 100 = -64 = (8j)^2
    $$

    $$
    t_1 = \frac{-6 + 8j}{2} = -3 + 4j, \qquad t_2 = \frac{-6 - 8j}{2} = -3 - 4j
    $$

  * **Krok 2 — obliczeniowe wyznaczenie pierwiastków z $t_1 = -3 + 4j$:**
    Szukamy $z = x + jy$ ($x, y \in \mathbb{R}$) spełniającego $(x + jy)^2 = -3 + 4j$. Porównując
    część rzeczywistą, część urojoną oraz moduły $\lvert z\rvert^2 = \lvert -3 + 4j\rvert = \sqrt{9 + 16} = 5$,
    zapisujemy układ:

    $$
    \begin{cases}
    x^2 - y^2 = -3 \\
    x^2 + y^2 = 5 \\
    2xy = 4
    \end{cases}
    $$

    Dodając pierwsze dwa równania, mamy $2x^2 = 2 \implies x^2 = 1 \implies x = \pm 1$; odejmując je,
    mamy $2y^2 = 8 \implies y^2 = 4 \implies y = \pm 2$. Z warunku $2xy = 4 > 0$ znaki $x$ oraz $y$
    są zgodne, co daje $z \in \{1 + 2j,\ -1 - 2j\}$.
  * **Krok 3 — pierwiastki z $t_2 = -3 - 4j$:**
    Analogiczny układ z warunkiem $2xy = -4 < 0$ (przeciwne znaki $x$ i $y$) daje $z \in \{1 - 2j,\ -1 + 2j\}$.

* **Czy metoda „graficzna” będzie szybsza? — NIE wyznaczy pierwszego pierwiastka bez rachunku, ALE natychmiast daje trzy pozostałe przez odbicia w osiach!**
  * Wykres rzeczywisty $y = x^4 + 6x^2 + 25 \ge 25$ nie przecina osi $OX$, a na płaszczyźnie zespolonej
    argument liczby $-3 + 4j$ wynosi $\pi - \arctan\frac{4}{3}$ (kąt nietablicowy), więc z samego
    rysunku koła nie odczytamy dokładnie współrzędnych bez rozwiązania układu z Kroku 2.
  * Natomiast po obliczeniu **jednego** punktu $(1, 2)$, rysunek na płaszczyźnie Gaussa natychmiast
    zastępuje Krok 3: z parzystości $w(-z) = w(z)$ i rzeczywistych współczynników pierwiastki tworzą
    **prostokąt symetryczny względem obu osi układu** o wierzchołkach $(\pm 1, \pm 2)$, więc trzy
    pozostałe punkty $(1, -2), (-1, 2), (-1, -2)$ spisujemy w sekundę z odbić lustrzanych.

* **Wynik:**

  $$
  \boxed{w(z) = (z - 1 - 2j)(z + 1 + 2j)(z - 1 + 2j)(z + 1 - 2j)}
  $$

* **Sprawdzenie:** $\left[(z - 1)^2 + 4\right]\left[(z + 1)^2 + 4\right] = \left(z^2 - 2z + 5\right)\left(z^2 + 2z + 5\right) = \left(z^2 + 5\right)^2 - 4z^2 = z^4 + 6z^2 + 25$.

---

### 3.2

* **Dane:** $w(z) = z^4 - (3 + 2j)^4$.
* **Metoda obliczeniowa — przebieg krok po kroku:**
  * **Krok 1 — sprowadzenie równania $w(z) = 0$ do pierwiastków z jedynki:**
    Ponieważ $3 + 2j \ne 0$, dzielimy równanie $z^4 = (3 + 2j)^4$ stronami przez $(3 + 2j)^4$
    i podstawiamy $u = \frac{z}{3 + 2j}$:

    $$
    u^4 = 1 = 1(\cos 0 + j\sin 0) \implies u_k = \cos\frac{2k\pi}{4} + j\sin\frac{2k\pi}{4}
    \in \{1,\ j,\ -1,\ -j\}
    $$

  * **Krok 2 — obliczenie czterech pierwiastków $z_k = (3 + 2j)u_k$:**

    $$
    \begin{aligned}
    z_0 &= (3 + 2j) \cdot 1 = 3 + 2j, \\
    z_1 &= (3 + 2j) \cdot j = 3j + 2j^2 = -2 + 3j, \\
    z_2 &= (3 + 2j) \cdot (-1) = -3 - 2j, \\
    z_3 &= (3 + 2j) \cdot (-j) = -3j - 2j^2 = 2 - 3j
    \end{aligned}
    $$

    *(Gdybyśmy użyli czysto siłowego rachunku: $(3 + 2j)^2 = 5 + 12j$, $(3 + 2j)^4 = -119 + 120j$,
    i dopiero potem rozwiązywali $z^4 = -119 + 120j$ układami równań kwadratowych — rachunek zająłby
    całą stronę zamiast dwóch linijek!)*

* **Czy metoda „graficzna” będzie szybsza? — ZDECYDOWANIE TAK (najszybsza metoda w całym zestawie!):**
  * Z równania $z^4 = (3 + 2j)^4$ znamy od ręki jeden wierzchołek na siatce kratowej: $z_0 = (3, 2)$.
    Cztery pierwiastki czwartego stopnia tworzą zawsze **kwadrat o środku w $(0, 0)$**. Obracając
    wektor $[3, 2]$ na kratce kolejno o $90^\circ$ ($[x, y] \to [-y, x] \to [-x, -y] \to [y, -x]$),
    odczytujemy wprost z rysunku cztery wierzchołki: $(3, 2)$, $(-2, 3)$, $(-3, -2)$, $(2, -3)$ —
    w kilka sekund i bez żadnych rachunków na liczbach zespolonych!

  ```text
                         Im
                         ^
            z1=(-2,3) *  |
                       \ |        * z0=(3,2)
                        \|    . '
       ------------------+------------------> Re
                   . '   |\
       z2=(-3,-2) *      | \
                         |  * z3=(2,-3)
  ```

* **Wynik:**

  $$
  \boxed{w(z) = (z - 3 - 2j)(z + 2 - 3j)(z + 3 + 2j)(z - 2 + 3j)}
  $$

* **Sprawdzenie:** $(z - 3 - 2j)(z + 3 + 2j) = z^2 - (5 + 12j)$ oraz $(z + 2 - 3j)(z - 2 + 3j) = z^2 + (5 + 12j)$,
  a ich iloczyn wynosi $z^4 - (5 + 12j)^2 = z^4 - (3 + 2j)^4$.

---

### 3.3

* **Dane:** $w(z) = \left(1 + j\sqrt{3}\right)z^4 + 8$.
* **Metoda obliczeniowa — przebieg krok po kroku:**
  * **Krok 1 — wyznaczenie $z^4$ przez usunięcie niewymierności/urojoności z mianownika sprzężeniem:**

    $$
    \left(1 + j\sqrt{3}\right)z^4 + 8 = 0 \implies
    z^4 = \frac{-8}{1 + j\sqrt{3}}
    = \frac{-8\left(1 - j\sqrt{3}\right)}{\left(1 + j\sqrt{3}\right)\left(1 - j\sqrt{3}\right)}
    = \frac{-8 + 8\sqrt{3}j}{1 + 3} = -2 + 2\sqrt{3}j
    $$

  * **Krok 2 — postać trygonometryczna liczby $-2 + 2\sqrt{3}j$:**

    $$
    \left\lvert -2 + 2\sqrt{3}j\right\rvert = \sqrt{(-2)^2 + \left(2\sqrt{3}\right)^2} = \sqrt{4 + 12} = 4
    $$

    $$
    \cos\varphi = \frac{-2}{4} = -\frac{1}{2}, \quad
    \sin\varphi = \frac{2\sqrt{3}}{4} = \frac{\sqrt{3}}{2}
    \implies \varphi = \frac{2\pi}{3}
    $$

  * **Krok 3 — obliczenie czterech pierwiastków ze wzoru Moivre'a ($\sqrt[4]{4} = \sqrt{2}$):**

    $$
    z_k = \sqrt{2}\left(\cos\frac{\frac{2\pi}{3} + 2k\pi}{4} + j\sin\frac{\frac{2\pi}{3} + 2k\pi}{4}\right)
    = \sqrt{2}\left(\cos\left(\frac{\pi}{6} + \frac{k\pi}{2}\right) + j\sin\left(\frac{\pi}{6} + \frac{k\pi}{2}\right)\right),
    \qquad k = 0, 1, 2, 3
    $$

    Obliczamy kolejno wartości dla $k = 0, 1, 2, 3$:
    * $k = 0$ ($\frac{\pi}{6}$): $z_0 = \sqrt{2}\left(\frac{\sqrt{3}}{2} + j\frac{1}{2}\right) = \frac{\sqrt{6}}{2} + j\frac{\sqrt{2}}{2}$;
    * $k = 1$ ($\frac{2\pi}{3}$): $z_1 = \sqrt{2}\left(-\frac{1}{2} + j\frac{\sqrt{3}}{2}\right) = -\frac{\sqrt{2}}{2} + j\frac{\sqrt{6}}{2}$;
    * $k = 2$ ($\frac{7\pi}{6}$): $z_2 = \sqrt{2}\left(-\frac{\sqrt{3}}{2} - j\frac{1}{2}\right) = -\frac{\sqrt{6}}{2} - j\frac{\sqrt{2}}{2}$;
    * $k = 3$ ($\frac{5\pi}{3}$): $z_3 = \sqrt{2}\left(\frac{1}{2} - j\frac{\sqrt{3}}{2}\right) = \frac{\sqrt{2}}{2} - j\frac{\sqrt{6}}{2}$.
  * **Krok 4 — uwzględnienie współczynnika wiodącego $a_4 = 1 + j\sqrt{3}$ przed iloczynem czynników liniowych.**

* **Czy metoda „graficzna” będzie szybsza? — TAK przy wyznaczaniu kątów i obrotach kwadratu, ale z ważną pułapką współczynnika wiodącego!**
  * Na płaszczyźnie Gaussa wektor $1 + j\sqrt{3}$ ma długość $2$ i kąt $60^\circ$, a wektor $-8$ ma
    długość $8$ i kąt $180^\circ$. Geometrycznie iloraz ma więc promień $8 / 2 = 4$ i kąt
    $180^\circ - 60^\circ = 120^\circ$ (omijamy Krok 1 i Krok 2!), a pierwiastki czwartego stopnia
    to kwadrat na okręgu $R = \sqrt{2}$ z pierwszym wierzchołkiem pod kątem $120^\circ / 4 = 30^\circ$
    i kolejnymi obróconymi co $90^\circ$ (omijamy trzy z czterech rachunków w Kroku 3!).
  * **Pułapka metody graficznej:** sam rysunek czterech pierwiastków na płaszczyźnie zespolonej **nie
    przechowuje informacji o współczynniku wiodącym $1 + j\sqrt{3}$** — identyczny rysunek ma
    wielomian unormowany $z^4 + 2 - 2\sqrt{3}j$. Czynnik $1 + j\sqrt{3}$ trzeba dopisać z postaci algebraicznej.

* **Wynik:**

  $$
  \boxed{
  w(z) = \left(1 + j\sqrt{3}\right)
  \left(z - \frac{\sqrt{6}}{2} - j\frac{\sqrt{2}}{2}\right)
  \left(z + \frac{\sqrt{2}}{2} - j\frac{\sqrt{6}}{2}\right)
  \left(z + \frac{\sqrt{6}}{2} + j\frac{\sqrt{2}}{2}\right)
  \left(z - \frac{\sqrt{2}}{2} + j\frac{\sqrt{6}}{2}\right)
  }
  $$

* **Sprawdzenie:** $z_0^4 = \left(\frac{\sqrt{6} + j\sqrt{2}}{2}\right)^4 = \left(1 + j\sqrt{3}\right)^2 = -2 + 2\sqrt{3}j$,
  więc $\left(1 + j\sqrt{3}\right)z_0^4 + 8 = -8 + 8 = 0$.

---

## Zadanie 4

Podajemy ogólną postać rozkładu funkcji wymiernej na ułamki proste nad $\mathbb{R}$ metodą obliczeniową
i sprawdzamy, na ile wykres funkcji lub mianownika może ten proces przyspieszyć.

### 4.1

* **Dane:** $\dfrac{2x^2 - 7x}{(x - 3)^3\left(x^2 + 4\right)^2}$, dziedzina: $x \in \mathbb{R} \setminus \{3\}$.
* **Metoda obliczeniowa:**
  * **Krok 1 — porównanie stopni i sprawdzenie skracalności:**
    $\deg L = 2$, $\deg M = 3 + 2 \cdot 2 = 7$. Ponieważ $2 < 7$, ułamek jest właściwy (część
    wielomianowa wynosi $0$). Wartość licznika w $x = 3$ wynosi $2 \cdot 9 - 21 = -3 \ne 0$, a jego
    pierwiastki $x = 0$ i $x = \frac{7}{2}$ nie zerują $x^2 + 4$, więc ułamek jest nieskracalny.
  * **Krok 2 — badanie wyróżnika czynnika kwadratowego:**
    Dla $x^2 + 4$: $\Delta = 0^2 - 4 \cdot 1 \cdot 4 = -16 < 0$ — trójmian nierozkładalny nad $\mathbb{R}$.
  * **Krok 3 — zapis łańcuchów ułamków prostych:**
    Czynnik $(x - 3)^3$ daje $3$ ułamki ze stałymi w licznikach, a $\left(x^2 + 4\right)^2$ daje $2$
    ułamki z dwumianami liniowymi w licznikach.

* **Czy metoda „graficzna” będzie szybsza? — RÓWNIE SZYBKA (wspomaga ocenę nierozkładalności):**
  * Wykres paraboli $y = x^2 + 4$ to parabola $y = x^2$ przesunięta o $4$ jednostki w górę — bez
    liczenia $\Delta$ widzimy z wykresu brak przecięć z osią $OX$ (nierozkładalność nad $\mathbb{R}$),
    a dla funkcji wymiernej asymptotę poziomą $y = 0$ (brak części wielomianowej) i jedyną asymptotę
    pionową $x = 3$. Rachunek zajmuje jednak tyle samo czasu (kilka sekund).

* **Wynik:**

  $$
  \boxed{
  \frac{2x^2 - 7x}{(x - 3)^3\left(x^2 + 4\right)^2}
  = \frac{A}{x - 3} + \frac{B}{(x - 3)^2} + \frac{C}{(x - 3)^3}
  + \frac{Dx + E}{x^2 + 4} + \frac{Fx + G}{\left(x^2 + 4\right)^2},
  \qquad A, B, C, D, E, F, G \in \mathbb{R}
  }
  $$

* **Sprawdzenie:** łączna liczba stałych wynosi $3 + 2 + 2 = 7 = \deg M$.

---

### 4.2

* **Dane:** $\dfrac{3x^4 - 2}{x^4 - 2x^3 + 2x - 1}$, dziedzina: $x \in \mathbb{R} \setminus \{-1, 1\}$.
* **Metoda obliczeniowa (dzielenie wielomianów + trzykrotny schemat Hornera):**
  * **Krok 1 — wydzielenie części wielomianowej (ułamek niewłaściwy, $\deg L = \deg M = 4$):**

    $$
    3x^4 - 2 = 3\left(x^4 - 2x^3 + 2x - 1\right) + \left(6x^3 - 6x + 1\right)
    \implies \frac{3x^4 - 2}{x^4 - 2x^3 + 2x - 1} = 3 + \frac{6x^3 - 6x + 1}{x^4 - 2x^3 + 2x - 1}
    $$

  * **Krok 2 — rozkład mianownika $M(x) = x^4 - 2x^3 + 0x^2 + 2x - 1$ schematem Hornera:**
    Kandydatami na pierwiastki wymierne są dzielniki wyrazu wolnego: $\pm 1$. Ponieważ suma
    współczynników wynosi $1 - 2 + 0 + 2 - 1 = 0$, liczba $x_0 = 1$ jest pierwiastkiem. Dzielimy
    wielokrotnie przez $(x - 1)$ w tabeli Hornera aż do uzyskania niezerowej reszty:

| Wiersz schematu Hornera | $x^4$ | $x^3$ | $x^2$ | $x^1$ | $x^0$ / reszta |
| :--- | :---: | :---: | :---: | :---: | :---: |
| Współczynniki $M(x)$ | $1$ | $-2$ | $0$ | $2$ | $-1$ |
| $1$. dzielenie przez $(x - 1)$, $x_0 = 1$ | $1$ | $-1$ | $-1$ | $1$ | $0$ |
| $2$. dzielenie przez $(x - 1)$, $x_0 = 1$ | $1$ | $0$ | $-1$ | $0$ | — |
| $3$. dzielenie przez $(x - 1)$, $x_0 = 1$ | $1$ | $1$ | $0$ | — | — |

* **Wniosek ze schematu Hornera:** po trzech dzieleniach bez reszty ostatni iloraz ma współczynniki
  $1, 1$, czyli jest równy $x + 1$. Stąd pełny rozkład mianownika to:

  $$
  x^4 - 2x^3 + 2x - 1 = (x - 1)^3(x + 1)
  $$

  Wartości licznika w $x = \pm 1$ wynoszą $3(\pm 1)^4 - 2 = 1 \ne 0$, więc ułamek jest nieskracalny.

* **Czy metoda „graficzna” będzie szybsza? — NIE (ryzyko pomylenia krotności na szkicu!), choć asymptota pozioma od razu daje $3$:**
  * Z wykresu funkcji wymiernej natychmiast widać asymptotę poziomą $y = \lim_{x \to \pm\infty} \frac{3x^4 - 2}{x^4 - \ldots} = 3$
    (część wielomianowa). Na szkicu mianownika $y = M(x)$ widać przecięcie osi $OX$ w $x = -1$
    (pierwiastek nieparzystej krotności, tutaj $1$) oraz punkt przegięcia z poziomą styczną w $x = 1$
    (krotność nieparzysta $\ge 3$). Sam odręczny wykres nie odróżni jednak na oko krotności $3$ od np.
    krotności $5$ przy wielomianach wyższych stopni, podczas gdy tabela Hornera rozstrzyga krotność
    $3$ bezbłędnie w trzech wierszach dodawania.

* **Wynik:**

  $$
  \boxed{
  \frac{3x^4 - 2}{x^4 - 2x^3 + 2x - 1}
  = 3 + \frac{A}{x - 1} + \frac{B}{(x - 1)^2} + \frac{C}{(x - 1)^3} + \frac{D}{x + 1},
  \qquad A, B, C, D \in \mathbb{R}
  }
  $$

  *(W konwencji z nieoznaczoną stałą częścią wielomianową: $A_0 + \frac{A}{x - 1} + \frac{B}{(x - 1)^2} + \frac{C}{(x - 1)^3} + \frac{D}{x + 1}$,
  gdzie $A_0, A, B, C, D \in \mathbb{R}$.)*

* **Sprawdzenie:** liczba stałych w części ułamkowej $3 + 1 = 4 = \deg M$; wymnożenie
  $(x - 1)^3(x + 1) = \left(x^3 - 3x^2 + 3x - 1\right)(x + 1) = x^4 - 2x^3 + 2x - 1$.

---

### 4.3

* **Dane:** $\dfrac{5x^3}{\left(x^4 + 4\right)^2}$, dziedzina: $x \in \mathbb{R}$.
* **Metoda obliczeniowa (pierwiastki zespolone ze wzoru Moivre'a i parowanie sprzężeń — uniwersalny algorytm dla każdego wielomianu nad $\mathbb{R}$):**
  * **Krok 1 — stopnie:** $\deg L = 3 < 8 = \deg M$ (ułamek właściwy, brak części wielomianowej).
  * **Krok 2 — obliczeniowy rozkład $x^4 + 4$ nad $\mathbb{R}$ przez pierwiastki zespolone:**
    Rozwiązujemy $x^4 = -4 = 4(\cos\pi + j\sin\pi)$ ze wzoru Moivre'a:

    $$
    x_k = \sqrt[4]{4}\left(\cos\frac{\pi + 2k\pi}{4} + j\sin\frac{\pi + 2k\pi}{4}\right)
    = \sqrt{2}\left(\pm\frac{\sqrt{2}}{2} \pm j\frac{\sqrt{2}}{2}\right)
    \in \{1 + j,\ 1 - j,\ -1 + j,\ -1 - j\}
    $$

    Łączymy w pary pierwiastki wzajemnie sprzężone, otrzymując dwa nierozkładalne trójmiany rzeczywiste:

    $$
    (x - 1 - j)(x - 1 + j) = (x - 1)^2 + 1 = x^2 - 2x + 2
    $$

    $$
    (x + 1 - j)(x + 1 + j) = (x + 1)^2 + 1 = x^2 + 2x + 2
    $$

    *(Alternatywnie rachunkowo przez dopełnienie Sophie Germain: $x^4 + 4 = (x^2 + 2)^2 - 4x^2 = (x^2 - 2x + 2)(x^2 + 2x + 2)$.)*
    Stąd $\left(x^4 + 4\right)^2 = \left(x^2 - 2x + 2\right)^2\left(x^2 + 2x + 2\right)^2$.

* **Czy metoda „graficzna” będzie szybsza? — Wykres rzeczywisty ZAWODZI (groźna pułapka!), ale płaszczyzna Gaussa przyspiesza Krok 2:**
  * **Pułapka wykresu rzeczywistego:** wykres funkcji $y = x^4 + 4$ wygląda jak spłaszczona parabola
    o wierzchołku $(0, 4)$, leżąca w całości nad osią $OX$ (brak miejsc zerowych). Patrząc wyłącznie
    na wykres w $\mathbb{R}^2$, można błędnie uznać $x^4 + 4$ za nierozkładalny, podczas gdy nad
    $\mathbb{R}$ **żaden wielomian stopnia $> 2$ nie jest nierozkładalny**!
  * **Płaszczyzna zespolona Gaussa:** zaznaczenie czterech pierwiastków równania $z^4 = -4$ na okręgu
    o promieniu $\sqrt{2}$ pod kątami $45^\circ, 135^\circ, 225^\circ, 315^\circ$ od razu daje
    kwadrat $(\pm 1, \pm 1)$ i pionowe pary sprzężone $(1, \pm 1)$ oraz $(-1, \pm 1)$, skąd w pamięci
    spisujemy $(x - 1)^2 + 1$ i $(x + 1)^2 + 1$.

* **Wynik:**

  $$
  \boxed{
  \frac{5x^3}{\left(x^4 + 4\right)^2}
  = \frac{Ax + B}{x^2 - 2x + 2} + \frac{Cx + D}{\left(x^2 - 2x + 2\right)^2}
  + \frac{Ex + F}{x^2 + 2x + 2} + \frac{Gx + H}{\left(x^2 + 2x + 2\right)^2},
  \qquad A, B, C, D, E, F, G, H \in \mathbb{R}
  }
  $$

* **Sprawdzenie:** liczba parametrów wynosi $4 \cdot 2 = 8 = \deg M$.

---

## Zadanie 5

Wyznaczamy dokładne wartości współczynników ułamków prostych nad $\mathbb{R}$ klasyczną **metodą
obliczeniową współczynników nieoznaczonych** (układy równań z porównania współczynników wielomianów
oraz podstawianie pierwiastków mianownika) i oceniamy, czy metoda graficzna mogłaby być szybsza.

### 5.1

* **Dane:** $\dfrac{4x - 10}{(x - 1)(x - 2)(x - 3)}$, dziedzina: $x \in \mathbb{R} \setminus \{1, 2, 3\}$.
* **Metoda obliczeniowa (współczynniki nieoznaczone i układ $3$ równań liniowych):**
  * **Krok 1 — zapis rozkładu i sprowadzenie do wspólnego mianownika:**

    $$
    \frac{4x - 10}{(x - 1)(x - 2)(x - 3)} = \frac{A}{x - 1} + \frac{B}{x - 2} + \frac{C}{x - 3}
    $$

    Po pomnożeniu obu stron przez $(x - 1)(x - 2)(x - 3)$ otrzymujemy tożsamość wielomianową:

    $$
    4x - 10 = A(x - 2)(x - 3) + B(x - 1)(x - 3) + C(x - 1)(x - 2)
    $$

  * **Krok 2 — uporządkowanie wyrazów względem potęg $x$ i układ równań:**

    $$
    4x - 10 = (A + B + C)x^2 + (-5A - 4B - 3C)x + (6A + 3B + 2C)
    $$

    Porównując współczynniki przy $x^2, x^1, x^0$ po obu stronach:

    $$
    \begin{cases}
    A + B + C = 0 \\
    -5A - 4B - 3C = 4 \\
    6A + 3B + 2C = -10
    \end{cases}
    $$

  * **Krok 3 — rozwiązanie układu metodą eliminacji:**
    Dodając $3$-krotność równania $(1)$ do równania $(2)$, eliminujemy $C$:
    $-2A - B = 4 \implies B = -2A - 4$. Z równania $(1)$ wyznaczamy $C = -A - B = A + 4$.
    Wstawiamy $B$ i $C$ do równania $(3)$:

    $$
    6A + 3(-2A - 4) + 2(A + 4) = -10 \implies 2A - 4 = -10 \implies A = -3
    $$

    Stąd $B = -2(-3) - 4 = 2$ oraz $C = -3 + 4 = 1$.
    *(Wariant szybszy w ramach metody obliczeniowej — podstawienie miejsc zerowych mianownika wprost
    do tożsamości z Kroku 1: dla $x = 1$ mamy $-6 = 2A \implies A = -3$; dla $x = 2$ mamy
    $-2 = -B \implies B = 2$; dla $x = 3$ mamy $2 = 2C \implies C = 1$.)*

* **Czy metoda „graficzna” będzie szybsza? — NIE!**
  * Wykres funkcji $y = \frac{4x - 10}{(x - 1)(x - 2)(x - 3)}$ pokazuje od razu pionowe asymptoty
    $x = 1, 2, 3$ oraz **znaki** współczynników ($A < 0, B > 0, C > 0$, z kierunku ucieczki gałęzi
    do $\pm\infty$ po prawej stronie każdej asymptoty), ale z wykresu nie sposób odczytać dokładnych
    amplitud liczbowych $-3, 2, 1$. Metoda obliczeniowa (zwłaszcza podstawienie $x = 1, 2, 3$) trwa
    kilkanaście sekund i jest bezkonkurencyjna.

* **Wynik:**

  $$
  \boxed{\frac{4x - 10}{(x - 1)(x - 2)(x - 3)} = -\frac{3}{x - 1} + \frac{2}{x - 2} + \frac{1}{x - 3}}
  $$

* **Sprawdzenie:** dla $x = 0$: lewa strona $= \frac{-10}{-6} = \frac{5}{3}$, prawa strona
  $= 3 - 1 - \frac{1}{3} = \frac{5}{3}$.

---

### 5.2

* **Dane:** $\dfrac{8}{x^2 - 4x + 2}$, dziedzina: $x \in \mathbb{R} \setminus \left\{2 - \sqrt{2},\ 2 + \sqrt{2}\right\}$.
* **Metoda obliczeniowa (wyróżnik $\Delta$ + układ $2$ równań liniowych):**
  * **Krok 1 — obliczenie pierwiastków mianownika:**

    $$
    \Delta = (-4)^2 - 4 \cdot 1 \cdot 2 = 16 - 8 = 8, \qquad \sqrt{\Delta} = 2\sqrt{2}
    $$

    $$
    x_1 = \frac{4 + 2\sqrt{2}}{2} = 2 + \sqrt{2}, \qquad
    x_2 = \frac{4 - 2\sqrt{2}}{2} = 2 - \sqrt{2}
    $$

  * **Krok 2 — metoda współczynników nieoznaczonych:**

    $$
    \frac{8}{\left(x - 2 - \sqrt{2}\right)\left(x - 2 + \sqrt{2}\right)}
    = \frac{A}{x - 2 - \sqrt{2}} + \frac{B}{x - 2 + \sqrt{2}}
    $$

    Mnożąc przez wspólny mianownik i porządkując względem $x$:

    $$
    8 = A\left(x - 2 + \sqrt{2}\right) + B\left(x - 2 - \sqrt{2}\right)
    = (A + B)x + \left[\left(-2 + \sqrt{2}\right)A + \left(-2 - \sqrt{2}\right)B\right]
    $$

  * **Krok 3 — rozwiązanie układu równań:**

    $$
    \begin{cases}
    A + B = 0 \implies B = -A \\
    \left(-2 + \sqrt{2}\right)A - \left(-2 - \sqrt{2}\right)A = 8
    \end{cases}
    $$

    Z drugiego równania mamy $2\sqrt{2}\,A = 8 \implies A = \frac{8}{2\sqrt{2}} = 2\sqrt{2}$, a stąd
    $B = -2\sqrt{2}$.

* **Czy metoda „graficzna” będzie szybsza? — ZDECYDOWANIE NIE!**
  * Szkic paraboli $y = (x - 2)^2 - 2$ potwierdza jedynie w sekundę, że wierzchołek $(2, -2)$ leży
    pod osią $OX$, więc istnieją dwa rzeczywiste pierwiastki symetryczne względem $x = 2$. Ponieważ
    jednak zarówno miejsca zerowe $2 \pm \sqrt{2}$, jak i szukane współczynniki $\pm 2\sqrt{2}$ są
    **liczbami niewymiernymi**, żaden odczyt z wykresu nie da dokładnego wyniku — rachunek algebraiczny
    jest jedyną drogą.

* **Wynik:**

  $$
  \boxed{\frac{8}{x^2 - 4x + 2} = \frac{2\sqrt{2}}{x - 2 - \sqrt{2}} - \frac{2\sqrt{2}}{x - 2 + \sqrt{2}}}
  $$

* **Sprawdzenie:** dla $x = 2$: lewa strona $= \frac{8}{-2} = -4$, prawa strona
  $= \frac{2\sqrt{2}}{-\sqrt{2}} - \frac{2\sqrt{2}}{\sqrt{2}} = -2 - 2 = -4$.

---

### 5.3

* **Dane:** $\dfrac{x^2 - 3x + 6}{x^4 - 5x^2 + 4}$, dziedzina: $x \in \mathbb{R} \setminus \{-2, -1, 1, 2\}$.
* **Metoda obliczeniowa (rozkład dwukwadratowy + układ $4$ równań liniowych / metoda podstawiania):**
  * **Krok 1 — rozkład mianownika podstawieniem $t = x^2$:**

    $$
    t^2 - 5t + 4 = 0, \quad \Delta = 25 - 16 = 9 \implies t_1 = 1,\ t_2 = 4
    $$

    $$
    x^4 - 5x^2 + 4 = \left(x^2 - 1\right)\left(x^2 - 4\right) = (x - 1)(x + 1)(x - 2)(x + 2)
    $$

  * **Krok 2 — sprowadzenie rozkładu do wspólnego mianownika:**

    $$
    \frac{x^2 - 3x + 6}{(x - 1)(x + 1)(x - 2)(x + 2)}
    = \frac{A}{x - 1} + \frac{B}{x + 1} + \frac{C}{x - 2} + \frac{D}{x + 2}
    $$

    $$
    \begin{aligned}
    x^2 - 3x + 6 &= A(x + 1)\left(x^2 - 4\right) + B(x - 1)\left(x^2 - 4\right) \\
    &\quad + C\left(x^2 - 1\right)(x + 2) + D\left(x^2 - 1\right)(x - 2)
    \end{aligned}
    $$

  * **Krok 3 — obliczenie współczynników (porównanie obu wariantów rachunkowych):**
    * **Wariant A — układ $4$ równań z porównania potęg $x^3, x^2, x^1, x^0$:**

      $$
      \begin{cases}
      x^3:\quad A + B + C + D = 0 \\
      x^2:\quad A - B + 2C - 2D = 1 \\
      x^1:\quad -4A - 4B - C - D = -3 \\
      x^0:\quad -4A + 4B - 2C + 2D = 6
      \end{cases}
      $$

      Równania $(1)$ i $(3)$ zawierają tylko sumy $S_1 = A + B$ i $S_2 = C + D$:
      $S_1 + S_2 = 0$ oraz $-4S_1 - S_2 = -3 \implies -3S_1 = -3 \implies A + B = 1$ oraz $C + D = -1$.
      Równania $(2)$ i $(4)$ zawierają tylko różnice $R_1 = A - B$ i $R_2 = C - D$:
      $R_1 + 2R_2 = 1$ oraz $-4R_1 - 2R_2 = 6 \implies -3R_1 = 7 \implies A - B = -\frac{7}{3}$ oraz
      $C - D = \frac{5}{3}$. Stąd natychmiast:

      $$
      A = -\frac{2}{3}, \qquad B = \frac{5}{3}, \qquad C = \frac{1}{3}, \qquad D = -\frac{4}{3}
      $$

    * **Wariant B — podstawienie pierwiastków $x \in \{1, -1, 2, -2\}$ do tożsamości z Kroku 2:**
      * $x = 1$: $4 = A \cdot 2 \cdot (-3) = -6A \implies A = -\frac{2}{3}$;
      * $x = -1$: $10 = B \cdot (-2) \cdot (-3) = 6B \implies B = \frac{5}{3}$;
      * $x = 2$: $4 = C \cdot 3 \cdot 4 = 12C \implies C = \frac{1}{3}$;
      * $x = -2$: $16 = D \cdot 3 \cdot (-4) = -12D \implies D = -\frac{4}{3}$.

* **Czy metoda „graficzna” będzie szybsza? — NIE!**
  * Wykres wielomianu $y = x^4 - 5x^2 + 4$ (kształt litery „W” symetryczny względem osi $OY$) pozwala
    wprawdzie dostrzec cztery całkowite przecięcia z osią $OX$ w $\pm 1$ i $\pm 2$, lecz samo
    podstawienie $t = x^2$ robi to w jednej linijce, a ułamkowych współczynników $-\frac{2}{3}, \frac{5}{3}, \frac{1}{3}, -\frac{4}{3}$
    z wykresu nie wyznaczymy. Najszybszy jest tu rachunkowy Wariant B (podstawianie miejsc zerowych).

* **Wynik:**

  $$
  \boxed{
  \frac{x^2 - 3x + 6}{x^4 - 5x^2 + 4}
  = -\frac{2}{3(x - 1)} + \frac{5}{3(x + 1)} + \frac{1}{3(x - 2)} - \frac{4}{3(x + 2)}
  }
  $$

* **Sprawdzenie:** dla $x = 0$: lewa strona $= \frac{6}{4} = \frac{3}{2}$, prawa strona
  $= \frac{2}{3} + \frac{5}{3} - \frac{1}{6} - \frac{2}{3} = \frac{3}{2}$.

---

### 5.4

* **Dane:** $\dfrac{2x^3 + 5x^2 + 3x + 1}{x^2\left(x^2 + 1\right)^2}$, dziedzina: $x \in \mathbb{R} \setminus \{0\}$.
* **Metoda obliczeniowa (współczynniki nieoznaczone i kaskadowy układ $6$ równań liniowych):**
  * **Krok 1 — zapis rozkładu kanonicznego ($\deg L = 3 < 6 = \deg M$, $x^2 + 1$ ma $\Delta = -4 < 0$):**

    $$
    \frac{2x^3 + 5x^2 + 3x + 1}{x^2\left(x^2 + 1\right)^2}
    = \frac{A}{x} + \frac{B}{x^2} + \frac{Cx + D}{x^2 + 1} + \frac{Ex + F}{\left(x^2 + 1\right)^2}
    $$

  * **Krok 2 — mnożenie przez $x^2\left(x^2 + 1\right)^2$ i rozwinięcie potęg:**

    $$
    2x^3 + 5x^2 + 3x + 1
    = Ax\left(x^4 + 2x^2 + 1\right) + B\left(x^4 + 2x^2 + 1\right)
    + (Cx + D)\left(x^4 + x^2\right) + (Ex + F)x^2
    $$

    Po pogrupowaniu wyrazów względem kolejnych potęg $x$:

    $$
    2x^3 + 5x^2 + 3x + 1
    = (A + C)x^5 + (B + D)x^4 + (2A + C + E)x^3 + (2B + D + F)x^2 + Ax + B
    $$

  * **Krok 3 — kaskadowe (trójkątne) rozwiązanie układu $6$ równań bez macierzy odwrotnych:**

    $$
    \begin{cases}
    x^0:\quad B = 1 \\
    x^1:\quad A = 3 \\
    x^5:\quad A + C = 0 \implies C = -A = -3 \\
    x^4:\quad B + D = 0 \implies D = -B = -1 \\
    x^3:\quad 2A + C + E = 2 \implies 6 - 3 + E = 2 \implies E = -1 \\
    x^2:\quad 2B + D + F = 5 \implies 2 - 1 + F = 5 \implies F = 4
    \end{cases}
    $$

* **Czy metoda „graficzna” będzie szybsza? — ZDECYDOWANIE NIE (całkowicie bezradna)!**
  * Na osi rzeczywistej funkcja ma wyłącznie jedną asymptotę pionową $x = 0$ (czynnik $\left(x^2 + 1\right)^2$
    jest zawsze dodatni i gładki, więc nie generuje żadnych cech szczególnych na wykresie pozwalających
    oddzielić $\frac{Cx + D}{x^2 + 1}$ od $\frac{Ex + F}{(x^2 + 1)^2}$, podobnie jak przy $x = 0$
    wykres nie rozdzieli wkładu $\frac{A}{x}$ od silniejszego $\frac{B}{x^2}$). Natomiast układ
    obliczeniowy z Kroku 3 jest z natury **trójkątny** i rozwiązuje się w kilkanaście sekund podstawianiem
    w przód!

* **Wynik:**

  $$
  \boxed{
  \frac{2x^3 + 5x^2 + 3x + 1}{x^2\left(x^2 + 1\right)^2}
  = \frac{3}{x} + \frac{1}{x^2} - \frac{3x + 1}{x^2 + 1} + \frac{-x + 4}{\left(x^2 + 1\right)^2}
  }
  $$

* **Sprawdzenie:** dla $x = 1$: lewa strona $= \frac{11}{4}$, prawa strona
  $= 3 + 1 - \frac{4}{2} + \frac{3}{4} = \frac{11}{4}$; dla $x = -1$: lewa strona $= \frac{1}{4}$,
  prawa strona $= -3 + 1 - \frac{-2}{2} + \frac{5}{4} = \frac{1}{4}$.

---

## Zadanie 6

Podajemy ogólną postać rozkładu funkcji wymiernej na ułamki proste nad $\mathbb{C}$ (bez obliczania
stałych), wyznaczając pierwiastki mianownika metodą obliczeniową i porównując ją z interpretacją
na płaszczyźnie Gaussa.

### 6.1

* **Dane:** $\dfrac{4z + 3j}{z^2 - 2jz + 3}$, stopień licznika $1 < 2 = \deg M$.
* **Metoda obliczeniowa (wyróżnik $\Delta$ trójmianu o współczynnikach zespolonych):**

  $$
  \Delta = (-2j)^2 - 4 \cdot 1 \cdot 3 = 4j^2 - 12 = -4 - 12 = -16 = (4j)^2
  $$

  $$
  z_1 = \frac{2j + 4j}{2} = 3j, \qquad z_2 = \frac{2j - 4j}{2} = -j
  \implies z^2 - 2jz + 3 = (z - 3j)(z + j)
  $$

  Dziedzina: $z \in \mathbb{C} \setminus \{-j, 3j\}$; licznik w $3j$ i $-j$ jest niezerowy ($15j, -j$).

* **Czy metoda „graficzna” będzie szybsza? — NIE!**
  * Funkcja zmiennej zespolonej $\mathbb{C} \to \mathbb{C}$ ma wykres w $\mathbb{R}^4$, więc zwykły
    wykres nie istnieje. Na płaszczyźnie Gaussa równanie $(z - j)^2 = -4 = (2j)^2$ oznacza wprawdzie
    dwa punkty na osi $\text{Im}$ w odległości $2$ w górę i w dół od punktu $j$ (czyli $3j$ oraz $-j$),
    lecz policzenie $\Delta = -16$ zajmuje dosłownie jedną linijkę i jest szybsze od analizy geometrycznej.

* **Wynik:**

  $$
  \boxed{
  \frac{4z + 3j}{z^2 - 2jz + 3} = \frac{A}{z - 3j} + \frac{B}{z + j},
  \qquad A, B \in \mathbb{C}
  }
  $$

* **Sprawdzenie:** $(z - 3j)(z + j) = z^2 - 2jz - 3j^2 = z^2 - 2jz + 3$.

---

### 6.2

* **Dane:** $\dfrac{z^4 + 3z - 2}{z^2\left(z^2 + 9\right)(z + 3j)^2}$.
* **Metoda obliczeniowa:**
  Rozwiązujemy $z^2 + 9 = 0 \implies z^2 = -9 = (3j)^2 \implies z = \pm 3j$, zapisujemy
  $z^2 + 9 = (z - 3j)(z + 3j)$ i **dodajemy wykładniki przy powtarzającym się czynniku $(z + 3j)$**:

  $$
  z^2\left(z^2 + 9\right)(z + 3j)^2 = z^2(z - 3j)(z + 3j)(z + 3j)^2 = z^2(z - 3j)(z + 3j)^3
  $$

  Dziedzina: $z \in \mathbb{C} \setminus \{0, 3j, -3j\}$; $\deg L = 4 < 6 = \deg M$; ułamek
  nieskracalny (wartości licznika: $-2 \ne 0$ dla $z = 0$ oraz $79 \pm 9j \ne 0$ dla $z = \pm 3j$).

* **Czy metoda „graficzna” będzie szybsza? — RÓWNIE SZYBKA, a przy tym świetnie chroni przed błędem krotności:**
  * Naniesienie biegunów z poszczególnych nawiasów na oś urojoną płaszczyzny Gaussa — punkt $(0, 0)$
    (dwukrotnie), punkty $(0, 3)$ i $(0, -3)$ z $z^2 + 9$ oraz ponownie punkt $(0, -3)$ (dwukrotnie)
    z $(z + 3j)^2$ — wizualnie pokazuje **nałożenie się aż trzech biegunów w punkcie $(0, -3)$**,
    eliminując najczęstszy błąd rachunkowy (wypisanie osobnych ułamków dla $z^2 + 9$ i dla $(z + 3j)^2$).

* **Wynik:**

  $$
  \boxed{
  \frac{z^4 + 3z - 2}{z^2\left(z^2 + 9\right)(z + 3j)^2}
  = \frac{A}{z} + \frac{B}{z^2} + \frac{C}{z - 3j} + \frac{D}{z + 3j}
  + \frac{E}{(z + 3j)^2} + \frac{F}{(z + 3j)^3},
  \qquad A, B, C, D, E, F \in \mathbb{C}
  }
  $$

* **Sprawdzenie:** liczba parametrów wynosi $2 + 1 + 3 = 6 = \deg M$.

---

### 6.3

* **Dane:** $\dfrac{z^7 + z^2}{\left(z^4 + 4\right)^2}$, stopień licznika $7 < 8 = \deg M$.
* **Metoda obliczeniowa (wzór Moivre'a dla $z^4 = -4$):**
  Zapisujemy $-4 = 4(\cos\pi + j\sin\pi)$. Cztery pierwiastki równania $z^4 + 4 = 0$ wynoszą:

  $$
  z_k = \sqrt[4]{4}\left(\cos\frac{\pi + 2k\pi}{4} + j\sin\frac{\pi + 2k\pi}{4}\right)
  = \sqrt{2}\left(\cos\left(\frac{\pi}{4} + \frac{k\pi}{2}\right) + j\sin\left(\frac{\pi}{4} + \frac{k\pi}{2}\right)\right),
  \qquad k = 0, 1, 2, 3
  $$

  Podstawiając $k = 0, 1, 2, 3$, otrzymujemy $z_0 = 1 + j$, $z_1 = -1 + j$, $z_2 = -1 - j$, $z_3 = 1 - j$.
  Dziedzina: $z \in \mathbb{C} \setminus \{1 + j, -1 + j, -1 - j, 1 - j\}$. Ułamek jest nieskracalny
  ($\lvert z_k\rvert = \sqrt{2}$, natomiast pierwiastki licznika $z^2\left(z^5 + 1\right)$ mają
  moduł $0$ lub $1$). W $\left(z^4 + 4\right)^2$ każdy z czterech pierwiastków ma krotność $2$.

* **Czy metoda „graficzna” będzie szybsza? — TAK przy wyznaczaniu wszystkich $4$ biegunów!**
  * Na płaszczyźnie Gaussa okrąg o promieniu $R = \sqrt{2}$ przecina dwusieczne czterech ćwiartek
    ($45^\circ, 135^\circ, 225^\circ, 315^\circ$) dokładnie w wierzchołkach kratowych kwadratu
    $(\pm 1, \pm 1)$ (przekątna kwadratu jednostkowego ma długość $\sqrt{2}$). Z rysunku odczytujemy
    więc bieguny $\pm 1 \pm j$ natychmiast, bez czterokrotnego rozpisywania wzoru Moivre'a.

* **Wynik:**

  $$
  \boxed{
  \begin{aligned}
  \frac{z^7 + z^2}{\left(z^4 + 4\right)^2}
  &= \frac{A}{z - 1 - j} + \frac{B}{(z - 1 - j)^2}
  + \frac{C}{z + 1 - j} + \frac{D}{(z + 1 - j)^2} \\
  &\quad + \frac{E}{z + 1 + j} + \frac{F}{(z + 1 + j)^2}
  + \frac{G}{z - 1 + j} + \frac{H}{(z - 1 + j)^2},
  \qquad A, B, C, D, E, F, G, H \in \mathbb{C}
  \end{aligned}
  }
  $$

* **Sprawdzenie:** liczba parametrów wynosi $4 \cdot 2 = 8 = \deg M$.

---

## Zadanie 7

Wyznaczamy dokładny rozkład na ułamki proste nad $\mathbb{C}$ obliczeniowym wzorem z pochodną
$a_i = \frac{f(z_i)}{g'(z_i)}$ dla jednokrotnych pierwiastków mianownika $g(z)$ i analizujemy rolę
geometrii płaszczyzny zespolonej.

### 7.1

* **Dane:** $\dfrac{4z^2 + 1}{z^4 - 1}$, dziedzina: $z \in \mathbb{C} \setminus \{1, -1, j, -j\}$.
* **Metoda obliczeniowa (wzór residuowy $a_i = \frac{f(z_i)}{g'(z_i)}$ krok po kroku):**
  * **Krok 1 — wyznaczenie pierwiastków mianownika $g(z) = z^4 - 1$:**

    $$
    z^4 - 1 = \left(z^2 - 1\right)\left(z^2 + 1\right) = (z - 1)(z + 1)(z - j)(z + j)
    $$

    Pierwiastki są cztery i wszystkie jednokrotne: $z_1 = 1$, $z_2 = -1$, $z_3 = j$, $z_4 = -j$.
  * **Krok 2 — obliczenie pochodnej $g'(z) = 4z^3$ oraz wartości $f(z_i)$ i $g'(z_i)$:**
    Dla $f(z) = 4z^2 + 1$ obliczamy:
    * dla $z_1 = 1$: $f(1) = 4 \cdot 1 + 1 = 5$, $\quad g'(1) = 4 \cdot 1^3 = 4$;
    * dla $z_2 = -1$: $f(-1) = 4 \cdot 1 + 1 = 5$, $\quad g'(-1) = 4 \cdot (-1)^3 = -4$;
    * dla $z_3 = j$: $f(j) = 4j^2 + 1 = -3$, $\quad g'(j) = 4j^3 = -4j$;
    * dla $z_4 = -j$: $f(-j) = 4(-j)^2 + 1 = -3$, $\quad g'(-j) = 4(-j)^3 = 4j$.
  * **Krok 3 — obliczenie ilorazów $a_i = \frac{f(z_i)}{g'(z_i)}$ (z usunięciem $j$ z mianownika):**

    $$
    a_1 = \frac{5}{4}, \qquad
    a_2 = \frac{5}{-4} = -\frac{5}{4}
    $$

    $$
    a_3 = \frac{-3}{-4j} = \frac{3}{4j} = \frac{3 \cdot j}{4j \cdot j} = -\frac{3}{4}j, \qquad
    a_4 = \frac{-3}{4j} = \frac{-3 \cdot j}{4j \cdot j} = \frac{3}{4}j
    $$

* **Czy metoda „graficzna” będzie szybsza? — TAK do odczytu biegunów i relacji symetrii, NIE do obliczenia samych ułamków $\frac{5}{4}$ i $\frac{3}{4}$:**
  * Na płaszczyźnie Gaussa pierwiastki $z^4 = 1$ odczytujemy z rysunku bez rachunków jako przecięcia
    okręgu jednostkowego z osiami: $(1, 0), (-1, 0), (0, 1), (0, -1)$. Symetria środkowa i osiowa
    pokazuje ponadto, że $a_2 = -a_1$ oraz $a_4 = \overline{a_3} = -a_3$, co skraca liczbę potrzebnych
    rachunków z czterech do dwóch ($a_1$ i $a_3$). Same wartości liczbowe $\frac{5}{4}$ oraz $-\frac{3}{4}j$
    wymagają jednak wzoru obliczeniowego $a_i = \frac{f(z_i)}{g'(z_i)}$, który jest tu błyskawiczny.

* **Wynik:**

  $$
  \boxed{
  \frac{4z^2 + 1}{z^4 - 1}
  = \frac{5}{4(z - 1)} - \frac{5}{4(z + 1)} - \frac{3j}{4(z - j)} + \frac{3j}{4(z + j)}
  }
  $$

* **Sprawdzenie:** dla $z = 2$: lewa strona $= \frac{17}{15}$; prawa strona
  $= \frac{5}{4} - \frac{5}{12} + \frac{-3j}{4(2 - j)} + \frac{3j}{4(2 + j)} = \frac{5}{6} + \frac{-6j + 3 - (-6j - 3)}{20} = \frac{5}{6} + \frac{3}{10} = \frac{17}{15}$.

---

### 7.2

* **Dane:** $\dfrac{z^{2020}}{z^{2021} + 1}$, dziedzina: $z \in \mathbb{C} \setminus \{z_0, z_1, \ldots, z_{2020}\}$.
* **Metoda obliczeniowa (wzór Moivre'a + wzór residuowy $a_k = \frac{f(z_k)}{g'(z_k)}$):**
  * **Krok 1 — wyznaczenie wszystkich $2021$ pierwiastków mianownika $g(z) = z^{2021} + 1$:**
    Z równania $z^{2021} = -1 = 1(\cos\pi + j\sin\pi)$ ze wzoru Moivre'a otrzymujemy:

    $$
    z_k = \cos\frac{(2k + 1)\pi}{2021} + j\sin\frac{(2k + 1)\pi}{2021},
    \qquad k = 0, 1, \ldots, 2020
    $$

    Wszystkie $2021$ kątów w $[0, 2\pi)$ jest różnych, więc pierwiastki są jednokrotne, a ponieważ
    $\lvert z_k\rvert = 1$, dla każdego $k$ zachodzi $z_k \ne 0$ (oraz $z_k^{2020} \ne 0$).
  * **Krok 2 — obliczenie pochodnej $g'(z)$ i współczynników $a_k$:**
    Mamy $f(z) = z^{2020}$ oraz $g'(z) = \left(z^{2021} + 1\right)' = 2021z^{2020}$. Podstawiając do
    wzoru $a_k = \frac{f(z_k)}{g'(z_k)}$:

    $$
    a_k = \frac{z_k^{2020}}{2021z_k^{2020}} = \frac{1}{2021}, \qquad k = 0, 1, \ldots, 2020
    $$

* **Czy metoda „graficzna” będzie szybsza? — Fizyczny rysunek $2021$-kąta jest niemożliwy, ALE geometryczna symetria obrotowa daje wynik w pamięci!**
  * Narysowanie $2021$ wierzchołków na kartce i odczytanie z nich czegokolwiek w skali jest
    niewykonalne — dwuwierszowy rachunek analityczny $a_k = \frac{z_k^{2020}}{2021z_k^{2020}} = \frac{1}{2021}$
    jest tu bezkonkurencyjnie prosty.
  * Jednocześnie **rozumowanie geometryczne na płaszczyźnie Gaussa** natychmiast wyjaśnia ten wynik
    bez liczenia pochodnych: $2021$ biegunów tworzy $2021$-kąt foremny na okręgu $\lvert z\rvert = 1$,
    niezmienniczy względem obrotu o kąt $\alpha = \frac{2\pi}{2021}$ ($z \mapsto z_\alpha = z(\cos\alpha + j\sin\alpha)$).
    Przy takim obrocie funkcja przekształca się tak samo przy każdym wierzchołku, więc z symetrii
    wszystkie współczynniki $a_k$ muszą być sobie równe ($a_0 = a_1 = \ldots = a_{2020} = a$), a ponieważ
    dla dużych $\lvert z\rvert$ zachodzi $\frac{z^{2020}}{z^{2021} + 1} \sim \frac{1}{z}$ oraz
    $\sum_{k=0}^{2020}\frac{a}{z - z_k} \sim \frac{2021a}{z}$, w pamięci dostajemy $2021a = 1 \implies a = \frac{1}{2021}$.

* **Wynik:**

  $$
  \boxed{
  \frac{z^{2020}}{z^{2021} + 1}
  = \frac{1}{2021}\sum_{k=0}^{2020}\frac{1}{z - z_k}, \qquad
  \text{gdzie } z_k = \cos\frac{(2k + 1)\pi}{2021} + j\sin\frac{(2k + 1)\pi}{2021}
  }
  $$

* **Sprawdzenie:** suma współczynników $\sum_{k=0}^{2020} a_k = 2021 \cdot \frac{1}{2021} = 1$, a dla
  $z = 0$ prawa strona wynosi $-\frac{1}{2021}\sum_{k=0}^{2020}\overline{z_k} = 0$ (środek ciężkości
  wierzchołków wielokąta foremnego leży w $(0, 0)$), zgodnie z wartością $\frac{0^{2020}}{0^{2021} + 1} = 0$.

---

## Podsumowanie wyników i porównanie: metoda obliczeniowa vs metoda „graficzna”

| Podpunkt | Czy metoda graficzna jest szybsza? | Kiedy pomaga / dlaczego przegrywa | Wynik końcowy |
| :--- | :---: | :--- | :--- |
| **1.1** | **TAK** (po rozkładzie) | Dwa pięciokąty foremne na $\lvert z\rvert = 1$ od razu dają $3$ rzecz. i $8$ nierzecz. bez liczenia sinusów; ułamki z $\sqrt{5}$ wymagają rachunku | $z = 0$ (kr. $2$), $\zeta_k = \cos\frac{k\pi}{5} + j\sin\frac{k\pi}{5}$ (kr. $1$ dla $2 \mid k$, kr. $2$ dla $2 \nmid k$); rzecz.: $3$, w $\mathbb{C}$: $11$ (nierzecz.: $8$) |
| **1.2** | **TAK** (na płaszczyźnie $\mathbb{C}$) | Obrót $-\sqrt[3]{2}$ o $\pm 120^\circ$ od razu daje trójkąt równoboczny; wykres rzeczywisty $y = w(x)$ ukryłby $2$ pierwiastki zespolone | $z = 0$ (kr. $3$), $-\sqrt[3]{2}$ oraz $\frac{\sqrt[3]{2}}{2}\left(1 \pm j\sqrt{3}\right)$ (kr. $2$); rzecz.: $2$, w $\mathbb{C}$: $4$ (nierzecz.: $2$) |
| **1.3** | **TAK** (zliczanie i symetria) | Sześciokąt od $15^\circ$ mija oś $\text{Re}$ (tylko $z = 0$ jest rzecz.) i redukuje $6$ rachunków trygonometrycznych do $1$ | $z = 0$ oraz $\cos\left(\frac{\pi}{12} + \frac{k\pi}{3}\right) + j\sin\left(\frac{\pi}{12} + \frac{k\pi}{3}\right)$ ($k = 0, \ldots, 5$), kr. $1$; rzecz.: $1$, w $\mathbb{C}$: $7$ (nierzecz.: $6$) |
| **2** | **TAK w $\mathbb{C}$ / NIE w $\mathbb{R}$** | Wykres $y = w(x) > 0$ nie przecina $OX$; na płaszczyźnie $\mathbb{C}$ środek ciężkości $-\frac{1}{2}$ i okrąg $\lvert z\rvert = \sqrt{5}$ omijają dzielenie wielomianów | Pozostałe pierwiastki: $1 - 2j$, $-2 + j$, $-2 - j$ |
| **3.1** | **CZĘŚCIOWO** | Kąt $-3 + 4j$ jest nietablicowy (potrzebny układ równań), ale $3$ kolejne pierwiastki daje od razu symetria prostokąta $(\pm 1, \pm 2)$ | $(z - 1 - 2j)(z + 1 + 2j)(z - 1 + 2j)(z + 1 - 2j)$ |
| **3.2** | **ZDECYDOWANIE TAK** | Obrót wektora $[3, 2]$ co $90^\circ$ na kratce daje kwadrat w $3$ sekundy bez potęgowania | $(z - 3 - 2j)(z + 2 - 3j)(z + 3 + 2j)(z - 2 + 3j)$ |
| **3.3** | **TAK** (z uwagą na $a_4$) | Geometria kątów daje $120^\circ / 4 = 30^\circ$ i obroty co $90^\circ$; trzeba pamiętać o współczynniku $1 + j\sqrt{3}$ spoza rysunku | $\left(1 + j\sqrt{3}\right)\left(z - \frac{\sqrt{6}}{2} - j\frac{\sqrt{2}}{2}\right)\left(z + \frac{\sqrt{2}}{2} - j\frac{\sqrt{6}}{2}\right)\left(z + \frac{\sqrt{6}}{2} + j\frac{\sqrt{2}}{2}\right)\left(z - \frac{\sqrt{2}}{2} + j\frac{\sqrt{6}}{2}\right)$ |
| **4.1** | **RÓWNIE SZYBKA** | Parabola $y = x^2 + 4 \ge 4$ potwierdza brak pierwiastków rzeczywistych, asymptota $y = 0$ brak części wielomianowej | $\frac{A}{x - 3} + \frac{B}{(x - 3)^2} + \frac{C}{(x - 3)^3} + \frac{Dx + E}{x^2 + 4} + \frac{Fx + G}{(x^2 + 4)^2}$ |
| **4.2** | **NIE** (Horner pewniejszy) | Asymptota $y = 3$ daje stałą $3$, ale na szkicu łatwo pomylić krotność $3$ w $x = 1$; tabela Hornera jest szybka i ścisła | $3 + \frac{A}{x - 1} + \frac{B}{(x - 1)^2} + \frac{C}{(x - 1)^3} + \frac{D}{x + 1}$ |
| **4.3** | **NIE w $\mathbb{R}$ / TAK w $\mathbb{C}$** | Wykres $y = x^4 + 4 \ge 4$ ukrywa rozkładalność nad $\mathbb{R}$; kwadrat $(\pm 1, \pm 1)$ na płaszczyźnie $\mathbb{C}$ daje pary $(x \mp 1)^2 + 1$ | $\frac{Ax + B}{x^2 - 2x + 2} + \frac{Cx + D}{(x^2 - 2x + 2)^2} + \frac{Ex + F}{x^2 + 2x + 2} + \frac{Gx + H}{(x^2 + 2x + 2)^2}$ |
| **5.1** | **NIE** | Wykres pokazuje tylko asymptoty $x = 1, 2, 3$ i znaki $A, B, C$, ale nie ich wartości $-3, 2, 1$ | $-\frac{3}{x - 1} + \frac{2}{x - 2} + \frac{1}{x - 3}$ |
| **5.2** | **NIE** | Niewymierne bieguny $2 \pm \sqrt{2}$ i współczynniki $\pm 2\sqrt{2}$ są nieodczytywalne z wykresu | $\frac{2\sqrt{2}}{x - 2 - \sqrt{2}} - \frac{2\sqrt{2}}{x - 2 + \sqrt{2}}$ |
| **5.3** | **NIE** | Podstawianie $x = \pm 1, \pm 2$ daje ułamki $-\frac{2}{3}, \frac{5}{3}, \frac{1}{3}, -\frac{4}{3}$ w kilkanaście sekund; wykres nie poda ułamków | $-\frac{2}{3(x - 1)} + \frac{5}{3(x + 1)} + \frac{1}{3(x - 2)} - \frac{4}{3(x + 2)}$ |
| **5.4** | **NIE** | Brak asymptot rzeczywistych dla $(x^2 + 1)^2$; układ trójkątny $6 \times 6$ jest jedyną szybką drogą obliczeniową | $\frac{3}{x} + \frac{1}{x^2} - \frac{3x + 1}{x^2 + 1} + \frac{-x + 4}{(x^2 + 1)^2}$ |
| **6.1** | **NIE** | Policzenie $\Delta = -16$ trwa $5$ sekund; wykres w $\mathbb{R}^2$ nie istnieje | $\frac{A}{z - 3j} + \frac{B}{z + j}$, $A, B \in \mathbb{C}$ |
| **6.2** | **POMOCNICZA** | Zaznaczenie biegunów na osi $\text{Im}$ chroni przed przeoczeniem nałożenia w $-3j$ (krotność $3$) | $\frac{A}{z} + \frac{B}{z^2} + \frac{C}{z - 3j} + \frac{D}{z + 3j} + \frac{E}{(z + 3j)^2} + \frac{F}{(z + 3j)^3}$ |
| **6.3** | **TAK** (dla biegunów) | Okrąg $R = \sqrt{2}$ pod kątami $45^\circ + k\cdot 90^\circ$ od razu daje kratowe punkty $\pm 1 \pm j$ | suma $8$ ułamków prostych krotności $1$ i $2$ nad biegunami $\pm 1 \pm j$ |
| **7.1** | **CZĘŚCIOWO** | Bieguny $\pm 1, \pm j$ i symetrie $a_2 = -a_1$, $a_4 = -a_3$ widać z okręgu, ale $\frac{5}{4}$ i $-\frac{3}{4}j$ liczymy z $\frac{f(z_i)}{g'(z_i)}$ | $\frac{5}{4(z - 1)} - \frac{5}{4(z + 1)} - \frac{3j}{4(z - j)} + \frac{3j}{4(z + j)}$ |
| **7.2** | **NIE rysunkowo / TAK symetrią** | $2021$-kąta nie narysujemy, ale symetria obrotowa i granica w $\infty$ potwierdzają w pamięci wynik $\frac{1}{2021}$ z pochodnej | $\frac{1}{2021}\sum_{k=0}^{2020}\frac{1}{z - z_k}$, $z_k = \cos\frac{(2k + 1)\pi}{2021} + j\sin\frac{(2k + 1)\pi}{2021}$ |
