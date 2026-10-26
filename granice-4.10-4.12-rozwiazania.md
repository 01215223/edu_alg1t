# Granice funkcji — rozwiązania ćwiczeń 4.10–4.12

W rozwiązaniach nie korzystam z gotowych wzorów na granice wyrażeń logarytmicznych ani z reguły de l’Hospitala. Potrzebny fakt o logarytmie wyprowadzam poniżej bezpośrednio z jego definicji całkowej.

## Dwa uzasadnienia pomocnicze

### Granica logarytmu — wyprowadzona z definicji

Dla \(u>-1\), z definicji logarytmu naturalnego
\[
\ln(1+u)=\int_0^u\frac{dt}{1+t}.
\]
Dla \(u\ne0\), po podstawieniu \(t=su\), otrzymujemy
\[
\frac{\ln(1+u)}u=\int_0^1\frac{ds}{1+su}.
\]
Jeśli \(|u|<1\), to
\[
\left|\frac{\ln(1+u)}u-1\right|
=\left|\int_0^1\frac{-su}{1+su}\,ds\right|
\leq \frac{|u|}{1-|u|}.
\]
W szczególności, gdy \(|u|<\tfrac12\), prawa strona jest mniejsza niż \(2|u|\). Zatem dla dowolnego \(\varepsilon>0\), wybierając \(0<|u|<\min(\tfrac12,\tfrac\varepsilon2)\), dostajemy
\[
\left|\frac{\ln(1+u)}u-1\right|<\varepsilon.
\]
To jest uzasadnienie z definicji (przez oszacowanie), że iloraz ten dąży do \(1\). Będziemy stosować oszacowanie także wtedy, gdy \(u\) jest wyrażeniem zależnym od \(x\) i \(u(x)\to0\).

### Podstawowa granica trygonometryczna

Dla \(0<|t|<\pi/2\) zachodzi nierówność
\[
\cos t\leq\frac{\sin t}{t}\leq1.
\]
Ponieważ \(\cos t\to1\) (ciągłość cosinusa), z twierdzenia o trzech funkcjach wynika
\[
\lim_{t\to0}\frac{\sin t}{t}=1.
\]
Wszystkie poniższe użycia tej granicy odnoszą się do tej nierówności, a nie do reguły de l’Hospitala.

---

## Ćwiczenie 4.10

### 1. \(\displaystyle\lim_{x\to1}\frac{x^3-3x^2+3x-1}{x^3-x^2-x+1}\)

Rozkładamy licznik i mianownik na czynniki:
\[
 x^3-3x^2+3x-1=(x-1)^3,
\]
\[
 x^3-x^2-x+1=x^2(x-1)-1(x-1)=(x-1)(x^2-1)=(x-1)^2(x+1).
\]
Dla \(x\ne1\) ułamek jest więc równy
\[
\frac{(x-1)^3}{(x-1)^2(x+1)}=\frac{x-1}{x+1}.
\]
W otoczeniu punktu \(1\) (z wyłączeniem samego punktu) mianownik \(x+1\) nie jest zerem, a wyrażenie po skróceniu jest ciągłe. Stąd
\[
\boxed{\lim_{x\to1}\frac{x^3-3x^2+3x-1}{x^3-x^2-x+1}=0.}
\]

### 2. \(\displaystyle\lim_{x\to0^+}\frac{x-\sqrt{x}}{x+\sqrt{x}}\)

Dla \(x>0\) wyłączamy \(\sqrt{x}\) w liczniku i mianowniku:
\[
\frac{x-\sqrt{x}}{x+\sqrt{x}}
=\frac{\sqrt{x}(\sqrt{x}-1)}{\sqrt{x}(\sqrt{x}+1)}
=\frac{\sqrt{x}-1}{\sqrt{x}+1}.
\]
Gdy \(x\to0^+\), ciągłość pierwiastka daje \(\sqrt{x}\to0\), więc
\[
\boxed{\lim_{x\to0^+}\frac{x-\sqrt{x}}{x+\sqrt{x}}=-1.}
\]

### 3. \(\displaystyle\lim_{x\to0}\frac{\tan 3x}{\sin 7x}\)

Dla \(x\) bliskich zeru, ale niezerowych, przekształcamy:
\[
\frac{\tan 3x}{\sin 7x}
=\frac{\sin 3x}{\cos 3x\,\sin 7x}
=\frac37\,\frac{\sin 3x}{3x}\,\frac{7x}{\sin 7x}\,\frac1{\cos 3x}.
\]
Z uzasadnionej wyżej granicy \(\sin t/t\to1\), ciągłości cosinusa i \(\cos0=1\), każdy z trzech czynników poza \(3/7\) dąży do \(1\). Zatem
\[
\boxed{\lim_{x\to0}\frac{\tan 3x}{\sin 7x}=\frac37.}
\]

### 4. \(\displaystyle\lim_{x\to-1}\frac{\sin(x^2-1)}{x+1}\)

Dla \(x\ne-1\) zapisujemy \(x^2-1=(x-1)(x+1)\), a następnie
\[
\frac{\sin(x^2-1)}{x+1}
=(x-1)\frac{\sin(x^2-1)}{x^2-1}.
\]
Gdy \(x\to-1\), mamy \(x^2-1\to0\). Zatem drugi czynnik dąży do \(1\) na mocy granicy \(\sin t/t\to1\), a pierwszy do \(-2\). Stąd
\[
\boxed{\lim_{x\to-1}\frac{\sin(x^2-1)}{x+1}=-2.}
\]

### 5. \(\displaystyle\lim_{x\to1^+}\left(\frac{x+1}{2x}\right)^{\!\frac3{x-1}}\)

Dla \(x>1\) podstawa jest dodatnia, więc możemy zastosować logarytm. Oznaczmy
\[
F(x)=\left(\frac{x+1}{2x}\right)^{\!\frac3{x-1}},\qquad
u(x)=-\frac{x-1}{2x}.
\]
Wtedy \(\frac{x+1}{2x}=1+u(x)>0\), a \(u(x)\to0\) przy \(x\to1^+\). Logarytm wyrażenia wynosi
\[
\ln F(x)=\frac3{x-1}\ln(1+u(x))
=\frac3{x-1}\,u(x)\,\frac{\ln(1+u(x))}{u(x)}
=-\frac3{2x}\,\frac{\ln(1+u(x))}{u(x)}.
\]
Z wyprowadzonego wyżej oszacowania logarytmu ostatni iloraz dąży do \(1\), a \(x\to1\). Wobec tego \(\ln F(x)\to-\tfrac32\). Ponieważ funkcja wykładnicza jest ciągła,
\[
\boxed{\lim_{x\to1^+}\left(\frac{x+1}{2x}\right)^{\!\frac3{x-1}}=e^{-3/2}.}
\]

### 6. \(\displaystyle\lim_{x\to-\infty}\bigl(3x+1+\sqrt{9x^2-2}\bigr)\)

Dla dostatecznie ujemnych \(x\) wyrażenie pod pierwiastkiem jest dodatnie. Racjonalizujemy sumę \(3x+\sqrt{9x^2-2}\):
\[
\sqrt{9x^2-2}+3x
=\frac{(\sqrt{9x^2-2}+3x)(\sqrt{9x^2-2}-3x)}{\sqrt{9x^2-2}-3x}
=\frac{-2}{\sqrt{9x^2-2}-3x}.
\]
Gdy \(x\to-\infty\), mianownik dąży do \(+\infty\) (na przykład jest nie mniejszy niż \(-3x\)), zatem ten ułamek dąży do zera. Ostatecznie
\[
\boxed{\lim_{x\to-\infty}\bigl(3x+1+\sqrt{9x^2-2}\bigr)=1.}
\]

---

## Ćwiczenie 4.11

Rozważamy \(f(x)=(1-\sin x)^{1/x}\) w otoczeniu zera, z wyłączeniem \(x=0\). Ponieważ \(1-\sin x\to1\), podstawa jest dodatnia w pewnym otoczeniu zera i możemy logarytmować. Oznaczmy \(u(x)=-\sin x\). Wówczas
\[
\ln f(x)=\frac{\ln(1-\sin x)}x
=\frac{\ln(1+u(x))}{u(x)}\,\frac{-\sin x}{x}.
\]
Dla \(x\ne0\) dostatecznie bliskich zeru oba ilorazy są określone. Pierwszy dąży do \(1\) na mocy oszacowania wyprowadzonego z definicji logarytmu, a drugi dąży do \(-1\cdot1=-1\), ponieważ \(\sin x/x\to1\). Wniosek jest taki sam z obu stron:
\[
\lim_{x\to0^-}\ln f(x)=-1,
\qquad
\lim_{x\to0^+}\ln f(x)=-1.
\]
Z ciągłości funkcji wykładniczej otrzymujemy granice jednostronne samej funkcji:
\[
\boxed{\lim_{x\to0^-}(1-\sin x)^{1/x}=e^{-1}},
\qquad
\boxed{\lim_{x\to0^+}(1-\sin x)^{1/x}=e^{-1}}.
\]
Są one równe, więc granica obustronna istnieje i wynosi
\[
\boxed{\lim_{x\to0}(1-\sin x)^{1/x}=e^{-1}.}
\]

---

## Ćwiczenie 4.12

### 1. Wykazać, że \(\displaystyle\lim_{x\to0}(1+|x|)^{1/x}\) nie istnieje

Najpierw obliczymy granice jednostronne, korzystając z tego samego oszacowania logarytmu.

Dla \(x>0\) mamy \(|x|=x\). Zatem
\[
\ln\left((1+|x|)^{1/x}\right)=\frac{\ln(1+x)}x\longrightarrow1,
\]
bo jest to iloraz \(\ln(1+u)/u\) dla \(u=x\). W konsekwencji
\[
\lim_{x\to0^+}(1+|x|)^{1/x}=e.
\]
Dla \(x<0\) mamy \(|x|=-x\), więc
\[
\ln\left((1+|x|)^{1/x}\right)=\frac{\ln(1-x)}x
=-\frac{\ln(1+(-x))}{-x}\longrightarrow-1.
\]
Stąd
\[
\lim_{x\to0^-}(1+|x|)^{1/x}=e^{-1}.
\]
Granice jednostronne są różne (\(e\ne e^{-1}\)). Gdyby istniała granica obustronna, obie granice jednostronne musiałyby być równe tej samej liczbie. Otrzymana sprzeczność dowodzi, że
\[
\boxed{\lim_{x\to0}(1+|x|)^{1/x}\text{ nie istnieje}.}
\]

### 2. Wykazać, że \(\displaystyle\lim_{x\to-\infty}\sin 3x\) nie istnieje

Z definicji granicy w \(-\infty\), jeśli granica równałaby się \(L\), to dla każdego \(\varepsilon>0\) istniałoby \(A\), takie że dla wszystkich \(x<A\) zachodziłoby \(|\sin 3x-L|<\varepsilon\). Wybierzmy dwa ciągi:
\[
 x_n=-\frac\pi6-\frac{2\pi n}{3},
 \qquad
y_n=\frac\pi6-\frac{2\pi n}{3},\qquad n=1,2,\ldots
\]
Oba dążą do \(-\infty\), ale
\[
\sin(3x_n)=\sin\left(-\frac\pi2-2\pi n\right)=-1,
\qquad
\sin(3y_n)=\sin\left(\frac\pi2-2\pi n\right)=1.
\]
Gdyby granica \(L\) istniała, podstawienie każdego z tych ciągów do definicji granicy dawałoby jednocześnie \(-1=L\) i \(1=L\), co jest niemożliwe. Zatem
\[
\boxed{\lim_{x\to-\infty}\sin 3x\text{ nie istnieje}.}
\]
