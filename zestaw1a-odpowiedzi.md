# Odpowiedzi do zadań z zestawu 1a

---

## Zadanie 1

Dane są liczby:
$$z_1 = 3 + 2j, \quad z_2 = 2 - 5j$$

### 1.1
Obliczyć $z_1^2 + jz_2$ oraz $\text{Re}(z_1 \cdot z_2)$.

* **Obliczenie $z_1^2 + jz_2$:**
  $$z_1^2 = (3 + 2j)^2 = 3^2 + 2 \cdot 3 \cdot 2j + (2j)^2 = 9 + 12j - 4 = 5 + 12j$$
  $$jz_2 = j(2 - 5j) = 2j - 5j^2 = 2j + 5 = 5 + 2j$$
  $$z_1^2 + jz_2 = (5 + 12j) + (5 + 2j) = 10 + 14j$$

* **Obliczenie $\text{Re}(z_1 \cdot z_2)$:**
  $$z_1 \cdot z_2 = (3 + 2j)(2 - 5j) = 6 - 15j + 4j - 10j^2 = 6 - 11j + 10 = 16 - 11j$$
  $$\text{Re}(z_1 \cdot z_2) = 16$$

---

### 1.2
Obliczyć $|2\bar{z}_1 + \text{Im } z_2|$.

* Mamy $\bar{z}_1 = 3 - 2j$, więc:
  $$2\bar{z}_1 = 2(3 - 2j) = 6 - 4j$$
* Ponieważ $z_2 = 2 - 5j$, to $\text{Im } z_2 = -5$ (uwaga: część urojona jest liczbą rzeczywistą).
* Zatem:
  $$2\bar{z}_1 + \text{Im } z_2 = (6 - 4j) + (-5) = 1 - 4j$$
* Moduł:
  $$|2\bar{z}_1 + \text{Im } z_2| = |1 - 4j| = \sqrt{1^2 + (-4)^2} = \sqrt{1 + 16} = \sqrt{17}$$

---

### 1.3
Obliczyć $\frac{\bar{z}_2 - j|z_1 + 2j|}{z_1}$.

* Mamy $\bar{z}_2 = 2 + 5j$.
* Obliczamy $|z_1 + 2j|$:
  $$z_1 + 2j = (3 + 2j) + 2j = 3 + 4j$$
  $$|z_1 + 2j| = |3 + 4j| = \sqrt{3^2 + 4^2} = \sqrt{9 + 16} = \sqrt{25} = 5$$
* Licznik ułamka:
  $$\bar{z}_2 - j|z_1 + 2j| = (2 + 5j) - 5j = 2$$
* Dzielenie przez $z_1 = 3 + 2j$:
  $$\frac{2}{3 + 2j} = \frac{2(3 - 2j)}{(3 + 2j)(3 - 2j)} = \frac{6 - 4j}{3^2 + 2^2} = \frac{6 - 4j}{13} = \frac{6}{13} - \frac{4}{13}j$$

---

## Zadanie 2

Czy podane równości zachodzą dla dowolnych $z, z_1, z_2 \in \mathbb{C}$?

### 2.1 $\text{Im}(z_1 + z_2) = \text{Im } z_1 + \text{Im } z_2$
* **Odpowiedź:** **TAK** (równość zachodzi dla dowolnych liczb zespolonych).
* **Uzasadnienie:**
  Niech $z_1 = x_1 + j y_1$ oraz $z_2 = x_2 + j y_2$, gdzie $x_1, x_2, y_1, y_2 \in \mathbb{R}$.
  Wtedy:
  $$z_1 + z_2 = (x_1 + x_2) + j(y_1 + y_2)$$
  $$\text{Im}(z_1 + z_2) = y_1 + y_2 = \text{Im } z_1 + \text{Im } z_2$$

---

### 2.2 $\text{Re}(z_1 \cdot z_2) = \text{Re } z_1 \cdot \text{Re } z_2$
* **Odpowiedź:** **NIE** (równość na ogół nie zachodzi).
* **Kontrprzykład:**
  Niech $z_1 = j$ oraz $z_2 = j$.
  Wtedy:
  $$\text{Re } z_1 = 0, \quad \text{Re } z_2 = 0 \implies \text{Re } z_1 \cdot \text{Re } z_2 = 0$$
  Jednak:
  $$z_1 \cdot z_2 = j^2 = -1 \implies \text{Re}(z_1 \cdot z_2) = -1 \ne 0$$
  *(Ogólny wzór: $\text{Re}(z_1 \cdot z_2) = \text{Re } z_1 \cdot \text{Re } z_2 - \text{Im } z_1 \cdot \text{Im } z_2$).*

---

### 2.3 $|z_1 + z_2| = |z_1| + |z_2|$
* **Odpowiedź:** **NIE** (na ogół zachodzi jedynie nierówność trójkąta $|z_1 + z_2| \le |z_1| + |z_2|$).
* **Kontrprzykład:**
  Niech $z_1 = 1$ oraz $z_2 = -1$.
  Wtedy:
  $$|z_1 + z_2| = |1 + (-1)| = |0| = 0$$
  Natomiast:
  $$|z_1| + |z_2| = |1| + |-1| = 1 + 1 = 2 \ne 0$$
  *(Równość zachodzi tylko wtedy, gdy liczby leżą na tej samej półprostej wychodzącej z początku układu współrzędnych, tj. $z_1 = 0$ lub $z_2 = k z_1$ dla pewnego $k \ge 0$).*

---

### 2.4 $z - \bar{z} = 2j \text{Im } z$
* **Odpowiedź:** **TAK** (równość zachodzi dla dowolnego $z \in \mathbb{C}$).
* **Uzasadnienie:**
  Niech $z = x + jy$, gdzie $x, y \in \mathbb{R}$. Wtedy $\bar{z} = x - jy$ oraz $\text{Im } z = y$.
  Stąd:
  $$z - \bar{z} = (x + jy) - (x - jy) = 2jy = 2j \text{Im } z$$

---

## Zadanie 3

Zapisać w postaci trygonometrycznej: $z = r(\cos \varphi + j \sin \varphi)$, gdzie $r = |z|$, a $\varphi \in [0, 2\pi)$ (lub $\varphi \in (-\pi, \pi]$).

### 3.1
* **$z_1 = 8$:**
  $$r = |8| = 8, \quad \varphi = 0$$
  $$z_1 = 8(\cos 0 + j \sin 0)$$

* **$z_2 = -3$:**
  $$r = |-3| = 3, \quad \varphi = \pi$$
  $$z_2 = 3(\cos \pi + j \sin \pi)$$

* **$z_3 = \pi j$:**
  $$r = |\pi j| = \pi, \quad \varphi = \frac{\pi}{2}$$
  $$z_3 = \pi \left(\cos \frac{\pi}{2} + j \sin \frac{\pi}{2}\right)$$

---

### 3.2
* **$z_4 = 1 - j$:**
  $$r = \sqrt{1^2 + (-1)^2} = \sqrt{2}$$
  $$\cos \varphi = \frac{1}{\sqrt{2}} = \frac{\sqrt{2}}{2}, \quad \sin \varphi = -\frac{1}{\sqrt{2}} = -\frac{\sqrt{2}}{2} \implies \varphi = \frac{7\pi}{4} \quad \left(\text{lub } -\frac{\pi}{4}\right)$$
  $$z_4 = \sqrt{2}\left(\cos \frac{7\pi}{4} + j \sin \frac{7\pi}{4}\right) = \sqrt{2}\left(\cos\left(-\frac{\pi}{4}\right) + j \sin\left(-\frac{\pi}{4}\right)\right)$$

* **$z_5 = \sqrt{2}j - \sqrt{2} = -\sqrt{2} + \sqrt{2}j$:**
  $$r = \sqrt{(-\sqrt{2})^2 + (\sqrt{2})^2} = \sqrt{2 + 2} = \sqrt{4} = 2$$
  $$\cos \varphi = -\frac{\sqrt{2}}{2}, \quad \sin \varphi = \frac{\sqrt{2}}{2} \implies \varphi = \frac{3\pi}{4}$$
  $$z_5 = 2\left(\cos \frac{3\pi}{4} + j \sin \frac{3\pi}{4}\right)$$

---

### 3.3
* **$z_6 = 1 + j\sqrt{3}$:**
  $$r = \sqrt{1^2 + (\sqrt{3})^2} = \sqrt{1 + 3} = \sqrt{4} = 2$$
  $$\cos \varphi = \frac{1}{2}, \quad \sin \varphi = \frac{\sqrt{3}}{2} \implies \varphi = \frac{\pi}{3}$$
  $$z_6 = 2\left(\cos \frac{\pi}{3} + j \sin \frac{\pi}{3}\right)$$

* **$z_7 = \sqrt{6} - j\sqrt{2}$:**
  $$r = \sqrt{(\sqrt{6})^2 + (-\sqrt{2})^2} = \sqrt{6 + 2} = \sqrt{8} = 2\sqrt{2}$$
  $$\cos \varphi = \frac{\sqrt{6}}{2\sqrt{2}} = \frac{\sqrt{3}}{2}, \quad \sin \varphi = -\frac{\sqrt{2}}{2\sqrt{2}} = -\frac{1}{2} \implies \varphi = \frac{11\pi}{6} \quad \left(\text{lub } -\frac{\pi}{6}\right)$$
  $$z_7 = 2\sqrt{2}\left(\cos \frac{11\pi}{6} + j \sin \frac{11\pi}{6}\right) = 2\sqrt{2}\left(\cos\left(-\frac{\pi}{6}\right) + j \sin\left(-\frac{\pi}{6}\right)\right)$$

---

## Zadanie 4

Zapisać w postaci algebraicznej następujące liczby:

### 4.1
* **$z_1 = 4(\cos \pi + j \sin \pi)$:**
  $$\cos \pi = -1, \quad \sin \pi = 0$$
  $$z_1 = 4(-1 + j \cdot 0) = -4$$

* **$z_2 = \sqrt{2}\left(\cos\left(\frac{3\pi}{4}\right) + j \sin\left(\frac{3\pi}{4}\right)\right)$:**
  $$\cos\left(\frac{3\pi}{4}\right) = -\frac{\sqrt{2}}{2}, \quad \sin\left(\frac{3\pi}{4}\right) = \frac{\sqrt{2}}{2}$$
  $$z_2 = \sqrt{2}\left(-\frac{\sqrt{2}}{2} + j \frac{\sqrt{2}}{2}\right) = -1 + j$$

---

### 4.2
* **$z_3 = 2\left(\cos\left(-\frac{16\pi}{3}\right) + j \sin\left(-\frac{16\pi}{3}\right)\right)$:**
  Redukujemy kąt o wielokrotność $2\pi$:
  $$-\frac{16\pi}{3} = -5\frac{1}{3}\pi = -6\pi + \frac{2\pi}{3}$$
  Zatem:
  $$\cos\left(-\frac{16\pi}{3}\right) = \cos\left(\frac{2\pi}{3}\right) = -\frac{1}{2}$$
  $$\sin\left(-\frac{16\pi}{3}\right) = \sin\left(\frac{2\pi}{3}\right) = \frac{\sqrt{3}}{2}$$
  Stąd:
  $$z_3 = 2\left(-\frac{1}{2} + j \frac{\sqrt{3}}{2}\right) = -1 + j\sqrt{3}$$

---

## Zadanie 5

Zilustrować na płaszczyźnie zespolonej zbiór liczb zespolonych spełniających podany warunek:

### 5.1a: $1 \le |z| < 3$
* **Opis geometryczny:**
  Pierścień kołowy o środku w punkcie $z_0 = 0$ (początek układu współrzędnych):
  * Promień wewnętrzny $r_1 = 1$, promień zewnętrzny $r_2 = 3$.
  * Brzeg wewnętrzny $|z| = 1$ (okrąg o promieniu 1) **należy** do zbioru (linia ciągła).
  * Brzeg zewnętrzny $|z| = 3$ (okrąg o promieniu 3) **nie należy** do zbioru (linia przerywana).

---

### 5.1b: $1 \le |z + 2 - j| < 3$
* **Przekształcenie:**
  $$|z - (-2 + j)| \in [1, 3)$$
* **Opis geometryczny:**
  Pierścień kołowy o środku w punkcie $z_0 = -2 + j$ (współrzędne $(-2, 1)$):
  * Promień wewnętrzny $r_1 = 1$, promień zewnętrzny $r_2 = 3$.
  * Wewnętrzny okrąg o środku w $(-2, 1)$ i promieniu 1 **należy** do zbioru (linia ciągła).
  * Zewnętrzny okrąg o środku w $(-2, 1)$ i promieniu 3 **nie należy** do zbioru (linia przerywana).

---

### 5.2a: $-\frac{3\pi}{4} \le \arg(z) < \frac{2\pi}{3}$
* **Opis geometryczny:**
  Nieskończony wycinek kątowy (kąt płaski) o wierzchołku w punkcie $z = 0$ (bez samego wierzchołka, gdyż dla $z = 0$ argument jest nieokreślony):
  * Ograniczony półprostą o kącie nachylenia $-\frac{3\pi}{4}$ (lub $\frac{5\pi}{4}$) – ta półprosta **należy** do zbioru (linia ciągła).
  * Ograniczony półprostą o kącie nachylenia $\frac{2\pi}{3}$ (lub $120^\circ$) – ta półprosta **nie należy** do zbioru (linia przerywana).
  * Obszar rozciąga się przeciwnie do ruchu wskazówek zegara od kąta $-\frac{3\pi}{4}$ do $\frac{2\pi}{3}$.

---

### 5.2b: $-\frac{3\pi}{4} \le \arg(z - 1 + j) < \frac{2\pi}{3}$
* **Przekształcenie:**
  Niech $w = z - (1 - j)$. Wtedy warunek to $-\frac{3\pi}{4} \le \arg(w) < \frac{2\pi}{3}$.
* **Opis geometryczny:**
  Jest to wycinek kątowy z podpunktu 5.2a przesunięty o wektor $[1, -1]$:
  * Wierzchołek w punkcie $z_0 = 1 - j$ (współrzędne $(1, -1)$), sam wierzchołek nie należy do zbioru.
  * Półprosta wychodząca z $(1, -1)$ pod kątem $-\frac{3\pi}{4}$ **należy** do zbioru (linia ciągła).
  * Półprosta wychodząca z $(1, -1)$ pod kątem $\frac{2\pi}{3}$ **nie należy** do zbioru (linia przerywana).

---

### 5.3: $|z + j|^2 \le (z - \bar{z})j + 3$
* **Rozwiązanie algebraiczne:**
  Niech $z = x + jy$, gdzie $x, y \in \mathbb{R}$.
  * Lewa strona:
    $$|x + j(y + 1)|^2 = x^2 + (y + 1)^2 = x^2 + y^2 + 2y + 1$$
  * Prawa strona:
    $$z - \bar{z} = 2jy \implies (z - \bar{z})j = (2jy)j = 2j^2y = -2y$$
    $$(z - \bar{z})j + 3 = -2y + 3$$
  * Nierówność:
    $$x^2 + y^2 + 2y + 1 \le -2y + 3$$
    $$x^2 + y^2 + 4y - 2 \le 0$$
    Dopełniając do kwadratu dla $y$:
    $$x^2 + (y + 2)^2 - 4 - 2 \le 0 \iff x^2 + (y + 2)^2 \le 6$$
* **Opis geometryczny:**
  Koło domknięte o środku w punkcie $(0, -2)$ (czyli $z_0 = -2j$) i promieniu $R = \sqrt{6}$. Wraz z brzegiem (okręgiem $x^2 + (y + 2)^2 = 6$, linia ciągła).

---

### 5.4: $\left|\frac{z - j}{z + 2 + j}\right| \ge 1$
* **Rozwiązanie:**
  Dziedzina: $z \ne -2 - j$.
  $$\frac{|z - j|}{|z - (-2 - j)|} \ge 1 \iff |z - j| \ge |z - (-2 - j)|$$
  Geometrycznie oznacza to zbiór punktów $z$, których odległość od punktu $A = j = (0, 1)$ jest większa bądź równa odległości od punktu $B = -2 - j = (-2, -1)$.
* **Wyznaczenie symetralnej:**
  * Środek odcinka $AB$:
    $$S = \frac{A + B}{2} = \left(\frac{0 + (-2)}{2}, \frac{1 + (-1)}{2}\right) = (-1, 0)$$
  * Wektor $\vec{AB} = [-2 - 0, -1 - 1] = [-2, -2]$.
  * Równanie symetralnej: prosta prostopadła do wektora $[-2, -2]$ przechodząca przez $(-1, 0)$:
    $$-2(x - (-1)) - 2(y - 0) = 0 \iff -2(x + 1) - 2y = 0 \iff x + y + 1 = 0 \iff y = -x - 1$$
* **Wybór półpłaszczyzny:**
  Sprawdzamy np. punkt $B(-2, -1)$: odległość od $B$ wynosi 0, od $A$ wynosi $\sqrt{8} > 0$, więc nierówność jest spełniona. Punkt $B$ leży poniżej/na lewo od prostej $x + y + 1 = 0$.
  Formalnie podstawiając $z = x + jy$:
  $$x^2 + (y - 1)^2 \ge (x + 2)^2 + (y + 1)^2$$
  $$x^2 + y^2 - 2y + 1 \ge x^2 + 4x + 4 + y^2 + 2y + 1$$
  $$-2y \ge 4x + 2y + 4 \iff -4y \ge 4x + 4 \iff x + y + 1 \le 0$$
* **Opis geometryczny:**
  Domknięta półpłaszczyzna leżąca poniżej i na prostej $y = -x - 1$ (czyli $x + y + 1 \le 0$) z wyłączeniem punktu $z = -2 - j$ (gdyż nie należy on do dziedziny wyrażenia).

---

### 5.5a: $|z - j| + |z + j| = 4$
* **Rozwiązanie geometryczne:**
  Warunek ma postać:
  $$|z - F_1| + |z - F_2| = 2a$$
  gdzie $F_1 = j = (0, 1)$, $F_2 = -j = (0, -1)$, a stała suma odległości wynosi $2a = 4 \implies a = 2$.
  * Ogniska leżą na osi urojonej (pionowej).
  * Odległość między ogniskami: $2c = |j - (-j)| = 2 \implies c = 1$.
  * Ponieważ $2a = 4 > 2c = 2$, równanie to opisuje **elipsę**.
  * Środek elipsy: $(0, 0)$.
  * Półosie:
    * Wielka półoś (pionowa): $a = 2$.
    * Mała półoś (pozioma): $b = \sqrt{a^2 - c^2} = \sqrt{2^2 - 1^2} = \sqrt{3}$.
  * Równanie we współrzędnych kartezjańskich:
    $$\frac{x^2}{3} + \frac{y^2}{4} = 1$$
* **Opis geometryczny:**
  Elipsa o środku w $(0, 0)$, wierzchołkach na osi pionowej w $(0, 2)$ i $(0, -2)$, wierzchołkach na osi poziomej w $(\sqrt{3}, 0)$ i $(-\sqrt{3}, 0)$, oraz ogniskach w $(0, 1)$ i $(0, -1)$.

---

### 5.5b: $|z - j| + |z + j| = 2$
* **Rozwiązanie geometryczne:**
  Mamy sumę odległości punktu $z$ od $F_1(0, 1)$ oraz $F_2(0, -1)$ równą $2$.
  * Odległość między punktami $F_1$ i $F_2$ wynosi dokładnie $|F_1 - F_2| = 2$.
  * Z nierówności trójkąta dla dowolnego punktu $z$:
    $$|z - j| + |z + j| \ge |(z - j) - (z + j)| = |-2j| = 2$$
  * Równość zachodzi wtedy i tylko wtedy, gdy punkt $z$ leży na odcinku łączącym punkty $F_1(0, 1)$ i $F_2(0, -1)$.
* **Opis geometryczny:**
  Odcinek na osi urojonej łączący punkty $-j$ oraz $j$ (czyli odcinek na osi OY dla $x = 0$ i $y \in [-1, 1]$).

---

### 5.6: $|z - 1| = |2jz + 1|$
* **Rozwiązanie algebraiczne:**
  Wyłączamy $2j$ z prawej strony (lub przekształcamy bezpośrednio):
  $$|2jz + 1| = \left|2j\left(z + \frac{1}{2j}\right)\right| = |2j| \cdot \left|z - \frac{1}{2}j\right| = 2 \left|z - \frac{1}{2}j\right|$$
  Zatem:
  $$|z - 1| = 2\left|z - \frac{1}{2}j\right|$$
  Podnosząc obustronnie do kwadratu:
  $$|z - 1|^2 = 4\left|z - \frac{1}{2}j\right|^2$$
  Niech $z = x + jy$:
  $$(x - 1)^2 + y^2 = 4\left[x^2 + \left(y - \frac{1}{2}\right)^2\right]$$
  $$x^2 - 2x + 1 + y^2 = 4\left[x^2 + y^2 - y + \frac{1}{4}\right] = 4x^2 + 4y^2 - 4y + 1$$
  Upraszczamy:
  $$3x^2 + 3y^2 + 2x - 4y = 0$$
  Dzielimy przez 3:
  $$x^2 + \frac{2}{3}x + y^2 - \frac{4}{3}y = 0$$
  Dopełniamy do kwadratów:
  $$\left(x + \frac{1}{3}\right)^2 - \frac{1}{9} + \left(y - \frac{2}{3}\right)^2 - \frac{4}{9} = 0$$
  $$\left(x + \frac{1}{3}\right)^2 + \left(y - \frac{2}{3}\right)^2 = \frac{5}{9}$$
* **Opis geometryczny:**
  Jest to okrąg (okrąg Apoloniusza) o środku w punkcie:
  $$S = \left(-\frac{1}{3}, \frac{2}{3}\right) \quad \left(z_0 = -\frac{1}{3} + \frac{2}{3}j\right)$$
  i promieniu:
  $$R = \frac{\sqrt{5}}{3}$$

---

### 5.7: $\text{Re}\left(\frac{z + j}{z - j}\right) \le 0$
* **Rozwiązanie:**
  Dziedzina: $z \ne j$ (czyli $(x, y) \ne (0, 1)$).
  Niech $z = x + jy$:
  $$\frac{z + j}{z - j} = \frac{x + j(y + 1)}{x + j(y - 1)} = \frac{[x + j(y + 1)][x - j(y - 1)]}{x^2 + (y - 1)^2}$$
  Licznik:
  $$[x + j(y + 1)][x - j(y - 1)] = x^2 - jx(y - 1) + jx(y + 1) + (y + 1)(y - 1)$$
  $$= x^2 + (y^2 - 1) + j[ -xy + x + xy + x ] = (x^2 + y^2 - 1) + 2xj$$
  Część rzeczywista wynosi zatem:
  $$\text{Re}\left(\frac{z + j}{z - j}\right) = \frac{x^2 + y^2 - 1}{x^2 + (y - 1)^2}$$
  Warunek $\text{Re} \le 0$:
  $$\frac{x^2 + y^2 - 1}{x^2 + (y - 1)^2} \le 0$$
  Ponieważ mianownik $x^2 + (y - 1)^2 > 0$ dla $z \ne j$, nierówność sprowadza się do:
  $$x^2 + y^2 - 1 \le 0 \iff x^2 + y^2 \le 1 \quad \text{oraz} \quad z \ne j$$
* **Opis geometryczny:**
  Koło domknięte o środku w $(0, 0)$ i promieniu $R = 1$ ($|z| \le 1$), **z wyłączeniem punktu** $z = j = (0, 1)$.

---

## Zadanie 6

Wyznaczyć argument główny $\arg(z) \in (-\pi, \pi]$ (lub $[0, 2\pi)$) oraz moduł podanych liczb (wykorzystać funkcje $\arcsin$ lub $\arctg$):

### 6.1: $z_1 = 1 + 2j$
* **Moduł:**
  $$|z_1| = \sqrt{1^2 + 2^2} = \sqrt{1 + 4} = \sqrt{5}$$
* **Ćwiartka:** I ćwiartka ($x = 1 > 0, y = 2 > 0$).
* **Argument główny:**
  * Za pomocą $\arctg$:
    $$\arg(z_1) = \arctg\left(\frac{y}{x}\right) = \arctg(2)$$
  * Za pomocą $\arcsin$:
    $$\arg(z_1) = \arcsin\left(\frac{y}{|z_1|}\right) = \arcsin\left(\frac{2}{\sqrt{5}}\right) = \arcsin\left(\frac{2\sqrt{5}}{5}\right)$$

---

### 6.2: $z_2 = 3j - 4 = -4 + 3j$
* **Moduł:**
  $$|z_2| = \sqrt{(-4)^2 + 3^2} = \sqrt{16 + 9} = \sqrt{25} = 5$$
* **Ćwiartka:** II ćwiartka ($x = -4 < 0, y = 3 > 0$).
* **Argument główny:**
  * Za pomocą $\arctg$:
    Dla punktów w II ćwiartce kąt to $\pi + \arctg\left(\frac{y}{x}\right) = \pi - \arctg\left(\frac{3}{4}\right)$:
    $$\arg(z_2) = \pi - \arctg\left(\frac{3}{4}\right)$$
  * Za pomocą $\arcsin$:
    Kąt w II ćwiartce o sinusie równym $\frac{3}{5}$:
    $$\arg(z_2) = \pi - \arcsin\left(\frac{3}{5}\right)$$

---

### 6.3: $z_3 = 5 - 2j$
* **Moduł:**
  $$|z_3| = \sqrt{5^2 + (-2)^2} = \sqrt{25 + 4} = \sqrt{29}$$
* **Ćwiartka:** IV ćwiartka ($x = 5 > 0, y = -2 < 0$).
* **Argument główny:**
  * W przedziale $(-\pi, \pi]$:
    * Za pomocą $\arctg$:
      $$\arg(z_3) = \arctg\left(\frac{-2}{5}\right) = -\arctg\left(\frac{2}{5}\right)$$
    * Za pomocą $\arcsin$:
      $$\arg(z_3) = \arcsin\left(\frac{-2}{\sqrt{29}}\right) = -\arcsin\left(\frac{2\sqrt{29}}{29}\right)$$
  * W przedziale $[0, 2\pi)$:
    $$\arg(z_3) = 2\pi - \arctg\left(\frac{2}{5}\right) = 2\pi - \arcsin\left(\frac{2}{\sqrt{29}}\right)$$

---

### 6.4: $z_4 = -6 - 8j$
* **Moduł:**
  $$|z_4| = \sqrt{(-6)^2 + (-8)^2} = \sqrt{36 + 64} = \sqrt{100} = 10$$
* **Ćwiartka:** III ćwiartka ($x = -6 < 0, y = -8 < 0$).
* **Argument główny:**
  * W konwencji $(-\pi, \pi]$:
    * Za pomocą $\arctg$:
      $$\arg(z_4) = -\pi + \arctg\left(\frac{-8}{-6}\right) = -\pi + \arctg\left(\frac{4}{3}\right)$$
    * Za pomocą $\arcsin$:
      $$\arg(z_4) = -\pi - \arcsin\left(\frac{-8}{10}\right) = -\pi + \arcsin\left(\frac{4}{5}\right)$$
  * W konwencji $[0, 2\pi)$:
    $$\arg(z_4) = \pi + \arctg\left(\frac{4}{3}\right) = \pi + \arcsin\left(\frac{4}{5}\right)$$
