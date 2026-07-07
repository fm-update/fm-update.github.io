# FM Update 2026 — Abstract Book

A formal abstract book for the Formal Methods Update Meeting 2026, typeset with
the Dagstuhl Reports LaTeX class (`dagrep`).

## Files

- `main.tex` — the abstract book source
- `Makefile` — build target: `make`
- `dagrep.cls` — Dagstuhl Reports class file (**not included**; see below)

## Getting `dagrep.cls`

The `dagrep` class ships with the Dagstuhl author kit. Two options:

1. Download the current author kit from Dagstuhl:
   <https://submission.dagstuhl.de/documentation/authors>, then copy `dagrep.cls`
   (and `dagrep-logo.pdf`, if present) into this directory.

2. On a TeX Live install with the full collection, `dagrep.cls` is usually
   already on the search path, in which case `make` will find it without a
   local copy.

## Building

```
make
```

This runs `pdflatex` three times to resolve the table of contents and
cross-references. Output: `main.pdf`.

To clean intermediates:

```
make clean
```

## What's inside

- Front matter: title, editors (organising committee), keywords, seminar dates
- Executive summary of FM Update 2026
- Table of contents
- Overview of talks: all 24 contributed talks plus 2 tutorials, in schedule order
- Participant list

Each abstract carries author, affiliation, license marker (Creative Commons
Attribution, per Dagstuhl convention), joint-work credits where applicable,
and a reference to the underlying paper where one exists.

## Editing

- Update abstracts by editing the corresponding `\subsection{...}` block in
  `main.tex`.
- Update the participant list under `\begin{participants} ... \end{participants}`.
- To add a talk, copy an existing `\subsection` block and adjust
  `\abstracttitle`, `\abstractauthor`, `\jointwork`/`\abstractref` as needed.
