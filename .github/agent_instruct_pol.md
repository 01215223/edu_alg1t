# Instrukcje dla agenta — zestawy zadań z algebry w Markdown o maksymalnej kompatybilności

| Pole | Wartość |
| :--- | :--- |
| Wersja dokumentu | 1.0 |
| Data audytu referencyjnego | 2026-10-11 |
| Repozytorium | `01215223/edu_alg1t` |
| Brief źródłowy | `.github/null.md` (tylko do odczytu) |
| Silnik matematyki GitHuba | MathJax 3 (LaTeX w Markdown) |
| Zakres instrukcji | sposób rozwiązywania zestawów + format plików `zestawN-odpowiedzi.md` |
| Status plików zadań | tylko do odczytu — nie edytuj bez wyraźnej zgody użytkownika |

> Wszystkie reguły oznaczone jako **zweryfikowane** zostały przetestowane narzędziem z sekcji 12
> (MathJax 3 z pakietem `AllPackages` oraz KaTeX w trybie `strict:'error'`) na 741 wyrażeniach
> matematycznych występujących w tym repozytorium, a zachowania składni Markdown — parserem
> CommonMark/GFM z rozszerzeniem math.

## Spis treści

1. [Misja i źródło wymagań](#1-misja-i-źródło-wymagań)
2. [Mapa repozytorium i stan prac](#2-mapa-repozytorium-i-stan-prac)
3. [Nazewnictwo plików i struktura](#3-nazewnictwo-plików-i-struktura)
4. [Procedura pracy krok po kroku](#4-procedura-pracy-krok-po-kroku)
5. [Wymagania merytoryczne wobec rozwiązań](#5-wymagania-merytoryczne-wobec-rozwiązań)
6. [Konwencje matematyczne repozytorium](#6-konwencje-matematyczne-repozytorium)
7. [Format Markdown — reguły kompatybilności](#7-format-markdown--reguły-kompatybilności)
8. [Lista kontrolna — Definition of Done](#8-lista-kontrolna--definition-of-done)
9. [Znane defekty istniejących plików](#9-znane-defekty-istniejących-plików)
10. [Git — branche, commity, PR](#10-git--branche-commity-pr)
11. [Załącznik A — kanoniczny szablon rozwiązania](#11-załącznik-a--kanoniczny-szablon-rozwiązania)
12. [Załącznik B — skrypt audytujący](#12-załącznik-b--skrypt-audytujący)
13. [English version](#13-english-version)

---

## 1. Misja i źródło wymagań

Brief `.github/null.md` zawiera 6 wymagań. Poniżej ich mapowanie na sekcje tego dokumentu.

| # | Wymaganie z briefu (dosłownie) | Realizacja |
| :---: | :--- | :--- |
| 1 | „to jest repozytorium zadań z algebry matematycznej w języku polskim” | §5.3, §6 |
| 2 | „wykonaj wszystkie zadania zapisane jako zestawy w osobnych plikach markdown” | §2, §4, §5 |
| 3 | „zapisz przebieg wykonania tych zadań i wyniki w osobnych plikach markdown” | §3, §5, §11 |
| 4 | „utrzymuj maksymalną kompatybilność markdown z Githubem” | §7 |
| 5 | „sprawdź czy markdown jest wyświetlany poprawnie” | §8, §12 |
| 6 | „utrzymuj ten sam styl formatowania markdown w repozytorium” | §6, §7, §11 |

Cel nadrzędny: plik rozwiązań ma być (a) poprawny merytorycznie i kompletny, (b) renderowany
identycznie dobrze na GitHubie, w VS Code, w Obsidianie i na GitLabie, (c) nieodróżnialny stylistycznie
od istniejących plików `zestaw0-odpowiedzi.md` i `zestaw1a-odpowiedzi.md`.

---

## 2. Mapa repozytorium i stan prac

| Plik | Rola | Linie | Stan na 2026-10-11 |
| :--- | :--- | :---: | :--- |
| `.github/null.md` | brief użytkownika | 6 | tylko do odczytu, brak H1 (zamierzone) |
| `zestaw0.md` | zadania: trygonometria, działania algebraiczne | 55 | **defekty formatu** (§9), CRLF |
| `zestaw0-odpowiedzi.md` | rozwiązania zestawu 0 | 183 | kompletny, czysty — **wzorzec stylu** |
| `zestaw1.md` | zadania: liczby zespolone | 39 | nadpisany przez `zestaw1a.md` |
| `zestaw1a.md` | zadania: liczby zespolone (korekta LaTeX) | 39 | wersja obowiązująca |
| `zestaw1a-odpowiedzi.md` | rozwiązania zestawu 1/1a | 386 | kompletny, **12 wzorów czerwonych na GitHubie** (§9) |
| `zestaw2.md` | zadania: potęgi, pierwiastki, równania w ℂ | 28 | **brak pliku odpowiedzi** |
| `zestaw2-odpowiedzi.md` | — | — | **DO UTWORZENIA — pierwszy task** |

Wnioski operacyjne:

* `zestaw1.md` i `zestaw1a.md` różnią się **dokładnie jedną linią** (35): w `1a` jest `$\arcsin$`,
  w `1` goły tekst `arcsin`. Traktuj `zestaw1a.md` jako obowiązujący; `zestaw1a-odpowiedzi.md`
  pokrywa oba pliki. **Nie twórz duplikatu** `zestaw1-odpowiedzi.md`, chyba że użytkownik o to poprosi.
* Repozytorium nie ma `README.md`, `.gitattributes`, `.gitignore` ani katalogu `tools/`.
  Rekomendacje są w §9 — **nie dodawaj ich bez zgody użytkownika**.
* Nie ma żadnego pliku z obrazami; zadania graficzne rozwiązuje się opisem i tabelami współrzędnych (§5.2).

---

## 3. Nazewnictwo plików i struktura

| Co | Konwencja | Przykład |
| :--- | :--- | :--- |
| Zestaw zadań | `zestawN.md` (tylko odczyt) | `zestaw2.md` |
| Rozwiązania | `zestawN-odpowiedzi.md`, katalog główny | `zestaw2-odpowiedzi.md` |
| Wariant zestawu | `zestawNa.md` → `zestawNa-odpowiedzi.md` | `zestaw1a-odpowiedzi.md` |
| Diagram (opcjonalnie) | `assets/zestawN-zadM.svg` | `assets/zestaw2-zad3.svg` |
| Narzędzia (za zgodą) | `tools/md-audit.js` | §12 |

Zasady twarde:

* Nazwy plików: małe litery, **wyłącznie ASCII**, bez spacji i polskich znaków, separator `-`.
* Nowe pliki zawsze w katalogu głównym repozytorium (płaska struktura, jak dotąd).
* Zakaz tworzenia: kopii plików zadań, plików `.pdf`/`.docx`, katalogów `build/`, `node_modules/`,
  plików tymczasowych (`*.tmp`, `draft.md`).
* Zakaz edycji: `.github/null.md`, `zestawN.md`, `zestawN-odpowiedzi.md` innych niż własny bieżący zestaw.

---

## 4. Procedura pracy krok po kroku

1. **Przeczytaj cały zestaw** i wypisz checklistę wszystkich punktów i podpunktów dokładnie
   w numeracji źródłowej (`1`, `1.1`, `5.2b`, `6.4`). Żaden podpunkt nie może zostać pominięty —
   także pytania opisowe wplecione w treść (np. „Jakie kąty skierowane odpowiadają tym wierzchołkom?”).
2. **Rozwiąż wszystko niezależnie od formatowania.** Zweryfikuj każdy wynik drugą metodą:
   podstawienie, sprawdzenie modułu i argumentu, niezależny rachunek symboliczny (np. `sympy`),
   test numeryczny. Dla liczb zespolonych: podnieś wynik do odpowiedniej potęgi / pomnóż z powrotem.
3. **Zapisz do `zestawN-odpowiedzi.md`** wg szablonu z §11, zachowując konwencje z §6 i format z §7.
4. **Uruchom audyt** z §12 na katalogu repozytorium. Oczekiwany rezultat: `0` problemów i kod wyjścia `0`.
   Jeśli skrypt wykrywa defekty w plikach, których nie edytujesz — odnotuj je w opisie PR (§9), nie naprawiaj.
5. **Sprawdź render** na GitHubie (widok pliku, nie podgląd surowego Markdown) + przejdź checklistę §8.
6. **Commit i PR** wg §10.

Reguły pracy:

* Jeden zestaw = jeden plik = jeden commit. Nie mieszaj nowych rozwiązań z poprawkami formatowania.
* Jeśli polecenie jest niejednoznaczne (np. przedział argumentu, konwencja `Arg` vs `arg`),
  **rozwiąż obie interpretacje** i jawnie napisz przyjęte założenie — tak jak `zestaw1a-odpowiedzi.md`.
* Jeśli treść zadania zawiera błąd (np. `zestaw0.md` podaje `sin(-π/2) = -√4/2` w tabeli),
  rozwiązuj zgodnie z matematyką i dodaj uwagę `> **Uwaga do treści:** …` na początku pliku.
* Nie zmyślaj wyników. Gdy czegoś nie da się policzyć dokładnie — napisz wprost, co jest przybliżeniem.

---

## 5. Wymagania merytoryczne wobec rozwiązań

* **Numeracja 1:1 z zestawem:** `## Zadanie 1`, `### 1.1`, `### 5.2b`. Nie scalaj i nie pomijaj podpunktów.
* **Pokazuj przebieg**, nie tylko wynik: każdy istotny krok jako osobny wzór blokowy. Brief wymaga
  „przebiegu wykonania” (pkt 3).
* **Wynik końcowy wyróżniony** ramką: `$$\boxed{...}$$` (styl `zestaw0-odpowiedzi.md`) albo
  pogrubiona etykieta `* **Wynik:** $...$`. W nowo tworzonych plikach stosuj `\boxed{}` konsekwentnie.
* **Dziedzina i wykluczenia** zawsze jawne (np. „dziedzina: $z \ne j$”), także gdy wynik jest „ładny”.
* **Wartości dokładne** (`\sqrt{2}`, `\frac{\pi}{4}`, `2\sqrt{2}`), nie przybliżenia dziesiętne.
  Przybliżenie tylko gdy polecenie każe użyć kalkulatora (np. `zestaw2.md` 1.5) — wtedy podaj
  wartość dokładną **i** przybliżoną z 4 miejscami po przecinku, oznaczoną `\approx`.
* **Pytania rozstrzygnięciowe** („Czy podane równości zachodzą…?”): zaczynaj od **TAK**/**NIE**,
  potem dowód albo kontrprzykład, potem warunek, kiedy równość jednak zachodzi.
* **Zadania graficzne:** agent nie rysuje — patrz §5.2.
* **Język:** polski, styl matematyczny bezosobowy („Mamy”, „Zatem”, „Stąd”, „Podstawiając”,
  „Dopełniając do kwadratu”), terminologia z §5.3. Bez kolokwializmów i bez pierwszej osoby liczby mnogiej
  w formie potocznej.
* **Długość:** tyle kroków, ile potrzeba; żadnego „lania wody”. Każdy wzór musi coś wnosić.

### 5.1 Wzorzec rozwiązania podpunktu

1. **Dane / założenia** — co wiemy, jaka konwencja.
2. **Przekształcenie** — sprowadzenie do postaci znanej (np. `z = x + jy`).
3. **Rachunek** — kroki jako osobne `$$`.
4. **Wynik** — w `\boxed{}`.
5. **Sprawdzenie / interpretacja** — podstawienie wstecz, sens geometryczny, przypadek brzegowy.

### 5.2 Playbooki typów zadań

| Typ zadania | Co musi się znaleźć w odpowiedzi |
| :--- | :--- |
| Obliczeniowe (działania na ℂ) | każdy krok algebraiczny, postać `a + jb`, wynik w ramce |
| „Czy równość zachodzi?” | **TAK/NIE**, dowód ogólny albo kontrprzykład liczbowy, warunek równości |
| Zbiory na płaszczyźnie (zadania graficzne) | przekształcenie do `x, y`; nazwa figury; środek/promień/półosie/ogniska; **które brzegi należą do zbioru** (linia ciągła vs przerywana); tabela punktów kontrolnych; opcjonalnie szkic ASCII w bloku kodu |
| Równania w ℂ | pełny zbiór rozwiązań (wszystkie pierwiastki), postać algebraiczna i trygonometryczna, opis szkicu zbioru rozwiązań |
| Potęgi i pierwiastki | moduł i argument wyjściowy, wzór Moivre'a, wszystkie `n` pierwiastków, wartości na okręgu |
| Działania algebraiczne | przemienna tak/nie + kontrprzykład, łączność tak/nie + kontrprzykład, element neutralny (dwustronny!) albo dowód braku, dodatkowo: element odwrotny, pochłaniający, idempotentność, struktura (grupa/ciało) |
| Wielo-kąty foremne | promień `R`, kąt początkowy, lista kątów `\alpha_0 + \frac{2\pi k}{n}`, lista współrzędnych wierzchołków |

Zadania graficzne — format obowiązkowy (tak robi `zestaw0-odpowiedzi.md`):

* tabela współrzędnych z kolumnami: kąt/punkt, współrzędne, dodatkowe przecięcia;
* opis słowny figury i jej parametrów;
* jawne wskazanie brzegów należących i nienależących do zbioru;
* opcjonalnie szkic ASCII w ogrodzonym bloku kodu (```text), bo tylko blok kodu gwarantuje
  stałą szerokość znaku.

### 5.3 Słownik terminologii (polski ↔ notacja)

| Termin PL | Notacja / wzór | Uwaga |
| :--- | :--- | :--- |
| moduł | `\lvert z\rvert` | w tabelach zawsze `\lvert \rvert`, nie `\|` |
| argument główny | `\arg(z)`, `\operatorname{Arg}(z)` | zawsze podaj przedział |
| sprzężenie | `\overline{z}` | repo używa też `\bar{z}` — w nowych plikach `\overline{z}` |
| część rzeczywista / urojona | `\text{Re}(z)`, `\text{Im } z` | `\text{Im }` ze spacją wewnątrz `\text{}` |
| postać algebraiczna / trygonometryczna | `a + jb` / `r(\cos\varphi + j\sin\varphi)` | jednostka urojona `j` |
| wzór Moivre'a | `(\cos\varphi + j\sin\varphi)^n` | „Moivre'a”, nie „de Moivre'a” |
| pierścień kołowy | `r_1 \le \lvert z - z_0\rvert < r_2` | brzegi: ciągła/przerywana |
| wycinek kątowy | `\alpha \le \arg(z - z_0) < \beta` | bez wierzchołka, gdy `z_0` wykluczone |
| półpłaszczyzna | `ax + by + c \le 0` | podaj równanie brzegu |
| okrąg Apoloniusza | `\lvert z - A\rvert = k\lvert z - B\rvert` | `k \ne 1` |
| elipsa / ogniska / półosie | `\frac{x^2}{b^2} + \frac{y^2}{a^2} = 1` | warunek `2a > 2c`, inaczej odcinek |
| ćwiartka układu | I–IV | podawaj znaki `x, y` |
| działanie łączne / przemienne | `(a*b)*c = a*(b*c)` / `a*b = b*a` | kontrprzykład liczbowy obowiązkowy przy „nie” |
| element neutralny / odwrotny / pochłaniający | `e*a = a*e = a` | neutralny musi być **dwustronny** |
| grupa abelowa / ciało | — | jako własność dodatkowa |

---

## 6. Konwencje matematyczne repozytorium

| Zagadnienie | Obowiązuje | Zakazane / ryzykowne |
| :--- | :--- | :--- |
| Jednostka urojona | `j` (jak w `zestaw1.md`, `zestaw1a.md`, `zestaw2.md`) | `i`, `\imath`, `\mathrm{i}` |
| Część rzeczywista/urojona | `\text{Re}(z)`, `\text{Im } z` | `Re z` bez `\text{}`, `Im` jako tekst |
| Sprzężenie | `\overline{z}` | `\conj{z}` (nie istnieje) |
| Zbiory liczbowe | `\mathbb{R}`, `\mathbb{C}`, `\mathbb{Z}`, `\mathbb{N}` | `\RR`, `\CC` (**zweryfikowane: czerwone na GitHubie**) |
| Arcus tangens | `\operatorname{arctg}` lub `\arctan` | `\arctg`, `\arcctg`, `\tg`, `\ctg` (**zweryfikowane: czerwone na GitHubie**) |
| Argument | jawna konwencja `(-\pi,\pi]` lub `[0,2\pi)`, obie gdy nieustalone | wynik bez konwencji |
| Kąty | radiany `\frac{5\pi}{6}` | stopnie, chyba że zadanie używa stopni |
| Zbiory w nawiasach | `\{x, y\}`, `\left\{ \right\}` | `{x, y}` bez `\` |
| Odstępy | `\quad` między warunkami, `\,` przy skalarze, `\ ` w `\text{Im } z` | wiele `$$` w jednej linii |
| Nawiasy skalowane | `\left( \right)`, `\left\lvert \right\rvert` | ręczne `(` przy `\frac` |
| Wynik końcowy | `\boxed{}` | samo pogrubienie bez wzoru |
| Układy równań i wieloliniowe przekształcenia | `aligned`, `cases`, `array` wewnątrz `$$` | `align`, `equation`, `gather`, `\tag`, `\label` |
| Macierze | `pmatrix`, `bmatrix`, `vmatrix` | `tabular`, `\hline` poza `array` |
| Symbole wewnątrz wzorów | makra LaTeX (`\le`, `\in`, `\emptyset`, `\times`, `\to`, `\infty`, `\pm`) | surowe Unicode (`≤`, `∈`, `∅`, `×`, `→`, `∞`, `−`) |

### 6.1 Tabela zgodności makr — zweryfikowana

Legenda: OK = renderuje poprawnie, RED = MathJax renderuje czerwony tekst „undefined”,
FAIL = błąd parsera.

| Wyrażenie | GitHub (MathJax) | KaTeX (VS Code / Obsidian / GitLab) | Werdykt |
| :--- | :---: | :---: | :--- |
| `\operatorname{arctg}(2)` | OK | OK | **używaj** dla polskiej notacji |
| `\arctan(2)`, `\arcsin(2)`, `\cot x` | OK | OK | używaj dla notacji ANSI |
| `\arctg(2)` | **RED** | OK | **zakazane** — 12 takich wzorów jest dziś w `zestaw1a-odpowiedzi.md` |
| `\tg x`, `\ctg x`, `\arcctg x` | **RED** | OK | **zakazane** → `\tan`, `\cot`, `\operatorname{arcctg}` |
| `\RR`, `\CC`, `\eps`, `\foobar` | **RED** | FAIL | **zakazane** → `\mathbb{R}`, `\varepsilon` |
| `\degree` | OK | OK | dopuszczalne, preferuj `^\circ` |
| `\emptyset` | OK | OK | używaj; surowe `∅` → **FAIL** w KaTeX strict |
| `\begin{aligned} … \end{aligned}` | OK | OK | **używaj** |
| `\begin{align} … \end{align}` | OK | tylko w trybie display | unikaj |
| `\tag{1}` | OK | tylko w display | **nie używaj** |
| `\begin{tabular}` | FAIL | FAIL | **zakazane** → `\begin{array}` |
| `\boxed{…}` | OK | OK | używaj na wynik |
| `\implies`, `\iff` | OK | OK | używaj |
| `\lvert z\rvert`, `\left\lvert z\right\rvert` | OK | OK | **obowiązkowe w tabelach** |
| `\overline{z}`, `\bar{z}` | OK | OK | standaryzuj na `\overline{z}` |
| `\text{Re}(z)`, `\text{Im } z`, `\Re z`, `\Im z` | OK | OK | używaj konsekwentnie |
| `\text{ąęśćżźńół}` | OK | OK | polskie znaki w `\text{}` są bezpieczne |
| `\mathbb{R}\times\mathbb{R}`, `\sqrt[3]{ab}`, `\substack`, `\vec{AB}` | OK | OK | bezpieczne |
| `\begin{array}{\|c\|c\|}\hline … \end{array}` | OK | OK | bezpieczne (w bloku `$$`) |

Wzory sprawdzone w repozytorium: 741 wyrażeń, z czego 12 renderuje się na czerwono na GitHubie
(wszystkie przez `\arctg`). Pełna lista w §9.

---

## 7. Format Markdown — reguły kompatybilności

### 7.1 Plik i znaki

* Kodowanie **UTF-8 bez BOM**, końce linii **LF** (`\n`), plik kończy się znakiem nowej linii.
* **Bez znaków TAB** — wyłącznie spacje. Bez spacji na końcu linii. Bez spacji nierozdzielających
  (U+00A0, U+2007, U+202F).
* Polskie znaki diakrytyczne w tekście — tak. W matematyce — wyłącznie makra LaTeX (§6).
* Symbole typograficzne dozwolone w prozie: `–`, `—`, `„ ”`, `→`, `✓`. W matematyce — żadnego z nich.
* Preferuj jedną myśl na linię; długie akapity dziel pustą linią, nie twardym przełamaniem.

### 7.2 Nagłówki

* **Dokładnie jeden H1** na plik, w pierwszej linii (GitHub używa go jako tytułu strony).
* Wyłącznie nagłówki ATX (`##`), nigdy setext (`===` / `---` pod tekstem).
* **Bez skoków poziomów:** H1 → H2 → H3. Nie zaczynaj od `####` (błąd `zestaw0.md`).
* Pusta linia przed i po każdym nagłówku.
* Wzorzec hierarchii dla pliku rozwiązań: `# tytuł` → `## Zadanie N` → `### N.M`.
* Nie używaj nagłówków jako „pogrubionego tekstu” ani do numerowania treści, która nie jest sekcją.
* Matematyka w nagłówku jest dopuszczalna (repo tak robi), ale **nie linkuj do takich nagłówków**:
  kotwice GitHuba dla nagłówków z `$…$` są nieprzewidywalne.

### 7.3 Akapity, listy, separatory

* Pusta linia przed i po: nagłówku, liście, tabeli, bloku `$$`, separatorze `---`, bloku kodu.
* **Jeden znacznik listy na linię, na początku linii.** Nigdy `tekst:* punkt pierwszy* punkt drugi` —
  **zweryfikowane:** parser zwraca wtedy jeden akapit z gwiazdkami, a nie listę (błąd w `zestaw0.md` L8 i L36).
* Znaczniki: `*` dla list nieuporządkowanych (konwencja repo), `1.` dla uporządkowanych.
* Wcięcie zagnieżdżenia = szerokość znacznika rodzica: **2 spacje** pod `* `, **3 spacje** pod `1. `.
  **Zweryfikowane:** blok `$$` wcięty o 4+ spacje względem kolumny treści rodzica zamienia się w blok kodu.
* Separator `---` **tylko z pustymi liniami z obu stron**. **Zweryfikowane:** `---` bezpośrednio pod
  tekstem tworzy nagłówek setext H2 (błąd w `zestaw0.md` L29 — ostatnie zdanie zadania 3 stało się nagłówkiem).
* Podpunkty zadań: `* **1.1** treść` (styl `zestaw1.md` i obu plików odpowiedzi).
* Twarde przełamanie linii: unikaj. Jeśli jest konieczne — użyj `\` na końcu linii (GitHub to wspiera),
  nie dwóch spacji (błąd: 10 wystąpień w `zestaw0.md`).
* Cytat na początku pliku (`>`) stosuj na założenia i uwagi do treści — jak w `zestaw0-odpowiedzi.md`.

### 7.4 Tabele

* Wyłącznie tabele GFM: wiersz nagłówka, wiersz wyrównania (`| :--- |`, `| :---: |`, `| ---: |`), wiersze danych.
* Pusta linia przed tabelą i po niej.
* W komórkach **tylko matematyka inline** `$…$`. **Zweryfikowane:** `$$…$$` w komórce degraduje się
  do matematyki inline i psuje rytm tabeli.
* **Zweryfikowane:** surowy znak `|` wewnątrz wzoru rozbija komórkę (`$\lvert z\rvert$` jest bezpieczne,
  `$|z|$` nie). W tabelach zawsze `\lvert … \rvert`, `\vert`, `\mid`.
* Łamanie linii w komórce: `<br>`. Nie próbuj wstawiać list ani bloków do komórek.
* Maksymalnie 5–6 kolumn (czytelność na mobile), komórki krótkie.
* Literalna kreska pionowa w tekście komórki: `\|`.

### 7.5 Matematyka

* **Inline:** `$x+1$` — dolary muszą przylegać do wzoru, bez spacji przy delimiterach.
  GitHub może nie rozpoznać wzoru przy `$ x $`, a `$` przed cyfrą bywa czytany jako waluta
  (`$5`). **Zweryfikowane:** `$ 5 i $ 10` zamienia się w wyrażenie matematyczne.
* **Wariant GitHub-only:** `` $`x_1 * y`$ `` gdy wzór zawiera znaki kolizyjne z Markdown
  (`_`, `*`, `|`, `` ` ``). **Uwaga:** nie działa w KaTeX — używaj tylko w ostateczności.
* **Blok:** `$$` na osobnych liniach, puste linie wokół, treść między nimi:

  $$
  \lvert z_1 + z_2\rvert \le \lvert z_1\rvert + \lvert z_2\rvert
  $$

* Wewnątrz elementu listy blok `$$` wcinaj do kolumny treści (2 spacje dla `* `, 3 dla `1. `)
  i oddzielaj pustymi liniami — wtedy pozostaje częścią tego samego punktu listy.
* **Wariant GitHub-only:** blok ogrodzony trzema backtickami z językiem `math` (bez `$$`).
  Na GitHubie renderuje się poprawnie, ale VS Code / Obsidian / GitLab pokażą zwykły blok kodu.
  **Domyślnie używaj `$$`.**
* **Zakazane delimitery:** `\( … \)` i `\[ … \]` — GitHub ich nie wspiera.
* **Literalny dolar:** `\$` wewnątrz wzoru, `<span>$</span>` poza wzorem (dokumentacja GitHuba).
* **Zakaz definicji makr:** `\newcommand`, `\renewcommand`, `\def`, `\require{}` — każdy blok `$$`
  jest kompilowany niezależnie, makra nie przetrwają do następnego wzoru.
* **Łamanie linii we wzorach:** `\\` wyłącznie wewnątrz `aligned` / `cases` / `array` / macierzy.
  **Zweryfikowane:** gołe `\\` na poziomie głównym bloku daje ostrzeżenie w KaTeX
  („in LaTeX, `\\` does nothing in display mode”).
* Kilka wyrażeń obok siebie: jedno `$$` z `\quad`, nie wiele `$$` w jednej linii
  (błąd `zestaw2.md`: 12 linii, gdzie `$$` dzieli linię z tekstem punktu — **zweryfikowane:**
  taki wzór renderuje się jako inline, nie jako blok).

### 7.6 HTML, linki, obrazy

* HTML — tylko minimalnie i tylko z listy: `<br>`, `<sub>`, `<sup>`, `<span>`, `<details>`,
  `<summary>`, `<div align="center">`, `<img src="assets/…" width="…">`, `<kbd>`.
  GitHub sanityzuje HTML (`<script>`, `<style>`, `<iframe>`, atrybuty zdarzeń są wycinane),
  a inne renderery mogą wyciąć całość — dlatego HTML używaj tylko tam, gdzie Markdown nie wystarczy.
* Linki wyłącznie **względne**: `[zestaw 2](zestaw2.md)`, `[brief](null.md)` (z pliku w `.github/`).
* Obrazy: `![opis alternatywny](assets/zestaw2-zad3.svg)` — alt obowiązkowy, SVG preferowany,
  rozmiar przez `<img … width="480">`.
* Kotwice wewnętrzne tylko do nagłówków bez matematyki (§7.2).
* Dla zadań „zaznacz na płaszczyźnie”: tabela współrzędnych jest obowiązkowa, obrazek opcjonalny.

---

## 8. Lista kontrolna — Definition of Done

Plik `zestawN-odpowiedzi.md` jest gotowy, gdy wszystkie punkty są spełnione:

- [ ] Odpowiedziano na **każdy** punkt i podpunkt zestawu, w numeracji źródłowej.
- [ ] Każdy wynik jest zweryfikowany drugą metodą (podstawienie / rachunek niezależny).
- [ ] Wyniki końcowe wyróżnione `\boxed{}` lub etykietą **Wynik**/**Odpowiedź**.
- [ ] Podane dziedziny, założenia i wykluczenia (np. `z \ne j`), a przy pytaniach rozstrzygnięciowych **TAK/NIE** + uzasadnienie.
- [ ] Zadania graficzne mają współrzędne, opis figury i status brzegów (ciągła/przerywana).
- [ ] Jednostka urojona `j`; brak `\arctg`, `\tg`, `\ctg`, `\arcctg`, `\RR`, `\CC` w jakimkolwiek wzorze.
- [ ] Brak delimiterów `\( \)` / `\[ \]`; brak `\newcommand` / `\require`; brak `\tag` / `\label` / `align` / `tabular`.
- [ ] Wszystkie `$$` na osobnych liniach, z pustymi liniami wokół, z wcięciem zgodnym z listą.
- [ ] W tabelach brak `$$` i brak surowego `|` we wzorach (użyte `\lvert \rvert`).
- [ ] Dokładnie jeden H1, brak skoków poziomów nagłówków, puste linie wokół bloków.
- [ ] Każdy `---` ma puste linie z obu stron; żaden znacznik listy nie jest wklejony w akapit.
- [ ] Plik: UTF-8 bez BOM, LF, bez TAB-ów, bez spacji na końcu linii, z końcową nową linią.
- [ ] Skrypt audytujący (§12) zwraca `0` problemów i kod wyjścia `0` dla tego pliku.
- [ ] Podgląd na GitHubie sprawdzony wizualnie: nagłówki, tabele, wzory, listy, separatory.
- [ ] Styl nieodróżnialny od `zestaw0-odpowiedzi.md` / `zestaw1a-odpowiedzi.md`.

---

## 9. Znane defekty istniejących plików

Stan z audytu 2026-10-11 (narzędzie z §12). **Pliki zadań są tylko do odczytu** — defekty
zgłaszaj w opisie PR, nie naprawiaj bez zgody użytkownika.

| Plik | Problemy | Szczegóły |
| :--- | :---: | :--- |
| `zestaw1a-odpowiedzi.md` | 12 | L332–L386 (12 wystąpień `\arctg`) — **na GitHubie renderuje się jako czerwony tekst „undefined”**; zamiennik: `\operatorname{arctg}` |
| `zestaw0.md` | 15 | CRLF w 55/56 linii; L2 skok nagłówka H1→H4; L8 i L36 znaczniki listy wklejone w akapit (treść ginie jako lista); L29 `---` bez pustej linii → zdanie staje się nagłówkiem H2; 10 twardych przełamań linii (spacje na końcu) |
| `zestaw2.md` | 12 | L4–L9, L17–L22: `$$…$$` w jednej linii z tekstem punktu → wzory renderują się inline zamiast blokowo |
| `.github/null.md` | 1 | brak H1 — zamierzone (to brief w formie listy), nie naprawiać |
| `zestaw0-odpowiedzi.md`, `zestaw1.md`, `zestaw1a.md` | 0 | czyste |

Uwaga o `zestaw1.md` L35: `arcsin` i `arctg` są tam gołym tekstem poza matematyką — w `zestaw1a.md`
poprawiono tylko `\arcsin`. W odpowiedziach zapisuj obie funkcje jako wzory: `$\arcsin$`,
`$\operatorname{arctg}$`.

Rekomendacje (do wdrożenia wyłącznie za zgodą użytkownika):

* `.gitattributes` z `* text=auto eol=lf` i `*.md text eol=lf` — eliminuje problem CRLF z `zestaw0.md`.
* `README.md` z indeksem zestawów i linkami do plików odpowiedzi.
* `tools/md-audit.js` (skrypt z §12) + `.gitignore` z `node_modules/`.
* Jednorazowa naprawa formatu `zestaw0.md` i `zestaw2.md` w osobnym, opisowym commicie.
* Wymiana `\arctg` → `\operatorname{arctg}` w `zestaw1a-odpowiedzi.md`.

---

## 10. Git — branche, commity, PR

* Praca na branchu sesji; nigdy na `main`. Przed zmianami: `git status`, `git diff`.
* Commit message: tryb rozkazujący, po polsku, zwięzły — `Dodaj rozwiązania zestawu 2`,
  `Popraw renderowanie wzorów w zestawie 1a`. Bez kropek na końcu, bez emoji.
* Jeden zestaw = jeden commit. Poprawki formatu istniejących plików — osobny commit.
* Nie commituj: `node_modules/`, plików tymczasowych, wygenerowanego HTML/PDF, dużych plików binarnych.
* W opisie PR zamieść: listę utworzonych/zmienionych plików, checklistę §8, wynik audytu §12
  (liczba wyrażeń i liczba problemów) oraz odnotowane defekty plików, których nie edytowano (§9).
* Nie używaj `--force` na branchu współdzielonym; nie scalaj PR bez zgody użytkownika.

---

## 11. Załącznik A — kanoniczny szablon rozwiązania

Skopiuj strukturę i uzupełnij treścią. Zwróć uwagę na puste linie, wcięcia `$$` w listach (2 spacje)
oraz na `\lvert \rvert` w tabelach.

````markdown
# Algebra – Zestaw N – rozwiązania

> **Założenia i konwencje.** Jednostka urojona: $j$. Argument główny: $\arg(z) \in (-\pi, \pi]$
> (wartości w $[0, 2\pi)$ podane dodatkowo). Wartości dokładne; przybliżenia tylko tam,
> gdzie polecenie wymaga kalkulatora.
>
> **Uwaga do treści zadania N.M:** … (tylko jeśli treść zawiera błąd lub niejednoznaczność).

---

## Zadanie 1

Krótkie przywołanie, czego dotyczy zadanie (jedno zdanie, opcjonalnie).

### 1.1

* **Dane:** $z_1 = 3 + 2j$, $z_2 = 2 - 5j$
* **Krok 1 — kwadrat $z_1$:**

  $$z_1^2 = (3 + 2j)^2 = 9 + 12j + (2j)^2 = 5 + 12j$$

* **Krok 2 — iloczyn $jz_2$:**

  $$jz_2 = j(2 - 5j) = 2j - 5j^2 = 5 + 2j$$

* **Wynik:**

  $$\boxed{z_1^2 + jz_2 = 10 + 14j}$$

* **Sprawdzenie:** $\text{Re} = 10$, $\text{Im} = 14$; moduł $\lvert 10 + 14j\rvert = \sqrt{296} = 2\sqrt{74}$.

---

## Zadanie 2 — czy równości zachodzą dla dowolnych $z, z_1, z_2 \in \mathbb{C}$?

### 2.1

* **Odpowiedź:** **TAK**
* **Uzasadnienie:** niech $z_1 = x_1 + jy_1$, $z_2 = x_2 + jy_2$, gdzie $x_k, y_k \in \mathbb{R}$. Wtedy

  $$z_1 + z_2 = (x_1 + x_2) + j(y_1 + y_2) \implies \text{Im}(z_1 + z_2) = y_1 + y_2 = \text{Im } z_1 + \text{Im } z_2$$

### 2.2

* **Odpowiedź:** **NIE**
* **Kontrprzykład:** $z_1 = z_2 = j$

  $$\text{Re } z_1 \cdot \text{Re } z_2 = 0 \ne -1 = \text{Re}(j^2) = \text{Re}(z_1 z_2)$$

* **Warunek równości:** $\text{Re}(z_1 z_2) = \text{Re } z_1 \cdot \text{Re } z_2 - \text{Im } z_1 \cdot \text{Im } z_2$,
  więc równość zachodzi wtedy i tylko wtedy, gdy $\text{Im } z_1 \cdot \text{Im } z_2 = 0$.

---

## Zadanie 5 — zbiory na płaszczyźnie zespolonej

### 5.1a

* **Przekształcenie:** niech $z = x + jy$; warunek przyjmuje postać

  $$1 \le \lvert z\rvert < 3 \iff 1 \le \sqrt{x^2 + y^2} < 3 \iff 1 \le x^2 + y^2 < 9$$

* **Opis geometryczny:** pierścień kołowy o środku $z_0 = 0$, promień wewnętrzny $r_1 = 1$,
  promień zewnętrzny $r_2 = 3$.
* **Brzegi:** okrąg $x^2 + y^2 = 1$ **należy** do zbioru (linia ciągła); okrąg $x^2 + y^2 = 9$
  **nie należy** (linia przerywana).

| Punkt kontrolny | Współrzędne | $\lvert z\rvert$ | Należy do zbioru |
| :--- | :---: | :---: | :---: |
| $A$ | $(1, 0)$ | $1$ | tak (brzeg) |
| $B$ | $(2, 0)$ | $2$ | tak |
| $C$ | $(3, 0)$ | $3$ | nie (brzeg) |

```text
        y
        ^            . . . .
        |        . ´         ` .
        |      /   -------       \      r2 = 3  (przerywana)
        |     |    |     |    |
 ------ O ----|----|-----|----|---> x
        |     |    |     |    |
        |      \   -------   /         r1 = 1  (ciągła)
        |        ` .       . '
```

---

## Podsumowanie wyników

| Podpunkt | Wynik |
| :--- | :--- |
| 1.1 | $10 + 14j$ oraz $\text{Re}(z_1 z_2) = 16$ |
| 2.1 | TAK |
| 2.2 | NIE — kontrprzykład $z_1 = z_2 = j$ |
| 5.1a | pierścień $1 \le \lvert z\rvert < 3$, brzeg wewnętrzny należy |
````

---

## 12. Załącznik B — skrypt audytujący

Skrypt sprawdza pliki `.md` pod kątem wszystkich reguł z §7 i §6. **Nie ma go w repozytorium**
(decyzja użytkownika: w tym kroku powstają tylko instrukcje). Zapisz go jako `tools/md-audit.js`
i uruchom, jeśli użytkownik zgodzi się na dodanie narzędzi.

Użycie:

```bash
npm i --no-save mathjax-full katex   # jednorazowo, poza repo lub w tools/
node tools/md-audit.js .             # kod wyjścia 0 = brak problemów
```

Co jest sprawdzane:

* plik: BOM, CRLF, brak końcowej nowej linii, spacje nierozdzielające;
* matematyka: czerwony tekst w MathJax (GitHub), błędy KaTeX strict, zakazane makra,
  spacje przy `$`, `$` przed cyfrą, delimitery `\( \)` / `\[ \]`, `\newcommand` / `\require`;
* struktura: liczba H1, skoki poziomów nagłówków, pułapka setext `---`, znaczniki listy wklejone
  w akapit, `$$` współdzielące linię z tekstem, TAB-y, spacje na końcu linii, `|` we wzorach w tabelach;
* fragmenty w blokach kodu i w `` `kodzie inline` `` są wygaszane, więc przykłady w dokumentacji
  nie generują fałszywych alarmów.

````javascript
#!/usr/bin/env node
/* tools/md-audit.js — audyt zgodnosci Markdown + matematyki (MathJax/GitHub oraz KaTeX).
   Uzycie:  node tools/md-audit.js [katalog]      (kod wyjscia 0 = brak problemow)
   Zaleznosci: npm i --no-save mathjax-full katex                                    */
const fs = require('fs');
const path = require('path');
const katex = require('katex');
const { mathjax } = require('mathjax-full/js/mathjax.js');
const { TeX } = require('mathjax-full/js/input/tex.js');
const { SVG } = require('mathjax-full/js/output/svg.js');
const { liteAdaptor } = require('mathjax-full/js/adaptors/liteAdaptor.js');
const { RegisterHTMLHandler } = require('mathjax-full/js/handlers/html.js');
const { AllPackages } = require('mathjax-full/js/input/tex/AllPackages.js');

const adaptor = liteAdaptor();
RegisterHTMLHandler(adaptor);
const texJax = new TeX({ packages: AllPackages });
const mjDoc = mathjax.document('', { InputJax: texJax, OutputJax: new SVG({ fontCache: 'none' }) });

const FENCE = /^(\s*)(`{3,}|~{3,})(.*)$/;

/* Wygasza wszystko, co nie jest matematyka: ploty kodu (oprocz math) i kod inline.
   Dzieki temu audyt nie raportuje falszywych problemow dla przykladow w dokumentacji. */
function maskCode(src) {
  let open = null;
  return src.split('\n').map(line => {
    const m = FENCE.exec(line);
    if (m) {
      const len = m[2].length, ch = m[2][0], info = m[3].trim();
      if (!open) { open = { len, ch, math: info === 'math' }; return open.math ? line : ' '.repeat(line.length); }
      if (ch === open.ch && len >= open.len && info === '') { const was = open.math; open = null; return was ? line : ' '.repeat(line.length); }
      return open.math ? line : ' '.repeat(line.length);
    }
    if (open) return open.math ? line : line.replace(/[^\n]/g, ' ');
    return line.replace(/`[^`\n]*`/g, s => ' '.repeat(s.length));
  }).join('\n');
}

function mathSpans(src) {
  const out = [];
  let m;
  const base = maskCode(src);
  const fenceRe = new RegExp('`{3,}math\\r?\\n([\\s\\S]*?)`{3,}', 'g');
  while ((m = fenceRe.exec(base))) out.push({ k: 'math-fence', t: m[1], i: m.index, d: true });
  const noFenceMath = base.replace(fenceRe, s => s.replace(/[^\n]/g, ' '));
  const dispRe = /\$\$([\s\S]+?)\$\$/g;
  const ranges = [];
  while ((m = dispRe.exec(noFenceMath))) { ranges.push([m.index, m.index + m[0].length]); out.push({ k: '$$', t: m[1], i: m.index, d: true }); }
  let masked = '', p = 0;
  for (const [a, b] of ranges) { masked += noFenceMath.slice(p, a) + ' '.repeat(b - a); p = b; }
  masked += noFenceMath.slice(p);
  const inlRe = /\$([^$\n]+)\$/g;
  while ((m = inlRe.exec(masked))) out.push({ k: '$', t: m[1], i: m.index, d: false, raw: m[0] });
  return out;
}

const mjRed = (t, d) => {
  try {
    const s = adaptor.innerHTML(mjDoc.convert(t, { display: !!d }));
    return /fill="red"|stroke="red"|color:red/i.test(s);
  } catch { return true; }
};
const ktFail = (t, d) => {
  try {
    katex.renderToString(t, { throwOnError: true, strict: 'error', displayMode: !!d });
    return null;
  } catch (e) { return String(e.message || e).replace('KaTeX parse error: ', '').slice(0, 100); }
};

/* Makra, ktore GitHub (MathJax) renderuje jako czerwony tekst "undefined" */
const FORBIDDEN = ['\\arctg', '\\arcctg', '\\tg', '\\ctg', '\\cosec', '\\ch', '\\sh', '\\degree',
                   '\\RR', '\\NN', '\\ZZ', '\\QQ', '\\CC', '\\eps'];
const FORBIDDEN_RE = FORBIDDEN.map(x => new RegExp(x.replace(/\\/g, '\\\\') + '(?![a-zA-Z])'));

const root = process.argv[2] || '.';
const walk = d => fs.readdirSync(d, { withFileTypes: true }).flatMap(e =>
  (e.name === '.git' || e.name === 'node_modules') ? []
    : e.isDirectory() ? walk(path.join(d, e.name))
    : e.name.endsWith('.md') ? [path.join(d, e.name)] : []);

let nMath = 0, problems = 0;
for (const f of walk(root)) {
  const src = fs.readFileSync(f, 'utf8');
  const plain = maskCode(src);
  const L = src.split(/\r?\n/);
  const LP = plain.split(/\r?\n/);
  const issues = [];
  const lineOf = idx => src.slice(0, idx).split(/\r?\n/).length;

  /* --- A. plik i znaki --- */
  const crlf = (src.match(/\r\n/g) || []).length;
  if (crlf) issues.push(`CRLF: ${crlf}/${L.length} linii (oczekiwano LF)`);
  if (src.charCodeAt(0) === 0xFEFF) issues.push('BOM UTF-8 na poczatku pliku');
  if (src.length && !src.endsWith('\n')) issues.push('brak koncowego znaku nowej linii');
  if (/[\u00A0\u2007\u202F]/.test(src)) issues.push('twarda/waska spacja (U+00A0 / U+2007 / U+202F)');

  /* --- B. matematyka --- */
  for (const s of mathSpans(src)) {
    nMath++;
    const ln = lineOf(s.i);
    const bad = FORBIDDEN.filter((_, k) => FORBIDDEN_RE[k].test(s.t));
    if (bad.length) issues.push(`L${ln}: zakazane makro ${bad.join(', ')} (GitHub/MathJax: czerwony tekst)`);
    else if (mjRed(s.t, s.d)) issues.push(`L${ln}: MathJax/GitHub renderuje na CZERWONO: ${s.t.trim().slice(0, 60)}`);
    const kf = ktFail(s.t, s.d);
    if (kf) issues.push(`L${ln}: KaTeX (VS Code/Obsidian/GitLab): ${kf} :: ${s.t.trim().slice(0, 50)}`);
    if (s.k === '$' && (/^\s/.test(s.t) || /\s$/.test(s.t))) issues.push(`L${ln}: spacja przy delimiterze '$' — GitHub moze nie rozpoznac wzoru`);
    if (s.k === '$' && /^[0-9]/.test(src.slice(s.i + s.raw.length))) issues.push(`L${ln}: '$' tuz przed cyfra — ryzyko interpretacji jako waluta`);
  }
  if (/\\\[[\s\S]*?\\\]|\\\(/.test(plain)) issues.push('delimitery \\[ \\] lub \\( \\) — GitHub ich nie wspiera (uzyj $ oraz $$)');
  if (/\\newcommand|\\renewcommand|\\require\{/.test(plain)) issues.push('\\newcommand / \\renewcommand / \\require — makra nie dzialaja miedzy wzorami');

  /* --- C. struktura Markdown --- */
  let h1 = 0, lastLvl = 0;
  L.forEach((raw, i) => {
    const line = LP[i] ?? '', prev = LP[i - 1] ?? '';
    const n = i + 1;
    const h = /^(#{1,6})\s/.exec(raw);
    if (h) {
      const lvl = h[1].length;
      if (lvl === 1) h1++;
      if (lastLvl && lvl > lastLvl + 1) issues.push(`L${n}: skok poziomu naglowka H${lastLvl} -> H${lvl}`);
      lastLvl = lvl;
    }
    if (!line.trim()) return;
    if (/^(-{3,}|_{3,})\s*$/.test(line) && prev.trim() !== '' && !/^#{1,6}\s/.test(prev) && !/^\s*\|/.test(prev))
      issues.push(`L${n}: '---' bez pustej linii powyzej = naglowek setext H2, nie <hr>`);
    const glued = [...line.matchAll(/[^\s*\\]\* (?=\S)/g)].filter(x => x.index > 0);
    if (glued.length && !/^\s*([-*+]|\d+\.)\s/.test(line)) issues.push(`L${n}: ${glued.length} znacznik(ow) listy wklejony w tekst akapitu`);
    const t = line.trim();
    if (t.includes('$$') && !/^\$\$$/.test(t) && !/^\$\$[^$]*\$\$$/.test(t)) issues.push(`L${n}: '$$' w jednej linii z tekstem — wzor nie bedzie blokowy`);
    if (/^\t/.test(raw)) issues.push(`L${n}: wciecie znakiem TAB (uzyj spacji)`);
    if (/[^\s] {2,}$/.test(raw)) issues.push(`L${n}: twarde przełamanie linii (spacje na koncu)`);
    if (/^\s*\|/.test(line)) for (const s of mathSpans(line)) if (s.k === '$' && /(?<!\\)\|/.test(s.t)) issues.push(`L${n}: znak '|' wewnatrz wzoru w tabeli — uzyj \\lvert ... \\rvert`);
  });
  if (h1 !== 1) issues.push(`${h1} naglowkow H1 (oczekiwano dokladnie 1)`);

  if (issues.length) {
    problems += issues.length;
    console.log(`\n${path.relative(root, f) || path.basename(f)} — ${issues.length}`);
    issues.forEach(x => console.log('  • ' + x));
  }
}
console.log(`\nSprawdzono ${nMath} wyrazen matematycznych; problemow: ${problems}`);
process.exit(problems ? 1 : 0);
````

Szybkie kontrole bez zależności (wystarczy `grep`):

```bash
grep -n -- '\\arctg\|\\arcctg\|\\tg\|\\ctg\|\\RR\|\\CC' *.md   # zakazane makra
grep -nP '\r$' *.md                                            # konce linii CRLF
grep -nP ' {2,}$' *.md                                         # spacje na koncu linii
grep -nP '^\t' *.md                                            # wciecia TAB
grep -n -- '\$ \| \$' *.md                                     # spacje przy dolarach
grep -nP '^[^-#\s|].*\n?^---$' *.md                            # (orientacyjnie) '---' bez pustej linii
```

---
