# Export Instructions

## Goal
Prepare **From the Storm to the Fire: The Truth Behind the Silence — Early Reader Edition** for clean PDF ebook export.

The raw manuscript currently lives in the top-level `README.md`. Do not export that file directly until it has been split, cleaned, and proofed.

---

## Recommended Export Workflow

### Step 1 — Preserve Raw Source

Create:

```text
book/source/raw-manuscript.md
```

Copy the current raw manuscript into that file before any restructuring.

### Step 2 — Build Clean Chapter Files

Create:

```text
book/chapters/
```

Use this naming pattern:

```text
chapter-01-the-storm-outside.md
chapter-02-the-fire-ignites.md
chapter-03-pain-takes-root.md
```

Each chapter should use consistent markdown:

```markdown
# Part I — The Storm

## Chapter 1 — The Storm Outside

Body text...
```

### Step 3 — Create Front Matter

Create:

```text
book/front-matter/
```

Suggested files:

```text
01-title-page.md
02-copyright.md
03-dedication.md
04-content-note.md
05-memoir-disclaimer.md
06-author-note.md
07-table-of-contents.md
```

### Step 4 — Create Back Matter

Create:

```text
book/back-matter/
```

Suggested files:

```text
01-final-thought-the-ember-that-stayed.md
02-survival-terms-in-plain-english.md
03-author-notes.md
04-about-the-author.md
05-from-testimony-to-tools.md
```

### Step 5 — Remove Draft Artifacts

Before export, remove:

- duplicate chapters,
- repeated final thoughts,
- accidental AI/editor notes,
- placeholder headings,
- accidental page numbers,
- incomplete table of contents markers,
- duplicate front matter,
- alternate chapter versions not selected for the Early Reader Edition.

### Step 6 — Move Clean Source to Production Repo

Once chapters are cleaned, copy them into:

```text
from-storm-to-fire-book-production/book/chapters/
```

Then use the production workflow:

```bash
python3 scripts/build_pdf.py --input-dir book/chapters --output exports/final-payhip.pdf --title "From the Storm to the Fire" --author "Daniel Bret Lingar"
```

### Step 7 — Proof the PDF

Review the proof on:

- phone,
- desktop,
- tablet if possible.

Check:

- title page,
- copyright,
- page breaks,
- chapter openers,
- table of contents,
- repeated sections,
- missing chapters,
- readability on black/dark design,
- crisis/content note visibility.

### Step 8 — Export Final Files

Target files:

```text
exports/from-the-storm-to-the-fire-early-reader-edition.pdf
exports/from-the-storm-to-the-fire-free-sample.pdf
```

Optional:

```text
exports/from-the-storm-to-the-fire-early-reader-edition.epub
```

---

## Recommended First Public Release

**Early Reader Edition**

Reason:

- The manuscript is powerful and close enough for early readers.
- It still benefits from reader feedback.
- It gives you room to revise before a final edition.

---

## Do Not Upload Until

- Duplicate chapters are removed.
- Draft artifacts are removed.
- Sensitive names/legal allegations are reviewed.
- The final PDF is reviewed on multiple devices.
- Storefront copy is finalized.
- Content note and memoir disclaimer are visible.

---

## Publication Standard

The final PDF should feel raw, but not messy.

The reader should feel the voice, not the draft process.
