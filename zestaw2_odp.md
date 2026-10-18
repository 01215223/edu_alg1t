# Algebra — Zestaw 2: rozwiązania

Poniżej pełny przebieg rozwiązań w notacji zespolonej; \(j^2=-1\), a liczba \(z=re^{j\varphi}\) ma moduł \(r\) i argument \(\varphi\). Wzór de Moivre’a: \((re^{j\varphi})^n=r^ne^{jn\varphi}\). [ppl-ai-file-upload.s3.amazonaws](https://ppl-ai-file-upload.s3.amazonaws.com/web/direct-files/attachments/51255189/b058a360-2142-4783-a8fc-9506488f9d39/zestaw2.md?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Checksum-Mode=ENABLED&X-Amz-Credential=ASIA2F3EMEYEWZYUT2GM%2F20261018%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Date=20261018T182241Z&X-Amz-Expires=931&X-Amz-Security-Token=IQoJb3JpZ2luX2VjEFIaCXVzLWVhc3QtMSJHMEUCIQDug%2BytufmhIXP8t2vEAEaInM3YrTqqwdQzZ7cDX12u%2FAIgaDDRa96M%2BOnajabmBZylgtaRr8i6APHdGuq6lGrcbTwqgAUIGhABGgw2OTk3NTMzMDk3MDUiDEoR3HTRhLOTkLqmkyrdBBuTk50VcpTGkWUJrS%2F7%2FezhLWEdyZCFpxK4zM0cbb%2FXlxzOLr1krg03%2Bj9qMECVTkeNuZYYydSytPOMSqvkJBygasi0FHTFUxxMdmliyLqdT81D1lt9Not1ZiaytPWZf5Hg%2FDU6P39eU2KGyoYd6s2Y0F9JjBeXwkyRtf0YUnOnVJOXaY9KH7USc08NQmTwo65pBh29KuSl%2F725eYLfHj1zpVSShopnEBPfU%2FPveBrz9XB4mPJ%2FYG2EF6iVWSJt9X4yTmQaqTyptD%2FHHqHPVoAe4QeS5vrLopu%2Fj3DbhFzEGYMTYHXKpQnZ82xKw0wlu8L1AcpC3wGnYGgzDsWCTGiEt%2F%2BtCZsDM5%2FJVszjQRZygS9OBEOHW%2BiCszor8ZKk7OISjn6zye6%2B7%2FOwrpBsrGolshGaPSo2yJxeyeVY1Dj6sLt%2BJnEL1MxtGqcy5d3cyn8lcCLAir7BH7KDfZRiD6kn39gobOPdomkXAWJO4ZXx9%2BmA%2Ft6JHmjWBtWf5dqyP2DI3K%2F%2BqS1xPouzCj85IjwU8gl0AN38e62eKaG07T2Q2BEnFe7BbvCn5vIxorXGTocf3E%2BQIvkTO%2FGc%2BESrlk9p1rqLlHWbss5XLvKP%2BlsUzF02G%2FErYSLDX8SK8QKjBojB7Ls0QvbfbEVQv0kRZOGahuhr1LsebQ87gADaXHYHodaAS9r7gSQD%2BVVbwg5HooLHqf%2BOE8YB7ypXJnvELkdlINK0FEHKICDv4it%2BTCDRsN%2BomPpc%2BjUnvKg1Z%2F48IJbDO1XlhII%2BxOYm3hyKoX4Kq9UYYwVMufmb5XWVMMGI1NYGOpgBR4KnZeWD1cZryqrkWUm7OAagUTndD0EBmocqOhQBM6u1Lhlsy4lu1VmKRScAvedTjtkaGw9xCS3BQ9hvM24PmJdalDMDy7TWT8Pbgue6YFsc2eIoYBBL4cxm0wAd6w0OU8nndwMssRptMcox6E9l1M1dRLz3ylRx20IvtmQ%2BlEUMuNHqWFYrsUAxNXO3ZTK1Cw8sGKrS7F8%3D&X-Amz-SignedHeaders=host&x-id=GetObject&X-Amz-Signature=cd2ba8013079b73744e4d9b7dd335a6d26dd135c10ccfb508e9829e9a3478413)

## Zadanie 1 — potęgi i pierwiastki

### 1.1

\[
\frac{(-2+2\sqrt3j)^{21}}{(2-2j)^{26}}
\]

Zapisujemy w postaci wykładniczej:

\[
-2+2\sqrt3j=4e^{j\frac{2\pi}{3}},
\qquad
2-2j=2\sqrt2e^{-j\frac{\pi}{4}}.
\]

Stąd:

\[
(-2+2\sqrt3j)^{21}=4^{21}e^{j14\pi}=4^{21},
\]

\[
(2-2j)^{26}=(2\sqrt2)^{26}e^{-j\frac{13\pi}{2}}
=2^{39}e^{-j\frac{\pi}{2}}=-2^{39}j.
\]

Zatem:

\[
\frac{4^{21}}{-2^{39}j}
=\frac{2^{42}}{-2^{39}j}
=\frac{8}{-j}=8j.
\]

\[
\boxed{\frac{(-2+2\sqrt3j)^{21}}{(2-2j)^{26}}=8j}
\]

### 1.2

\[
\left(\frac{2j-4}{j+3}\right)^{101}
\]

Najpierw upraszczamy podstawę:

\[
\frac{-4+2j}{3+j}
=\frac{(-4+2j)(3-j)}{(3+j)(3-j)}
=\frac{-10+10j}{10}
=-1+j.
\]

Ponadto:

\[
-1+j=\sqrt2e^{j\frac{3\pi}{4}}.
\]

Więc:

\[
(-1+j)^{101}
=(\sqrt2)^{101}e^{j\frac{303\pi}{4}}
=2^{50}\sqrt2e^{j\frac{303\pi}{4}}.
\]

Ponieważ \(\frac{303\pi}{4}=75\pi+\frac{3\pi}{4}\), mamy:

\[
e^{j\frac{303\pi}{4}}
=e^{j75\pi}e^{j\frac{3\pi}{4}}
=-e^{j\frac{3\pi}{4}}
=e^{-j\frac{\pi}{4}}.
\]

Zatem:

\[
\boxed{\left(\frac{2j-4}{j+3}\right)^{101}=2^{50}(1-j)}
\]

### 1.3

\[
\sqrt{7-24j}
\]

Szukamy \(z=x+yj\) takiego, że \(z^2=7-24j\):

\[
(x+yj)^2=x^2-y^2+2xyj=7-24j.
\]

Układ równań:

\[
x^2-y^2=7,
\qquad
2xy=-24.
\]

Rozwiązaniem jest \(x=4,\ y=-3\) lub \(x=-4,\ y=3\). Zatem:

\[
\boxed{\sqrt{7-24j}=\pm(4-3j)}
\]

### 1.4

\[
\sqrt{3j-\sqrt3}
\]

Moduł i argument:

\[
3j-\sqrt3=\sqrt6e^{j\frac{2\pi}{3}}.
\]

Pierwiastki czwartego stopnia:

\[
z_k=6^{1/4}e^{j\left(\frac{2\pi/3+2k\pi}{4}\right)}
=6^{1/4}e^{j\left(\frac{\pi}{6}+\frac{k\pi}{2}\right)},
\qquad k=0,1,2,3.
\]

Czyli:

\[
\boxed{
z_k=6^{1/4}\left[
\cos\left(\frac{\pi}{6}+\frac{k\pi}{2}\right)
+j\sin\left(\frac{\pi}{6}+\frac{k\pi}{2}\right)
\right],
\quad k=0,1,2,3
}
\]

Wartości przybliżone:

\[
\boxed{
\begin{aligned}
z_0&\approx1.1815+0.6821j,\\
z_1&\approx-0.6821+1.1815j,\\
z_2&\approx-1.1815-0.6821j,\\
z_3&\approx0.6821-1.1815j.
\end{aligned}}
\]

### 1.5

\[
\sqrt{-4+3j}
\]

Moduł:

\[
|-4+3j|=\sqrt{16+9}=5.
\]

Argument, z kalkulatora:

\[
\varphi=\pi-\arctan\frac34\approx2.4981.
\]

Zatem:

\[
-4+3j=5e^{j2.4981}.
\]

Pierwiastki sześcienne:

\[
\boxed{
z_k=5^{1/3}e^{j\left(\frac{2.4981+2k\pi}{3}\right)},
\qquad k=0,1,2.
}
\]

Wartości przybliżone:

\[
\boxed{
\begin{aligned}
z_0&\approx1.1506+1.2650j,\\
z_1&\approx-1.6708+0.3640j,\\
z_2&\approx0.5202-1.6289j.
\end{aligned}}
\]

### 1.6

\[
\sqrt{(1-j\sqrt3)(2j-2)}
\]

Najpierw obliczamy iloczyn:

\[
(1-j\sqrt3)(2j-2)
=2j-2-2\sqrt3j^2+2\sqrt3j
=-4+3j.
\]

Czyli zadanie sprowadza się do:

\[
\sqrt{-4+3j}.
\]

Ponieważ:

\[
-4+3j=5e^{j2.4981},
\]

to:

\[
\boxed{
z_k=5^{1/5}e^{j\left(\frac{2.4981+2k\pi}{5}\right)},
\qquad k=0,1,2,3,4.
}
\]

Wartości przybliżone:

\[
\boxed{
\begin{aligned}
z_0&\approx1.3660+0.3660j,\\
z_1&\approx0.0740+1.4123j,\\
z_2&\approx-1.3203+0.5068j,\\
z_3&\approx-0.8900-1.0991j,\\
z_4&\approx0.7702-1.1861j.
\end{aligned}}
\]

## Zadanie 2 — wzór de Moivre’a

Korzystamy z:

\[
(\cos x+j\sin x)^4=\cos4x+j\sin4x.
\]

Rozwijamy przez wzór dwumianowy:

\[
(\cos x+j\sin x)^4
=c^4+4c^3(js)+6c^2(js)^2+4c(js)^3+(js)^4,
\]

gdzie \(c=\cos x\), \(s=\sin x\). Ponieważ \(j^2=-1\), \(j^3=-j\), \(j^4=1\), otrzymujemy:

\[
(\cos x+j\sin x)^4
=(c^4-6c^2s^2+s^4)
+j(4c^3s-4cs^3).
\]

Porównując części rzeczywistą i urojoną:

\[
\boxed{\cos4x=8\cos^4x-8\cos^2x+1}
\]

\[
\boxed{\sin4x=4\sin x\cos x(\cos^2x-\sin^2x)}
\]

## Zadanie 3 — równania

### 3.1

\[
(z^4-16)(z^2-4j+3)=0
\]

Rozpatrujemy osobno oba czynniki.

**Pierwszy czynnik:**

\[
z^4=16=16e^{j2k\pi}.
\]

Zatem:

\[
z_k=2e^{j\left(\frac{\pi}{4}+\frac{k\pi}{2}\right)},
\qquad k=0,1,2,3.
\]

Czyli:

\[
z\in\{\sqrt2+\sqrt2j,\ -\sqrt2+\sqrt2j,\ -\sqrt2-\sqrt2j,\ \sqrt2-\sqrt2j\}.
\]

**Drugi czynnik:**

\[
z^2-4j+3=0
\implies z^2=-3+4j.
\]

Ponieważ:

\[
(1+2j)^2=1-4+4j=-3+4j,
\]

to:

\[
z=\pm(1+2j).
\]

Zatem:

\[
\boxed{
z\in\{\pm(\sqrt2+\sqrt2j),\ \pm(\sqrt2-\sqrt2j),\ \pm(1+2j)\}
}
\]

Dokładniej:

\[
\boxed{
\begin{aligned}
&\sqrt2+\sqrt2j,\quad -\sqrt2+\sqrt2j,\\
&-\sqrt2-\sqrt2j,\quad \sqrt2-\sqrt2j,\\
&1+2j,\quad -1-2j.
\end{aligned}}
\]

**Szkic:** cztery pierwiastki z \(z^4=16\) leżą na okręgu o promieniu \(2\), pod kątami \(45^\circ,135^\circ,225^\circ,315^\circ\). Dwa pozostałe rozwiązania to punkty \((1,2)\) i \((-1,-2)\).

### 3.2

\[
|z|^2+z=7-j
\]

Niech \(z=x+yj\). Wtedy \(|z|^2=x^2+y^2\), więc:

\[
x^2+y^2+x+yj=7-j.
\]

Porównujemy części urojone:

\[
y=-1.
\]

Porównujemy części rzeczywiste:

\[
x^2+1+x=7
\implies x^2+x-6=0.
\]

Stąd:

\[
(x+3)(x-2)=0
\implies x=-3\ \text{lub}\ x=2.
\]

Zatem:

\[
\boxed{z=2-j\quad\text{lub}\quad z=-3-j}
\]

**Szkic:** dwa punkty na prostej \(y=-1\): \((2,-1)\) oraz \((-3,-1)\).

### 3.3

\[
z^4|z|=-8(\overline z)^2
\]

Niech \(z=re^{j\varphi}\). Wtedy \(\overline z=re^{-j\varphi}\), więc:

\[
r^4e^{j4\varphi}\cdot r=-8r^2e^{-j2\varphi}.
\]

Czyli:

\[
r^3e^{j4\varphi}=-8e^{-j2\varphi}.
\]

Dla \(r=0\) dostajemy rozwiązanie \(z=0\).

Dla \(r>0\):

\[
r^3=8\implies r=2,
\]

oraz:

\[
e^{j6\varphi}=-1=e^{j(\pi+2k\pi)}.
\]

Zatem:

\[
6\varphi=\pi+2k\pi
\implies
\varphi=\frac{\pi}{6}+\frac{k\pi}{3},
\qquad k=0,1,\dots,5.
\]

Zatem:

\[
\boxed{
z=0
\quad\text{lub}\quad
z=2e^{j\left(\frac{\pi}{6}+\frac{k\pi}{3}\right)},
\qquad k=0,1,\dots,5.
}
\]

**Szkic:** początek układu oraz sześć punktów na okręgu o promieniu \(2\), co \(60^\circ\), zaczynając od kąta \(30^\circ\).

### 3.4

\[
z^2-z=\frac{2j-14}{j+3}
\]

Najpierw upraszczamy prawą stronę:

\[
\frac{2j-14}{j+3}
=\frac{(-14+2j)(3-j)}{10}
=\frac{-40+20j}{10}
=-4+2j.
\]

Zatem:

\[
z^2-z+4-2j=0.
\]

Rozwiązujemy wzorem kwadratowym:

\[
z=\frac{1\pm\sqrt{1-4(4-2j)}}{2}
=\frac{1\pm\sqrt{-15+8j}}{2}.
\]

Ponieważ:

\[
(1+4j)^2=1-16+8j=-15+8j,
\]

to:

\[
z=\frac{1\pm(1+4j)}{2}.
\]

Zatem:

\[
\boxed{z=1+2j\quad\text{lub}\quad z=-2j}
\]

**Szkic:** punkty \((1,2)\) oraz \((0,-2)\).

### 3.5

\[
(z-j)^4=(\sqrt3+j)^6
\]

Zapisujemy:

\[
\sqrt3+j=2e^{j\frac{\pi}{6}}.
\]

Zatem:

\[
(\sqrt3+j)^6=2^6e^{j\pi}=-64.
\]

Równanie ma postać:

\[
(z-j)^4=-64=64e^{j\pi}.
\]

Stąd:

\[
z-j=64^{1/4}e^{j\left(\frac{\pi+2k\pi}{4}\right)}
=2\sqrt2e^{j\left(\frac{\pi}{4}+\frac{k\pi}{2}\right)},
\qquad k=0,1,2,3.
\]

Czyli:

\[
\boxed{
z=j+2\sqrt2e^{j\left(\frac{\pi}{4}+\frac{k\pi}{2}\right)},
\qquad k=0,1,2,3.
}
\]

Wartości dokładne:

\[
\boxed{
\begin{aligned}
z_0&=2+3j,\\
z_1&=-2+3j,\\
z_2&=-2-j,\\
z_3&=2-j.
\end{aligned}}
\]

**Szkic:** cztery wierzchołki kwadratu o środku \(j\), czyli punkcie \((0,1)\).

### 3.6

\[
z^4=-\overline z^4
\]

Równoważnie:

\[
z^4+\overline z^4=0.
\]

Niech \(z=re^{j\varphi}\). Wtedy:

\[
z^4+\overline z^4
=r^4e^{j4\varphi}+r^4e^{-j4\varphi}
=2r^4\cos4\varphi.
\]

Zatem:

\[
2r^4\cos4\varphi=0.
\]

Dostajemy dwa przypadki:

\[
r=0\implies z=0,
\]

albo:

\[
\cos4\varphi=0
\implies
4\varphi=\frac{\pi}{2}+k\pi
\implies
\varphi=\frac{\pi}{8}+\frac{k\pi}{4}.
\]

Zatem:

\[
\boxed{
z=0
\quad\text{lub}\quad
z=re^{j\left(\frac{\pi}{8}+\frac{k\pi}{4}\right)},
\qquad r>0,\ k=0,1,\dots,7.
}
\]

**Szkic:** początek układu oraz osiem półprostych wychodzących z początku układu, co \(45^\circ\); pierwszy kierunek ma kąt \(22{,}5^\circ\).

## Zadanie 4 — trójkąt równoboczny

Jeden wierzchołek:

\[
A=5-2j.
\]

Środek trójkąta:

\[
S=1+2j.
\]

Wektor od środka do znanego wierzchołka:

\[
A-S=(5-2j)-(1+2j)=4-4j.
\]

Pozostałe wierzchołki otrzymujemy przez obrót tego wektora o \(\pm120^\circ\):

\[
B=S+(A-S)e^{j\frac{2\pi}{3}},
\qquad
C=S+(A-S)e^{-j\frac{2\pi}{3}}.
\]

Obliczamy:

\[
B=(1+2j)+(4-4j)e^{j\frac{2\pi}{3}}
=(2\sqrt3-1)+(4+2\sqrt3)j,
\]

\[
C=(1+2j)+(4-4j)e^{-j\frac{2\pi}{3}}
=(-1-2\sqrt3)+(2-2\sqrt3)j.
\]

Zatem:

\[
\boxed{
B=(2\sqrt3-1)+(4+2\sqrt3)j
}
\]

\[
\boxed{
C=(-1-2\sqrt3)+(2-2\sqrt3)j
}
\]

Przybliżenie:

\[
\boxed{
B\approx2.4641+7.4641j,
\qquad
C\approx-4.4641+0.5359j.
}
\]

## Zadanie 5 — funkcje trygonometryczne zespolone

### 5.1

\[
\cos(j\pi-\pi)
\]

Ponieważ cosinus jest funkcją parzystą:

\[
\cos(j\pi-\pi)=\cos(-\pi+j\pi)=\cos(\pi-j\pi).
\]

Ze wzoru:

\[
\cos(a+bj)=\cos a\cosh b-j\sin a\sinh b.
\]

Dla \(a=\pi\), \(b=-1\):

\[
\cos(\pi-j\pi)
=\cos\pi\cosh1-j\sin\pi\sinh1
=-\cosh1.
\]

Zatem:

\[
\boxed{\cos(j\pi-\pi)=-\cosh\pi\approx-11.5920}
\]

### 5.2

\[
\sin\left(\frac{\pi}{2}+7j\right)
\]

Ze wzoru:

\[
\sin(a+bj)=\sin a\cosh b+j\cos a\sinh b.
\]

Dla \(a=\frac{\pi}{2}\), \(b=7\):

\[
\sin\left(\frac{\pi}{2}+7j\right)
=\sin\frac{\pi}{2}\cosh7+j\cos\frac{\pi}{2}\sinh7.
\]

Ponieważ \(\sin\frac{\pi}{2}=1\) oraz \(\cos\frac{\pi}{2}=0\):

\[
\boxed{\sin\left(\frac{\pi}{2}+7j\right)=\cosh7\approx548.3170}
\]
