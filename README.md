# Modular Resume

## About
I was inspired to make this after finding [Peter Zhang's Modular-Resume repo](https://github.com/petezh/Modular-Resume), so just read the first section of that for an overview of what this is for.

This is my own version that I built a few months before knowing Peter's template existed. In comparison, my version lets [moderncv](https://ctan.org/pkg/moderncv?lang=en) handle most of the design choices, **minimizing the file tree's complexity**. But check out Peter's version if you want lower-level control of graphics!

## Instructions
Usage is **very simple** and **modular**, the only prerequisite being basic LaTeX.

1. Customize your basic info in `layout.sty`. This will become a short header and footer that is automatically included in every template.
2. For each entry you might want in any template,
	1. Duplicate and rename a `<Entry Alias>.tex` file (each contains a single `\cventry` call) in `/entries`. Entries can be for any resume section, including experience, jobs, and research.
	2. You can probably just pattern-match how to fill the `\cventry` fields from my examples, or you can read [moderncv's documentation of it](https://mirrors.mit.edu/CTAN/macros/latex/contrib/moderncv/manual/moderncv_userguide.pdf#page=5).
3. For each template you want,
	1. Duplicate and rename a template folder in `/templates`, and rename the `<First Name>_<Last Name>_resume.tex` file in it.
	2. Change section/subsection header names as needed.
	3. Use `\input{<Entry Alias>}` to import the corresponding entries.
	4. Build the `.tex` file to render updates.