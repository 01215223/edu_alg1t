# Agent instructions: solving algebra problem sets in GitHub-ready Markdown

| Field | Value |
| :--- | :--- |
| Document | English edition, version 2.0 |
| Last updated | 2026-10-11 |
| Repository | `01215223/edu_alg1t` |
| Source brief | [`.github/null.md`](null.md) — 6 requirements, Polish, read-only |
| Polish edition | [`agent_instruct_pol.md`](agent_instruct_pol.md) — canonical and more detailed |
| GitHub math engine | MathJax 3 over GitHub-flavoured Markdown (GFM) |
| Other renderers targeted | KaTeX (VS Code, Obsidian, GitLab), any CommonMark/GFM parser |
| Scope | how to solve the sets, and how to format `zestawN-odpowiedzi.md` |
| Status of task files | read-only — never edit without explicit user approval |
| Language of deliverables | Polish — this instruction file is the only English artifact |

> Rules marked **verified** were tested on 2026-10-11 with the audit tool in
> [§13](#13-appendix-b-audit-tool-and-quick-checks): every math expression in the repository was rendered
> through MathJax 3 (package `AllPackages`, red-output detection) and KaTeX (`strict: 'error'`), and the
> Markdown structure was checked against the GFM/CommonMark rules quoted below.

Delivery brief in one sentence: this repository holds Polish algebra problem sets; the agent must solve
every set, record both the working and the results in a separate Polish Markdown file per set, keep the
Markdown maximally compatible with GitHub (and with other renderers), verify that the file renders
correctly, and keep one consistent formatting style.

## Contents

1. [Quick start for an agent](#1-quick-start-for-an-agent)
2. [Mission and source of requirements](#2-mission-and-source-of-requirements)
3. [Repository map and current status](#3-repository-map-and-current-status)
4. [File naming and structure](#4-file-naming-and-structure)
5. [Step-by-step workflow](#5-step-by-step-workflow)
6. [Mathematical requirements for solutions](#6-mathematical-requirements-for-solutions)
7. [Repository math conventions](#7-repository-math-conventions)
8. [Markdown rules for maximum GitHub compatibility](#8-markdown-rules-for-maximum-github-compatibility)
9. [Definition of Done](#9-definition-of-done)
10. [Known defects and inconsistencies](#10-known-defects-and-inconsistencies)
11. [Git workflow](#11-git-workflow)
12. [Appendix A: canonical answer file template](#12-appendix-a-canonical-answer-file-template)
13. [Appendix B: audit tool and quick checks](#13-appendix-b-audit-tool-and-quick-checks)

---

## 1. Quick start for an agent

Work through these six steps in order. Never skip steps 3–5: they decide whether the file is accepted.

1. **Read the whole set first.** Open `zestawN.md`, list every item and sub-item in the source numbering
   (`1`, `1.1`, `5.2b`, `6.4`) and tick each one off as you solve it. Descriptive questions embedded in the
   text count as items (for example "What properties do addition and multiplication have…?", "Are there any
   other properties…?", "Which directed angles correspond to these vertices?").
2. **Solve everything independently of formatting.** Produce exact values, then verify every result with a
   second, independent method: substitution back, modulus/argument check, symbolic computation, or a
   numerical test.
3. **Write `zestawN-odpowiedzi.md`** at the repository root (flat structure), following the template in
   [§12](#12-appendix-a-canonical-answer-file-template), the math conventions in [§7](#7-repository-math-conventions)
   and the Markdown rules in [§8](#8-markdown-rules-for-maximum-github-compatibility). The file content is
   Polish — see the output kit in [§6.3](#63-polish-output-kit-terminology-and-phrasing).
4. **Run the audit** from [§13](#13-appendix-b-audit-tool-and-quick-checks) on the file you created.
   Expect zero problems and exit code `0` for that file.
5. **Check the rendered page on GitHub** (the file view, not the raw Markdown) and walk the checklist in
   [§9](#9-definition-of-done).
6. **Commit and open a pull request** per [§11](#11-git-workflow). One set equals one answer file equals one
   commit.

Never edit: [`.github/null.md`](null.md), any `zestawN.md` (they are read-only inputs), and answer files of
sets other than the one you are currently solving.

---

## 2. Mission and source of requirements

The brief [`.github/null.md`](null.md) contains six requirements. They map onto this document as follows.

| # | Brief requirement (original Polish) | English rendering | Implemented in |
| :---: | :--- | :--- | :--- |
| 1 | to jest repozytorium zadań z algebry matematycznej w języku polskim | this is a repository of mathematical algebra tasks in Polish | §6.3, §7 |
| 2 | wykonaj wszystkie zadania zapisane jako zestawy w osobnych plikach markdown | solve all tasks written as sets in separate Markdown files | §3, §4, §6 |
| 3 | zapisz przebieg wykonania tych zadań i wyniki w osobnych plikach markdown | record both the working and the results in separate Markdown files | §5, §6, §12 |
| 4 | utrzymuj maksymalną kompatybilność markdown z Githubem | keep maximum Markdown compatibility with GitHub | §8 |
| 5 | sprawdź czy markdown jest wyświetlany poprawnie | verify that the Markdown renders correctly | §9, §13 |
| 6 | utrzymuj ten sam styl formatowania markdown w repozytorium | keep one consistent Markdown formatting style | §7, §8, §12 |

Two policy decisions follow from requirement 1 and from the brief being Polish:

* **The deliverables stay Polish.** Item text, headings (`## Zadanie 1`, `## Podsumowanie wyników`), labels
  (**Dane**, **Wynik**, **Sprawdzenie**, **TAK**, **NIE**), notes and the summary table are written in Polish.
  This instruction file is the only English document in the repository.
* **English readers must still be able to write Polish answers.** [§6.3](#63-polish-output-kit-terminology-and-phrasing)
  provides the PL ↔ EN terminology and the phrasebook.

Overriding goal: the answer file must be (a) mathematically correct and complete, (b) rendered equally well
on GitHub, in VS Code, in Obsidian and on GitLab, and (c) stylistically indistinguishable from the existing
answer files.

---

## 3. Repository map and current status

Line counts measured on 2026-10-11.

| File | Role | Lines | Status (2026-10-11) |
| :--- | :--- | :---: | :--- |
| `.github/null.md` | the user's brief (6 requirements) | 6 | read-only; has no H1 on purpose |
| `zestaw0.md` | tasks: trigonometry, algebraic operations | 55 | **15 format defects** (§10), CRLF on all lines |
| `zestaw0-odpowiedzi.md` | solutions to set 0 | 183 | complete, clean — **style reference** |
| `zestaw1.md` | tasks: complex numbers | 39 | superseded by `zestaw1a.md` |
| `zestaw1a.md` | tasks: complex numbers (LaTeX fix) | 39 | **authoritative version** |
| `zestaw1a-odpowiedzi.md` | solutions to set 1/1a | 386 | complete; **12 expressions render red on GitHub** |
| `zestaw2.md` | tasks: powers, roots, equations in ℂ | 28 | **no answer file yet** |
| `zestaw2-odpowiedzi.md` | — | — | **to be created — the first deliverable** |

Operational conclusions:

* `zestaw1.md` and `zestaw1a.md` differ in exactly **one line** (line 35): `zestaw1a.md` wraps `$\arcsin$`
  in math, `zestaw1.md` leaves the bare word `arcsin`. Treat `zestaw1a.md` as authoritative, and **do not
  create** `zestaw1-odpowiedzi.md` — `zestaw1a-odpowiedzi.md` already covers both files.
* The repository has no `README.md`, no `.gitattributes`, no `.gitignore` and no `tools/` directory.
  Adding any of them requires user consent (§10).
* There are no image assets. Drawing tasks ("mark on the plane…") are answered with coordinate tables,
  figure descriptions and ASCII sketches — see [§6.2](#62-playbooks-by-task-type).
* The two answer files use somewhat different result-highlighting styles. For new files follow
  [§7](#7-repository-math-conventions) and box results with `\boxed{}` consistently; when in doubt, copy the
  structure of `zestaw0-odpowiedzi.md`, the cleanest file.

---

## 4. File naming and structure

| What | Convention | Example |
| :--- | :--- | :--- |
| Task set | `zestawN.md` (read-only) | `zestaw2.md` |
| Solutions | `zestawN-odpowiedzi.md`, repository root | `zestaw2-odpowiedzi.md` |
| Set variant | `zestawNa.md` → `zestawNa-odpowiedzi.md` | `zestaw1a-odpowiedzi.md` |
| Diagram (optional, consent required) | `assets/zestawN-zadM.svg` | `assets/zestaw2-zad3.svg` |
| Tooling (consent required) | `tools/md-audit.js` | §13 |

Hard rules:

* File names: lowercase, **ASCII only**, no spaces, no Polish diacritics, hyphen as separator.
* New files always live in the repository root (flat structure, as everywhere else in this repository).
* Do not create: copies of task files, `.pdf`/`.docx` exports, `build/` or `node_modules/` directories,
  temporary files (`*.tmp`, `draft.md`).
* Do not edit: `.github/null.md`, any `zestawN.md`, or another set's answer file.

---

## 5. Step-by-step workflow

1. **Read the entire set** and write out a checklist of all items and sub-items in the exact source
   numbering. Nothing may be skipped — including descriptive questions woven into the text
   (for example "Jakie kąty skierowane odpowiadają tym wierzchołkom?" / "Which directed angles correspond to
   these vertices?").
2. **Solve everything independently of formatting.** Verify every result with a second method: substitution
   back, modulus and argument check, independent symbolic computation (e.g. `sympy`), numeric test. For
   complex numbers, raise the result to the appropriate power, or multiply back.
3. **Write the file `zestawN-odpowiedzi.md`** per the template in [§12](#12-appendix-a-canonical-answer-file-template),
   keeping the conventions of [§7](#7-repository-math-conventions) and the formatting of
   [§8](#8-markdown-rules-for-maximum-github-compatibility).
4. **Run the audit** from [§13](#13-appendix-b-audit-tool-and-quick-checks). Expected result for your file:
   `0` problems, exit code `0`. If the tool reports defects in files you are not editing, record them in the
   pull-request description (§10) — do not fix them.
5. **Check the render** on GitHub (the file view, not a raw Markdown preview) and walk the checklist in §9.
6. **Commit and open the PR** per [§11](#11-git-workflow).

Working rules:

* One set = one file = one commit. Never mix new solutions with formatting fixes of other files.
* If an instruction is ambiguous (argument range, `Arg` versus `arg`, which boundary belongs to the set),
  **solve every interpretation** and state the assumption explicitly, as `zestaw1a-odpowiedzi.md` does.
* If the statement contains an error or a typo, solve according to mathematics and add a note
  `> **Uwaga do treści:** …` at the top of the file.
* Never invent results. When something cannot be computed exactly, say plainly what is an approximation.
* Keep the wording impersonal and technical, in Polish: "Mamy", "Zatem", "Stąd", "Podstawiając",
  "Dopełniając do kwadratu". No colloquialisms, no first person.

---

## 6. Mathematical requirements for solutions

* **Numbering 1:1 with the set:** `## Zadanie 1`, `### 1.1`, `### 5.2b`. Never merge or skip sub-items.
* **Show the working, not just the answer.** Brief item 3 requires the "course of execution": every
  meaningful step as its own display block, then the final result boxed with `\boxed{}`.
* **Domains, assumptions and exclusions are always explicit** (for example "dziedzina: $z \ne j$",
  "równość zachodzi wtedy i tylko wtedy, gdy …"), including when the result looks clean.
* **Exact values only** (`\sqrt{2}`, `\frac{\pi}{4}`, `2\sqrt{2}`), never decimal approximations — except
  where the task explicitly demands a calculator (for example `zestaw2.md` item 1.5). Then give the exact
  value **and** the approximation with four decimal places, marked `\approx`.
* **Yes/no questions** ("Czy podane równości zachodzą…?" / "Do the following equalities hold…?"): start with
  **TAK** or **NIE**, then give a general proof or a numeric counterexample, then state the condition under
  which the equality does hold.
* **Drawing tasks:** the agent cannot draw. Provide exact coordinate tables, a geometric description
  (figure, centre, radius, semi-axes, foci), an explicit statement of which boundaries belong to the set
  (solid versus dashed), and optionally an ASCII sketch inside a fenced `text` code block. See
  [§6.2](#62-playbooks-by-task-type) for the mandatory format.
* **Length:** as many steps as the solution needs, and no filler. Every formula must add something.

### 6.1 Per-item solution pattern

1. **Given / assumptions** — what is known, which convention is adopted.
2. **Transformation** — reduce to a known form (for example `z = x + jy`).
3. **Computation** — the steps, each as its own display block.
4. **Result** — boxed with `\boxed{}`.
5. **Check / interpretation** — substitution back, geometric meaning, boundary case.

### 6.2 Playbooks by task type

| Task type | What the answer must contain |
| :--- | :--- |
| Computations on complex numbers | every algebraic step, the `a + jb` form, the result boxed |
| "Does the equality hold?" | **TAK**/**NIE**, a general proof or a numeric counterexample, the equality condition |
| Sets in the plane (drawing tasks) | conversion to `x, y`; name of the figure; centre, radius, semi-axes, foci; **which boundaries belong to the set** (solid versus dashed); a table of control points; optionally an ASCII sketch in a code block |
| Equations in ℂ | the complete solution set (all roots), algebraic and trigonometric form, a description of the sketch of the solution set |
| Powers and roots | modulus and principal argument, de Moivre's formula, all `n` roots, their positions on the circle |
| Algebraic operations | commutativity yes/no plus counterexample, associativity yes/no plus counterexample, the identity element (two-sided!) or a proof that none exists; additionally: inverse elements, absorbing element, idempotence, the resulting structure (group, field) |
| Regular `n`-gons | radius `R`, starting angle, the angle list `\alpha_0 + \frac{2\pi k}{n}`, the list of vertex coordinates |

Mandatory format for drawing tasks (this is how `zestaw0-odpowiedzi.md` does it):

* a coordinate table with columns: angle/point, coordinates, extra intersections;
* a verbal description of the figure and its parameters;
* an explicit statement of which boundaries are included and which are excluded;
* optionally an ASCII sketch inside a fenced code block tagged `text`, because only a code block guarantees
  a constant character width.

### 6.3 Polish output kit: terminology and phrasing

The deliverable text is Polish. Use this table to write it correctly.

| Polish term | English | Notation / note |
| :--- | :--- | :--- |
| moduł | modulus (absolute value) | `\lvert z\rvert` — inside tables always `\lvert \rvert`, never a raw vertical bar |
| argument główny | principal argument | `\arg(z)`, `\operatorname{Arg}(z)` — always state the interval |
| sprzężenie | conjugate | `\overline{z}` (the repository also uses `\bar{z}`; new files use `\overline{z}`) |
| część rzeczywista / urojona | real / imaginary part | `\text{Re}(z)`, `\text{Im } z` |
| postać algebraiczna / trygonometryczna | algebraic / trigonometric form | `a + jb` / `r(\cos\varphi + j\sin\varphi)` |
| wzór Moivre'a | de Moivre's formula | `(\cos\varphi + j\sin\varphi)^n` |
| pierścień kołowy | annulus | `r_1 \le \lvert z - z_0\rvert < r_2` — state boundary inclusion |
| wycinek kątowy | angular sector | `\alpha \le \arg(z - z_0) < \beta` — no apex when `z_0` is excluded |
| półpłaszczyzna | half-plane | `ax + by + c \le 0` — give the boundary equation |
| okrąg Apoloniusza | circle of Apollonius | `\lvert z - A\rvert = k\lvert z - B\rvert`, `k \ne 1` |
| elipsa, ogniska, półosie | ellipse, foci, semi-axes | `\frac{x^2}{b^2} + \frac{y^2}{a^2} = 1`; if `2a \le 2c` the set degenerates to a segment |
| ćwiartka układu | quadrant of the coordinate system | I–IV; state the signs of `x` and `y` |
| dziedzina, wykluczenia | domain, exclusions | always list them |
| brzeg należy / nie należy | boundary included / excluded | solid versus dashed line |
| kontrprzykład | counterexample | mandatory whenever the answer is "no" |
| działanie łączne / przemienne | associative / commutative operation | `(a*b)*c = a*(b*c)` / `a*b = b*a` |
| element neutralny / odwrotny / pochłaniający | identity / inverse / absorbing element | the identity must be **two-sided** |
| idempotentność | idempotence | `x * x = x` |
| grupa abelowa / ciało | abelian group / field | state as an extra property |
| przybliżenie | approximation | four decimal places with `\approx`, exact value first |
| n-kąt foremny, wierzchołki | regular n-gon, vertices | list angles and coordinates |

Phrasebook: **Dane:** (Given), **Krok 1 — …** (Step 1 — …), **Wynik:** (Result),
**Odpowiedź:** (Answer), **Sprawdzenie:** (Verification), **Uzasadnienie:** (Justification),
Mamy (We have), Zatem / Stąd (Hence), Podstawiając (Substituting), Dopełniając do kwadratu (Completing the
square), Korzystamy ze wzoru (We use the formula), Niech … (Let …), gdzie (where), dla dowolnych (for
arbitrary), dla każdego (for every), istnieje / nie istnieje (there exists / there is no),
**TAK** / **NIE** (yes / no), Uwaga do treści (note on the statement).

Polish typography: use a decimal comma in approximations (`1{,}4142`), radians rather than degrees, and the
straight quotation style of the existing files.

---

## 7. Repository math conventions

| Topic | Required | Forbidden or risky |
| :--- | :--- | :--- |
| Imaginary unit | `j` (as in all `zestawN.md` files) | `i`, `\imath`, `\mathrm{i}` |
| Real / imaginary part | `\text{Re}(z)`, `\text{Im } z` | `Re z` without `\text{}` |
| Conjugate | `\overline{z}` | `\bar{z}` (legacy), `\conj{z}` (does not exist) |
| Number sets | `\mathbb{R}`, `\mathbb{C}`, `\mathbb{Z}`, `\mathbb{N}` | `\RR`, `\CC` (**verified: render red on GitHub**) |
| Inverse tangent | `\operatorname{arctg}` or `\arctan` | `\arctg`, `\arcctg`, `\tg`, `\ctg` (**verified: render red on GitHub**) |
| Argument | an explicit convention: `(-\pi,\pi]` or `[0,2\pi)`; give both when the task does not fix one | a result with no stated interval |
| Angles | radians: `\frac{5\pi}{6}` | degrees, unless the task itself uses degrees |
| Sets in braces | `\{x, y\}`, `\left\{ \right\}` | `{x, y}` without a backslash |
| Spacing | `\quad` between conditions, `\,` before a scalar, `\ ` in `\text{Im } z` | several display blocks on one line |
| Scaled delimiters | `\left( \right)`, `\left\lvert \right\rvert` | hand-sized parentheses around `\frac` |
| Final result | `\boxed{}` | bold text without the formula |
| Systems and multi-line derivations | `aligned`, `cases`, `array` inside a display block | `align`, `equation`, `gather`, `\tag`, `\label` |
| Matrices | `pmatrix`, `bmatrix`, `vmatrix` | `tabular`, `\hline` outside `array` |
| Symbols inside math | LaTeX macros (`\le`, `\in`, `\emptyset`, `\times`, `\to`, `\infty`, `\pm`) | raw Unicode symbols inside math (`≤`, `∈`, `∅`, `×`, `→`) |

### 7.1 Verified macro compatibility

Legend: OK = renders correctly; RED = MathJax renders a red "undefined" text; FAIL = parser error.
MathJax is what GitHub uses; KaTeX is what VS Code, Obsidian and GitLab use.

| Expression | GitHub (MathJax) | KaTeX | Verdict |
| :--- | :---: | :---: | :--- |
| `\operatorname{arctg}(2)` | OK | OK | **use** for Polish notation |
| `\arctan(2)`, `\arcsin(2)`, `\cot x` | OK | OK | use for ANSI notation |
| `\arctg(2)` | **RED** | OK | **forbidden** — 12 such expressions exist today in `zestaw1a-odpowiedzi.md` |
| `\tg x`, `\ctg x`, `\arcctg x` | **RED** | OK | **forbidden** → `\tan`, `\cot`, `\operatorname{arcctg}` |
| `\RR`, `\CC`, `\eps`, `\foobar` | **RED** | FAIL | **forbidden** → `\mathbb{R}`, `\varepsilon` |
| `\degree` | OK | OK | allowed, but prefer `^\circ` for consistency |
| `\emptyset` | OK | OK | use it; a raw `∅` fails in KaTeX strict mode |
| `\begin{aligned} … \end{aligned}` | OK | OK | **use** |
| `\begin{align} … \end{align}` | OK | display mode only | avoid |
| `\tag{1}` | OK | display mode only | **do not use** |
| `\begin{tabular}` | FAIL | FAIL | **forbidden** → `\begin{array}` |
| `\boxed{…}` | OK | OK | use for results |
| `\implies`, `\iff` | OK | OK | use |
| `\lvert z\rvert`, `\left\lvert z\right\rvert` | OK | OK | **mandatory inside tables** |
| `\overline{z}`, `\bar{z}` | OK | OK | standardise on `\overline{z}` |
| `\text{Re}(z)`, `\text{Im } z`, `\Re z`, `\Im z` | OK | OK | use consistently |
| `\text{ąęśćżźńół}` | OK | OK | Polish diacritics inside `\text{}` are safe |
| `\mathbb{R}\times\mathbb{R}`, `\sqrt[3]{ab}`, `\substack`, `\vec{AB}` | OK | OK | safe |
| `\begin{array}{\|c\|c\|}\hline … \end{array}` | OK | OK | safe (inside a display block) |

**Forbidden everywhere** (any custom macro, and in particular): `\arctg`, `\arcctg`, `\tg`, `\ctg`,
`\cosec`, `\ch`, `\sh`, `\RR`, `\NN`, `\ZZ`, `\QQ`, `\CC`, `\eps`. Use `\operatorname{arctg}`,
`\tan`, `\cot`, `\csc`, `\cosh`, `\sinh`, `\mathbb{R}`, `\varepsilon`.

**Forbidden environments and commands:** `tabular`, `enumerate`, `\hline` outside `array`,
`\newcommand`, `\renewcommand`, `\def`, `\require{}`, `\tag`, `\label`; avoid `align`, `equation` and
`gather` (portable only inside display math).

**Forbidden delimiters:** `\( … \)` and `\[ … \]` — GitHub supports only `$…$`, `$$…$$`, the GitHub-only
double-backtick dollar form, and the GitHub-only fenced block tagged `math`.

Note on the imaginary unit: the repository convention is `j` because all task statements use `j`.
`zestaw0-odpowiedzi.md` uses `i` once, in the interpretation paragraph of task 4e — a legacy inconsistency
recorded in §10. New files use `j` throughout.

---

## 8. Markdown rules for maximum GitHub compatibility

### 8.1 File and characters

* Encoding **UTF-8 without BOM**, line endings **LF**, the file ends with a newline.
* No TAB characters — spaces only. No trailing spaces. No non-breaking or narrow spaces
  (U+00A0, U+2007, U+202F).
* Polish diacritics in prose: yes. Inside math: use LaTeX macros only (§7).
* Typographic symbols allowed in prose: `–`, `—`, `„ ”`, `→`, `✓`. Inside math: none of them.
* Prefer one thought per line; separate long paragraphs with a blank line rather than a hard break.

### 8.2 Headings

* **Exactly one H1** per file, on the first line (GitHub uses it as the page title).
* ATX headings only (`##`), never setext (`===` or `---` underlined text).
* **No level jumps:** H1 → H2 → H3. Never start with `####` (defect in `zestaw0.md`).
* A blank line before and after every heading.
* Hierarchy pattern for an answer file: `# title` → `## Zadanie N` → `### N.M`.
* Never use headings as bold text or to number content that is not a section.
* Math in headings is allowed (the repository does it), but **never link to such headings**: GitHub anchor
  slugs for headings containing `$…$` are unpredictable.

### 8.3 Paragraphs, lists, separators

* A blank line before and after: a heading, a list, a table, a display `$$` block, a `---` separator,
  a code fence.
* **One list marker per line, at the start of the line.** Writing `text:* first item* second item` produces
  a single paragraph with literal asterisks, not a list — **verified**, and it is the defect at lines 8
  and 36 of `zestaw0.md`.
* Markers: `*` for unordered lists (repository convention), `1.` for ordered lists.
* Nested indentation equals the width of the parent marker: **2 spaces** under `* `, **3 spaces** under `1. `.
  **Verified:** a display block indented 4 or more spaces beyond the parent content column turns into a code
  block.
* The `---` separator only with blank lines on both sides. **Verified:** `---` directly after a text line
  creates a setext H2 heading (defect at line 29 of `zestaw0.md`, where the last sentence of task 3 became a
  heading).
* Sub-items of a task are written as `* **1.1** content` (the style of `zestaw1.md` and both answer files).
* Avoid hard line breaks. When one is unavoidable, use a backslash at the end of the line (GitHub supports
  it), never two trailing spaces (defect: 10 occurrences in `zestaw0.md`).
* Use a block quote (`>`) at the top of the file for assumptions and for notes on the statement, as
  `zestaw0-odpowiedzi.md` does.

### 8.4 Tables

* GFM tables only: a header row, an alignment row (`| :--- |`, `| :---: |`, `| ---: |`), data rows.
* A blank line before and after the table.
* Inside cells use **inline math only**. **Verified:** `$$…$$` in a cell degrades to inline math and breaks
  the rhythm of the table.
* **Verified:** a raw vertical bar inside a formula splits the cell (`\lvert z\rvert` is safe, a raw pair of
  bars is not). Inside tables always use `\lvert … \rvert`, `\vert` or `\mid`.
* Line breaks inside a cell: `<br>`. Do not put lists or blocks inside cells.
* At most 5–6 columns (mobile readability); keep cells short.
* A literal vertical bar in cell text: `\|`.

### 8.5 Math

* **Inline:** `$x+1$` — the dollar signs must hug the formula, no space next to the delimiters. GitHub may
  fail to recognise `$ x $`, and a `$` before a digit can be read as a currency amount. **Verified:** the
  text `$ 5 i $ 10` turns into a math expression.
* **GitHub-only variant:** `` $`x_1 * y`$ `` when the formula contains characters that clash with Markdown
  (`_`, `*`, `|`, a backtick). Caution: this does not work in KaTeX — use it only as a last resort.
* **Display block:** `$$` on its own lines, with blank lines around the block and the formula in between.
  The formula below is a working example — a `$$` block indented to the content column of a `* ` item:

  $$
  \lvert z_1 + z_2\rvert \le \lvert z_1\rvert + \lvert z_2\rvert
  $$

* Inside a list item, indent the display block to the content column (2 spaces under `* `, 3 spaces under
  `1. `) and separate it with blank lines — then it remains part of that list item.
* **GitHub-only variant:** a fenced block with the `math` info string (without `$$`). It renders on GitHub
  but shows as a plain code block in VS Code, Obsidian and GitLab. **Default to `$$`.**
* **Forbidden delimiters:** `\( … \)` and `\[ … \]` — GitHub does not support them.
* **A literal dollar sign:** `\$` inside math, `<span>$</span>` outside math (GitHub documentation).
* **No macro definitions:** `\newcommand`, `\renewcommand`, `\def`, `\require{}` — every display block is
  compiled independently, so macros never survive into the next expression.
* **Line breaks inside formulas:** `\\` only inside `aligned`, `cases`, `array` or matrices.
  **Verified:** a bare `\\` at the top level of a display block makes KaTeX warn
  ("in LaTeX, `\\` does nothing in display mode").
* Several expressions side by side: one display block with `\quad`, never several `$$` on one line — that is
  the defect in `zestaw2.md` (12 lines where `$$` shares a line with the list text; **verified:** such a
  formula renders inline instead of as a block).

### 8.6 HTML, links, images

* HTML only sparingly and only from this list: `<br>`, `<sub>`, `<sup>`, `<span>`, `<details>`, `<summary>`,
  `<div align="center">`, `<img src="assets/…" width="…">`, `<kbd>`. GitHub sanitises HTML (`<script>`,
  `<style>`, `<iframe>` and event attributes are stripped out), and other renderers may drop all of it —
  so use HTML only where Markdown cannot express the intent.
* Links must be **relative**: `[zestaw 2](../zestaw2.md)`, `[brief](null.md)` (from a file inside `.github/`).
* Images: `![alt text describing the figure](assets/zestaw2-zad3.svg)` — alt text is mandatory, SVG is
  preferred, size via `<img … width="480">`.
* Internal anchors only for headings that contain no math (§8.2).
* For "mark on the plane" tasks a coordinate table is mandatory; an image is optional.

---

## 9. Definition of Done

An answer file `zestawN-odpowiedzi.md` is ready when every box is ticked:

- [ ] Every item and sub-item of the set is answered, in the source numbering.
- [ ] Every result is verified by a second, independent method (substitution or independent computation).
- [ ] Final results are highlighted with `\boxed{}` (or a bold **Wynik**/**Odpowiedź** label, consistently).
- [ ] Domains, assumptions and exclusions are stated (for example `z \ne j`), and yes/no questions start with **TAK**/**NIE** plus justification.
- [ ] Drawing tasks include coordinates, a description of the figure and the boundary status (solid versus dashed).
- [ ] The imaginary unit is `j`; no `\arctg`, `\tg`, `\ctg`, `\arcctg`, `\RR`, `\CC` in any formula.
- [ ] No `\( \)` or `\[ \]` delimiters; no `\newcommand` / `\require`; no `\tag` / `\label` / `align` / `tabular`.
- [ ] All `$$` are on their own lines, with blank lines around them and list-compatible indentation.
- [ ] No `$$` inside tables and no raw vertical bars inside table formulas (use `\lvert \rvert`).
- [ ] Exactly one H1, no heading level jumps, blank lines around every block.
- [ ] Every `---` has blank lines on both sides; no list marker is glued into a paragraph.
- [ ] The file is UTF-8 without BOM, LF only, no TABs, no trailing spaces, and ends with a newline.
- [ ] The audit script (§13) reports `0` problems for the file you created.
- [ ] The rendered page has been checked visually on GitHub: headings, tables, formulas, lists, separators.
- [ ] The style is indistinguishable from `zestaw0-odpowiedzi.md`.

---

## 10. Known defects and inconsistencies

Audited on 2026-10-11 with the tool from §13. **Task files are read-only** — report the defects in the pull
request, do not fix them without the user's approval.

| File | Issues | Details |
| :--- | :---: | :--- |
| `zestaw1a-odpowiedzi.md` | 12 | lines 332–386: 12 formulas contain `\arctg` (16 occurrences) and **render as red "undefined" text on GitHub**; replace with `\operatorname{arctg}` |
| `zestaw0.md` | 15 | CRLF on all 55 lines; line 2 jumps from H1 to H4; lines 8 and 36 have list markers glued into a paragraph (the content is lost as a list); line 29 has `---` without a preceding blank line, so the last sentence of task 3 becomes an H2 heading; 10 hard line breaks (trailing spaces) at lines 22–26, 32–34, 36 and 39 |
| `zestaw2.md` | 12 | lines 4–9 and 17–22: `$$…$$` shares a line with the list text, so the formulas render inline instead of as blocks |
| `.github/null.md` | 1 | no H1 — intentional (it is a brief in list form); do not "fix" it |
| `zestaw0-odpowiedzi.md`, `zestaw1.md`, `zestaw1a.md` | 0 | clean |

Style inconsistencies (they render fine, but note them when writing new files):

* `zestaw1a-odpowiedzi.md` uses `\bar{z}` 14 times; the convention for new files is `\overline{z}`.
* `zestaw1a-odpowiedzi.md` writes `$|z_1 + 2j|$` with raw bars. That is acceptable outside tables; inside
  tables always use `\lvert … \rvert`.
* The two answer files highlight results differently (`zestaw0-odpowiedzi.md` boxes results four times;
  `zestaw1a-odpowiedzi.md` uses bold **Wynik**/**Odpowiedź** labels). New files box the result.
* `zestaw0-odpowiedzi.md` line 160 and line 183 use `i` for the imaginary unit inside an interpretation
  paragraph, while every task statement uses `j`.
* In `zestaw1.md` line 35 the words `arcsin` and `arctg` are plain text outside math; `zestaw1a.md` fixes
  only `\arcsin`. Write both as formulas in answers: `$\arcsin$`, `$\operatorname{arctg}$`.

Recommendations — to be implemented **only with the user's consent**:

* a `.gitattributes` file with `* text=auto eol=lf` and `*.md text eol=lf`, which removes the CRLF problem;
* a `README.md` indexing the sets and linking to the answer files;
* `tools/md-audit.js` (the script from §13) plus a `.gitignore` containing `node_modules/`;
* one dedicated commit fixing the formatting of `zestaw0.md` and `zestaw2.md`;
* replacing `\arctg` with `\operatorname{arctg}` in `zestaw1a-odpowiedzi.md`.

---

## 11. Git workflow

* Work on the session branch; never on `main`. Before any change run `git status` and `git diff`.
* Commit messages: imperative mood, Polish, concise, no trailing period, no emoji — for example
  `Dodaj rozwiązania zestawu 2`, `Popraw renderowanie wzorów w zestawie 1a`.
* One set = one commit. Formatting fixes of existing files go into a separate commit.
* Never commit `node_modules/`, temporary files, generated HTML/PDF, or large binaries.
* The pull-request description must contain: the list of created/modified files, the §9 checklist, the §13
  audit result (number of expressions checked and number of problems), and the defects observed in files
  that were **not** edited (§10).
* Never use `--force` on a shared branch. Never merge a pull request without the user's approval.

---

## 12. Appendix A: canonical answer file template

Copy this structure and fill it in. Mind the blank lines, the two-space indentation of display blocks inside
list items, and the use of `\lvert \rvert` inside tables.

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

## 13. Appendix B: audit tool and quick checks

The script checks `.md` files against every rule in §7 and §8. It is **not** part of the repository (the
current decision is that only instructions are produced); store it outside the repository, or add it as
`tools/md-audit.js` once the user consents.

Usage:

```bash
npm i --no-save mathjax-full katex            # once, outside the repository (for example in /tmp)
node /tmp/mdaudit/md-audit.js .               # audit every .md file; exit code 0 = no problems
node /tmp/mdaudit/md-audit.js zestaw2-odpowiedzi.md   # audit a single file
```

What it checks:

* file level: BOM, CRLF, missing final newline, non-breaking or narrow spaces;
* math level: red output in MathJax (GitHub), KaTeX strict-mode errors, forbidden macros, spaces next to
  `$`, a `$` before a digit, `\( \)` / `\[ \]` delimiters, `\newcommand` / `\require`;
* structure level: number of H1 headings, heading level jumps, the setext `---` trap, list markers glued
  into a paragraph, `$$` sharing a line with text, TABs, trailing spaces, raw vertical bars inside table
  formulas;
* everything inside code fences and inline code is blanked out first, so documentation examples never
  raise false alarms.

This English edition of the script differs from the Polish one in four small ways, all corrections of
internal inconsistencies:

1. heading structure is checked on code-masked lines, so a Markdown template embedded in a fenced block is
   not counted as a second H1;
2. whitespace-only `$…$` matches are ignored, which removes a false positive on lines that discuss dollar
   delimiters;
3. a single `.md` file may be passed as the argument, which makes the "audit one deliverable" workflow exact;
4. `\degree` is no longer treated as forbidden, because it renders correctly in both engines; the style
   guide still prefers `^\circ`.

````javascript
#!/usr/bin/env node
/* md-audit.js - Markdown + math compatibility audit for this repository.
   Usage:   node md-audit.js [path]     path = repository directory or a single .md file
   Exit:    0 = no problems, 1 = problems found
   Install: npm i --no-save mathjax-full katex
   Deltas vs the Polish edition (.github/agent_instruct_pol.md), see section 13:
     1. heading structure is checked on code-masked lines (fenced templates do not count);
     2. whitespace-only $...$ matches are skipped (masking artefact on lines about dollars);
     3. a single .md file may be passed as the argument;
     4. \degree is allowed (renders in both engines; the guide still prefers ^\circ). */

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

/* Blank out everything that is not math: code fences (except ```math) and inline code.
   Documentation examples therefore never raise false alarms. */
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
  const fenceRe = new RegExp('`{3,}math\\\\r?\\\\n([\\\\s\\\\S]*?)`{3,}', 'g');
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

/* Macros that GitHub (MathJax) renders as red "undefined" text */
const FORBIDDEN = ['\\arctg', '\\arcctg', '\\tg', '\\ctg', '\\cosec', '\\ch', '\\sh',
                   '\\RR', '\\NN', '\\ZZ', '\\QQ', '\\CC', '\\eps'];
const FORBIDDEN_RE = FORBIDDEN.map(x => new RegExp(x.replace(/\\/g, '\\\\') + '(?![a-zA-Z])'));

const target = process.argv[2] || '.';
const walk = d => fs.readdirSync(d, { withFileTypes: true }).flatMap(e =>
  (e.name === '.git' || e.name === 'node_modules') ? []
    : e.isDirectory() ? walk(path.join(d, e.name))
    : e.name.endsWith('.md') ? [path.join(d, e.name)] : []);

let files;
try {
  files = fs.statSync(target).isFile() ? [target] : walk(target);
} catch {
  console.error(`md-audit: cannot read ${target}`);
  process.exit(2);
}

let nMath = 0, problems = 0;
for (const f of files) {
  const src = fs.readFileSync(f, 'utf8');
  const plain = maskCode(src);
  const L = src.split(/\r?\n/);
  const LP = plain.split(/\r?\n/);
  const issues = [];
  const lineOf = idx => src.slice(0, idx).split(/\r?\n/).length;

  /* --- A. file and characters --- */
  const crlf = (src.match(/\r\n/g) || []).length;
  if (crlf) issues.push(`CRLF: ${crlf}/${L.length} lines (expected LF)`);
  if (src.charCodeAt(0) === 0xFEFF) issues.push('UTF-8 BOM at the start of the file');
  if (src.length && !src.endsWith('\n')) issues.push('missing final newline');
  if (/[\u00A0\u2007\u202F]/.test(src)) issues.push('non-breaking or narrow space (U+00A0 / U+2007 / U+202F)');

  /* --- B. math --- */
  for (const s of mathSpans(src)) {
    if (!s.t.trim()) continue;
    nMath++;
    const ln = lineOf(s.i);
    const bad = FORBIDDEN.filter((_, k) => FORBIDDEN_RE[k].test(s.t));
    if (bad.length) issues.push(`L${ln}: forbidden macro ${bad.join(', ')} (GitHub/MathJax: red text)`);
    else if (mjRed(s.t, s.d)) issues.push(`L${ln}: MathJax/GitHub renders it in RED: ${s.t.trim().slice(0, 60)}`);
    const kf = ktFail(s.t, s.d);
    if (kf) issues.push(`L${ln}: KaTeX (VS Code/Obsidian/GitLab): ${kf} :: ${s.t.trim().slice(0, 50)}`);
    if (s.k === '$' && (/^\s/.test(s.t) || /\s$/.test(s.t))) issues.push(`L${ln}: space next to a '$' delimiter - GitHub may not recognise the formula`);
    if (s.k === '$' && /^[0-9]/.test(src.slice(s.i + s.raw.length))) issues.push(`L${ln}: '$' immediately before a digit - risk of currency interpretation`);
  }
  if (/\\\[[\s\S]*?\\\]|\\\(/.test(plain)) issues.push('\\[ \\] or \\( \\) delimiters - not supported by GitHub (use $ and $$)');
  if (/\\newcommand|\\renewcommand|\\require\{/.test(plain)) issues.push('\\newcommand / \\renewcommand / \\require - macros do not carry over between formulas');

  /* --- C. Markdown structure --- */
  let h1 = 0, lastLvl = 0;
  L.forEach((raw, i) => {
    const line = LP[i] ?? '', prev = LP[i - 1] ?? '';
    const n = i + 1;
    const h = /^(#{1,6})\s/.exec(line);
    if (h) {
      const lvl = h[1].length;
      if (lvl === 1) h1++;
      if (lastLvl && lvl > lastLvl + 1) issues.push(`L${n}: heading level jump H${lastLvl} -> H${lvl}`);
      lastLvl = lvl;
    }
    if (!line.trim()) return;
    if (/^(-{3,}|_{3,})\s*$/.test(line) && prev.trim() !== '' && !/^#{1,6}\s/.test(prev) && !/^\s*\|/.test(prev))
      issues.push(`L${n}: '---' without a preceding blank line = setext H2 heading, not a horizontal rule`);
    const glued = [...line.matchAll(/[^\s*\\]\* (?=\S)/g)].filter(x => x.index > 0);
    if (glued.length && !/^\s*([-*+]|\d+\.)\s/.test(line)) issues.push(`L${n}: ${glued.length} list marker(s) glued into a paragraph`);
    const t = line.trim();
    if (t.includes('$$') && !/^\$\$$/.test(t) && !/^\$\$[^$]*\$\$$/.test(t)) issues.push(`L${n}: '$$' on the same line as text - the formula will not be a display block`);
    if (/^\t/.test(raw)) issues.push(`L${n}: TAB indentation (use spaces)`);
    if (/[^\s] {2,}$/.test(raw)) issues.push(`L${n}: hard line break (trailing spaces)`);
    if (/^\s*\|/.test(line)) for (const s of mathSpans(line)) if (s.k === '$' && /(?<!\\)\|/.test(s.t)) issues.push(`L${n}: '|' inside a table formula - use \\lvert ... \\rvert`);
  });
  if (h1 !== 1) issues.push(`${h1} H1 headings (expected exactly 1)`);

  if (issues.length) {
    problems += issues.length;
    console.log(`\n${path.relative(target, f) || path.basename(f)} - ${issues.length}`);
    issues.forEach(x => console.log('  * ' + x));
  }
}
console.log(`\nChecked ${nMath} math expressions; problems: ${problems}`);
process.exit(problems ? 1 : 0);
````

Dependency-free spot checks (plain `grep`):

```bash
grep -n -- '\\arctg\|\\arcctg\|\\tg\|\\ctg\|\\RR\|\\CC' *.md   # forbidden macros (red on GitHub)
grep -nP '\r$' *.md                                           # CRLF line endings
grep -nP ' {2,}\r?$' *.md                                     # hard line breaks (trailing spaces)
grep -nP '^\t' *.md                                           # TAB indentation
grep -n -- '\$ \| \$\|\$[0-9]' *.md                           # spaces next to $ delimiters / $ before a digit
grep -nE '^---$' *.md                                         # list every ---; each needs blank lines around it
```
