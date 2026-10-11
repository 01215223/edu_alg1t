# Algebra – Zestaw 1 – rozwiązania

> **Założenia i konwencje.** Jednostka urojona: $j$; sprzężenie: $\overline{z}$; moduł: $|z|$.
> Argument główny podajemy w konwencji $\arg(z) \in (-\pi, \pi]$; równoważne wartości w konwencji
> $[0, 2\pi)$ podajemy dodatkowo. Wszystkie wyniki są dokładne — przybliżeń dziesiętnych nie używamy.
>
> **Uwaga do treści zadania 6.** W pliku `zestaw1.md` nazwy funkcji `arcsin` i `arctg` są zapisane
> tekstem zwykłym (poza matematyką); w rozwiązaniach zapisujemy je jako wzory: $\arcsin$ oraz
> $\operatorname{arctg}$. Plik `zestaw1.md` różni się od `zestaw1a.md` wyłącznie tym zapisem,
> więc rozwiązania poniżej pokrywają również zestaw 1a.

---

## Zadanie 1

Dane są liczby:

$$z_1 = 3 + 2j, \qquad z_2 = 2 - 5j$$

### 1.1

* **Szukane:** $z_1^2 + jz_2$ oraz $\text{Re}(z_1 \cdot z_2)$.
* **Krok 1 — kwadrat $z_1$:**

  $$z_1^2 = (3 + 2j)^2 = 3^2 + 2 \cdot 3 \cdot 2j + (2j)^2 = 9 + 12j - 4 = 5 + 12j$$

* **Krok 2 — iloczyn $jz_2$:**

  $$jz_2 = j(2 - 5j) = 2j - 5j^2 = 2j + 5 = 5 + 2j$$

* **Krok 3 — suma:**

  $$z_1^2 + jz_2 = (5 + 12j) + (5 + 2j) = 10 + 14j$$

* **Krok 4 — iloczyn $z_1 z_2$ (osobno, dla części rzeczywistej):**

  $$z_1 z_2 = (3 + 2j)(2 - 5j) = 6 - 15j + 4j - 10j^2 = 6 - 11j + 10 = 16 - 11j$$

* **Wynik:**

  $$\boxed{z_1^2 + jz_2 = 10 + 14j, \qquad \text{Re}(z_1 z_2) = 16}$$

* **Sprawdzenie:** $\text{Im}(z_1 z_2) = 3 \cdot (-5) + 2 \cdot 2 = -11$ — zgodnie z uzyskanym wynikiem; $|10 + 14j| = \sqrt{296} = 2\sqrt{74}$.

---

### 1.2

* **Szukane:** $|2\overline{z}_1 + \text{Im } z_2|$; dziedzina: dowolne $z_1, z_2 \in \mathbb{C}$.
* **Sprzężenie:** $\overline{z}_1 = 3 - 2j$, zatem

  $$2\overline{z}_1 = 2(3 - 2j) = 6 - 4j$$

* **Część urojona $z_2$:** z postaci $z_2 = 2 - 5j$ mamy $\text{Im } z_2 = -5$; jest to liczba rzeczywista, dodajemy ją do części rzeczywistej.

  $$2\overline{z}_1 + \text{Im } z_2 = (6 - 4j) + (-5) = 1 - 4j$$

* **Moduł:**

  $$\left|2\overline{z}_1 + \text{Im } z_2\right| = |1 - 4j| = \sqrt{1^2 + (-4)^2} = \sqrt{17}$$

* **Wynik:**

  $$\boxed{\left|2\overline{z}_1 + \text{Im } z_2\right| = \sqrt{17}}$$

* **Sprawdzenie:** $|1 - 4j|^2 = 1 + 16 = 17$, czyli $\sqrt{17}$ jest wartością dokładną.

---

### 1.3

* **Szukane:** $\frac{\overline{z}_2 - j|z_1 + 2j|}{z_1}$; dziedzina: $z_1 \ne 0$ — dla $z_1 = 3 + 2j$ spełnione.
* **Sprzężenie:** $\overline{z}_2 = 2 + 5j$.
* **Moduł $|z_1 + 2j|$:**

  $$z_1 + 2j = (3 + 2j) + 2j = 3 + 4j, \qquad |3 + 4j| = \sqrt{3^2 + 4^2} = \sqrt{25} = 5$$

* **Licznik ułamka:**

  $$\overline{z}_2 - j|z_1 + 2j| = (2 + 5j) - 5j = 2$$

* **Dzielenie przez $z_1$ (mnożenie licznika i mianownika przez sprzężenie mianownika):**

  $$\frac{2}{3 + 2j} = \frac{2(3 - 2j)}{(3 + 2j)(3 - 2j)} = \frac{6 - 4j}{3^2 + 2^2} = \frac{6 - 4j}{13} = \frac{6}{13} - \frac{4}{13}j$$

* **Wynik:**

  $$\boxed{\frac{\overline{z}_2 - j|z_1 + 2j|}{z_1} = \frac{6}{13} - \frac{4}{13}j}$$

* **Sprawdzenie:** $\left(\frac{6}{13} - \frac{4}{13}j\right)(3 + 2j) = \frac{18 + 8}{13} + \frac{-12 + 12}{13}j = \frac{26}{13} = 2$ — zgadza się z licznikiem ułamka.

---

## Zadanie 2

W każdym podpunkcie rozstrzygamy, czy równość zachodzi dla **dowolnych** liczb zespolonych, oraz podajemy warunek, przy którym zachodzi.

### 2.1

* **Odpowiedź:** **TAK** — równość zachodzi dla dowolnych $z_1, z_2 \in \mathbb{C}$.
* **Uzasadnienie:** niech $z_1 = x_1 + jy_1$, $z_2 = x_2 + jy_2$, gdzie $x_1, x_2, y_1, y_2 \in \mathbb{R}$. Wtedy

  $$z_1 + z_2 = (x_1 + x_2) + j(y_1 + y_2) \implies \text{Im}(z_1 + z_2) = y_1 + y_2 = \text{Im } z_1 + \text{Im } z_2$$

* **Wniosek:** część urojona jest funkcją addytywną — równość jest tożsamością.

---

### 2.2

* **Odpowiedź:** **NIE** — równość na ogół nie zachodzi.
* **Kontrprzykład:** $z_1 = z_2 = j$. Wtedy

  $$\text{Re } z_1 \cdot \text{Re } z_2 = 0 \cdot 0 = 0, \qquad \text{Re}(z_1 z_2) = \text{Re}(j^2) = \text{Re}(-1) = -1$$

  czyli $\text{Re}(z_1 z_2) = -1 \ne 0 = \text{Re } z_1 \cdot \text{Re } z_2$.
* **Warunek równości:** dla $z_k = x_k + jy_k$ zachodzi

  $$\text{Re}(z_1 z_2) = x_1 x_2 - y_1 y_2 = \text{Re } z_1 \cdot \text{Re } z_2 - \text{Im } z_1 \cdot \text{Im } z_2$$

  więc równość zachodzi wtedy i tylko wtedy, gdy $\text{Im } z_1 \cdot \text{Im } z_2 = 0$, czyli gdy co najmniej jedna z liczb jest rzeczywista.

---

### 2.3

* **Odpowiedź:** **NIE** — dla dowolnych liczb zachodzi jedynie nierówność trójkąta $|z_1 + z_2| \le |z_1| + |z_2|$.
* **Kontrprzykład:** $z_1 = 1$, $z_2 = -1$. Wtedy

  $$|z_1 + z_2| = |1 - 1| = 0, \qquad |z_1| + |z_2| = 1 + 1 = 2, \qquad 0 \ne 2$$

* **Warunek równości:** $|z_1 + z_2| = |z_1| + |z_2|$ zachodzi wtedy i tylko wtedy, gdy $z_1 = 0$, lub $z_2 = 0$, lub $z_2 = t\,z_1$ dla pewnego $t \ge 0$ (liczby leżą na tej samej półprostej wychodzącej z początku układu).

---

### 2.4

* **Odpowiedź:** **TAK** — równość zachodzi dla dowolnego $z \in \mathbb{C}$.
* **Uzasadnienie:** niech $z = x + jy$, gdzie $x, y \in \mathbb{R}$; wtedy $\overline{z} = x - jy$ oraz $\text{Im } z = y$. Stąd

  $$z - \overline{z} = (x + jy) - (x - jy) = 2jy = 2j\,\text{Im } z$$

* **Interpretacja:** wynik jest liczbą czysto urojoną (jak $2j\,\text{Im } z$) — równość jest tożsamością.

---

## Zadanie 3

Zapisujemy liczby w postaci trygonometrycznej $z = r(\cos \varphi + j \sin \varphi)$, gdzie $r = |z|$, a $\varphi \in \text{Arg}(z)$. Podajemy $\varphi$ w konwencji $(-\pi, \pi]$ oraz $[0, 2\pi)$.

### 3.1

* **Liczba $z_1 = 8$:** punkt $(8, 0)$ leży na dodatniej półosi rzeczywistej.

  $$r = |8| = 8, \qquad \varphi = 0$$

  $$\boxed{z_1 = 8(\cos 0 + j \sin 0)}$$

* **Liczba $z_2 = -3$:** punkt $(-3, 0)$ leży na ujemnej półosi rzeczywistej.

  $$r = |-3| = 3, \qquad \varphi = \pi$$

  $$\boxed{z_2 = 3(\cos \pi + j \sin \pi)}$$

* **Liczba $z_3 = \pi j$:** punkt $(0, \pi)$ leży na dodatniej półosi urojonej.

  $$r = |\pi j| = \pi, \qquad \varphi = \frac{\pi}{2}$$

  $$\boxed{z_3 = \pi\left(\cos \frac{\pi}{2} + j \sin \frac{\pi}{2}\right)}$$

---

### 3.2

* **Liczba $z_4 = 1 - j$:**

  $$r = \sqrt{1^2 + (-1)^2} = \sqrt{2}, \qquad \cos \varphi = \frac{1}{\sqrt{2}}, \qquad \sin \varphi = -\frac{1}{\sqrt{2}}$$

  Punkt leży w IV ćwiartce, więc $\varphi = -\frac{\pi}{4}$ (lub $\frac{7\pi}{4}$ w $[0, 2\pi)$):

  $$\boxed{z_4 = \sqrt{2}\left(\cos\left(-\frac{\pi}{4}\right) + j \sin\left(-\frac{\pi}{4}\right)\right) = \sqrt{2}\left(\cos \frac{7\pi}{4} + j \sin \frac{7\pi}{4}\right)}$$

* **Liczba $z_5 = \sqrt{2}j - \sqrt{2} = -\sqrt{2} + \sqrt{2}j$:**

  $$r = \sqrt{(-\sqrt{2})^2 + (\sqrt{2})^2} = \sqrt{4} = 2, \qquad \cos \varphi = -\frac{\sqrt{2}}{2}, \qquad \sin \varphi = \frac{\sqrt{2}}{2}$$

  Punkt leży w II ćwiartce, więc $\varphi = \frac{3\pi}{4}$:

  $$\boxed{z_5 = 2\left(\cos \frac{3\pi}{4} + j \sin \frac{3\pi}{4}\right)}$$

---

### 3.3

* **Liczba $z_6 = 1 + j\sqrt{3}$:**

  $$r = \sqrt{1^2 + (\sqrt{3})^2} = \sqrt{4} = 2, \qquad \cos \varphi = \frac{1}{2}, \qquad \sin \varphi = \frac{\sqrt{3}}{2}$$

  Punkt leży w I ćwiartce, więc $\varphi = \frac{\pi}{3}$:

  $$\boxed{z_6 = 2\left(\cos \frac{\pi}{3} + j \sin \frac{\pi}{3}\right)}$$

* **Liczba $z_7 = \sqrt{6} - j\sqrt{2}$:**

  $$r = \sqrt{(\sqrt{6})^2 + (-\sqrt{2})^2} = \sqrt{8} = 2\sqrt{2}$$

  $$\cos \varphi = \frac{\sqrt{6}}{2\sqrt{2}} = \frac{\sqrt{3}}{2}, \qquad \sin \varphi = -\frac{\sqrt{2}}{2\sqrt{2}} = -\frac{1}{2}$$

  Punkt leży w IV ćwiartce, więc $\varphi = -\frac{\pi}{6}$ (lub $\frac{11\pi}{6}$ w $[0, 2\pi)$):

  $$\boxed{z_7 = 2\sqrt{2}\left(\cos\left(-\frac{\pi}{6}\right) + j \sin\left(-\frac{\pi}{6}\right)\right) = 2\sqrt{2}\left(\cos \frac{11\pi}{6} + j \sin \frac{11\pi}{6}\right)}$$

---

## Zadanie 4

Zamieniamy postać trygonometryczną na algebraiczną, podstawiając wartości $\cos \varphi$ i $\sin \varphi$.

### 4.1

* **Liczba $z_1 = 4(\cos \pi + j \sin \pi)$:**

  $$\cos \pi = -1, \qquad \sin \pi = 0$$

  $$z_1 = 4(-1 + j \cdot 0) = -4$$

  $$\boxed{z_1 = -4}$$

* **Liczba $z_2 = \sqrt{2}\left(\cos \frac{3\pi}{4} + j \sin \frac{3\pi}{4}\right)$:**

  $$\cos \frac{3\pi}{4} = -\frac{\sqrt{2}}{2}, \qquad \sin \frac{3\pi}{4} = \frac{\sqrt{2}}{2}$$

  $$z_2 = \sqrt{2}\left(-\frac{\sqrt{2}}{2} + j\frac{\sqrt{2}}{2}\right) = -1 + j$$

  $$\boxed{z_2 = -1 + j}$$

* **Sprawdzenie:** $|z_1| = 4$ i $|z_2| = \sqrt{2}$ — zgodnie z modułami danych postaci trygonometrycznych.

---

### 4.2

* **Liczba $z_3 = 2\left(\cos\left(-\frac{16\pi}{3}\right) + j \sin\left(-\frac{16\pi}{3}\right)\right)$:**
* **Redukcja kąta** o wielokrotność $2\pi$:

  $$-\frac{16\pi}{3} = -6\pi + \frac{2\pi}{3}$$

  Ponieważ funkcje $\cos$ i $\sin$ mają okres $2\pi$, zachodzi

  $$\cos\left(-\frac{16\pi}{3}\right) = \cos \frac{2\pi}{3} = -\frac{1}{2}, \qquad \sin\left(-\frac{16\pi}{3}\right) = \sin \frac{2\pi}{3} = \frac{\sqrt{3}}{2}$$

* **Postać algebraiczna:**

  $$z_3 = 2\left(-\frac{1}{2} + j\frac{\sqrt{3}}{2}\right) = -1 + j\sqrt{3}$$

  $$\boxed{z_3 = -1 + j\sqrt{3}}$$

* **Sprawdzenie:** $|z_3| = \sqrt{(-1)^2 + (\sqrt{3})^2} = 2 = r$ oraz $\arg z_3 = \frac{2\pi}{3}$ — zgodnie z danymi.

---

## Zadanie 5

Zbiory ilustrujemy opisem figury oraz tabelą punktów kontrolnych. Brzeg **ciągły** oznacza punkty należące do zbioru, brzeg **przerywany** — punkty, które do zbioru nie należą. Szkice w blokach kodu są poglądowe (nie w skali) i pokazują, którą figurę należy narysować oraz która część brzegu należy do zbioru.

### 5.1a

* **Przekształcenie:** niech $z = x + jy$, $x, y \in \mathbb{R}$; wtedy $|z| = \sqrt{x^2 + y^2}$ i warunek przyjmuje postać

  $$1 \le \sqrt{x^2 + y^2} < 3 \iff 1 \le x^2 + y^2 < 9$$

* **Figura:** pierścień kołowy o środku $z_0 = 0$, promieniu wewnętrznym $r_1 = 1$ i promieniu zewnętrznym $r_2 = 3$.
* **Brzegi:** okrąg $x^2 + y^2 = 1$ **należy** do zbioru (linia ciągła); okrąg $x^2 + y^2 = 9$ **nie należy** (linia przerywana).

| Punkt | Współrzędne | $\lvert z\rvert$ | Należy do zbioru |
| :---: | :---: | :---: | :--- |
| $A$ | $(1, 0)$ | $1$ | tak — brzeg wewnętrzny |
| $B$ | $(2, 0)$ | $2$ | tak — wnętrze |
| $C$ | $(-2, 2)$ | $2\sqrt{2} < 3$ | tak — wnętrze |
| $D$ | $(0, 0)$ | $0$ | nie |
| $E$ | $(3, 0)$ | $3$ | nie — brzeg zewnętrzny |

* **Szkic:**

  ```text
            y
            ^
            |      . - - - - - .
            |    /               \
            |   |   _ - - - _     |
            |   |  /         \    |     r = 3  (brzeg przerywany)
            |   | |     *     |   |     r = 1  (brzeg ciagly)
  ----------+---|-|-----------|-|--------> x    * srodek (0, 0)
            |   |  \         /    |
            |   |   ' - - - '     |
            |    \               /
            |      ' - - - - - '
  ```

---

### 5.1b

* **Przekształcenie:** zapisujemy $z + 2 - j = z - (-2 + j)$, a następnie $z = x + jy$:

  $$1 \le |z - (-2 + j)| < 3 \iff 1 \le (x + 2)^2 + (y - 1)^2 < 9$$

* **Figura:** pierścień kołowy o środku $z_0 = -2 + j$ (punkt $(-2, 1)$), promieniu wewnętrznym $r_1 = 1$ i promieniu zewnętrznym $r_2 = 3$; jest to pierścień z podpunktu 5.1a przesunięty o wektor $[-2, 1]$.
* **Brzegi:** okrąg o środku $(-2, 1)$ i promieniu $1$ **należy** do zbioru (linia ciągła); okrąg o tym samym środku i promieniu $3$ **nie należy** (linia przerywana).

| Punkt | Współrzędne | Odległość od $(-2, 1)$ | Należy do zbioru |
| :---: | :---: | :---: | :--- |
| $A$ | $(-2, 1)$ | $0$ | nie — środek |
| $B$ | $(-1, 1)$ | $1$ | tak — brzeg wewnętrzny |
| $C$ | $(-2, 3)$ | $2$ | tak — wnętrze |
| $D$ | $(1, 1)$ | $3$ | nie — brzeg zewnętrzny |

---

### 5.2a

* **Przekształcenie:** niech $z = x + jy \ne 0$; $\arg(z)$ jest kątem skierowanym półprostej $Oz$ względem dodatniej półosi rzeczywistej, a sam punkt $z = 0$ nie ma określonego argumentu.
* **Figura:** wycinek kątowy (kąt płaski, obszar nieograniczony) o wierzchołku w punkcie $z = 0$ i rozwartości

  $$\frac{2\pi}{3} - \left(-\frac{3\pi}{4}\right) = \frac{17\pi}{12}$$

  czyli $255^\circ$; kierunki wyznacza obrót od kąta $-\frac{3\pi}{4}$ (włącznie) do $\frac{2\pi}{3}$ (bez końca), przeciwnie do ruchu wskazówek zegara. Wierzchołek $z = 0$ nie należy do zbioru (argument nieokreślony).

  Zapis w konwencji $[0, 2\pi)$ daje ten sam zbiór punktów: $\arg(z) \in \left[\frac{5\pi}{4}, 2\pi\right) \cup \left[0, \frac{2\pi}{3}\right)$.

* **Brzegi:**
  * półprosta $y = x$ dla $x \le 0$ (kąt $-\frac{3\pi}{4}$) **należy** do zbioru (linia ciągła);
  * półprosta $y = -\sqrt{3}\,x$ dla $x \le 0$ (kąt $\frac{2\pi}{3}$) **nie należy** (linia przerywana).

| Punkt | Współrzędne | $\arg z$ | Należy do zbioru |
| :---: | :---: | :---: | :--- |
| $A$ | $(1, 0)$ | $0$ | tak — wnętrze |
| $B$ | $(0, 1)$ | $\frac{\pi}{2}$ | tak — wnętrze |
| $C$ | $(0, -1)$ | $-\frac{\pi}{2}$ | tak — wnętrze |
| $D$ | $(-1, -1)$ | $-\frac{3\pi}{4}$ | tak — brzeg ciągły |
| $E$ | $(-1, \sqrt{3})$ | $\frac{2\pi}{3}$ | nie — brzeg przerywany |
| $F$ | $(-1, 0)$ | $\pi$ | nie |
| $G$ | $(0, 0)$ | nieokreślony | nie — wierzchołek |

* **Szkic** (kropki — wycinek należący do zbioru; klin po lewej stronie wierzchołka — obszar wykluczony):

  ```text
              y
              ^
               \    <- brzeg przerywany: kat 2*pi/3 (nie nalezy)
                \
  (klin         X . . . . . . . . . . . . . . . . . . . . . . . . . . . .> x
   wykluczony) /     obszar: wycinek o rozwartosci 17*pi/12 (255 st.)
              /      bez wierzcholka X = 0
             /
            /  <- brzeg ciagly: kat -3*pi/4 (nalezy)
  ```

---

### 5.2b

* **Przekształcenie:** zapisujemy $z - 1 + j = z - (1 - j)$ i wprowadzamy $w = z - (1 - j)$; warunek ma postać $-\frac{3\pi}{4} \le \arg(w) < \frac{2\pi}{3}$.
* **Figura:** wycinek kątowy z podpunktu 5.2a przesunięty o wektor $[1, -1]$ — wierzchołek w punkcie $z_0 = 1 - j$ (punkt $(1, -1)$), rozwartość $\frac{17\pi}{12}$; wierzchołek nie należy do zbioru.
* **Brzegi:**
  * półprosta $y = x - 2$ dla $x \le 1$ (kąt $-\frac{3\pi}{4}$ od wierzchołka) **należy** do zbioru (linia ciągła);
  * półprosta $y + 1 = -\sqrt{3}(x - 1)$ dla $x \le 1$ (kąt $\frac{2\pi}{3}$) **nie należy** (linia przerywana).

| Punkt | Współrzędne | $\arg(z - z_0)$ | Należy do zbioru |
| :---: | :---: | :---: | :--- |
| $A$ | $(2, -1)$ | $0$ | tak — wnętrze |
| $B$ | $(1, 0)$ | $\frac{\pi}{2}$ | tak — wnętrze |
| $C$ | $(0, -2)$ | $-\frac{3\pi}{4}$ | tak — brzeg ciągły |
| $D$ | $(0, 0)$ | $\frac{3\pi}{4}$ | nie |
| $E$ | $(1, -1)$ | nieokreślony | nie — wierzchołek |

---

### 5.3

* **Przekształcenie:** niech $z = x + jy$, $x, y \in \mathbb{R}$.
  * Lewa strona:

    $$|z + j|^2 = |x + j(y + 1)|^2 = x^2 + (y + 1)^2$$

  * Prawa strona — korzystamy z tożsamości $z - \overline{z} = 2j\,\text{Im } z$ (podpunkt 2.4):

    $$(z - \overline{z})j + 3 = (2jy)j + 3 = -2y + 3$$

  * Nierówność:

    $$x^2 + (y + 1)^2 \le -2y + 3 \iff x^2 + y^2 + 2y + 1 + 2y - 3 \le 0 \iff x^2 + y^2 + 4y - 2 \le 0$$

  * Dopełniamy do kwadratu względem $y$:

    $$x^2 + (y + 2)^2 - 6 \le 0 \iff x^2 + (y + 2)^2 \le 6$$

* **Figura:** koło domknięte o środku $z_0 = -2j$ (punkt $(0, -2)$) i promieniu $R = \sqrt{6}$; cały brzeg (okrąg $x^2 + (y + 2)^2 = 6$, linia ciągła) należy do zbioru.

| Punkt | Współrzędne | Odległość od $(0, -2)$ | Należy do zbioru |
| :---: | :---: | :---: | :--- |
| $A$ | $(0, -2)$ | $0$ | tak — środek |
| $B$ | $(0, 0)$ | $2 < \sqrt{6}$ | tak — wnętrze |
| $C$ | $(2, -2)$ | $2 < \sqrt{6}$ | tak — wnętrze |
| $D$ | $(3, -2)$ | $3 > \sqrt{6}$ | nie |

* **Szkic:**

  ```text
            y
            ^
            |
            |      . - - - .
  ----------+----/           \----------> x
            |   |      *      |      srodek (0, -2), R = sqrt(6)
            |    \    (0,-2) /
            |      ' - - - '
            |   kolo: x^2 + (y+2)^2 <= 6  (brzeg ciagly, nalezy)
  ```

---

### 5.4

* **Dziedzina:** $z \ne -2 - j$ (mianownik nie może być zerem).
* **Przekształcenie:** moduł ilorazu to iloraz modułów, zatem

  $$\left|\frac{z - j}{z + 2 + j}\right| \ge 1 \iff |z - j| \ge |z - (-2 - j)|$$

  Geometrycznie: odległość $z$ od punktu $A = j$ jest nie mniejsza niż odległość od punktu $B = -2 - j$; jest to półpłaszczyzna wyznaczona przez symetralną odcinka $AB$.
* **Rachunek:** niech $z = x + jy$ i podnieśmy nierówność obustronnie do kwadratu (obie strony są nieujemne):

  $$x^2 + (y - 1)^2 \ge (x + 2)^2 + (y + 1)^2$$

  $$x^2 + y^2 - 2y + 1 \ge x^2 + 4x + 4 + y^2 + 2y + 1$$

  $$-4x - 4y - 4 \ge 0 \iff x + y + 1 \le 0$$

* **Figura:** domknięta półpłaszczyzna $x + y + 1 \le 0$, czyli obszar poniżej prostej $y = -x - 1$, wraz z prostą graniczną (linia ciągła); zbiór jest **bez punktu** $z = -2 - j$ (punkt $(-2, -1)$ nie należy do dziedziny).

| Punkt | Współrzędne | $x + y + 1$ | Należy do zbioru |
| :---: | :---: | :---: | :--- |
| $A$ | $(-1, 0)$ | $0$ | tak — brzeg |
| $B$ | $(-3, 0)$ | $-2$ | tak — wnętrze |
| $C$ | $(0, -3)$ | $-2$ | tak — wnętrze |
| $D$ | $(0, 0)$ | $1$ | nie |
| $E$ | $(-2, -1)$ | $-2$ | nie — punkt wyłączony z dziedziny |

* **Szkic:**

  ```text
              y
              ^
              |\
              | \        <- brzeg: prosta y = -x - 1
              |  \          (linia ciagla, nalezy)
              |   \
   nalezy     |    \          nie nalezy
   x+y+1<=0   |     \         x + y + 1 > 0
              |      \
              |       \
  ------------+---------------------------> x
   (brzeg przecina osie w punktach (-1, 0) i (0, -1))
  ```

---

### 5.5a

* **Przekształcenie:** warunek $|z - j| + |z + j| = 4$ opisuje zbiór punktów, których suma odległości od punktów $F_1 = j$ (punkt $(0, 1)$) i $F_2 = -j$ (punkt $(0, -1)$) jest stała i równa $2a = 4$.
* **Parametry:** $a = 2$, odległość między ogniskami $2c = |F_1F_2| = 2$, czyli $c = 1$; ponieważ $2a = 4 > 2c = 2$, zbiorem jest **elipsa** o środku $S = (0, 0)$ i półosiach

  $$a = 2 \quad (\text{półoś wielka, pionowa}), \qquad b = \sqrt{a^2 - c^2} = \sqrt{4 - 1} = \sqrt{3} \quad (\text{półoś mała, pozioma})$$

* **Równanie:** $\frac{x^2}{3} + \frac{y^2}{4} = 1$; zbiór to sama elipsa (brzeg, linia ciągła) — punkty wewnątrz elipsy nie spełniają równania.

| Punkt | Współrzędne | Suma odległości od $(0, 1)$ i $(0, -1)$ | Należy do zbioru |
| :---: | :---: | :---: | :--- |
| $A$ | $(0, 2)$ | $1 + 3 = 4$ | tak — wierzchołek |
| $B$ | $(0, -2)$ | $3 + 1 = 4$ | tak — wierzchołek |
| $C$ | $(\sqrt{3}, 0)$ | $2 + 2 = 4$ | tak — wierzchołek |
| $D$ | $(0, 0)$ | $1 + 1 = 2 \ne 4$ | nie |
| $E$ | $(2, 0)$ | $2\sqrt{5} \ne 4$ | nie |

* **Szkic:**

  ```text
            y
            ^
            *  (0, 2)  wierzcholek
         .  |  .
      .     |     .        os wielka: pionowa, a = 2
    .      F1 *     .      ognisko (0, 1)
  --*---------|---------*------> x
  (-sqrt3)    |      (sqrt3, 0)   os mala: pozioma, b = sqrt(3)
    .      F2 *     .      ognisko (0, -1)
      .     |     .
         .  |  .
            *  (0, -2)  wierzcholek
  ```

---

### 5.5b

* **Przekształcenie:** suma odległości od $F_1 = (0, 1)$ i $F_2 = (0, -1)$ równa $2$; odległość między ogniskami wynosi $|F_1F_2| = 2$. Z nierówności trójkąta

  $$|z - j| + |z + j| \ge |(z - j) - (z + j)| = 2$$

  przy czym równość zachodzi wtedy i tylko wtedy, gdy punkt $z$ leży na odcinku o końcach $F_1$, $F_2$.
* **Figura:** **odcinek** (elipsa zdegenerowana) łączący punkty $-j$ i $j$: zbiór $\{z = jy : -1 \le y \le 1\}$, czyli odcinek na osi urojonej. Każdy punkt odcinka należy do zbioru (linia ciągła, w tym oba końce).

| Punkt | Współrzędne | Suma odległości od $(0, 1)$ i $(0, -1)$ | Należy do zbioru |
| :---: | :---: | :---: | :--- |
| $A$ | $(0, 1)$ | $0 + 2 = 2$ | tak — koniec |
| $B$ | $(0, 0)$ | $1 + 1 = 2$ | tak — punkt wewnętrzny |
| $C$ | $(0, -1)$ | $2 + 0 = 2$ | tak — koniec |
| $D$ | $(0, 2)$ | $1 + 3 = 4 \ne 2$ | nie |
| $E$ | $(1, 0)$ | $\sqrt{2} + \sqrt{2} \ne 2$ | nie |

* **Szkic:**

  ```text
  y
  ^
  *  (0, 1) = j   <- koniec odcinka (nalezy)
  |
  |  odcinek: x = 0, -1 <= y <= 1  (linia ciagla)
  |
  *  (0, -1) = -j <- koniec odcinka (nalezy)
  |
  ```

---

### 5.6

* **Przekształcenie:** wyłączamy $2j$ przed moduł z prawej strony:

  $$|2jz + 1| = \left|2j\left(z - \frac{j}{2}\right)\right| = 2\left|z - \frac{j}{2}\right|$$

  (bo $-\frac{1}{2j} = \frac{j}{2}$), skąd warunek

  $$|z - 1| = 2\left|z - \frac{j}{2}\right|$$

  jest równaniem okręgu Apoloniusza dla punktów $A = (1, 0)$, $B = (0, \frac{1}{2})$ i stosunku $k = 2 \ne 1$ (zbiór punktów o stałym stosunku odległości od dwóch ustalonych punktów).

* **Rachunek:** niech $z = x + jy$ i podnosimy do kwadratu:

  $$(x - 1)^2 + y^2 = 4\left[x^2 + \left(y - \frac{1}{2}\right)^2\right]$$

  $$x^2 - 2x + 1 + y^2 = 4x^2 + 4y^2 - 4y + 1$$

  $$3x^2 + 3y^2 + 2x - 4y = 0 \iff x^2 + y^2 + \frac{2}{3}x - \frac{4}{3}y = 0$$

  Dopełniamy do kwadratów:

  $$\left(x + \frac{1}{3}\right)^2 + \left(y - \frac{2}{3}\right)^2 = \frac{1}{9} + \frac{4}{9} = \frac{5}{9}$$

* **Figura:** okrąg (cały brzeg należy do zbioru, linia ciągła) o środku

  $$S = \left(-\frac{1}{3}, \frac{2}{3}\right) \quad \left(z_0 = -\frac{1}{3} + \frac{2}{3}j\right), \qquad R = \frac{\sqrt{5}}{3}$$

| Punkt | Współrzędne | Stosunek $\lvert z - 1\rvert : \lvert z - \frac{j}{2}\rvert$ | Należy do zbioru |
| :---: | :---: | :---: | :--- |
| $A$ | $(0, 0)$ | $1 : \frac{1}{2} = 2$ | tak |
| $B$ | $(-1, 1)$ | $\sqrt{5} : \frac{\sqrt{5}}{2} = 2$ | tak |
| $C$ | $S$ | $4 \ne 2$ | nie |
| $D$ | $(1, 0)$ | $0 : \frac{\sqrt{5}}{2} = 0$ | nie |

* **Szkic:**

  ```text
             y
             ^
             |    . - - .
             |  /   S   \        S = srodek (-1/3, 2/3)
  -----------*-           \      R = sqrt(5)/3
             |  \         .      okrag przechodzi przez (0,0) i (-1,1)
             |    ' - - - '
  ```

---

### 5.7

* **Dziedzina:** $z \ne j$ (w mianowniku $z - j \ne 0$).
* **Przekształcenie:** niech $z = x + jy$; mnożymy licznik i mianownik przez sprzężenie mianownika:

  $$\frac{z + j}{z - j} = \frac{x + j(y + 1)}{x + j(y - 1)} = \frac{[x + j(y + 1)][x - j(y - 1)]}{x^2 + (y - 1)^2}$$

  Licznik: $x^2 - jx(y-1) + jx(y+1) + (y+1)(y-1) = x^2 + y^2 - 1 + 2xj$, zatem

  $$\text{Re}\left(\frac{z + j}{z - j}\right) = \frac{x^2 + y^2 - 1}{x^2 + (y - 1)^2}$$

* **Nierówność:** dla $z \ne j$ mianownik $x^2 + (y - 1)^2 > 0$, więc

  $$\frac{x^2 + y^2 - 1}{x^2 + (y - 1)^2} \le 0 \iff x^2 + y^2 - 1 \le 0 \iff |z| \le 1$$

* **Figura:** koło domknięte $|z| \le 1$ o środku $0$ i promieniu $R = 1$ (brzeg $|z| = 1$ należy do zbioru, linia ciągła), **z wyłączeniem punktu** $z = j$ (punkt $(0, 1)$ nie należy do dziedziny).

| Punkt | Współrzędne | $\text{Re}\left(\frac{z + j}{z - j}\right)$ | Należy do zbioru |
| :---: | :---: | :---: | :--- |
| $A$ | $(0, 0)$ | $-1$ | tak — wnętrze |
| $B$ | $(1, 0)$ | $0$ | tak — brzeg |
| $C$ | $(0, \frac{1}{2})$ | $-3$ | tak — wnętrze |
| $D$ | $(0, 1)$ | nie istnieje | nie — punkt wyłączony |
| $E$ | $(0, 2)$ | $3$ | nie |

* **Szkic:**

  ```text
            y
            ^
            |    . - x - .     <- punkt (0,1) wylaczony (z = j)
            |  /           \
  ----------+-|------*------|-------> x     * srodek (0,0), R = 1
            |  \           /
            |    ' - - - '
            |   kolo |z| <= 1 (brzeg nalezy poza punktem (0,1))
  ```

---

## Zadanie 6

Dla każdej liczby wyznaczamy moduł $r = |z|$ i argument główny $\varphi = \arg(z)$, korzystając z funkcji $\operatorname{arctg}$ lub $\arcsin$. W konwencji $(-\pi, \pi]$ argument oznaczamy przez $\varphi$, w konwencji $[0, 2\pi)$ — przez $\varphi_{[0, 2\pi)}$.

### 6.1

* **Liczba $z_1 = 1 + 2j$** — I ćwiartka ($x = 1 > 0$, $y = 2 > 0$).
* **Moduł:**

  $$r = |z_1| = \sqrt{1^2 + 2^2} = \sqrt{5}$$

* **Argument główny** — w I ćwiartce $\varphi \in \left(0, \frac{\pi}{2}\right)$:

  $$\varphi = \operatorname{arctg}\left(\frac{y}{x}\right) = \operatorname{arctg}(2)$$

  Ta sama wartość z funkcji $\arcsin$ (w I ćwiartce $\arcsin \frac{y}{r}$ jest kątem szukanym):

  $$\varphi = \arcsin\left(\frac{2}{\sqrt{5}}\right) = \arcsin \frac{2\sqrt{5}}{5}$$

* **Wynik:**

  $$\boxed{|z_1| = \sqrt{5}, \qquad \arg z_1 = \operatorname{arctg}(2) = \arcsin \frac{2\sqrt{5}}{5}}$$

* **Sprawdzenie:** $\cos \varphi = \frac{1}{\sqrt{5}}$ i $\sin \varphi = \frac{2}{\sqrt{5}}$, więc $\sqrt{5}\left(\frac{1}{\sqrt{5}} + j\frac{2}{\sqrt{5}}\right) = 1 + 2j$ — zgodnie z danymi.

---

### 6.2

* **Liczba $z_2 = 3j - 4 = -4 + 3j$** — II ćwiartka ($x = -4 < 0$, $y = 3 > 0$).
* **Moduł:**

  $$r = |z_2| = \sqrt{(-4)^2 + 3^2} = \sqrt{25} = 5$$

* **Argument główny** — w II ćwiartce $\varphi \in \left(\frac{\pi}{2}, \pi\right]$:

  $$\varphi = \pi + \operatorname{arctg}\left(\frac{y}{x}\right) = \pi + \operatorname{arctg}\left(-\frac{3}{4}\right) = \pi - \operatorname{arctg}\left(\frac{3}{4}\right)$$

  Z funkcji $\arcsin$: $\sin \varphi = \frac{y}{r} = \frac{3}{5}$, a $\arcsin \frac{3}{5} \in \left(0, \frac{\pi}{2}\right)$ jest kątem z I ćwiartki o tej samej wartości sinusa, więc

  $$\varphi = \pi - \arcsin\left(\frac{3}{5}\right)$$

* **Wynik:**

  $$\boxed{|z_2| = 5, \qquad \arg z_2 = \pi - \operatorname{arctg}\left(\frac{3}{4}\right) = \pi - \arcsin\left(\frac{3}{5}\right)}$$

* **Sprawdzenie:** $\cos \varphi = -\cos\left(\operatorname{arctg} \frac{3}{4}\right) = -\frac{4}{5}$ i $5 \cdot \left(-\frac{4}{5} + j\frac{3}{5}\right) = -4 + 3j$ — zgodnie z danymi.

---

### 6.3

* **Liczba $z_3 = 5 - 2j$** — IV ćwiartka ($x = 5 > 0$, $y = -2 < 0$).
* **Moduł:**

  $$r = |z_3| = \sqrt{5^2 + (-2)^2} = \sqrt{29}$$

* **Argument główny** — w IV ćwiartce $\varphi \in \left(-\frac{\pi}{2}, 0\right)$:

  $$\varphi = \operatorname{arctg}\left(\frac{y}{x}\right) = \operatorname{arctg}\left(-\frac{2}{5}\right) = -\operatorname{arctg}\left(\frac{2}{5}\right)$$

  Z funkcji $\arcsin$: $\sin \varphi = \frac{-2}{\sqrt{29}}$, więc

  $$\varphi = \arcsin\left(-\frac{2}{\sqrt{29}}\right) = -\arcsin \frac{2\sqrt{29}}{29}$$

* **W konwencji $[0, 2\pi)$:**

  $$\varphi_{[0, 2\pi)} = 2\pi - \operatorname{arctg}\left(\frac{2}{5}\right) = 2\pi - \arcsin \frac{2\sqrt{29}}{29}$$

* **Wynik:**

  $$\boxed{|z_3| = \sqrt{29}, \qquad \arg z_3 = -\operatorname{arctg}\left(\frac{2}{5}\right) = -\arcsin \frac{2\sqrt{29}}{29}}$$

* **Sprawdzenie:** $\cos \varphi = \frac{5}{\sqrt{29}}$ i $\sqrt{29}\left(\frac{5}{\sqrt{29}} - j\frac{2}{\sqrt{29}}\right) = 5 - 2j$ — zgodnie z danymi.

---

### 6.4

* **Liczba $z_4 = -6 - 8j$** — III ćwiartka ($x = -6 < 0$, $y = -8 < 0$).
* **Moduł:**

  $$r = |z_4| = \sqrt{(-6)^2 + (-8)^2} = \sqrt{100} = 10$$

* **Argument główny** — w III ćwiartce $\varphi \in \left(-\pi, -\frac{\pi}{2}\right)$:

  $$\varphi = -\pi + \operatorname{arctg}\left(\frac{y}{x}\right) = -\pi + \operatorname{arctg}\left(\frac{-8}{-6}\right) = -\pi + \operatorname{arctg}\left(\frac{4}{3}\right)$$

  Z funkcji $\arcsin$: $\sin \varphi = \frac{y}{r} = -\frac{4}{5}$ oraz $\arcsin\left(-\frac{4}{5}\right) = -\arcsin \frac{4}{5}$, więc

  $$\varphi = -\pi - \arcsin\left(-\frac{4}{5}\right) = -\pi + \arcsin\left(\frac{4}{5}\right)$$

* **W konwencji $[0, 2\pi)$:**

  $$\varphi_{[0, 2\pi)} = \pi + \operatorname{arctg}\left(\frac{4}{3}\right) = \pi + \arcsin\left(\frac{4}{5}\right)$$

* **Wynik:**

  $$\boxed{|z_4| = 10, \qquad \arg z_4 = -\pi + \operatorname{arctg}\left(\frac{4}{3}\right) = -\pi + \arcsin\left(\frac{4}{5}\right)}$$

* **Sprawdzenie:** $\cos \varphi = -\cos\left(\operatorname{arctg}\frac{4}{3}\right) = -\frac{3}{5}$ i $10 \cdot \left(-\frac{3}{5} - j\frac{4}{5}\right) = -6 - 8j$ — zgodnie z danymi.

---

## Podsumowanie wyników

| Podpunkt | Wynik |
| :--- | :--- |
| 1.1 | $z_1^2 + jz_2 = 10 + 14j$; $\text{Re}(z_1 z_2) = 16$ |
| 1.2 | $\left\lvert 2\overline{z}_1 + \text{Im } z_2\right\rvert = \sqrt{17}$ |
| 1.3 | $\frac{6}{13} - \frac{4}{13}j$ |
| 2.1 | TAK — część urojona jest addytywna |
| 2.2 | NIE — kontrprzykład $z_1 = z_2 = j$; warunek: $\text{Im } z_1 \cdot \text{Im } z_2 = 0$ |
| 2.3 | NIE — kontrprzykład $z_1 = 1$, $z_2 = -1$; warunek: $z_2 = t z_1$, $t \ge 0$ |
| 2.4 | TAK — $z - \overline{z} = 2j\,\text{Im } z$ |
| 3.1 | $8(\cos 0 + j \sin 0)$; $3(\cos \pi + j \sin \pi)$; $\pi\left(\cos \frac{\pi}{2} + j \sin \frac{\pi}{2}\right)$ |
| 3.2 | $\sqrt{2}\left(\cos\left(-\frac{\pi}{4}\right) + j \sin\left(-\frac{\pi}{4}\right)\right)$; $2\left(\cos \frac{3\pi}{4} + j \sin \frac{3\pi}{4}\right)$ |
| 3.3 | $2\left(\cos \frac{\pi}{3} + j \sin \frac{\pi}{3}\right)$; $2\sqrt{2}\left(\cos\left(-\frac{\pi}{6}\right) + j \sin\left(-\frac{\pi}{6}\right)\right)$ |
| 4.1 | $z_1 = -4$; $z_2 = -1 + j$ |
| 4.2 | $z_3 = -1 + j\sqrt{3}$ |
| 5.1a | pierścień $1 \le \lvert z\rvert < 3$; brzeg wewnętrzny należy, zewnętrzny nie |
| 5.1b | pierścień o środku $-2 + j$, promienie $1$ i $3$; brzeg wewnętrzny należy |
| 5.2a | wycinek kątowy o wierzchołku $0$ i rozwartości $\frac{17\pi}{12}$; kąt $-\frac{3\pi}{4}$ należy |
| 5.2b | ten sam wycinek przesunięty o wektor $[1, -1]$; wierzchołek $1 - j$ nie należy |
| 5.3 | koło domknięte $x^2 + (y + 2)^2 \le 6$ (środek $-2j$, $R = \sqrt{6}$) |
| 5.4 | półpłaszczyzna $x + y + 1 \le 0$ bez punktu $-2 - j$ |
| 5.5a | elipsa $\frac{x^2}{3} + \frac{y^2}{4} = 1$ (ogniska $\pm j$, $a = 2$, $b = \sqrt{3}$) |
| 5.5b | odcinek o końcach $-j$ i $j$ (przypadek zdegenerowany) |
| 5.6 | okrąg o środku $-\frac{1}{3} + \frac{2}{3}j$ i promieniu $\frac{\sqrt{5}}{3}$ |
| 5.7 | koło $\lvert z\rvert \le 1$ bez punktu $j$ |
| 6.1 | $\lvert z_1\rvert = \sqrt{5}$, $\arg z_1 = \operatorname{arctg}(2) = \arcsin \frac{2\sqrt{5}}{5}$ |
| 6.2 | $\lvert z_2\rvert = 5$, $\arg z_2 = \pi - \operatorname{arctg} \frac{3}{4} = \pi - \arcsin \frac{3}{5}$ |
| 6.3 | $\lvert z_3\rvert = \sqrt{29}$, $\arg z_3 = -\operatorname{arctg} \frac{2}{5} = -\arcsin \frac{2\sqrt{29}}{29}$ |
| 6.4 | $\lvert z_4\rvert = 10$, $\arg z_4 = -\pi + \operatorname{arctg} \frac{4}{3} = -\pi + \arcsin \frac{4}{5}$ |
