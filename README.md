# Abstract Algebra

> Lecture notes and fully worked weekly homework for an abstract algebra course, written in Markdown with inline LaTeX, in a Chinese/English parallel structure.

This repository accompanies the course textbook **《抽象代数》 (Abstract Algebra) by Deng Shaoqiang (邓少强) & Zhu Fuhai (朱富海)**, Science Press — the standard text for the algebra track at Nankai University. Entry numbering in the notes follows the textbook (e.g. **Definition 1.1.4**), so the notes can be read side-by-side with the book.

## Repository structure

```
abstract-algebra/
├── cn/
│   ├── notes.md              # Chinese lecture notes (single file, all chapters)
│   └── homework/
│       └── week1.md … week26.md
├── en/
│   ├── notes.md              # English version of the notes (partial, WIP)
│   └── homework/
│       └── week1.md … week26.md
└── textbooks/
    ├── abstruct-algebra.pdf          # Scan of the textbook (219 pp.)
    └── abstruct-algebra_ocr.pdf      # OCR (searchable) copy
```

## The notes

`notes.md` is a single, continuously numbered reference organized as **10 chapters** with `##` headings:

1. Basic concepts of groups
2. Group homomorphisms and the structure of groups
3. Permutation groups and solvability
4. Group actions and the Sylow theorems
5. Rings and ideals
6. Unique factorization domains and Euclidean domains
7. Polynomials and power series
8. Modules and module homomorphisms
9. Finitely generated modules over PIDs
10. Field theory

Every statement is a bold-tagged entry — **Definition**, **Theorem**, **Lemma**, **Proposition**, **Example** — followed by the statement and proof, with mathematics typeset in `$…$` / `$$…$$` LaTeX. The Chinese version contains 92 entries.

## The homework

Each `homework/weekN.md` follows a fixed three-part format:

1. **Toolbox** — a blockquote restating the definitions and theorems needed for the week's problems;
2. **Problems** — the assigned exercises (`### 习题一` …);
3. **Solutions** — complete worked proofs (`### 解答 习题一` …), each ending with `$\blacksquare$`.

There are **26 weeks** of problem sets in each language. The largest set (`week9.md`, ~290 lines) covers group actions and their connection to Stiefel manifolds.

## Bilingual layout

- `cn/` — the authoritative Chinese version.
- `en/` — an English mirror with the same file layout.
  - **Status:** the English translation is **incomplete and machine-generated** (34 of 92 entries, formula errors). The Chinese version is the reliable one; treat `en/` as work in progress.
- `en/` and `cn/` files with the same name are intended to correspond section by section.

## The `textbooks/` folder

The PDFs here are **external reference material** (the scanned textbook and its OCR copy), not documents compiled from the notes. There is no build system; the notes are plain Markdown meant to be read directly on GitHub or any Markdown viewer with LaTeX rendering.

## Related repositories

See the other course-notes repositories in the same series: [advenced-algebra](https://github.com/wenje-ma/advenced-algebra), [topology](https://github.com/wenje-ma/topology), [real-analysis](https://github.com/wenje-ma/real-analysis), and the full list on the [profile page](https://github.com/wenje-ma).
