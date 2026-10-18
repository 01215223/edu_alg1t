# Algebra – Zestaw 2 – rozwiązania

> **Założenia i konwencje.** Jednostka urojona: $j$, gdzie $j^2 = -1$. Argument główny podajemy
> w przedziale $(-\pi, \pi]$; kąty pierwiastków wygodnie jest wypisywać w $[0, 2\pi)$. Postać
> trygonometryczna: $r(\cos\varphi + j\sin\varphi)$. Symbol $\sqrt[n]{w}$ oznacza **cały**
> $n$-elementowy zbiór pierwiastków — wypisujemy wszystkie wartości. Wyniki są dokładne;
> przybliżenia dziesiętne (cztery miejsca po przecinku) pojawiają się tylko tam, gdzie wymaga
> tego polecenie (zadanie 1.5 — argument „z kalkulatora”) oraz w kolumnach pomocniczych tabel.
> Przybliżenia oznaczamy $\approx$, a przecinek dziesiętny we wzorach zapisujemy jako ${,}$.
>
> **Narzędzie sprawdzające.** Każdy wynik zweryfikowano drugą metodą: niezależnym rachunkiem
> symbolicznym (`sympy`), podstawieniem wstecz, sprawdzeniem modułu i argumentu oraz — dla
> pierwiastków — wzorami Viète'a (suma wszystkich pierwiastków równa $0$, iloczyn równy
> $(-1)^{n+1}w$).
>
> **Uwaga organizacyjna.** Jest to samodzielne, pełne rozwiązanie zestawu 2 zapisane w pliku
> `zestaw2_odp2.md`. Wyniki są zgodne z plikami `zestaw2-odpowiedzi.md` i `zestaw2_odp.md`;
> różnice redakcyjne: w zadaniu 1.6 moduł pierwiastków uproszczono dokładnie do $\sqrt2$
> (bo $\sqrt[5]{4\sqrt2} = \sqrt[5]{2^{5/2}} = \sqrt2$), w zadaniu 1.3 pokazano przejście
> trygonometryczne wzorami na połówki kątów, a w zadaniu 3.6 podano równanie kartezjańskie
> wszystkich czterech prostych tworzących zbiór rozwiązań.

---

## Zadanie 1 — potęgi i pierwiastki liczb zespolonych

### 1.1

* **Dane:**

  $$
  \frac{\left(-2 + 2\sqrt3 j\right)^{21}}{(2 - 2j)^{26}}
  $$

* **Krok 1 — postać trygonometryczna obu podstaw:**

  $$
  \left\lvert -2 + 2\sqrt3 j\right\rvert = \sqrt{4 + 12} = 4, \qquad
  \cos\varphi_1 = -\frac{2}{4} = -\frac12, \quad \sin\varphi_1 = \frac{2\sqrt3}{4} = \frac{\sqrt3}{2}
  \implies \varphi_1 = \frac{2\pi}{3}
  $$

  $$
  \lvert 2 - 2j\rvert = \sqrt{4 + 4} = 2\sqrt2, \qquad
  \cos\varphi_2 = \frac{2}{2\sqrt2} = \frac{\sqrt2}{2}, \quad \sin\varphi_2 = -\frac{\sqrt2}{2}
  \implies \varphi_2 = -\frac{\pi}{4}
  $$

  czyli

  $$
  -2 + 2\sqrt3 j = 4\left(\cos\frac{2\pi}{3} + j\sin\frac{2\pi}{3}\right), \qquad
  2 - 2j = 2\sqrt2\left(\cos\left(-\frac{\pi}{4}\right) + j\sin\left(-\frac{\pi}{4}\right)\right)
  $$

* **Krok 2 — wzór Moivre'a dla licznika i mianownika:**

  $$
  \left(-2 + 2\sqrt3 j\right)^{21} = 4^{21}\left(\cos\left(21 \cdot \frac{2\pi}{3}\right)
  + j\sin\left(21 \cdot \frac{2\pi}{3}\right)\right)
  = 4^{21}\left(\cos 14\pi + j\sin 14\pi\right) = 4^{21} = 2^{42}
  $$

  $$
  (2 - 2j)^{26} = (2\sqrt2)^{26}\left(\cos\left(-\frac{26\pi}{4}\right)
  + j\sin\left(-\frac{26\pi}{4}\right)\right)
  = 2^{39}\left(\cos\left(-\frac{13\pi}{2}\right) + j\sin\left(-\frac{13\pi}{2}\right)\right)
  $$

  Ponieważ $-\frac{13\pi}{2} + 8\pi = \frac{3\pi}{2}$, mamy $\cos\left(-\frac{13\pi}{2}\right) = 0$
  i $\sin\left(-\frac{13\pi}{2}\right) = -1$, skąd

  $$
  (2 - 2j)^{26} = 2^{39}\left(\cos\frac{3\pi}{2} + j\sin\frac{3\pi}{2}\right) = -2^{39}j
  $$

* **Krok 3 — iloraz:**

  $$
  \frac{2^{42}}{-2^{39}j} = -\frac{8}{j} = -\frac{8j}{j^2} = 8j
  $$

* **Wynik:**

  $$
  \boxed{\frac{\left(-2 + 2\sqrt3 j\right)^{21}}{(2 - 2j)^{26}} = 8j}
  $$

* **Sprawdzenie (rachunek niezależny, bez argumentów).** Wykorzystujemy to, że
  $\left(-2 + 2\sqrt3 j\right)^3 = 4^3(\cos 2\pi + j\sin 2\pi) = 64$ oraz
  $(2 - 2j)^2 = 4 - 8j + 4j^2 = -8j$:

  $$
  \left(-2 + 2\sqrt3 j\right)^{21} = 64^7 = 2^{42}, \qquad
  (2 - 2j)^{26} = \left(-8j\right)^{13} = (-8)^{13}j^{13} = -2^{39}j
  $$

  bo $j^{13} = j^{12} \cdot j = j$. Stąd iloraz równa się $2^{42} : \left(-2^{39}j\right) = 8j$,
  co potwierdza wynik. Moduł wyniku: $\frac{4^{21}}{(2\sqrt2)^{26}} = \frac{2^{42}}{2^{39}} = 8$,
  argument: $\frac{\pi}{2}$ — zgadza się z liczbą $8j$.

### 1.2

* **Dane:**

  $$
  \left(\frac{2j - 4}{j + 3}\right)^{101}
  $$

* **Krok 1 — uproszczenie podstawy** (mnożymy licznik i mianownik przez sprzężenie mianownika;
  dziedzina: $j + 3 \ne 0$, co jest spełnione):

  $$
  \frac{2j - 4}{j + 3} = \frac{(-4 + 2j)(3 - j)}{(3 + j)(3 - j)}
  = \frac{-12 + 4j + 6j - 2j^2}{9 + 1} = \frac{-10 + 10j}{10} = -1 + j
  $$

* **Krok 2 — postać trygonometryczna i wzór Moivre'a:**

  $$
  \lvert -1 + j\rvert = \sqrt2, \qquad \cos\varphi = -\frac{\sqrt2}{2}, \quad
  \sin\varphi = \frac{\sqrt2}{2} \implies \varphi = \frac{3\pi}{4}
  $$

  $$
  (-1 + j)^{101} = \left(\sqrt2\right)^{101}\left(\cos\frac{303\pi}{4} + j\sin\frac{303\pi}{4}\right)
  $$

* **Krok 3 — redukcja modułu i kąta:**

  $$
  \left(\sqrt2\right)^{101} = 2^{101/2} = 2^{50}\sqrt2, \qquad
  \frac{303\pi}{4} = 76\pi - \frac{\pi}{4} \equiv -\frac{\pi}{4} \pmod{2\pi}
  $$

  Zatem

  $$
  (-1 + j)^{101} = 2^{50}\sqrt2\left(\cos\left(-\frac{\pi}{4}\right)
  + j\sin\left(-\frac{\pi}{4}\right)\right) = 2^{50}\sqrt2\left(\frac{\sqrt2}{2} - j\frac{\sqrt2}{2}\right)
  = 2^{50}(1 - j)
  $$

* **Wynik:**

  $$
  \boxed{\left(\frac{2j - 4}{j + 3}\right)^{101} = 2^{50}(1 - j) = 1\,125\,899\,906\,842\,624\,(1 - j)}
  $$

* **Sprawdzenie.** $(-1 + j)^2 = 1 - 2j + j^2 = -2j$, więc

  $$
  (-1 + j)^{101} = \left((-1 + j)^2\right)^{50}(-1 + j) = (-2j)^{50}(-1 + j)
  = 2^{50}j^{50}(-1 + j) = -2^{50}(-1 + j) = 2^{50}(1 - j)
  $$

  bo $j^{50} = \left(j^2\right)^{25} = -1$. Moduł: $2^{50}\sqrt2$, argument główny: $-\frac{\pi}{4}$ —
  zgodnie z wyliczeniem.

### 1.3

* **Dane:** $\sqrt{7 - 24j}$, czyli oba pierwiastki kwadratowe liczby $q = 7 - 24j$.
* **Krok 1 — moduł i argument liczby podpierwiastkowej:**

  $$
  \lvert q\rvert = \sqrt{49 + 576} = \sqrt{625} = 25, \qquad
  \cos\varphi = \frac{7}{25}, \quad \sin\varphi = -\frac{24}{25}
  \implies \varphi = -\arctan\frac{24}{7}
  $$

  (kąt $\varphi$ leży w IV ćwiartce, bo $\text{Re}(q) > 0$ i $\text{Im } q < 0$).

* **Krok 2 — moduł i kąty pierwiastków:**

  $$
  \rho = \sqrt{25} = 5, \qquad \varphi_k = \frac{\varphi}{2} + k\pi, \qquad k = 0, 1
  $$

  Wzory na połówki kąta (znaki wybieramy z ćwiartki: $\frac{\varphi}{2} \in \left(-\frac{\pi}{2}, 0\right)$,
  więc $\cos\frac{\varphi}{2} > 0$ i $\sin\frac{\varphi}{2} < 0$):

  $$
  \cos\frac{\varphi}{2} = \sqrt{\frac{1 + \cos\varphi}{2}} = \sqrt{\frac{32}{50}} = \frac45, \qquad
  \sin\frac{\varphi}{2} = -\sqrt{\frac{1 - \cos\varphi}{2}} = -\sqrt{\frac{18}{50}} = -\frac35
  $$

  Stąd

  $$
  z_0 = 5\left(\frac45 - j\frac35\right) = 4 - 3j, \qquad z_1 = -z_0 = -4 + 3j
  $$

* **Wynik:**

  $$
  \boxed{\sqrt{7 - 24j} = \pm(4 - 3j)}
  $$

* **Sprawdzenie.** Podniesienie do kwadratu:

  $$
  (4 - 3j)^2 = 16 - 24j + 9j^2 = 7 - 24j, \qquad (-4 + 3j)^2 = (4 - 3j)^2 = 7 - 24j
  $$

  Wzory Viète'a dla równania $z^2 - (7 - 24j) = 0$: suma pierwiastków
  $(4 - 3j) + (-4 + 3j) = 0$, iloczyn $(4 - 3j)(-4 + 3j) = -(7 - 24j) = -7 + 24j = (-1)^{2+1}q$.
  Oba pierwiastki mają moduł $5$ i leżą na okręgu o środku $0$ i promieniu $5$, w punktach
  $(4, -3)$ i $(-4, 3)$.

### 1.4

* **Dane:** $\sqrt[4]{3j - \sqrt3}$, czyli cztery pierwiastki czwartego stopnia z liczby
  $w = -\sqrt3 + 3j$.
* **Krok 1 — moduł i argument:**

  $$
  r = \lvert w\rvert = \sqrt{3 + 9} = \sqrt{12} = 2\sqrt3, \qquad
  \cos\varphi = \frac{-\sqrt3}{2\sqrt3} = -\frac12, \quad
  \sin\varphi = \frac{3}{2\sqrt3} = \frac{\sqrt3}{2} \implies \varphi = \frac{2\pi}{3}
  $$

* **Krok 2 — moduł i kąty pierwiastków:**

  $$
  \rho = \sqrt[4]{2\sqrt3} = \sqrt[8]{12} \approx 1{,}3643, \qquad
  \varphi_k = \frac{\frac{2\pi}{3} + 2k\pi}{4} = \frac{\pi}{6} + \frac{k\pi}{2},
  \qquad k = 0, 1, 2, 3
  $$

* **Wynik:**

  $$
  \boxed{z_k = \sqrt[8]{12}\left(\cos\left(\frac{\pi}{6} + \frac{k\pi}{2}\right)
  + j\sin\left(\frac{\pi}{6} + \frac{k\pi}{2}\right)\right), \qquad k = 0, 1, 2, 3}
  $$

| $k$ | Kąt $\varphi_k$ | Wartość dokładna | Przybliżenie |
| :---: | :---: | :--- | :--- |
| $0$ | $\frac{\pi}{6}$ | $\frac{\sqrt[8]{12}}{2}\left(\sqrt3 + j\right)$ | $1{,}1815 + 0{,}6821j$ |
| $1$ | $\frac{2\pi}{3}$ | $\frac{\sqrt[8]{12}}{2}\left(-1 + j\sqrt3\right)$ | $-0{,}6821 + 1{,}1815j$ |
| $2$ | $\frac{7\pi}{6}$ | $-\frac{\sqrt[8]{12}}{2}\left(\sqrt3 + j\right)$ | $-1{,}1815 - 0{,}6821j$ |
| $3$ | $\frac{5\pi}{3}$ | $\frac{\sqrt[8]{12}}{2}\left(1 - j\sqrt3\right)$ | $0{,}6821 - 1{,}1815j$ |

* **Interpretacja geometryczna.** Cztery pierwiastki to wierzchołki kwadratu wpisanego w okrąg
  o środku $0$ i promieniu $\rho = \sqrt[8]{12}$; kolejne kąty różnią się o $\frac{\pi}{2}$,
  a punkty $z_2 = -z_0$ i $z_3 = -z_1$ są antypodyczne.
* **Sprawdzenie.** Dla $k = 0$: $\lvert z_0\rvert^4 = \rho^4 = 2\sqrt3$ oraz
  $4\varphi_0 = \frac{2\pi}{3}$, więc

  $$
  z_0^4 = 2\sqrt3\left(\cos\frac{2\pi}{3} + j\sin\frac{2\pi}{3}\right)
  = 2\sqrt3\left(-\frac12 + j\frac{\sqrt3}{2}\right) = -\sqrt3 + 3j
  $$

  Wzory Viète'a dla $z^4 - w = 0$: suma czterech pierwiastków równa się $0$ (brak wyrazu $z^3$),
  a ich iloczyn wynosi

  $$
  z_0z_1z_2z_3 = (z_0z_1)^2 = \left(\rho^2 e^{j\frac{5\pi}{6}}\right)^2
  = 2\sqrt3 \cdot e^{j\frac{5\pi}{3}} = 2\sqrt3\left(\frac12 - j\frac{\sqrt3}{2}\right)
  = \sqrt3 - 3j = -w
  $$

  zgodnie z przewidywaną wartością $(-1)^{4+1}w = -w$.

### 1.5

* **Dane:** $\sqrt[3]{-4 + 3j}$; zgodnie z poleceniem argument wyznaczamy kalkulatorem.
* **Krok 1 — moduł i argument:**

  $$
  r = \lvert -4 + 3j\rvert = \sqrt{16 + 9} = 5, \qquad
  \cos\alpha = -\frac45, \quad \sin\alpha = \frac35
  \implies \alpha = \pi - \arctan\frac34 \approx 2{,}4981\ \text{rad}
  $$

  Kąt $\alpha$ leży w II ćwiartce ($\text{Re} < 0$, $\text{Im} > 0$); przybliżenie podano do
  czterech miejsc po przecinku, a wartość dokładna to $\alpha = \pi - \arctan\frac34$
  (również $\alpha = \pi - \arcsin\frac35$, bo trójkąt $3$–$4$–$5$).

* **Krok 2 — moduł i kąty pierwiastków:**

  $$
  \rho = \sqrt[3]{5} \approx 1{,}7100, \qquad
  \varphi_k = \frac{\alpha + 2k\pi}{3}, \qquad k = 0, 1, 2
  $$

* **Wynik:**

  $$
  \boxed{z_k = \sqrt[3]{5}\left(\cos\frac{\alpha + 2k\pi}{3} + j\sin\frac{\alpha + 2k\pi}{3}\right),
  \qquad k = 0, 1, 2, \qquad \alpha = \pi - \arctan\frac34 \approx 2{,}4981\ \text{rad}}
  $$

| $k$ | Kąt $\varphi_k$ (dokładnie) | $\varphi_k$ w radianach | $z_k$ (przybliżenie) |
| :---: | :--- | :---: | :--- |
| $0$ | $\frac{1}{3}\left(\pi - \arctan\frac34\right)$ | $0{,}8327$ | $1{,}1506 + 1{,}2650j$ |
| $1$ | $\frac{1}{3}\left(\pi - \arctan\frac34 + 2\pi\right)$ | $2{,}9271$ | $-1{,}6708 + 0{,}3640j$ |
| $2$ | $\frac{1}{3}\left(\pi - \arctan\frac34 + 4\pi\right)$ | $5{,}0215$ | $0{,}5202 - 1{,}6289j$ |

* **Interpretacja geometryczna.** Trzy pierwiastki to wierzchołki trójkąta równobocznego
  wpisanego w okrąg o środku $0$ i promieniu $\sqrt[3]{5}$: kąty różnią się o $\frac{2\pi}{3}$.
* **Sprawdzenie.** Dla każdego $k$ zachodzi $3\varphi_k = \alpha + 2k\pi$ oraz
  $\lvert z_k\rvert^3 = 5$, czyli

  $$
  z_k^3 = 5\left(\cos\alpha + j\sin\alpha\right) = 5\left(-\frac45 + j\frac35\right) = -4 + 3j
  $$

  Numerycznie: $(1{,}1506 + 1{,}2650j)^3 \approx -4 + 3j$, $(-1{,}6708 + 0{,}3640j)^3 \approx -4 + 3j$,
  $(0{,}5202 - 1{,}6289j)^3 \approx -4 + 3j$. Suma pierwiastków wynosi $0$ (brak wyrazu $z^2$
  w równaniu $z^3 + 4 - 3j = 0$), a ich iloczyn to $(-1)^{3+1}w = -4 + 3j$.

### 1.6

* **Dane:** $\sqrt[5]{(1 - j\sqrt3)(2j - 2)}$, czyli pięć pierwiastków piątego stopnia z iloczynu
  $w = (1 - j\sqrt3)(2j - 2)$.
* **Krok 1 — iloczyn w postaci algebraicznej:**

  $$
  w = (1 - \sqrt3 j)(-2 + 2j) = -2 + 2j + 2\sqrt3 j - 2\sqrt3 j^2
  = (2\sqrt3 - 2) + (2 + 2\sqrt3)j
  $$

* **Krok 2 — moduł i argument iloczynu** (z postaci trygonometrycznej czynników):

  $$
  1 - \sqrt3 j = 2\left(\cos\left(-\frac{\pi}{3}\right) + j\sin\left(-\frac{\pi}{3}\right)\right),
  \qquad
  2j - 2 = 2\sqrt2\left(\cos\frac{3\pi}{4} + j\sin\frac{3\pi}{4}\right)
  $$

  $$
  r = 2 \cdot 2\sqrt2 = 4\sqrt2 = 2^{5/2}, \qquad
  \varphi = -\frac{\pi}{3} + \frac{3\pi}{4} = \frac{-4\pi + 9\pi}{12} = \frac{5\pi}{12}
  $$

  Kontrola algebraiczna: $(2\sqrt3 - 2)^2 + (2 + 2\sqrt3)^2 = (16 - 8\sqrt3) + (16 + 8\sqrt3) = 32$,
  więc $\lvert w\rvert = \sqrt{32} = 4\sqrt2$; obie współrzędne są dodatnie, skąd potwierdzenie,
  że $\varphi \in \left(0, \frac{\pi}{2}\right)$.

* **Krok 3 — moduł i kąty pierwiastków:**

  $$
  \rho = \sqrt[5]{2^{5/2}} = 2^{1/2} = \sqrt2, \qquad
  \varphi_k = \frac{\frac{5\pi}{12} + 2k\pi}{5} = \frac{\pi}{12} + \frac{2k\pi}{5},
  \qquad k = 0, 1, 2, 3, 4
  $$

  Kąt początkowy to $\frac{\pi}{12} = \frac{5\pi}{60}$, a odstęp między kolejnymi kątami wynosi
  $\frac{2\pi}{5} = \frac{24\pi}{60}$, skąd kąty $\frac{5\pi}{60}$, $\frac{29\pi}{60}$,
  $\frac{53\pi}{60}$, $\frac{77\pi}{60}$ i $\frac{101\pi}{60}$.

* **Wynik:**

  $$
  \boxed{z_k = \sqrt2\left(\cos\left(\frac{\pi}{12} + \frac{2k\pi}{5}\right)
  + j\sin\left(\frac{\pi}{12} + \frac{2k\pi}{5}\right)\right), \qquad k = 0, 1, 2, 3, 4}
  $$

| $k$ | Kąt $\varphi_k$ | Wartość dokładna | Przybliżenie |
| :---: | :---: | :--- | :--- |
| $0$ | $\frac{5\pi}{60} = \frac{\pi}{12}$ | $\frac{\sqrt3 + 1}{2} + j\frac{\sqrt3 - 1}{2}$ | $1{,}3660 + 0{,}3660j$ |
| $1$ | $\frac{29\pi}{60}$ | $\sqrt2\left(\cos\frac{29\pi}{60} + j\sin\frac{29\pi}{60}\right)$ | $0{,}0740 + 1{,}4123j$ |
| $2$ | $\frac{53\pi}{60}$ | $\sqrt2\left(\cos\frac{53\pi}{60} + j\sin\frac{53\pi}{60}\right)$ | $-1{,}3203 + 0{,}5068j$ |
| $3$ | $\frac{77\pi}{60}$ | $\sqrt2\left(\cos\frac{77\pi}{60} + j\sin\frac{77\pi}{60}\right)$ | $-0{,}8900 - 1{,}0991j$ |
| $4$ | $\frac{101\pi}{60}$ | $\sqrt2\left(\cos\frac{101\pi}{60} + j\sin\frac{101\pi}{60}\right)$ | $0{,}7702 - 1{,}1861j$ |

  Wartość dokładna dla $k = 0$ wynika z $\cos\frac{\pi}{12} = \frac{\sqrt6 + \sqrt2}{4}$
  i $\sin\frac{\pi}{12} = \frac{\sqrt6 - \sqrt2}{4}$:

  $$
  \sqrt2 \cdot \frac{\sqrt6 + \sqrt2}{4} = \frac{\sqrt{12} + 2}{4} = \frac{\sqrt3 + 1}{2}, \qquad
  \sqrt2 \cdot \frac{\sqrt6 - \sqrt2}{4} = \frac{\sqrt{12} - 2}{4} = \frac{\sqrt3 - 1}{2}
  $$

  Kąty $\frac{29\pi}{60}$, $\frac{53\pi}{60}$, $\frac{77\pi}{60}$ i $\frac{101\pi}{60}$ nie są
  kątami specjalnymi, więc pozostałe pierwiastki zostawiamy w postaci trygonometrycznej.

* **Interpretacja geometryczna.** Pięć pierwiastków to wierzchołki pięciokąta foremnego
  na okręgu o środku $0$ i promieniu $\sqrt2$, obróconego o kąt początkowy $\frac{\pi}{12}$.
* **Sprawdzenie.** Dla $k = 0$: $\lvert z_0\rvert^5 = \left(\sqrt2\right)^5 = 4\sqrt2$ oraz
  $5\varphi_0 = \frac{5\pi}{12}$, więc

  $$
  z_0^5 = 4\sqrt2\left(\cos\frac{5\pi}{12} + j\sin\frac{5\pi}{12}\right)
  = 4\sqrt2\left(\frac{\sqrt6 - \sqrt2}{4} + j\frac{\sqrt6 + \sqrt2}{4}\right)
  = (2\sqrt3 - 2) + (2 + 2\sqrt3)j
  $$

  czyli dokładnie liczba $w$ spod pierwiastka. Suma pięciu pierwiastków wynosi $0$ (brak wyrazu
  $z^4$ w równaniu $z^5 - w = 0$), a ich iloczyn to $(-1)^{5+1}w = w$.

---

## Zadanie 2 — wzór Moivre'a: $\sin 4x$ i $\cos 4x$

* **Krok 1 — wzór Moivre'a dla $n = 4$ i dowolnego rzeczywistego $x$:**

  $$
  (\cos x + j\sin x)^4 = \cos 4x + j\sin 4x
  $$

* **Krok 2 — rozwinięcie lewej strony dwumianem Newtona:**

  $$
  (\cos x + j\sin x)^4 = \cos^4 x + 4j\cos^3 x \sin x + 6j^2\cos^2 x \sin^2 x
  + 4j^3\cos x \sin^3 x + j^4\sin^4 x
  $$

* **Krok 3 — uporządkowanie po $j^2 = -1$, $j^3 = -j$, $j^4 = 1$:**

  $$
  (\cos x + j\sin x)^4 = \left(\cos^4 x - 6\cos^2 x \sin^2 x + \sin^4 x\right)
  + j\left(4\cos^3 x \sin x - 4\cos x \sin^3 x\right)
  $$

* **Krok 4 — porównanie części rzeczywistych i urojonych:**

  $$
  \boxed{\cos 4x = \cos^4 x - 6\cos^2 x \sin^2 x + \sin^4 x}
  $$

  $$
  \boxed{\sin 4x = 4\cos^3 x \sin x - 4\cos x \sin^3 x
  = 4\sin x \cos x\left(\cos^2 x - \sin^2 x\right)}
  $$

* **Postacie równoważne** (po skorzystaniu z $\cos^2 x + \sin^2 x = 1$):

  $$
  \cos 4x = 8\cos^4 x - 8\cos^2 x + 1 = 8\sin^4 x - 8\sin^2 x + 1 = 1 - 8\sin^2 x \cos^2 x
  $$

  $$
  \sin 4x = 4\sin x \cos x\left(1 - 2\sin^2 x\right) = 2\sin 2x \cos 2x
  $$

* **Sprawdzenie.** Dla $x = \frac{\pi}{6}$ mamy $\cos x = \frac{\sqrt3}{2}$, $\sin x = \frac12$:

  $$
  \cos 4x = \cos\frac{2\pi}{3} = -\frac12, \qquad
  \left(\frac{\sqrt3}{2}\right)^4 - 6\left(\frac{\sqrt3}{2}\right)^2\left(\frac12\right)^2
  + \left(\frac12\right)^4 = \frac{9}{16} - \frac{18}{16} + \frac{1}{16} = -\frac{8}{16} = -\frac12
  $$

  $$
  \sin 4x = \sin\frac{2\pi}{3} = \frac{\sqrt3}{2}, \qquad
  4 \cdot \frac12 \cdot \frac{\sqrt3}{2}\left(\frac34 - \frac14\right) = \frac{\sqrt3}{2}
  $$

  Dla $x = \frac{\pi}{4}$: $\cos 4x = \cos\pi = -1$, a wzór daje
  $\frac14 - 6 \cdot \frac12 \cdot \frac12 + \frac14 = -1$; $\sin 4x = \sin\pi = 0$, a wzór daje
  $4 \cdot \frac{1}{\sqrt2} \cdot \frac{1}{\sqrt2} \cdot 0 = 0$. Obie tożsamości potwierdzono
  również symbolicznie (`sympy`): różnica lewej i prawej strony po uproszczeniu jest zerem.

---

## Zadanie 3 — równania w $\mathbb{C}$ i szkice zbiorów rozwiązań

Rozwiązujemy w zbiorze $\mathbb{C}$. Dla każdego równania podano pełny zbiór rozwiązań
(w postaci algebraicznej i trygonometrycznej) oraz dane do szkicu: tabelę współrzędnych
i opis figury.

### 3.1

* **Dane:** $(z^4 - 16)(z^2 - 4j + 3) = 0$.
* **Krok 1 — rozkład na czynniki.** Iloczyn jest równy zeru wtedy i tylko wtedy, gdy zeruje się
  co najmniej jeden czynnik:

  $$
  z^4 = 16 \quad \text{lub} \quad z^2 - 4j + 3 = 0
  $$

* **Krok 2 — pierwszy czynnik:** $16 = 16(\cos 0 + j\sin 0)$, więc

  $$
  z_k = 2\left(\cos\frac{k\pi}{2} + j\sin\frac{k\pi}{2}\right), \quad k = 0, 1, 2, 3
  \implies z \in \{2, 2j, -2, -2j\}
  $$

* **Krok 3 — drugi czynnik:** $z^2 = -3 + 4j$. Niech $z = a + bj$; wówczas

  $$
  a^2 - b^2 = -3, \qquad 2ab = 4, \qquad a^2 + b^2 = \lvert -3 + 4j\rvert = 5
  $$

  Dodając pierwsze i trzecie równanie: $2a^2 = 2$, czyli $a^2 = 1$ i $b^2 = 4$; z warunku
  $ab = 2 > 0$ liczby $a$ i $b$ mają ten sam znak, więc $z = \pm(1 + 2j)$.

* **Wynik:**

  $$
  \boxed{z \in \{2, 2j, -2, -2j, 1 + 2j, -1 - 2j\}}
  $$

* **Szkic zbioru rozwiązań** (sześć punktów):

| Punkt | $z$ | $(\text{Re}(z), \text{Im } z)$ | $\lvert z\rvert$ |
| :---: | :--- | :---: | :---: |
| $A$ | $2$ | $(2, 0)$ | $2$ |
| $B$ | $2j$ | $(0, 2)$ | $2$ |
| $C$ | $-2$ | $(-2, 0)$ | $2$ |
| $D$ | $-2j$ | $(0, -2)$ | $2$ |
| $E$ | $1 + 2j$ | $(1, 2)$ | $\sqrt5$ |
| $F$ | $-1 - 2j$ | $(-1, -2)$ | $\sqrt5$ |

```text
                  Im
                  ^
          (0, 2)  |  * (1, 2)
             *    |
                  |
   *--------------+--------------*-----> Re
 (-2, 0)         (0, 0)        (2, 0)
                  |
    (-1, -2) *    * (0, -2)
```

  Cztery punkty $A, B, C, D$ to wierzchołki kwadratu na okręgu o promieniu $2$, leżące na osiach
  układu; punkty $E$ i $F$ są antypodyczne względem początku układu i leżą na okręgu o promieniu
  $\sqrt5$. Wszystkie sześć punktów należy do zbioru (zbiór skończony — punkty zaznaczamy
  wypełnionymi kropkami).

* **Sprawdzenie.** $(\pm2)^4 - 16 = 0$, $(\pm2j)^4 - 16 = 16 - 16 = 0$ oraz
  $(1 + 2j)^2 - 4j + 3 = -3 + 4j - 4j + 3 = 0$, $(-1 - 2j)^2 - 4j + 3 = (1 + 2j)^2 - 4j + 3 = 0$.

### 3.2

* **Dane:** $\lvert z\rvert^2 + z = 7 - j$.
* **Krok 1 — podstawienie $z = x + jy$, $x, y \in \mathbb{R}$:**

  $$
  \lvert z\rvert^2 + z = x^2 + y^2 + x + jy = 7 - j
  $$

* **Krok 2 — porównanie części urojonych i rzeczywistych:**

  $$
  y = -1, \qquad x^2 + (-1)^2 + x = 7 \iff x^2 + x - 6 = 0 \iff (x + 3)(x - 2) = 0
  $$

  czyli $x = 2$ albo $x = -3$.

* **Wynik:**

  $$
  \boxed{z = 2 - j \quad \text{lub} \quad z = -3 - j}
  $$

* **Postać trygonometryczna i szkic:**

| $z$ | $(\text{Re}(z), \text{Im } z)$ | $\lvert z\rvert$ | Argument główny |
| :--- | :---: | :---: | :---: |
| $2 - j$ | $(2, -1)$ | $\sqrt5$ | $-\arctan\frac12$ |
| $-3 - j$ | $(-3, -1)$ | $\sqrt{10}$ | $-\pi + \arctan\frac13$ |

```text
                  Im
                  ^
   ---------------+---------------------------> Re
                  |
   (-3, -1) *     |     * (2, -1)
```

  Oba punkty leżą na prostej $y = -1$ (zbiór rozwiązań jest przecięciem tej prostej z okręgiem
  $\left(x + \frac12\right)^2 + y^2 = \frac{29}{4}$, bo $x^2 + y^2 + x = 7$ po dopełnieniu
  do kwadratu daje $\left(x + \frac12\right)^2 + y^2 = \frac{29}{4}$). Punkty należą do zbioru —
  zaznaczamy je wypełnionymi kropkami.

* **Sprawdzenie.** $\lvert 2 - j\rvert^2 + (2 - j) = 5 + 2 - j = 7 - j$ oraz
  $\lvert -3 - j\rvert^2 + (-3 - j) = 10 - 3 - j = 7 - j$.

### 3.3

* **Dane:** $z^4\lvert z\rvert = -8\overline{z}^{\,2}$.
* **Krok 1 — porównanie modułów** (korzystamy z $\lvert\overline{z}\rvert = \lvert z\rvert$):

  $$
  \lvert z\rvert^4 \cdot \lvert z\rvert = 8\left\lvert\overline{z}\right\rvert^2
  \iff \lvert z\rvert^5 = 8\lvert z\rvert^2
  \iff \lvert z\rvert^2\left(\lvert z\rvert^3 - 8\right) = 0
  \iff \lvert z\rvert = 0 \quad \text{lub} \quad \lvert z\rvert = 2
  $$

* **Krok 2 — przypadek $\lvert z\rvert = 0$:** $z = 0$ daje $0 = 0$, więc $z = 0$ jest rozwiązaniem.
* **Krok 3 — przypadek $\lvert z\rvert = 2$.** Niech $z = 2(\cos\varphi + j\sin\varphi)$. Wtedy
  $\overline{z}^{\,2} = 4(\cos 2\varphi - j\sin 2\varphi)$ oraz $z^4 = 16(\cos 4\varphi + j\sin 4\varphi)$,
  więc równanie przyjmuje postać

  $$
  32(\cos 4\varphi + j\sin 4\varphi) = -32(\cos 2\varphi - j\sin 2\varphi)
  = 32\left(\cos(\pi - 2\varphi) + j\sin(\pi - 2\varphi)\right)
  $$

  a stąd

  $$
  4\varphi \equiv \pi - 2\varphi \pmod{2\pi} \iff 6\varphi = \pi + 2k\pi
  \iff \varphi = \frac{\pi}{6} + \frac{k\pi}{3}, \qquad k = 0, 1, \ldots, 5
  $$

* **Wynik:**

  $$
  \boxed{z = 0 \quad \text{oraz} \quad
  z_k = 2\left(\cos\left(\frac{\pi}{6} + \frac{k\pi}{3}\right)
  + j\sin\left(\frac{\pi}{6} + \frac{k\pi}{3}\right)\right), \quad k = 0, 1, \ldots, 5}
  $$

| $k$ | Kąt $\varphi_k$ | Rozwiązanie $z_k$ | $(\text{Re}(z), \text{Im } z)$ |
| :---: | :---: | :--- | :---: |
| $0$ | $\frac{\pi}{6}$ | $\sqrt3 + j$ | $(\sqrt3, 1)$ |
| $1$ | $\frac{\pi}{2}$ | $2j$ | $(0, 2)$ |
| $2$ | $\frac{5\pi}{6}$ | $-\sqrt3 + j$ | $(-\sqrt3, 1)$ |
| $3$ | $\frac{7\pi}{6}$ | $-\sqrt3 - j$ | $(-\sqrt3, -1)$ |
| $4$ | $\frac{3\pi}{2}$ | $-2j$ | $(0, -2)$ |
| $5$ | $\frac{11\pi}{6}$ | $\sqrt3 - j$ | $(\sqrt3, -1)$ |

* **Szkic zbioru rozwiązań** (siedem punktów: początek układu i sześciokąt foremny na okręgu
  o promieniu $2$):

```text
                  Im
                  ^
   (-V3, 1) *     |  * (0, 2)  *  (V3, 1)
               \  |  /
                \ | /
   ----------------O------------------> Re
                / | \        (0, 0)
               /  |  \
   (-V3, -1) *    *     * (V3, -1)
                (0, -2)
```

  (V3 oznacza $\sqrt3$.) Sześć punktów niezerowych to wierzchołki sześciokąta foremnego
  wpisanego w okrąg o środku $0$ i promieniu $2$, obrócone o $\frac{\pi}{6}$ względem osi
  rzeczywistej; siódmym punktem jest środek tego okręgu.

* **Sprawdzenie.** Dla $z = \sqrt3 + j$: $z^2 = 2 + 2\sqrt3 j$, $z^4 = -8 + 8\sqrt3 j$,
  $\lvert z\rvert = 2$, więc lewa strona to $-16 + 16\sqrt3 j$; prawa strona to
  $-8\left(\sqrt3 - j\right)^2 = -8\left(2 - 2\sqrt3 j\right) = -16 + 16\sqrt3 j$. Równość zachodzi.
  Podobnie dla pozostałych kątów (warunek $6\varphi \equiv \pi \pmod{2\pi}$).

### 3.4

* **Dane:** $z^2 - z = \dfrac{2j - 14}{j + 3}$; dziedzina: $j + 3 \ne 0$ (spełniona).
* **Krok 1 — uproszczenie prawej strony:**

  $$
  \frac{2j - 14}{j + 3} = \frac{(-14 + 2j)(3 - j)}{(3 + j)(3 - j)}
  = \frac{-42 + 14j + 6j - 2j^2}{10} = \frac{-40 + 20j}{10} = -4 + 2j
  $$

* **Krok 2 — równanie kwadratowe i jego wyróżnik:**

  $$
  z^2 - z + 4 - 2j = 0, \qquad \Delta = 1 - 4(4 - 2j) = -15 + 8j
  $$

* **Krok 3 — pierwiastek z wyróżnika.** Szukamy $(a + bj)^2 = -15 + 8j$:

  $$
  a^2 - b^2 = -15, \qquad 2ab = 8, \qquad a^2 + b^2 = \lvert\Delta\rvert = 17
  $$

  Dodając pierwsze i trzecie równanie: $2a^2 = 2$, czyli $a^2 = 1$ i $b^2 = 16$; z warunku
  $ab = 4 > 0$ mamy $\sqrt{\Delta} = \pm(1 + 4j)$. Rzeczywiście:
  $(1 + 4j)^2 = 1 + 8j + 16j^2 = -15 + 8j$.

* **Krok 4 — wzory na pierwiastki równania:**

  $$
  z = \frac{1 \pm (1 + 4j)}{2} \implies z_1 = \frac{2 + 4j}{2} = 1 + 2j, \qquad
  z_2 = \frac{-4j}{2} = -2j
  $$

* **Wynik:**

  $$
  \boxed{z = 1 + 2j \quad \text{lub} \quad z = -2j}
  $$

* **Szkic zbioru rozwiązań** (dwa punkty):

| $z$ | $(\text{Re}(z), \text{Im } z)$ | $\lvert z\rvert$ | Argument główny |
| :--- | :---: | :---: | :---: |
| $1 + 2j$ | $(1, 2)$ | $\sqrt5$ | $\arctan 2$ |
| $-2j$ | $(0, -2)$ | $2$ | $-\frac{\pi}{2}$ |

```text
                  Im
                  ^
          (1, 2)  |
             *    |
                  |
   ---------------+---------------------> Re
                  |
                  * (0, -2)
```

* **Sprawdzenie.** $(1 + 2j)^2 - (1 + 2j) = -3 + 4j - 1 - 2j = -4 + 2j$ oraz
  $(-2j)^2 - (-2j) = -4 + 2j$ — obie wartości są równe prawej stronie.

### 3.5

* **Dane:** $(z - j)^4 = \left(\sqrt3 + j\right)^6$.
* **Krok 1 — prawa strona w postaci trygonometrycznej:**

  $$
  \sqrt3 + j = 2\left(\cos\frac{\pi}{6} + j\sin\frac{\pi}{6}\right) \implies
  \left(\sqrt3 + j\right)^6 = 2^6\left(\cos\pi + j\sin\pi\right) = -64
  $$

* **Krok 2 — podstawienie $w = z - j$:** równanie $w^4 = -64 = 64(\cos\pi + j\sin\pi)$ ma cztery
  rozwiązania o module $\sqrt[4]{64} = 2\sqrt2$ i kątach $\frac{\pi + 2k\pi}{4} = \frac{\pi}{4} + \frac{k\pi}{2}$:

  $$
  w_k = 2\sqrt2\left(\cos\left(\frac{\pi}{4} + \frac{k\pi}{2}\right)
  + j\sin\left(\frac{\pi}{4} + \frac{k\pi}{2}\right)\right), \quad k = 0, 1, 2, 3
  \implies w \in \{2 + 2j, -2 + 2j, -2 - 2j, 2 - 2j\}
  $$

* **Krok 3 — powrót do $z = w + j$:**

  $$
  z \in \{2 + 3j, -2 + 3j, -2 - j, 2 - j\}
  $$

* **Wynik:**

  $$
  \boxed{z \in \{2 + 3j, -2 + 3j, -2 - j, 2 - j\}}
  $$

* **Szkic zbioru rozwiązań** (kwadrat o boku $4$ i środku w punkcie $j$):

| $z$ | $(\text{Re}(z), \text{Im } z)$ | $\lvert z\rvert$ | $\lvert z - j\rvert$ |
| :--- | :---: | :---: | :---: |
| $2 + 3j$ | $(2, 3)$ | $\sqrt{13}$ | $2\sqrt2$ |
| $-2 + 3j$ | $(-2, 3)$ | $\sqrt{13}$ | $2\sqrt2$ |
| $-2 - j$ | $(-2, -1)$ | $\sqrt5$ | $2\sqrt2$ |
| $2 - j$ | $(2, -1)$ | $\sqrt5$ | $2\sqrt2$ |

```text
                  Im
                  ^
    (-2, 3) *-------------* (2, 3)
             |     *      |
             |   (0, 1)   |
   ----------+------------+------------> Re
             |            |
   (-2, -1) *--------------* (2, -1)
```

  Cztery punkty tworzą kwadrat o boku $4$, środku $j = (0, 1)$ i promieniu okręgu opisanego
  $2\sqrt2$; jego boki są równoległe do osi układu, a przekątna ma długość $4\sqrt2$.

* **Sprawdzenie.** Dla $z = 2 + 3j$: $w = z - j = 2 + 2j$, $w^2 = 8j$, $w^4 = -64$ — zgodnie
  z prawą stroną. Dla $z = -2 - j$: $w = -2 - 2j$, $w^2 = 8j$, $w^4 = -64$. Podobnie dla
  pozostałych dwóch rozwiązań ($w = -2 + 2j$ i $w = 2 - 2j$ dają $w^2 = -8j$ oraz $w^4 = -64$).

### 3.6

* **Dane:** $z^4 = -\overline{z}^{\,4}$, czyli $z^4 + \overline{z}^{\,4} = 0$.
* **Krok 1 — porównanie modułów.** Ponieważ $\left\lvert\overline{z}\right\rvert = \lvert z\rvert$, dla
  każdego $z$ zachodzi

  $$
  \left\lvert z^4\right\rvert = \left\lvert\overline{z}^{\,4}\right\rvert = \lvert z\rvert^4
  $$

  więc moduł nie jest niczym ograniczony — o zbiorze rozwiązań decyduje argument.
* **Krok 2 — postać trygonometryczna.** Niech $z = r(\cos\varphi + j\sin\varphi)$, $r \ge 0$.
  Wtedy $\overline{z}^{\,4} = r^4(\cos 4\varphi - j\sin 4\varphi)$ i równanie ma postać

  $$
  r^4(\cos 4\varphi + j\sin 4\varphi) = -r^4(\cos 4\varphi - j\sin 4\varphi)
  = r^4\left(\cos(\pi - 4\varphi) + j\sin(\pi - 4\varphi)\right)
  $$

* **Krok 3 — przypadek $r = 0$:** $z = 0$ spełnia równanie ($0 = 0$).
* **Krok 4 — przypadek $r > 0$:** po skróceniu przez $r^4$ otrzymujemy

  $$
  4\varphi \equiv \pi - 4\varphi \pmod{2\pi} \iff 8\varphi = \pi + 2k\pi
  \iff \varphi = \frac{\pi}{8} + \frac{k\pi}{4}, \qquad k = 0, 1, \ldots, 7
  $$

  Każde $r > 0$ jest dopuszczalne, więc zbiór rozwiązań tworzy osiem półprostych
  wychodzących z początku układu, czyli cztery proste przechodzące przez początek.

* **Wynik:**

  $$
  \boxed{z = t\left(\cos\left(\frac{\pi}{8} + \frac{k\pi}{4}\right)
  + j\sin\left(\frac{\pi}{8} + \frac{k\pi}{4}\right)\right), \qquad t \ge 0, \quad k = 0, 1, \ldots, 7}
  $$

  (dla $t = 0$ wszystkie osiem półprostych daje ten sam punkt $z = 0$).

* **Postać kartezjańska.** Z $z^4 + \overline{z}^{\,4} = 2\,\text{Re}\left(z^4\right) = 0$ oraz

  $$
  (x + jy)^4 = x^4 + 4jx^3y - 6x^2y^2 - 4jxy^3 + y^4
  $$

  otrzymujemy równanie $x^4 - 6x^2y^2 + y^4 = 0$, które po rozłożeniu na czynniki daje
  (bo $3 - 2\sqrt2 = \left(\sqrt2 - 1\right)^2$ i $3 + 2\sqrt2 = \left(\sqrt2 + 1\right)^2$):

  $$
  \left(y^2 - \left(3 - 2\sqrt2\right)x^2\right)\left(y^2 - \left(3 + 2\sqrt2\right)x^2\right) = 0
  \iff y = \pm\left(\sqrt2 - 1\right)x \quad \text{lub} \quad y = \pm\left(\sqrt2 + 1\right)x
  $$

| Prosta | Równanie | Kąty kierunkowe półprostych | Przykładowy punkt |
| :--- | :--- | :--- | :---: |
| $l_1$ | $y = \left(\sqrt2 - 1\right)x$ | $\frac{\pi}{8}$, $\frac{9\pi}{8}$ | $(1, \sqrt2 - 1)$ |
| $l_2$ | $y = \left(\sqrt2 + 1\right)x$ | $\frac{3\pi}{8}$, $\frac{11\pi}{8}$ | $(1, \sqrt2 + 1)$ |
| $l_3$ | $y = -\left(\sqrt2 + 1\right)x$ | $\frac{5\pi}{8}$, $\frac{13\pi}{8}$ | $(-1, \sqrt2 + 1)$ |
| $l_4$ | $y = -\left(\sqrt2 - 1\right)x$ | $\frac{7\pi}{8}$, $\frac{15\pi}{8}$ | $(-1, \sqrt2 - 1)$ |

* **Szkic zbioru rozwiązań** (osiem półprostych rozmieszczonych co $\frac{\pi}{4}$, wspólny
  początek w $z = 0$; szkic poglądowy — dokładne kąty w tabeli powyżej):

```text
                    Im
                    ^
               *    |    *
                 \  |  /
                  \ | /
   ------*----------O----------*---------> Re
                  / | \
                 /  |  \
               *    |    *
```

* **Brzegi.** Każda półprosta jest domknięta (zawiera punkt $z = 0$) i nieograniczona —
  rysujemy je linią **ciągłą**, wraz z zaznaczonym punktem $z = 0$.
* **Sprawdzenie.** Dla $\varphi = \frac{\pi}{8}$ i dowolnego $t > 0$:
  $z^4 = t^4 e^{j\frac{\pi}{2}} = t^4j$ oraz $-\overline{z}^{\,4} = -t^4e^{-j\frac{\pi}{2}} = t^4j$
  — równość zachodzi. Ogólnie warunek $8\varphi \equiv \pi \pmod{2\pi}$ gwarantuje
  $e^{4j\varphi} = -e^{-4j\varphi}$. Podstawienie kartezjańskie: dla punktu $(1, \sqrt2 - 1)$
  równanie $x^4 - 6x^2y^2 + y^4 = 0$ daje
  $1 - 6\left(3 - 2\sqrt2\right) + \left(3 - 2\sqrt2\right)^2 = 1 - 18 + 12\sqrt2 + 17 - 12\sqrt2 = 0$.

---

## Zadanie 4 — trójkąt równoboczny o danym wierzchołku i środku

### 4.1

* **Dane:** jeden wierzchołek $A = 5 - 2j$, środek trójkąta $S = 1 + 2j$.
* **Założenie.** W trójkącie równobocznym środek ciężkości, środek okręgu wpisanego i środek
  okręgu opisanego pokrywają się, więc pojęcie „środka” jest jednoznaczne; punkt $S$ jest
  środkiem okręgu opisanego i środkiem obrotu o $\frac{2\pi}{3}$ przenoszącego wierzchołki
  jeden na drugi.
* **Krok 1 — promień okręgu opisanego i kąt początkowy:**

  $$
  A - S = (5 - 2j) - (1 + 2j) = 4 - 4j, \qquad
  R = \lvert A - S\rvert = \sqrt{16 + 16} = 4\sqrt2, \qquad
  \alpha_0 = \arg(4 - 4j) = -\frac{\pi}{4}
  $$

* **Krok 2 — kąty pozostałych wierzchołków:**

  $$
  \alpha_k = -\frac{\pi}{4} + \frac{2k\pi}{3}, \qquad k = 0, 1, 2
  \implies \alpha_0 = -\frac{\pi}{4}, \quad \alpha_1 = \frac{5\pi}{12}, \quad
  \alpha_2 = -\frac{11\pi}{12}
  $$

* **Krok 3 — obrót wektora $A - S$ o $\pm\frac{2\pi}{3}$:** niech
  $\omega = \cos\frac{2\pi}{3} + j\sin\frac{2\pi}{3} = -\frac12 + j\frac{\sqrt3}{2}$. Wtedy

  $$
  (4 - 4j)\omega = (4 - 4j)\left(-\frac12 + j\frac{\sqrt3}{2}\right)
  = -2 + 2\sqrt3 j + 2j - 2\sqrt3 j^2 = (2\sqrt3 - 2) + (2\sqrt3 + 2)j
  $$

  $$
  (4 - 4j)\overline{\omega} = (4 - 4j)\left(-\frac12 - j\frac{\sqrt3}{2}\right)
  = -2 - 2\sqrt3 j + 2j + 2\sqrt3 j^2 = (-2 - 2\sqrt3) + (2 - 2\sqrt3)j
  $$

* **Krok 4 — dodanie środka $S$:**

  $$
  B = S + (A - S)\omega = (1 + 2j) + (2\sqrt3 - 2) + (2\sqrt3 + 2)j = (2\sqrt3 - 1) + (2\sqrt3 + 4)j
  $$

  $$
  C = S + (A - S)\overline{\omega} = (1 + 2j) + (-2 - 2\sqrt3) + (2 - 2\sqrt3)j
  = (-1 - 2\sqrt3) + (4 - 2\sqrt3)j
  $$

* **Wynik:**

  $$
  \boxed{B = (2\sqrt3 - 1) + (2\sqrt3 + 4)j, \qquad C = (-1 - 2\sqrt3) + (4 - 2\sqrt3)j}
  $$

  (kolejność $B$ i $C$ jest dowolna — odpowiada obu kierunkom obrotu).

| Wierzchołek | Wartość dokładna | Przybliżenie | $(\text{Re}, \text{Im})$ |
| :---: | :--- | :--- | :---: |
| $A$ | $5 - 2j$ | $5{,}0000 - 2{,}0000j$ | $(5, -2)$ |
| $B$ | $(2\sqrt3 - 1) + (2\sqrt3 + 4)j$ | $2{,}4641 + 7{,}4641j$ | $(2{,}4641, 7{,}4641)$ |
| $C$ | $(-1 - 2\sqrt3) + (4 - 2\sqrt3)j$ | $-4{,}4641 + 0{,}5359j$ | $(-4{,}4641, 0{,}5359)$ |
| $S$ | $1 + 2j$ | $1{,}0000 + 2{,}0000j$ | $(1, 2)$ |

* **Szkic** (rozmieszczenie poglądowe; trójkąt równoboczny o boku $4\sqrt6 \approx 9{,}7980$):

```text
                  Im
                  ^
                  |     * B (2,46; 7,46)
                  |
   * C (-4,46; 0,54)   * S (1, 2)
                  |
   ---------------+---------------------> Re
                  |
                  |            * A (5, -2)
```

* **Sprawdzenie — środek ciężkości:**

  $$
  \frac{A + B + C}{3} = \frac{\left(5 + 2\sqrt3 - 1 - 1 - 2\sqrt3\right)
  + j\left(-2 + 2\sqrt3 + 4 + 4 - 2\sqrt3\right)}{3} = \frac{3 + 6j}{3} = 1 + 2j = S
  $$

* **Sprawdzenie — długości boków:**

  $$
  \lvert A - B\rvert = \lvert A - S\rvert \cdot \lvert 1 - \omega\rvert
  = 4\sqrt2 \cdot \left\lvert \frac32 - j\frac{\sqrt3}{2}\right\rvert
  = 4\sqrt2 \cdot \sqrt{\frac94 + \frac34} = 4\sqrt2 \cdot \sqrt3 = 4\sqrt6
  $$

  Analogicznie $\lvert B - C\rvert = \lvert C - A\rvert = 4\sqrt6$, co jest zgodne ze wzorem
  $a = R\sqrt3$ na bok trójkąta równobocznego wpisanego w okrąg o promieniu $R$; numerycznie
  $a \approx 9{,}7980$. Wierzchołki leżą na okręgu o środku $S = 1 + 2j$ i promieniu $4\sqrt2$.

---

## Zadanie 5 — wartości zespolonych funkcji trygonometrycznych

* **Definicje** (przez funkcję wykładniczą; dla $z = a + jb$, $a, b \in \mathbb{R}$):

  $$
  \cos z = \frac{e^{jz} + e^{-jz}}{2}, \qquad \sin z = \frac{e^{jz} - e^{-jz}}{2j}
  $$

  $$
  \cos(a + jb) = \cos a \cosh b - j\sin a \sinh b, \qquad
  \sin(a + jb) = \sin a \cosh b + j\cos a \sinh b
  $$

  W szczególności $\cos(jb) = \cosh b$ i $\sin(jb) = j\sinh b$.

### 5.1 — $\cos(j\pi - \pi)$

* **Krok 1 — zapis w postaci $a + jb$:** $j\pi - \pi = -\pi + j\pi$, czyli $a = -\pi$, $b = \pi$.
* **Krok 2 — podstawienie do wzoru:**

  $$
  \cos(-\pi + j\pi) = \cos(-\pi)\cosh\pi - j\sin(-\pi)\sinh\pi = (-1)\cosh\pi - j \cdot 0 \cdot \sinh\pi = -\cosh\pi
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

  Wartość jest liczbą rzeczywistą ujemną, co potwierdza rachunek numeryczny:
  $\cosh\pi \approx 11{,}5920$.

### 5.2 — $\sin\left(\frac{\pi}{2} + 7j\right)$

* **Krok 1 — zapis w postaci $a + jb$:** $a = \frac{\pi}{2}$, $b = 7$.
* **Krok 2 — podstawienie do wzoru:**

  $$
  \sin\left(\frac{\pi}{2} + 7j\right) = \sin\frac{\pi}{2}\cosh 7 + j\cos\frac{\pi}{2}\sinh 7
  = 1 \cdot \cosh 7 + j \cdot 0 \cdot \sinh 7 = \cosh 7
  $$

* **Wynik:**

  $$
  \boxed{\sin\left(\frac{\pi}{2} + 7j\right) = \cosh 7 = \frac{e^{7} + e^{-7}}{2} \approx 548{,}3170}
  $$

* **Sprawdzenie (z definicji wykładniczej):**

  $$
  \sin\left(\frac{\pi}{2} + 7j\right) = \frac{e^{j\left(\frac{\pi}{2} + 7j\right)}
  - e^{-j\left(\frac{\pi}{2} + 7j\right)}}{2j}
  = \frac{e^{-7}e^{j\frac{\pi}{2}} - e^{7}e^{-j\frac{\pi}{2}}}{2j}
  = \frac{je^{-7} + je^{7}}{2j} = \frac{e^{7} + e^{-7}}{2} = \cosh 7
  $$

  Również ta wartość jest liczbą rzeczywistą (dodatnią), co potwierdza rachunek numeryczny:
  $\cosh 7 \approx 548{,}3170$.

---

## Podsumowanie wyników

| Podpunkt | Wynik |
| :--- | :--- |
| 1.1 | $8j$ |
| 1.2 | $2^{50}(1 - j) = 1\,125\,899\,906\,842\,624\,(1 - j)$ |
| 1.3 | $\pm(4 - 3j)$ |
| 1.4 | $z_k = \sqrt[8]{12}\left(\cos\left(\frac{\pi}{6} + \frac{k\pi}{2}\right) + j\sin\left(\frac{\pi}{6} + \frac{k\pi}{2}\right)\right)$, $k = 0, 1, 2, 3$ |
| 1.5 | $z_k = \sqrt[3]{5}\left(\cos\frac{\alpha + 2k\pi}{3} + j\sin\frac{\alpha + 2k\pi}{3}\right)$, $k = 0, 1, 2$, gdzie $\alpha = \pi - \arctan\frac34 \approx 2{,}4981$ rad |
| 1.6 | $z_k = \sqrt2\left(\cos\left(\frac{\pi}{12} + \frac{2k\pi}{5}\right) + j\sin\left(\frac{\pi}{12} + \frac{2k\pi}{5}\right)\right)$, $k = 0, 1, 2, 3, 4$ |
| 2 | $\cos 4x = \cos^4 x - 6\cos^2 x \sin^2 x + \sin^4 x$; $\sin 4x = 4\cos^3 x \sin x - 4\cos x \sin^3 x$ |
| 3.1 | $z \in \{2, 2j, -2, -2j, 1 + 2j, -1 - 2j\}$ |
| 3.2 | $z = 2 - j$ lub $z = -3 - j$ |
| 3.3 | $z = 0$ oraz $z_k = 2\left(\cos\left(\frac{\pi}{6} + \frac{k\pi}{3}\right) + j\sin\left(\frac{\pi}{6} + \frac{k\pi}{3}\right)\right)$, $k = 0, \ldots, 5$ |
| 3.4 | $z = 1 + 2j$ lub $z = -2j$ |
| 3.5 | $z \in \{2 + 3j, -2 + 3j, -2 - j, 2 - j\}$ |
| 3.6 | osiem półprostych $z = t\left(\cos\left(\frac{\pi}{8} + \frac{k\pi}{4}\right) + j\sin\left(\frac{\pi}{8} + \frac{k\pi}{4}\right)\right)$, $t \ge 0$, $k = 0, \ldots, 7$, czyli proste $y = \pm\left(\sqrt2 - 1\right)x$ i $y = \pm\left(\sqrt2 + 1\right)x$ |
| 4.1 | $B = (2\sqrt3 - 1) + (2\sqrt3 + 4)j$, $C = (-1 - 2\sqrt3) + (4 - 2\sqrt3)j$ |
| 5.1 | $\cos(j\pi - \pi) = -\cosh\pi \approx -11{,}5920$ |
| 5.2 | $\sin\left(\frac{\pi}{2} + 7j\right) = \cosh 7 \approx 548{,}3170$ |
