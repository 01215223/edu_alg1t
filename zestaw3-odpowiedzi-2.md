# Algebra – Zestaw 3 – rozwiązania

> **Założenia i konwencje.** Jednostka urojona: $j$, gdzie $j^2 = -1$. Moduł i sprzężenie liczby
> zespolonej oznaczamy odpowiednio $\lvert z\rvert$ oraz $\overline{z}$, a część rzeczywistą
> i urojoną: $\text{Re}(z)$ oraz $\text{Im } z$. Argument główny przyjmujemy w przedziale
> $(-\pi, \pi]$, natomiast kąty kolejnych pierwiastków z liczby zespolonej wygodnie indeksujemy
> w $[0, 2\pi)$. Wszystkie wyniki podajemy w postaci dokładnej.
>
> **Metodyka rozwiązań.** W całym zestawie stosujemy szybkie, bezrachunkowe metody algebraiczne
> i geometryczne: grupowanie wyrazów i wzory skróconego mnożenia nad $\mathbb{C}$ (z tożsamością
> $a^2 + b^2 = a^2 - (jb)^2$), obrót pierwiastków na okręgu zamiast wielokrotnego liczenia funkcji
> trygonometrycznych, wzory Viète'a zamiast pisemnego dzielenia wielomianów, metodę zakrywania
> Heaviside'a, rozkład teleskopowy, wydzielanie czynników mianownika w liczniku (zamiast układów
> wielu równań) oraz pochodną logarytmiczną.
>
> **Uwaga terminologiczna do zadania 1.** Pytanie „Ile jest różnych pierwiastków rzeczywistych?
> Ile zespolonych?” w praktyce akademickiej bywa rozumiane dwojako:
> 1. **ściśle zbiorowo ($\mathbb{R} \subset \mathbb{C}$):** każda liczba rzeczywista jest zarazem
>    liczbą zespoloną o zerowej części urojonej, więc wszystkie pierwiastki wielomianu są zespolone;
> 2. **potocznie rozłącznie:** przez „zespolone” rozumie się pierwiastki **nierzeczywiste**
>    ($z \in \mathbb{C} \setminus \mathbb{R}$, czyli $\text{Im } z \ne 0$).
>
> W każdym podpunkcie podajemy jawnie obie liczby: liczbę różnych pierwiastków rzeczywistych
> ($\in \mathbb{R}$), liczbę różnych pierwiastków nierzeczywistych ($\in \mathbb{C} \setminus \mathbb{R}$)
> oraz łączną liczbę różnych pierwiastków w $\mathbb{C}$.

---

## Zadanie 1

Wyznaczamy pierwiastki wielomianu, określamy ich krotności, zliczamy różne pierwiastki rzeczywiste
i zespolone oraz podajemy dokładne współrzędne i szkic na płaszczyźnie zespolonej.

### 1.1

* **Dane:** $w(z) = z^{17} + z^{12} - z^7 - z^2$, dziedzina: $z \in \mathbb{C}$.
* **Krok 1 — wyłączenie $z^2$ i błyskawiczne grupowanie par wyrazów (bez podstawień):**

  $$
  w(z) = z^2\left(z^{15} + z^{10} - z^5 - 1\right)
  = z^2\left[z^{10}\left(z^5 + 1\right) - \left(z^5 + 1\right)\right]
  = z^2\left(z^5 + 1\right)\left(z^{10} - 1\right)
  $$

* **Krok 2 — rozbicie $z^{10} - 1 = \left(z^5 - 1\right)\left(z^5 + 1\right)$ i odczyt krotności:**

  $$
  w(z) = z^2\left(z^5 + 1\right)^2\left(z^5 - 1\right)
  $$

  Wielomiany $z^5 - 1$ oraz $z^5 + 1$ mają wyłącznie pierwiastki jednokrotne i nie mają wspólnych
  pierwiastków (gdyż $z^5$ nie może być jednocześnie równe $1$ i $-1$). Z postaci
  $z^2\left(z^{10} - 1\right)\left(z^5 + 1\right)$ natychmiast odczytujemy geometrię całego zbioru:
  * z czynnika $z^2$ otrzymujemy pierwiastek $z = 0$ o **krotności $2$**;
  * czynnik $z^{10} - 1$ daje **wszystkie $10$ pierwiastków $10$. stopnia z jedynki**:

    $$
    \zeta_k = \cos\frac{k\pi}{5} + j\sin\frac{k\pi}{5}, \qquad k = 0, 1, \ldots, 9
    $$

    leżących w wierzchołkach dziesięciokąta foremnego na okręgu jednostkowym $\lvert z\rvert = 1$
    co kąt $\frac{2\pi}{10} = \frac{\pi}{5}$ ($36^\circ$);
  * ponieważ $\zeta_k^5 = \cos(k\pi) + j\sin(k\pi) = (-1)^k$, dla **$k$ parzystych**
    ($k \in \{0, 2, 4, 6, 8\}$) zachodzi $\zeta_k^5 = 1$ (**krotność $1$**), natomiast dla
    **$k$ nieparzystych** ($k \in \{1, 3, 5, 7, 9\}$) zachodzi $\zeta_k^5 = -1$, więc czynnik
    $z^5 + 1$ podnosi ich krotność do **krotności $2$**.

* **Krok 3 — dokładne współrzędne wszystkich wierzchołków z symetrii osiowej:**
  Wystarczą dwie wartości w I ćwiartce: $\cos\frac{\pi}{5} = \frac{\sqrt{5} + 1}{4}$,
  $\sin\frac{\pi}{5} = \frac{\sqrt{10 - 2\sqrt{5}}}{4}$ oraz $\cos\frac{2\pi}{5} = \frac{\sqrt{5} - 1}{4}$,
  $\sin\frac{2\pi}{5} = \frac{\sqrt{10 + 2\sqrt{5}}}{4}$. Pozostałe punkty powstają przez odbicia
  względem osi $\text{Im}$ ($\varphi \mapsto \pi - \varphi$) oraz osi $\text{Re}$
  ($\varphi \mapsto 2\pi - \varphi$).

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

* **Zaznaczenie na płaszczyźnie zespolonej (opis i szkic):**
  Na płaszczyźnie zaznaczamy początek układu $(0, 0)$ (krotność $2$) oraz $10$ wierzchołków
  dziesięciokąta foremnego wpisanego w okrąg o środku $(0, 0)$ i promieniu $R = 1$, rozmieszczonych
  co $36^\circ$ począwszy od punktu $(1, 0)$, na przemian o krotnościach $1$ (symbol `o`)
  i $2$ (symbol `@`):

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
     o : krotnosc 1  (k = 0, 2, 4, 6, 8;  katy 0, 72, 144, 216, 288 stopni)
     @ : krotnosc 2  (z = 0 oraz k = 1, 3, 5, 7, 9;  katy 36, 108, 180, 252, 324 stopni)
  ```

* **Liczba różnych pierwiastków:**
  * różnych pierwiastków **rzeczywistych** ($\in \mathbb{R}$): **$3$**, mianowicie $-1$, $0$, $1$;
  * różnych pierwiastków **nierzeczywistych** ($\in \mathbb{C} \setminus \mathbb{R}$): **$8$**;
  * łącznie różnych pierwiastków **zespolonych** ($\in \mathbb{C}$): **$11$**.

* **Wynik:**

  $$
  \boxed{
  \begin{aligned}
  &z = 0\ (\text{kr. } 2), \quad \zeta_k = \cos\frac{k\pi}{5} + j\sin\frac{k\pi}{5}
  \ \left(\text{kr. } 1 \text{ dla } k \in \{0,2,4,6,8\};\ \text{kr. } 2 \text{ dla } k \in \{1,3,5,7,9\}\right); \\
  &\text{różnych rzeczywistych: } 3\ (\{-1, 0, 1\}), \quad
  \text{zespolonych w } \mathbb{C}\text{: } 11\ (\text{w tym nierzeczywistych: } 8)
  \end{aligned}
  }
  $$

* **Sprawdzenie:** suma krotności wynosi $2 + 5 \cdot 1 + 5 \cdot 2 = 17 = \deg w$. Kontrola
  wartości dla $z = 2$: $w(2) = 2^2\left(2^{15} + 2^{10} - 2^5 - 1\right) = 4(32768 + 1024 - 32 - 1) = 135036$,
  natomiast z rozkładu $2^2 \cdot (32 + 1)^2 \cdot (32 - 1) = 4 \cdot 1089 \cdot 31 = 135036$.

---

### 1.2

* **Dane:** $w(z) = z^9 + 4z^6 + 4z^3$, dziedzina: $z \in \mathbb{C}$.
* **Krok 1 — wyłączenie $z^3$ i wzór skróconego mnożenia $(a + b)^2$ w jednej linijce:**

  $$
  w(z) = z^3\left(z^6 + 4z^3 + 4\right) = z^3\left(z^3 + 2\right)^2
  $$

* **Krok 2 — odczyt pierwiastków przez obrót geometryczny (bez rachunków na kątach):**
  * z czynnika $z^3$ mamy pierwiastek $z = 0$ o **krotności $3$**;
  * czynnik $z^3 + 2$ zeruje się dla $z^3 = -2$. Równanie to ma oczywisty pierwiastek rzeczywisty
    $z_1 = -\sqrt[3]{2}$ (leżący na ujemnej półosi rzeczywistej, kąt $\pi$, promień $R = \sqrt[3]{2}$).
    Pozostałe dwa pierwiastki tworzą z nim trójkąt równoboczny na okręgu $\lvert z\rvert = \sqrt[3]{2}$,
    więc leżą symetrycznie pod kątami $\pi \mp \frac{2\pi}{3} = \pm\frac{\pi}{3}$ (w $[0, 2\pi)$:
    $\frac{\pi}{3}$ oraz $\frac{5\pi}{3}$):

    $$
    z_0 = \sqrt[3]{2}\left(\cos\frac{\pi}{3} + j\sin\frac{\pi}{3}\right)
    = \frac{\sqrt[3]{2}}{2}\left(1 + j\sqrt{3}\right), \qquad
    z_1 = -\sqrt[3]{2}, \qquad
    z_2 = \frac{\sqrt[3]{2}}{2}\left(1 - j\sqrt{3}\right)
    $$

    Ponieważ wielomian $z^3 + 2$ ma trzy różne pierwiastki jednokrotne, a w rozkładzie występuje
    w kwadracie, każdy z pierwiastków $z_0, z_1, z_2$ ma **krotność $2$**.

* **Tabela współrzędnych** (promień okręgu $R = \sqrt[3]{2}$):

| Pierwiastek | Kąt $\varphi$ w $[0, 2\pi)$ | Krotność | Współrzędne $(\text{Re}(z), \text{Im } z)$ |
| :--- | :---: | :---: | :--- |
| $z = 0$ | — | $3$ | $(0, 0)$ — początek układu |
| $z_0 = \frac{\sqrt[3]{2}}{2}\left(1 + j\sqrt{3}\right)$ | $\frac{\pi}{3}$ | $2$ | $\left(\frac{\sqrt[3]{2}}{2}, \frac{\sqrt{3}\sqrt[3]{2}}{2}\right)$ |
| $z_1 = -\sqrt[3]{2}$ | $\pi$ | $2$ | $\left(-\sqrt[3]{2}, 0\right)$ |
| $z_2 = \frac{\sqrt[3]{2}}{2}\left(1 - j\sqrt{3}\right)$ | $\frac{5\pi}{3}$ | $2$ | $\left(\frac{\sqrt[3]{2}}{2}, -\frac{\sqrt{3}\sqrt[3]{2}}{2}\right)$ |

* **Zaznaczenie na płaszczyźnie zespolonej (opis i szkic):**
  Zaznaczamy początek układu $(0, 0)$ (krotność $3$) oraz trzy wierzchołki trójkąta równobocznego
  wpisanego w okrąg o środku $(0, 0)$ i promieniu $R = \sqrt[3]{2}$ pod kątami $60^\circ$,
  $180^\circ$, $300^\circ$ (każdy o krotności $2$):

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

* **Liczba różnych pierwiastków:**
  * różnych pierwiastków **rzeczywistych** ($\in \mathbb{R}$): **$2$**, mianowicie $0$ oraz $-\sqrt[3]{2}$;
  * różnych pierwiastków **nierzeczywistych** ($\in \mathbb{C} \setminus \mathbb{R}$): **$2$**;
  * łącznie różnych pierwiastków **zespolonych** ($\in \mathbb{C}$): **$4$**.

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

* **Sprawdzenie:** suma krotności wynosi $3 + 3 \cdot 2 = 9 = \deg w$. Ponadto
  $\left[\frac{\sqrt[3]{2}}{2}\left(1 \pm j\sqrt{3}\right)\right]^3 = 2\left(\cos(\pm\pi) + j\sin(\pm\pi)\right) = -2$,
  więc wszystkie trzy punkty zerują $z^3 + 2$.

---

### 1.3

* **Dane:** $w(z) = z^7 - jz$, dziedzina: $z \in \mathbb{C}$.
* **Krok 1 — wyłączenie $z$ i rozstrzygnięcie krotności w jednej linijce:**

  $$
  w(z) = z\left(z^6 - j\right)
  $$

  Pochodna wielomianu to $w'(z) = 7z^6 - j$. Dla $z = 0$ mamy $w'(0) = -j \ne 0$, a dla każdego
  rozwiązania równania $z^6 = j$ mamy $w'(z) = 7j - j = 6j \ne 0$. Wszystkie $7$ pierwiastków jest
  zatem **jednokrotnych** (krotność $1$).

* **Krok 2 — pierwiastki równania $z^6 = j$ i szybkie wyznaczenie postaci algebraicznej bez wzorów połówkowych:**
  Ponieważ $j = \cos\frac{\pi}{2} + j\sin\frac{\pi}{2}$ ma moduł $1$, sześć pierwiastków leży
  na okręgu jednostkowym $\lvert z\rvert = 1$ pod kątami rozmieszczonymi co $\frac{2\pi}{6} = \frac{\pi}{3}$ ($60^\circ$):

  $$
  z_k = \cos\left(\frac{\pi}{12} + \frac{k\pi}{3}\right) + j\sin\left(\frac{\pi}{12} + \frac{k\pi}{3}\right),
  \qquad k = 0, 1, 2, 3, 4, 5
  $$

  Zamiast pamięciowych wzorów na $\cos 15^\circ$, zauważamy natychmiast dwa pierwiastki leżące na
  dwusiecznej II i IV ćwiartki: ponieważ $(-j)^3 = -j^3 = j$, równanie $\left(z^2\right)^3 = (-j)^3$
  spełniają liczby o kwadracie równym $-j$, czyli $z_2 = -\frac{\sqrt{2}}{2} + j\frac{\sqrt{2}}{2}$
  (kąt $\frac{3\pi}{4}$) oraz $z_5 = -z_2 = \frac{\sqrt{2}}{2} - j\frac{\sqrt{2}}{2}$
  (kąt $\frac{7\pi}{4}$). Obracając $z_5$ o $+\frac{\pi}{3}$ (mnożenie przez $\frac{1 + j\sqrt{3}}{2}$),
  otrzymujemy $z_0$:

  $$
  z_0 = \frac{\sqrt{2}}{2}(1 - j) \cdot \frac{1 + j\sqrt{3}}{2}
  = \frac{\sqrt{2}}{4}\left[\left(1 + \sqrt{3}\right) + j\left(\sqrt{3} - 1\right)\right]
  = \frac{\sqrt{6} + \sqrt{2}}{4} + j\frac{\sqrt{6} - \sqrt{2}}{4}
  $$

  Punkt $z_1$ (kąt $\frac{5\pi}{12} = \frac{\pi}{2} - \frac{\pi}{12}$) powstaje z $z_0$ przez symetrię
  względem prostej $y = x$ (zamiana części rzeczywistej z urojoną), a punkty $z_3 = -z_0$ oraz
  $z_4 = -z_1$ są symetryczne względem początku układu!

* **Tabela współrzędnych:**

| Pierwiastek | Kąt $\varphi_k$ | Krotność | Współrzędne $(\text{Re}(z), \text{Im } z)$ |
| :--- | :---: | :---: | :--- |
| $z = 0$ | — | $1$ | $(0, 0)$ — początek układu |
| $z_0$ | $\frac{\pi}{12}$ | $1$ | $\left(\frac{\sqrt{6} + \sqrt{2}}{4}, \frac{\sqrt{6} - \sqrt{2}}{4}\right)$ |
| $z_1$ | $\frac{5\pi}{12}$ | $1$ | $\left(\frac{\sqrt{6} - \sqrt{2}}{4}, \frac{\sqrt{6} + \sqrt{2}}{4}\right)$ |
| $z_2$ | $\frac{3\pi}{4}$ | $1$ | $\left(-\frac{\sqrt{2}}{2}, \frac{\sqrt{2}}{2}\right)$ |
| $z_3 = -z_0$ | $\frac{13\pi}{12}$ | $1$ | $\left(-\frac{\sqrt{6} + \sqrt{2}}{4}, -\frac{\sqrt{6} - \sqrt{2}}{4}\right)$ |
| $z_4 = -z_1$ | $\frac{17\pi}{12}$ | $1$ | $\left(-\frac{\sqrt{6} - \sqrt{2}}{4}, -\frac{\sqrt{6} + \sqrt{2}}{4}\right)$ |
| $z_5 = -z_2$ | $\frac{7\pi}{4}$ | $1$ | $\left(\frac{\sqrt{2}}{2}, -\frac{\sqrt{2}}{2}\right)$ |

* **Zaznaczenie na płaszczyźnie zespolonej (opis i szkic):**
  Zaznaczamy początek układu $(0, 0)$ oraz sześć wierzchołków sześciokąta foremnego wpisanego
  w okrąg jednostkowy $\lvert z\rvert = 1$, obróconego o $15^\circ$ ($\frac{\pi}{12}$), czyli pod
  kątami $15^\circ, 75^\circ, 135^\circ, 195^\circ, 255^\circ, 315^\circ$ (wszystkie o krotności $1$):

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

* **Liczba różnych pierwiastków:**
  * różnych pierwiastków **rzeczywistych** ($\in \mathbb{R}$): **$1$**, mianowicie $z = 0$
    (żaden z kątów $\frac{\pi}{12} + \frac{k\pi}{3}$ nie jest wielokrotnością $\pi$, gdyż
    $1 + 4k$ jest nieparzyste i nie dzieli się przez $12$);
  * różnych pierwiastków **nierzeczywistych** ($\in \mathbb{C} \setminus \mathbb{R}$): **$6$**;
  * łącznie różnych pierwiastków **zespolonych** ($\in \mathbb{C}$): **$7$**.

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

* **Sprawdzenie:** suma krotności wynosi $1 + 6 \cdot 1 = 7 = \deg w$. Ponadto
  $z_0^2 = \left(\frac{\sqrt{6} + \sqrt{2}}{4} + j\frac{\sqrt{6} - \sqrt{2}}{4}\right)^2 = \frac{4\sqrt{3}}{8} + j\frac{4}{8} = \frac{\sqrt{3} + j}{2}$,
  skąd $z_0^6 = \left(\frac{\sqrt{3} + j}{2}\right)^3 = \cos\frac{\pi}{2} + j\sin\frac{\pi}{2} = j$.

---

## Zadanie 2

* **Dane:** $w(z) = z^4 + 2z^3 + 2z^2 + 10z + 25$ oraz pierwiastek $z_0 = 1 + 2j$.
* **Metoda szybka (sprzężenie + wzory Viète'a — bez potęgowania $(1 + 2j)^4$ i bez pisemnego dzielenia wielomianów):**
  * **Krok 1 — drugi pierwiastek z pary sprzężonej:**
    Wszystkie współczynniki wielomianu $w$ są rzeczywiste ($1, 2, 2, 10, 25 \in \mathbb{R}$), więc
    wraz z $z_0 = 1 + 2j$ pierwiastkiem jest również jego sprzężenie:

    $$
    z_1 = \overline{z_0} = 1 - 2j
    $$

    Suma i iloczyn tej pary wynoszą od ręki:

    $$
    z_0 + z_1 = 2\text{Re}(z_0) = 2, \qquad
    z_0 z_1 = \lvert z_0\rvert^2 = 1^2 + 2^2 = 5
    $$

  * **Krok 2 — suma i iloczyn pozostałych dwóch pierwiastków $z_2, z_3$ ze wzorów Viète'a dla stopnia $4$:**
    Dla unormowanego wielomianu $z^4 + a_3 z^3 + a_2 z^2 + a_1 z + a_0$ suma wszystkich czterech
    pierwiastków jest równa $-a_3 = -2$, a ich iloczyn jest równy $a_0 = 25$. Stąd:

    $$
    (z_0 + z_1) + (z_2 + z_3) = -2 \implies z_2 + z_3 = -2 - 2 = -4
    $$

    $$
    (z_0 z_1)(z_2 z_3) = 25 \implies z_2 z_3 = \frac{25}{5} = 5
    $$

  * **Krok 3 — równanie kwadratowe dla $z_2, z_3$ przez dopełnienie do kwadratu:**
    Ze wzorów Viète'a liczby $z_2, z_3$ są pierwiastkami trójmianu $z^2 - (z_2 + z_3)z + z_2 z_3 = z^2 + 4z + 5$:

    $$
    z^2 + 4z + 5 = (z + 2)^2 + 1 = (z + 2)^2 - j^2 = 0 \iff z = -2 \pm j
    $$

* **Wynik:**

  $$
  \boxed{\text{Pozostałe pierwiastki: } z_1 = 1 - 2j, \quad z_2 = -2 + j, \quad z_3 = -2 - j}
  $$

* **Sprawdzenie (druga metoda — jednoczesna weryfikacja tożsamości całego wielomianu):**
  Iloczyn obu trójmianów kwadratowych odpowiada grupowaniu przez różnicę kwadratów:

  $$
  \left(z^2 - 2z + 5\right)\left(z^2 + 4z + 5\right)
  = \left[\left(z^2 + z + 5\right) - 3z\right]\left[\left(z^2 + z + 5\right) + 3z\right]
  = \left(z^2 + z + 5\right)^2 - 9z^2
  = z^4 + 2z^3 + 2z^2 + 10z + 25 = w(z)
  $$

  Potwierdza to jednocześnie, że $z_0 = 1 + 2j$ istotnie był pierwiastkiem $w(z)$, a wyznaczona
  czwórka pierwiastków jest kompletna.

---

## Zadanie 3

Rozkładamy każdy wielomian na iloczyn czynników liniowych nad $\mathbb{C}$ (pamiętając o zachowaniu
współczynnika wiodącego przed iloczynem).

### 3.1

* **Dane:** $w(z) = z^4 + 6z^2 + 25$.
* **Metoda szybka (dopełnienie do kwadratu typu Sophie Germain i różnica kwadratów nad $\mathbb{C}$ — bez wyróżnika $\Delta$ i bez pierwiastkowania liczb zespolonych):**
  * **Krok 1 — dopełnienie $z^4 + 25$ do pełnego kwadratu $\left(z^2 + 5\right)^2$:**

    $$
    w(z) = \left(z^4 + 10z^2 + 25\right) - 4z^2 = \left(z^2 + 5\right)^2 - (2z)^2
    = \left(z^2 - 2z + 5\right)\left(z^2 + 2z + 5\right)
    $$

  * **Krok 2 — zamiana sumy kwadratów na różnicę kwadratów dzięki $4 = -(2j)^2$:**

    $$
    z^2 - 2z + 5 = (z - 1)^2 + 4 = (z - 1)^2 - (2j)^2 = (z - 1 - 2j)(z - 1 + 2j)
    $$

    $$
    z^2 + 2z + 5 = (z + 1)^2 + 4 = (z + 1)^2 - (2j)^2 = (z + 1 - 2j)(z + 1 + 2j)
    $$

* **Wynik:**

  $$
  \boxed{w(z) = (z - 1 - 2j)(z - 1 + 2j)(z + 1 - 2j)(z + 1 + 2j)}
  $$

* **Sprawdzenie:** dla $z = 1 + 2j$ mamy $z^2 = -3 + 4j$ oraz $z^4 = (-3 + 4j)^2 = -7 - 24j$, skąd
  $w(1 + 2j) = (-7 - 24j) + 6(-3 + 4j) + 25 = 0$; symetria znaków $(\pm 1 \pm 2j)$ wynika
  bezpośrednio z parzystości wielomianu $w(-z) = w(z)$ i rzeczywistych współczynników.

---

### 3.2

* **Dane:** $w(z) = z^4 - (3 + 2j)^4$.
* **Metoda szybka (dwukrotny wzór na różnicę kwadratów / obroty o $90^\circ$ — bez podnoszenia $3 + 2j$ do czwartej potęgi):**
  * **Krok 1 — tożsamość $z^4 - a^4 = (z - a)(z + a)(z - ja)(z + ja)$:**
    Dla dowolnego $a \in \mathbb{C}$, korzystając z $+a^2 = -(ja)^2$, otrzymujemy:

    $$
    z^4 - a^4 = \left(z^2 - a^2\right)\left(z^2 + a^2\right)
    = \left(z^2 - a^2\right)\left(z^2 - (ja)^2\right)
    = (z - a)(z + a)(z - ja)(z + ja)
    $$

  * **Krok 2 — podstawienie $a = 3 + 2j$ oraz obrót $ja = j(3 + 2j) = -2 + 3j$:**
    Cztery pierwiastki to $a, -a, ja, -ja$, czyli $3 + 2j$, $-3 - 2j$, $-2 + 3j$, $2 - 3j$.

* **Wynik:**

  $$
  \boxed{w(z) = (z - 3 - 2j)(z + 3 + 2j)(z + 2 - 3j)(z - 2 + 3j)}
  $$

* **Sprawdzenie:** iloczyn pierwszych dwóch czynników daje $z^2 - (3 + 2j)^2 = z^2 - (5 + 12j)$,
  a dwóch ostatnich $z^2 - (-2 + 3j)^2 = z^2 + (5 + 12j)$; ich iloczyn to $z^4 - (5 + 12j)^2 = z^4 - (3 + 2j)^4$.

---

### 3.3

* **Dane:** $w(z) = \left(1 + j\sqrt{3}\right)z^4 + 8$.
* **Metoda szybka (iloraz w postaci trygonometrycznej + wyznaczenie jednego pierwiastka $z_0$ i mnożenie przez $1, j, -1, -j$):**
  * **Krok 1 — równanie $z^4 = \frac{-8}{1 + j\sqrt{3}}$ od ręki w postaci trygonometrycznej:**
    Ponieważ $1 + j\sqrt{3} = 2\left(\cos\frac{\pi}{3} + j\sin\frac{\pi}{3}\right)$ oraz
    $-8 = 8(\cos\pi + j\sin\pi)$, dzieląc moduły ($8 / 2 = 4$) i odejmując kąty
    ($\pi - \frac{\pi}{3} = \frac{2\pi}{3}$), dostajemy natychmiast:

    $$
    z^4 = 4\left(\cos\frac{2\pi}{3} + j\sin\frac{2\pi}{3}\right)
    $$

  * **Krok 2 — wyznaczenie jednego pierwiastka $z_0$ i obrót o wielokrotności $90^\circ$:**
    Pierwiastek dla $k = 0$ ma moduł $\sqrt[4]{4} = \sqrt{2}$ oraz kąt $\frac{2\pi/3}{4} = \frac{\pi}{6}$:

    $$
    z_0 = \sqrt{2}\left(\cos\frac{\pi}{6} + j\sin\frac{\pi}{6}\right)
    = \sqrt{2}\left(\frac{\sqrt{3}}{2} + j\frac{1}{2}\right)
    = \frac{\sqrt{6}}{2} + j\frac{\sqrt{2}}{2}
    $$

    Pozostałe trzy pierwiastki równania $z^4 = z_0^4$ powstają przez mnożenie $z_0$ przez kolejne
    pierwiastki $4$. stopnia z jedynki ($j, -1, -j$), bez ponownego liczenia cosinusów i sinusów:

    $$
    z_1 = jz_0 = -\frac{\sqrt{2}}{2} + j\frac{\sqrt{6}}{2}, \qquad
    z_2 = -z_0 = -\frac{\sqrt{6}}{2} - j\frac{\sqrt{2}}{2}, \qquad
    z_3 = -jz_0 = \frac{\sqrt{2}}{2} - j\frac{\sqrt{6}}{2}
    $$

  * **Krok 3 — zapis rozkładu z zachowaniem współczynnika wiodącego $a_4 = 1 + j\sqrt{3}$:**
    Wielomian stopnia $4$ o współczynniku wiodącym $a_4$ i pierwiastkach $z_0, z_1, z_2, z_3$
    zapisujemy w postaci $w(z) = a_4\left(z - z_0\right)\left(z - z_1\right)\left(z - z_2\right)\left(z - z_3\right)$.

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

* **Sprawdzenie:** $z_0^2 = \left(\frac{\sqrt{6} + j\sqrt{2}}{2}\right)^2 = \frac{6 - 2 + 2j\sqrt{12}}{4} = 1 + j\sqrt{3}$,
  więc $z_0^4 = \left(1 + j\sqrt{3}\right)^2 = -2 + 2j\sqrt{3}$, skąd
  $\left(1 + j\sqrt{3}\right)z_0^4 = \left(1 + j\sqrt{3}\right)^3 = 2^3(\cos\pi + j\sin\pi) = -8$,
  czyli $w(z_0) = 0$ (i tak samo dla $jz_0, -z_0, -jz_0$, bo $(\pm j)^4 = (\pm 1)^4 = 1$).

---

## Zadanie 4

Podajemy ogólną postać rozkładu funkcji wymiernej na ułamki proste nad $\mathbb{R}$ (bez wyznaczania
współczynników). Dla ułamka właściwego (stopień licznika mniejszy od stopnia mianownika) łączna
liczba nieoznaczonych stałych rzeczywistych musi być równa stopniowi mianownika — służy to jako
natychmiastowy test poprawności.

### 4.1

* **Dane:** $\dfrac{2x^2 - 7x}{(x - 3)^3\left(x^2 + 4\right)^2}$, dziedzina: $x \in \mathbb{R} \setminus \{3\}$.
* **Krok 1 — sprawdzenie stopni i nierozkładalności czynników mianownika:**
  * stopień licznika wynosi $2$, a stopień mianownika $3 + 2 \cdot 2 = 7$ ($2 < 7$ — ułamek właściwy,
    brak części wielomianowej); ułamek jest nieskracalny, gdyż dla $x = 3$ licznik wynosi
    $18 - 21 = -3 \ne 0$, a pierwiastki licznika $0$ i $\frac{7}{2}$ nie zerują $x^2 + 4$;
  * czynnik $(x - 3)^3$ (liniowy krotności $3$) generuje trzy ułamki o stałych licznikach;
  * trójmian $x^2 + 4$ jest nierozkładalny nad $\mathbb{R}$ ($x^2 + 4 \ge 4 > 0$, $\Delta = -16 < 0$),
    więc $\left(x^2 + 4\right)^2$ generuje dwa ułamki o licznikach liniowych.

* **Wynik:**

  $$
  \boxed{
  \frac{2x^2 - 7x}{(x - 3)^3\left(x^2 + 4\right)^2}
  = \frac{A}{x - 3} + \frac{B}{(x - 3)^2} + \frac{C}{(x - 3)^3}
  + \frac{Dx + E}{x^2 + 4} + \frac{Fx + G}{\left(x^2 + 4\right)^2},
  \qquad A, B, C, D, E, F, G \in \mathbb{R}
  }
  $$

* **Sprawdzenie:** liczba parametrów wynosi $3 + 2 + 2 = 7$, czyli dokładnie tyle, ile wynosi
  stopień mianownika.

---

### 4.2

* **Dane:** $\dfrac{3x^4 - 2}{x^4 - 2x^3 + 2x - 1}$, dziedzina: $x \in \mathbb{R} \setminus \{-1, 1\}$ (po rozkładzie poniżej).
* **Krok 1 — część wielomianowa (ułamek niewłaściwy!):**
  Stopień licznika ($4$) jest równy stopniowi mianownika ($4$), więc przed rozkładem na ułamki
  proste występuje wielomian stopnia $4 - 4 = 0$, czyli stała $A_0 \in \mathbb{R}$ (z ilorazu
  współczynników wiodących od razu widać, że $A_0 = \frac{3}{1} = 3$, gdyż
  $3x^4 - 2 = 3\left(x^4 - 2x^3 + 2x - 1\right) + \left(6x^3 - 6x + 1\right)$).
* **Krok 2 — jednolinijkowy rozkład mianownika bez schematu Hornera (grupowanie wyrazów skrajnych i środkowych):**

  $$
  x^4 - 2x^3 + 2x - 1 = \left(x^4 - 1\right) - 2x\left(x^2 - 1\right)
  = \left(x^2 - 1\right)\left(x^2 - 2x + 1\right)
  = (x - 1)(x + 1)(x - 1)^2
  = (x - 1)^3(x + 1)
  $$

  Ułamek jest nieskracalny, ponieważ dla $x = \pm 1$ licznik przyjmuje wartość $3(\pm 1)^4 - 2 = 1 \ne 0$.

* **Wynik:**

  $$
  \boxed{
  \frac{3x^4 - 2}{x^4 - 2x^3 + 2x - 1}
  = 3 + \frac{A}{x - 1} + \frac{B}{(x - 1)^2} + \frac{C}{(x - 1)^3} + \frac{D}{x + 1},
  \qquad A, B, C, D \in \mathbb{R}
  }
  $$

  *(Gdy w zapisie ogólnej postaci pozostawia się niewyznaczoną również część wielomianową stopnia $0$,
  zapis ma postać $A_0 + \frac{A}{x - 1} + \frac{B}{(x - 1)^2} + \frac{C}{(x - 1)^3} + \frac{D}{x + 1}$,
  gdzie $A_0, A, B, C, D \in \mathbb{R}$.)*

* **Sprawdzenie:** w części ułamkowej liczba stałych wynosi $3 + 1 = 4 = \deg M$, a rozwinięcie
  $(x - 1)^3(x + 1) = \left(x^3 - 3x^2 + 3x - 1\right)(x + 1) = x^4 - 2x^3 + 2x - 1$ odtwarza mianownik.

---

### 4.3

* **Dane:** $\dfrac{5x^3}{\left(x^4 + 4\right)^2}$, dziedzina: $x \in \mathbb{R}$ (bo $x^4 + 4 \ge 4 > 0$).
* **Krok 1 — sprawdzenie stopni:** stopień licznika $3 < 8$ (stopień mianownika), ułamek właściwy
  i nieskracalny.
* **Krok 2 — rozkład $x^4 + 4$ nad $\mathbb{R}$ tożsamością Sophie Germain (dopełnienie do kwadratu):**
  Wielomian stopnia $4$ jest nad $\mathbb{R}$ zawsze rozkładalny! Dodajemy i odejmujemy $4x^2$:

  $$
  x^4 + 4 = \left(x^4 + 4x^2 + 4\right) - 4x^2 = \left(x^2 + 2\right)^2 - (2x)^2
  = \left(x^2 - 2x + 2\right)\left(x^2 + 2x + 2\right)
  $$

  Oba trójmiany mają ujemny wyróżnik ($\Delta = 4 - 8 = -4 < 0$) i są różne, więc cały mianownik
  ma rozkład kanoniczny nad $\mathbb{R}$:

  $$
  \left(x^4 + 4\right)^2 = \left(x^2 - 2x + 2\right)^2\left(x^2 + 2x + 2\right)^2
  $$

* **Wynik:**

  $$
  \boxed{
  \frac{5x^3}{\left(x^4 + 4\right)^2}
  = \frac{Ax + B}{x^2 - 2x + 2} + \frac{Cx + D}{\left(x^2 - 2x + 2\right)^2}
  + \frac{Ex + F}{x^2 + 2x + 2} + \frac{Gx + H}{\left(x^2 + 2x + 2\right)^2},
  \qquad A, B, C, D, E, F, G, H \in \mathbb{R}
  }
  $$

* **Sprawdzenie:** liczba parametrów wynosi $4 \cdot 2 = 8 = \deg M$, a iloczyn
  $\left[(x^2 + 2) - 2x\right]\left[(x^2 + 2) + 2x\right] = x^4 + 4x^2 + 4 - 4x^2 = x^4 + 4$ jest dokładny.

---

## Zadanie 5

Wyznaczamy pełne rozkłady na ułamki proste nad $\mathbb{R}$, eliminując rozwiązywanie układów
równań liniowych na rzecz metody zakrywania Heaviside'a, rozkładu teleskopowego oraz wydzielania
czynników mianownika w liczniku.

### 5.1

* **Dane:** $\dfrac{4x - 10}{(x - 1)(x - 2)(x - 3)}$, dziedzina: $x \in \mathbb{R} \setminus \{1, 2, 3\}$.
* **Metoda szybka — reguła zakrywania Heaviside'a** (dla jednokrotnego pierwiastka $x_i$ współczynnik
  przy $\frac{1}{x - x_i}$ otrzymujemy, zakrywając $(x - x_i)$ i podstawiając $x = x_i$ do reszty wyrażenia):
  * dla $x = 1$ (zakrywamy $x - 1$):

    $$
    A = \left.\frac{4x - 10}{(x - 2)(x - 3)}\right\rvert_{x = 1} = \frac{4 - 10}{(-1)(-2)} = \frac{-6}{2} = -3
    $$

  * dla $x = 2$ (zakrywamy $x - 2$):

    $$
    B = \left.\frac{4x - 10}{(x - 1)(x - 3)}\right\rvert_{x = 2} = \frac{8 - 10}{1 \cdot (-1)} = \frac{-2}{-1} = 2
    $$

  * dla $x = 3$ (zakrywamy $x - 3$):

    $$
    C = \left.\frac{4x - 10}{(x - 1)(x - 2)}\right\rvert_{x = 3} = \frac{12 - 10}{2 \cdot 1} = \frac{2}{2} = 1
    $$

* **Wynik:**

  $$
  \boxed{\frac{4x - 10}{(x - 1)(x - 2)(x - 3)} = -\frac{3}{x - 1} + \frac{2}{x - 2} + \frac{1}{x - 3}}
  $$

* **Sprawdzenie:** po pierwsze $A + B + C = -3 + 2 + 1 = 0$, co zgadza się z brakiem wyrazu $x^2$
  w liczniku ($\deg L = 1 \le \deg M - 2$); po drugie dla $x = 0$ lewa strona wynosi
  $\frac{-10}{-6} = \frac{5}{3}$, a prawa $3 - 1 - \frac{1}{3} = \frac{5}{3}$.

---

### 5.2

* **Dane:** $\dfrac{8}{x^2 - 4x + 2}$, dziedzina: $x \in \mathbb{R} \setminus \left\{2 - \sqrt{2},\ 2 + \sqrt{2}\right\}$.
* **Metoda szybka — dopełnienie do kwadratu + rozkład teleskopowy (bez wyróżnika i bez układu równań):**
  * **Krok 1 — rozkład mianownika z dopełnienia do kwadratu:**

    $$
    x^2 - 4x + 2 = (x - 2)^2 - 2 = \left(x - 2 - \sqrt{2}\right)\left(x - 2 + \sqrt{2}\right)
    $$

  * **Krok 2 — tożsamość teleskopowa $\dfrac{1}{\alpha\beta} = \dfrac{1}{\beta - \alpha}\left(\dfrac{1}{\alpha} - \dfrac{1}{\beta}\right)$:**
    Różnica obu czynników jest stała i równa $\left(x - 2 + \sqrt{2}\right) - \left(x - 2 - \sqrt{2}\right) = 2\sqrt{2}$, stąd od ręki:

    $$
    \frac{8}{\left(x - 2 - \sqrt{2}\right)\left(x - 2 + \sqrt{2}\right)}
    = \frac{8}{2\sqrt{2}}\left(\frac{1}{x - 2 - \sqrt{2}} - \frac{1}{x - 2 + \sqrt{2}}\right)
    = \frac{2\sqrt{2}}{x - 2 - \sqrt{2}} - \frac{2\sqrt{2}}{x - 2 + \sqrt{2}}
    $$

* **Wynik:**

  $$
  \boxed{\frac{8}{x^2 - 4x + 2} = \frac{2\sqrt{2}}{x - 2 - \sqrt{2}} - \frac{2\sqrt{2}}{x - 2 + \sqrt{2}}}
  $$

* **Sprawdzenie:** dla $x = 2$ lewa strona daje $\frac{8}{4 - 8 + 2} = -4$, a prawa
  $\frac{2\sqrt{2}}{-\sqrt{2}} - \frac{2\sqrt{2}}{\sqrt{2}} = -2 - 2 = -4$.

---

### 5.3

* **Dane:** $\dfrac{x^2 - 3x + 6}{x^4 - 5x^2 + 4}$, dziedzina: $x \in \mathbb{R} \setminus \{-2, -1, 1, 2\}$.
* **Metoda szybka — zakrywanie Heaviside'a na postaci półrozłożonej:**
  * **Krok 1 — rozkład mianownika dwukwadratowego:**

    $$
    x^4 - 5x^2 + 4 = \left(x^2 - 1\right)\left(x^2 - 4\right) = (x - 1)(x + 1)(x - 2)(x + 2)
    $$

  * **Krok 2 — obliczenie współczynników w pamięci:**
    Zamiast mnożyć za każdym razem trzy nawiasy liniowe, zostawiamy drugi czynnik kwadratowy
    nierozłożony: dla $x = \pm 1$ wyrażenie $x^2 - 4$ ma tę samą wartość $-3$, a dla $x = \pm 2$
    wyrażenie $x^2 - 1$ ma tę samą wartość $+3$:

    $$
    A_1 = \left.\frac{x^2 - 3x + 6}{(x + 1)\left(x^2 - 4\right)}\right\rvert_{x = 1}
    = \frac{1 - 3 + 6}{2 \cdot (-3)} = -\frac{2}{3}, \qquad
    A_2 = \left.\frac{x^2 - 3x + 6}{(x - 1)\left(x^2 - 4\right)}\right\rvert_{x = -1}
    = \frac{1 + 3 + 6}{(-2) \cdot (-3)} = \frac{5}{3}
    $$

    $$
    A_3 = \left.\frac{x^2 - 3x + 6}{\left(x^2 - 1\right)(x + 2)}\right\rvert_{x = 2}
    = \frac{4 - 6 + 6}{3 \cdot 4} = \frac{1}{3}, \qquad
    A_4 = \left.\frac{x^2 - 3x + 6}{\left(x^2 - 1\right)(x - 2)}\right\rvert_{x = -2}
    = \frac{4 + 6 + 6}{3 \cdot (-4)} = -\frac{4}{3}
    $$

* **Wynik:**

  $$
  \boxed{
  \frac{x^2 - 3x + 6}{x^4 - 5x^2 + 4}
  = -\frac{2}{3(x - 1)} + \frac{5}{3(x + 1)} + \frac{1}{3(x - 2)} - \frac{4}{3(x + 2)}
  }
  $$

* **Sprawdzenie:** suma współczynników wynosi $\frac{-2 + 5 + 1 - 4}{3} = 0$ (zgodnie z tym, że
  $\deg L = 2 \le \deg M - 2$), a dla $x = 0$ lewa strona jest równa $\frac{6}{4} = \frac{3}{2}$,
  prawa zaś $\frac{2}{3} + \frac{5}{3} - \frac{1}{6} - \frac{2}{3} = \frac{3}{2}$.

---

### 5.4

* **Dane:** $\dfrac{2x^3 + 5x^2 + 3x + 1}{x^2\left(x^2 + 1\right)^2}$, dziedzina: $x \in \mathbb{R} \setminus \{0\}$.
* **Metoda szybka — algebraiczne wydzielenie czynników mianownika w liczniku (3 linijki zamiast układu 6 równań!):**
  * **Krok 1 — wyeliminowanie wyrazów stopnia $< 2$, aby reszta podzieliła się przez $x^2$:**
    W liczniku wyrazy najniższych potęg tworzą dwumian $3x + 1$. Mnożąc go przez $\left(x^2 + 1\right)$,
    otrzymujemy $(3x + 1)\left(x^2 + 1\right) = 3x^3 + x^2 + 3x + 1$, co ma identyczną końcówkę
    $3x + 1$. Zatem różnica dzieli się bez reszty przez $x^2$:

    $$
    2x^3 + 5x^2 + 3x + 1
    = (3x + 1)\left(x^2 + 1\right) + \left(-x^3 + 4x^2\right)
    = (3x + 1)\left(x^2 + 1\right) + x^2(-x + 4)
    $$

  * **Krok 2 — rozbicie ułamka i skrócenie czynników $\left(x^2 + 1\right)$ oraz $x^2$:**

    $$
    \frac{2x^3 + 5x^2 + 3x + 1}{x^2\left(x^2 + 1\right)^2}
    = \frac{3x + 1}{x^2\left(x^2 + 1\right)} + \frac{-x + 4}{\left(x^2 + 1\right)^2}
    $$

  * **Krok 3 — elementarna tożsamość $\dfrac{1}{x^2\left(x^2 + 1\right)} = \dfrac{\left(x^2 + 1\right) - x^2}{x^2\left(x^2 + 1\right)} = \dfrac{1}{x^2} - \dfrac{1}{x^2 + 1}$:**

    $$
    \frac{3x + 1}{x^2\left(x^2 + 1\right)}
    = (3x + 1)\left(\frac{1}{x^2} - \frac{1}{x^2 + 1}\right)
    = \frac{3}{x} + \frac{1}{x^2} - \frac{3x + 1}{x^2 + 1}
    $$

* **Wynik:**

  $$
  \boxed{
  \frac{2x^3 + 5x^2 + 3x + 1}{x^2\left(x^2 + 1\right)^2}
  = \frac{3}{x} + \frac{1}{x^2} - \frac{3x + 1}{x^2 + 1} + \frac{-x + 4}{\left(x^2 + 1\right)^2}
  }
  $$

* **Sprawdzenie:** dla $x = 1$ lewa strona wynosi $\frac{2 + 5 + 3 + 1}{1 \cdot 4} = \frac{11}{4}$,
  a prawa $3 + 1 - \frac{4}{2} + \frac{3}{4} = 2 + \frac{3}{4} = \frac{11}{4}$; dla $x = -1$ lewa
  strona wynosi $\frac{-2 + 5 - 3 + 1}{1 \cdot 4} = \frac{1}{4}$, a prawa
  $-3 + 1 - \frac{-2}{2} + \frac{5}{4} = -1 + \frac{5}{4} = \frac{1}{4}$.

---

## Zadanie 6

Podajemy ogólną postać rozkładu funkcji wymiernej na ułamki proste nad $\mathbb{C}$ (bez wyznaczania
wartości współczynników). Z zasadniczego twierdzenia algebry każdy wielomian nad $\mathbb{C}$ rozkłada
się wyłącznie na czynniki liniowe $(z - z_0)^m$, z których każdy daje łańcuch
$\frac{A_1}{z - z_0} + \ldots + \frac{A_m}{(z - z_0)^m}$ o stałych zespolonych $A_k \in \mathbb{C}$.

### 6.1

* **Dane:** $\dfrac{4z + 3j}{z^2 - 2jz + 3}$, stopień licznika $1 < 2$ (ułamek właściwy).
* **Krok 1 — rozkład mianownika nad $\mathbb{C}$ przez dopełnienie do kwadratu (lub wzory Viète'a w pamięci):**
  Ponieważ $(-j)^2 = -1$ oraz $4 = -(2j)^2$:

  $$
  z^2 - 2jz + 3 = (z - j)^2 + 4 = (z - j)^2 - (2j)^2 = (z - 3j)(z + j)
  $$

  *(Równoważnie ze wzorów Viète'a: szukamy dwóch liczb o sumie $2j$ i iloczynie $3$; są to $3j$
  oraz $-j$, bo $(3j)(-j) = -3j^2 = 3$.)*
  Dziedzina: $z \in \mathbb{C} \setminus \{-j, 3j\}$; licznik nie zeruje się w żadnym z tych punktów
  ($15j \ne 0$, $-j \ne 0$).

* **Wynik:**

  $$
  \boxed{
  \frac{4z + 3j}{z^2 - 2jz + 3} = \frac{A}{z - 3j} + \frac{B}{z + j},
  \qquad A, B \in \mathbb{C}
  }
  $$

* **Sprawdzenie:** $(z - 3j)(z + j) = z^2 + jz - 3jz - 3j^2 = z^2 - 2jz + 3$; liczba parametrów $2 = \deg M$.

---

### 6.2

* **Dane:** $\dfrac{z^4 + 3z - 2}{z^2\left(z^2 + 9\right)(z + 3j)^2}$.
* **Krok 1 — pełny rozkład mianownika i zgrupowanie powtarzających się czynników (kluczowa pułapka!):**
  Korzystając z $z^2 + 9 = z^2 - (3j)^2 = (z - 3j)(z + 3j)$, łączymy identyczne czynniki $(z + 3j)$:

  $$
  z^2\left(z^2 + 9\right)(z + 3j)^2 = z^2(z - 3j)(z + 3j)(z + 3j)^2 = z^2(z - 3j)(z + 3j)^3
  $$

  Dziedzina: $z \in \mathbb{C} \setminus \{0, 3j, -3j\}$. Stopień licznika $4 < 6$ (stopień mianownika
  $2 + 1 + 3 = 6$ — brak części wielomianowej), a ułamek jest nieskracalny (w $z = 0$ licznik
  wynosi $-2 \ne 0$, a w $z = \pm 3j$ wynosi $79 \pm 9j \ne 0$).

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

* **Dane:** $\dfrac{z^7 + z^2}{\left(z^4 + 4\right)^2}$, stopień licznika $7 < 8$ (ułamek właściwy).
* **Krok 1 — błyskawiczne wyznaczenie pierwiastków $z^4 + 4 = 0$ z tożsamości $(1 + j)^2 = 2j$:**
  Ponieważ $(1 + j)^2 = 2j$, mamy od ręki $(1 + j)^4 = (2j)^2 = -4$. Zatem pierwiastkiem równania
  $z^4 = -4$ jest $z_0 = 1 + j$, a wszystkie cztery pierwiastki powstają przez mnożenie $1 + j$
  przez $\{1, j, -1, -j\}$ (obroty o $90^\circ$):

  $$
  z \in \{1 + j,\ -1 + j,\ -1 - j,\ 1 - j\}
  $$

  *(Ten sam wynik daje natychmiast rozkład Sophie Germain z zadania 4.3:
  $(z - 1)^2 + 1 = 0 \implies z = 1 \pm j$ oraz $(z + 1)^2 + 1 = 0 \implies z = -1 \pm j$.)*
  Dziedzina: $z \in \mathbb{C} \setminus \{1 + j, -1 + j, -1 - j, 1 - j\}$. Ułamek jest nieskracalny
  (pierwiastki mianownika mają moduł $\sqrt{2}$, a pierwiastki licznika $z^2\left(z^5 + 1\right)$
  mają moduł $0$ lub $1$). Każdy z czterech czynników liniowych ma w $\left(z^4 + 4\right)^2$ krotność $2$:

  $$
  \left(z^4 + 4\right)^2 = (z - 1 - j)^2(z + 1 - j)^2(z + 1 + j)^2(z - 1 + j)^2
  $$

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

* **Sprawdzenie:** liczba parametrów wynosi $4 \cdot 2 = 8 = \deg M$, a iloczyn par sprzężonych daje
  $\left[(z - 1)^2 + 1\right]\left[(z + 1)^2 + 1\right] = \left(z^2 - 2z + 2\right)\left(z^2 + 2z + 2\right) = z^4 + 4$.

---

## Zadanie 7

Korzystamy ze wzoru residuowego podanego przed zadaniem 7: dla wielomianu
$g(z) = \left(z - z_1\right) \cdot \ldots \cdot \left(z - z_n\right)$ o różnych pierwiastkach
jednokrotnych $z_1, \ldots, z_n$ oraz $\deg f < \deg g$ współczynniki rozkładu
$\frac{f(z)}{g(z)} = \sum_{i=1}^n \frac{a_i}{z - z_i}$ wyrażają się wzorem $a_i = \frac{f(z_i)}{g'(z_i)}$.
Dodatkowo pokazujemy jednowierszowe skróty algebraiczne potwierdzające oba wyniki.

### 7.1

* **Dane:** $\dfrac{4z^2 + 1}{z^4 - 1}$, dziedzina: $z \in \mathbb{C} \setminus \{1, -1, j, -j\}$.
* **Krok 1 — pierwiastki mianownika i uproszczenie wzoru $a_i = \frac{f(z_i)}{g'(z_i)}$ przed podstawianiem:**
  Mamy $f(z) = 4z^2 + 1$, $g(z) = z^4 - 1$ oraz $g'(z) = 4z^3$. Pierwiastki $z^4 = 1$ to cztery
  różne liczby $z_1 = 1$, $z_2 = -1$, $z_3 = j$, $z_4 = -j$.
  **Chwyt upraszczający:** ponieważ dla każdego z tych pierwiastków zachodzi $z_i^4 = 1$, mnożymy
  licznik i mianownik ułamka $\frac{4z_i^2 + 1}{4z_i^3}$ przez $z_i$, eliminując całkowicie dzielenie
  przez potęgi $j$:

  $$
  a_i = \frac{f(z_i)}{g'(z_i)} = \frac{4z_i^2 + 1}{4z_i^3}
  = \frac{z_i\left(4z_i^2 + 1\right)}{4z_i^4} = \frac{z_i\left(4z_i^2 + 1\right)}{4}
  $$

* **Krok 2 — odczyt współczynników w pamięci:**
  * dla $z_i = \pm 1$ mamy $z_i^2 = 1$, więc $a_{1,2} = \frac{\pm 1 \cdot (4 + 1)}{4} = \pm\frac{5}{4}$
    (tj. $a_1 = \frac{5}{4}$ przy $z - 1$ oraz $a_2 = -\frac{5}{4}$ przy $z + 1$);
  * dla $z_i = \pm j$ mamy $z_i^2 = -1$, więc $a_{3,4} = \frac{\pm j \cdot (-4 + 1)}{4} = \mp\frac{3}{4}j$
    (tj. $a_3 = -\frac{3}{4}j$ przy $z - j$ oraz $a_4 = \frac{3}{4}j$ przy $z + j$).

* **Wynik:**

  $$
  \boxed{
  \frac{4z^2 + 1}{z^4 - 1}
  = \frac{5}{4(z - 1)} - \frac{5}{4(z + 1)} - \frac{3j}{4(z - j)} + \frac{3j}{4(z + j)}
  }
  $$

* **Sprawdzenie (druga metoda — dwuwierszowy rozkład kaskadowy bez pochodnych):**
  Zapisujemy licznik jako kombinację $\left(z^2 + 1\right)$ i $\left(z^2 - 1\right)$:
  $4z^2 + 1 = \frac{5}{2}\left(z^2 + 1\right) + \frac{3}{2}\left(z^2 - 1\right)$. Dzieląc przez
  $z^4 - 1 = \left(z^2 - 1\right)\left(z^2 + 1\right)$ i stosując tożsamość teleskopową, dostajemy:

  $$
  \frac{4z^2 + 1}{z^4 - 1}
  = \frac{5}{2\left(z^2 - 1\right)} + \frac{3}{2\left(z^2 + 1\right)}
  = \frac{5}{4}\left(\frac{1}{z - 1} - \frac{1}{z + 1}\right)
  + \frac{3}{4j}\left(\frac{1}{z - j} - \frac{1}{z + j}\right)
  $$

  co wobec $\frac{1}{j} = -j$ daje dokładnie ten sam rozkład.

---

### 7.2

* **Dane:** $\dfrac{z^{2020}}{z^{2021} + 1}$, dziedzina: $z \in \mathbb{C} \setminus \{z_0, z_1, \ldots, z_{2020}\}$ (gdzie $z_k$ zdefiniowano poniżej).
* **Krok 1 — pierwiastki mianownika $g(z) = z^{2021} + 1$:**
  Rozwiązujemy równanie $z^{2021} = -1 = \cos\pi + j\sin\pi$. Otrzymujemy $2021$ różnych
  pierwiastków jednokrotnych na okręgu jednostkowym $\lvert z_k\rvert = 1$ (w szczególności $z_k \ne 0$):

  $$
  z_k = \cos\frac{(2k + 1)\pi}{2021} + j\sin\frac{(2k + 1)\pi}{2021}, \qquad k = 0, 1, \ldots, 2020
  $$

* **Krok 2 — natychmiastowe skrócenie we wzorze $a_k = \frac{f(z_k)}{g'(z_k)}$:**
  Mamy $f(z) = z^{2020}$ oraz $g'(z) = 2021z^{2020}$. Ponieważ $z_k \ne 0$, czynnik $z_k^{2020} \ne 0$
  skraca się w każdym z $2021$ współczynników:

  $$
  a_k = \frac{f(z_k)}{g'(z_k)} = \frac{z_k^{2020}}{2021z_k^{2020}} = \frac{1}{2021},
  \qquad k = 0, 1, \ldots, 2020
  $$

* **Wynik:**

  $$
  \boxed{
  \frac{z^{2020}}{z^{2021} + 1}
  = \frac{1}{2021}\sum_{k=0}^{2020}\frac{1}{z - z_k}, \qquad
  \text{gdzie } z_k = \cos\frac{(2k + 1)\pi}{2021} + j\sin\frac{(2k + 1)\pi}{2021}
  }
  $$

* **Sprawdzenie (druga metoda — jednowierszowa pochodna logarytmiczna):**
  Dla wielomianu unormowanego $g(z) = \prod_{k=0}^{2020}\left(z - z_k\right)$ reguła różniczkowania
  iloczynu po podzieleniu przez $g(z)$ daje klasyczną tożsamość $\frac{g'(z)}{g(z)} = \sum_{k=0}^{2020}\frac{1}{z - z_k}$.
  Ponieważ $g'(z) = 2021z^{2020}$, dzieląc obie strony przez $2021$ otrzymujemy tożsamościowo
  $\frac{z^{2020}}{z^{2021} + 1} = \frac{1}{2021}\sum_{k=0}^{2020}\frac{1}{z - z_k}$. Dodatkowo dla
  $z = 0$ lewa strona wynosi $0$, a po prawej stronie w sumie $-\frac{1}{2021}\sum_{k=0}^{2020}\overline{z_k}$
  wektory wierzchołków $2021$-kąta foremnego sumują się do $0$.

---

## Podsumowanie wyników

| Podpunkt | Zastosowana metoda szybka | Wynik końcowy |
| :--- | :--- | :--- |
| **1.1** | Grupowanie $z^2(z^5 + 1)(z^{10} - 1)$ + symetria $\sqrt[10]{1}$ | $z = 0$ (kr. $2$), $\zeta_k = \cos\frac{k\pi}{5} + j\sin\frac{k\pi}{5}$ (kr. $1$ dla $2 \mid k$, kr. $2$ dla $2 \nmid k$); rzecz.: $3$, w $\mathbb{C}$: $11$ (nierzecz.: $8$) |
| **1.2** | Pełny kwadrat $z^3(z^3 + 2)^2$ + obrót o $\pm\frac{2\pi}{3}$ | $z = 0$ (kr. $3$), $-\sqrt[3]{2}$ oraz $\frac{\sqrt[3]{2}}{2}\left(1 \pm j\sqrt{3}\right)$ (kr. $2$); rzecz.: $2$, w $\mathbb{C}$: $4$ (nierzecz.: $2$) |
| **1.3** | Obrót $z_5 = \frac{\sqrt{2}}{2}(1 - j)$ o $\frac{\pi}{3}$ + pochodna $w'$ | $z = 0$ oraz $\cos\left(\frac{\pi}{12} + \frac{k\pi}{3}\right) + j\sin\left(\frac{\pi}{12} + \frac{k\pi}{3}\right)$ ($k = 0, \ldots, 5$), kr. $1$; rzecz.: $1$, w $\mathbb{C}$: $7$ (nierzecz.: $6$) |
| **2** | Sprzężenie $\overline{z_0}$ + wzory Viète'a dla stopnia $4$ | Pozostałe pierwiastki: $1 - 2j$, $-2 + j$, $-2 - j$ |
| **3.1** | Dopełnienie $(z^2 + 5)^2 - (2z)^2$ i $+4 = -(2j)^2$ | $(z - 1 - 2j)(z - 1 + 2j)(z + 1 - 2j)(z + 1 + 2j)$ |
| **3.2** | Tożsamość $z^4 - a^4 = (z \mp a)(z \mp ja)$ | $(z - 3 - 2j)(z + 3 + 2j)(z + 2 - 3j)(z - 2 + 3j)$ |
| **3.3** | Postać trygonometryczna + obroty $z_0, jz_0, -z_0, -jz_0$ | $\left(1 + j\sqrt{3}\right)\left(z - \frac{\sqrt{6}}{2} - j\frac{\sqrt{2}}{2}\right)\left(z + \frac{\sqrt{2}}{2} - j\frac{\sqrt{6}}{2}\right)\left(z + \frac{\sqrt{6}}{2} + j\frac{\sqrt{2}}{2}\right)\left(z - \frac{\sqrt{2}}{2} + j\frac{\sqrt{6}}{2}\right)$ |
| **4.1** | Stopnie ($2 < 7$) i nierozkładalność $x^2 + 4$ | $\frac{A}{x - 3} + \frac{B}{(x - 3)^2} + \frac{C}{(x - 3)^3} + \frac{Dx + E}{x^2 + 4} + \frac{Fx + G}{(x^2 + 4)^2}$ |
| **4.2** | Iloraz wiodący $3$ + grupowanie $(x^4 - 1) - 2x(x^2 - 1)$ | $3 + \frac{A}{x - 1} + \frac{B}{(x - 1)^2} + \frac{C}{(x - 1)^3} + \frac{D}{x + 1}$ |
| **4.3** | Tożsamość Sophie Germain $(x^2 + 2)^2 - (2x)^2$ | $\frac{Ax + B}{x^2 - 2x + 2} + \frac{Cx + D}{(x^2 - 2x + 2)^2} + \frac{Ex + F}{x^2 + 2x + 2} + \frac{Gx + H}{(x^2 + 2x + 2)^2}$ |
| **5.1** | Zakrywanie Heaviside'a | $-\frac{3}{x - 1} + \frac{2}{x - 2} + \frac{1}{x - 3}$ |
| **5.2** | Kwadrat $(x - 2)^2 - 2$ + rozkład teleskopowy | $\frac{2\sqrt{2}}{x - 2 - \sqrt{2}} - \frac{2\sqrt{2}}{x - 2 + \sqrt{2}}$ |
| **5.3** | Zakrywanie na postaci półrozłożonej $(x^2 - 1)(x^2 - 4)$ | $-\frac{2}{3(x - 1)} + \frac{5}{3(x + 1)} + \frac{1}{3(x - 2)} - \frac{4}{3(x + 2)}$ |
| **5.4** | Wydzielenie $(3x + 1)(x^2 + 1) + x^2(-x + 4)$ | $\frac{3}{x} + \frac{1}{x^2} - \frac{3x + 1}{x^2 + 1} + \frac{-x + 4}{(x^2 + 1)^2}$ |
| **6.1** | Kwadrat $(z - j)^2 - (2j)^2$ / wzory Viète'a | $\frac{A}{z - 3j} + \frac{B}{z + j}$, $A, B \in \mathbb{C}$ |
| **6.2** | Rozkład $z^2 + 9 = (z \mp 3j)$ i scalenie $(z + 3j)^3$ | $\frac{A}{z} + \frac{B}{z^2} + \frac{C}{z - 3j} + \frac{D}{z + 3j} + \frac{E}{(z + 3j)^2} + \frac{F}{(z + 3j)^3}$ |
| **6.3** | Tożsamość $(1 + j)^4 = -4$ i obroty o $90^\circ$ | suma $8$ ułamków prostych krotności $1$ i $2$ nad biegunami $\pm 1 \pm j$ |
| **7.1** | Skrócenie $a_i = \frac{z_i(4z_i^2 + 1)}{4}$ dzięki $z_i^4 = 1$ | $\frac{5}{4(z - 1)} - \frac{5}{4(z + 1)} - \frac{3j}{4(z - j)} + \frac{3j}{4(z + j)}$ |
| **7.2** | Skrócenie $z_k^{2020}$ / pochodna logarytmiczna $\frac{g'}{g}$ | $\frac{1}{2021}\sum_{k=0}^{2020}\frac{1}{z - z_k}$, $z_k = \cos\frac{(2k + 1)\pi}{2021} + j\sin\frac{(2k + 1)\pi}{2021}$ |
