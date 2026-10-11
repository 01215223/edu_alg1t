## English version

This section restates the same rules for agents that do not read Polish. The repository content and
all deliverables stay in Polish.

### Mission

This repo holds Polish university algebra problem sets (`zestawN.md`) and their worked solutions
(`zestawN-odpowiedzi.md`). The brief in `.github/null.md` requires: solve every problem set, record
both the working and the results in separate Markdown files, keep maximum GitHub Markdown
compatibility, verify that the Markdown renders correctly, and keep one consistent formatting style.

### Hard rules

1. **Never edit** `.github/null.md` or any `zestawN.md` (they are read-only inputs). Add only
   `zestawN-odpowiedzi.md` at the repo root. ASCII-only, lowercase, hyphenated file names.
2. **One set = one answer file = one commit.** Answer every item and sub-item using the source
   numbering (`## Zadanie 1`, `### 1.1`). Never skip descriptive questions embedded in a task.
3. **Show the working**, not just the answer: one display block per meaningful step, then box the
   final result with `\boxed{…}`. State domains, exclusions and conventions. Verify every result by
   a second, independent method. For yes/no questions answer **TAK/NIE** first, then give a proof or
   a numeric counterexample plus the equality condition.
4. **Drawing tasks**: you cannot draw, so give exact coordinate tables, a geometric description
   (figure, centre, radius, semi-axes, foci), which boundaries belong to the set (solid vs dashed),
   and optionally an ASCII sketch inside a fenced code block.
5. **Exact values only** (`\sqrt{2}`, `\frac{\pi}{4}`). Decimals only when the task demands a
   calculator — then give exact plus `\approx` with four decimal places.

### Repository math conventions

Imaginary unit is **`j`**, never `i`. Use `\text{Re}(z)`, `\text{Im } z`, `\overline{z}`,
`\mathbb{R}`, `\mathbb{C}`. Always state the argument convention (`(-\pi,\pi]` or `[0,2\pi)`) and
give both when the task does not fix one. Radians, not degrees. Multi-line derivations use
`aligned` / `cases` / `array` inside a `$$` block.

### Verified renderer compatibility (MathJax on GitHub vs KaTeX elsewhere)

* **Banned** (GitHub renders red "undefined"): `\arctg`, `\arcctg`, `\tg`, `\ctg`, `\cosec`, `\ch`,
  `\sh`, `\RR`, `\NN`, `\ZZ`, `\QQ`, `\CC`, `\eps`, and any other custom macro.
  Use `\operatorname{arctg}`, `\arctan`, `\tan`, `\cot`, `\mathbb{R}`, `\varepsilon`.
* **Banned environments/commands**: `tabular`, `enumerate`, `\hline` outside `array`,
  `\newcommand`, `\renewcommand`, `\def`, `\require{}`, `\tag`, `\label`; avoid `align`,
  `equation`, `gather` (portable only inside display math).
* **Banned delimiters**: `\( … \)` and `\[ … \]` — GitHub supports only `$…$`, `$$…$$`, the
  GitHub-only double-backtick dollar form, and the GitHub-only fenced block tagged `math`.
* Raw Unicode math symbols (`∅`, `≤`, `∈`, `×`, `→`) may break KaTeX strict mode — always use LaTeX
  macros inside math. Polish diacritics inside `\text{…}` are safe in both engines.

### Verified Markdown rules (GitHub-flavoured)

* UTF-8 without BOM, **LF** line endings, trailing newline, no tabs, no trailing spaces,
  no non-breaking spaces.
* Exactly **one H1** per file, ATX headings only, no level jumps, blank line around every block.
* Blank line around headings, lists, tables, `$$` blocks, code fences and `---`.
* `---` directly after a text line becomes a **setext H2**, not a horizontal rule.
* One list marker per line at the start of the line. `text:* a* b` renders as a paragraph with
  literal asterisks, not as a list.
* List nesting indent = parent marker width (2 spaces for `* `, 3 for `1. `); a `$$` block indented
  4+ spaces beyond the content column becomes a code block.
* `$$` must be alone on its lines; `* **1.1** $$…$$` renders inline, not as a display block.
* Inline math must hug its delimiters (`$x+1$`, never `$ x+1 $`), and a closing `$` followed by a
  digit can be read as currency. Escape literal dollars as `\$` (inside math) or `<span>$</span>`.
* Tables: GFM only, inline math only, and never a raw `|` inside math — use `\lvert … \rvert`.
  Line breaks inside cells with `<br>`.
* HTML only from a small allowlist (`<br>`, `<sub>`, `<sup>`, `<span>`, `<details>`, `<summary>`,
  `<div align="center">`, `<img>`); GitHub sanitises it and other renderers may drop it.
* Relative links and relative image paths (`assets/…`) with mandatory alt text.

### Definition of Done

Every sub-item answered and independently verified, results boxed, conventions stated, no banned
macros or delimiters, all `$$` on their own lines, no `|` inside table math, one H1 with no level
jumps, blank lines around every block, `---` never glued to text, LF-only clean file, the audit
script from §12 returning zero problems and exit code 0, and the rendered page visually checked on
GitHub. Style must be indistinguishable from `zestaw0-odpowiedzi.md`.

### Current state (audit 2026-10-11, 741 math expressions)

`zestaw2-odpowiedzi.md` is **missing** — that is the next deliverable. `zestaw1.md` and `zestaw1a.md`
are duplicates differing in one line (35); `zestaw1a` is authoritative, so do not create
`zestaw1-odpowiedzi.md`. Outstanding defects to report but not fix without approval: 12 red
`\arctg` formulas in `zestaw1a-odpowiedzi.md`, 15 formatting issues in `zestaw0.md`
(CRLF, glued bullets at L8/L36, setext trap at L29, H1→H4 jump, 10 trailing-space breaks) and 12
inline-`$$` issues in `zestaw2.md`.
