# Writing Toolkit

Curated collection of LaTeX templates and document-building utilities for **streamlining writing**.
I wrote these tools for my own use and I refine them as I go. 

My workflow is essentially filesystem-first.
For focused writing I use Texmaker.
I sometimes brainstorm in Writer, as it feels more like working on paper.
Collaborative projects tend to end up on Overleaf for convenience, although I still favour working locally with Texmaker whenever my colleagues have the patience for it.
For Python, Markdown and most other plain-text files I use Kate.
For HTML and CSS I use VSCodium.
My VSCodium setup as it was when I briefly used it as a general-purpose editor is included.
Ultimately, for clear thinking, nothing replaces pen and paper.

While the current focus is on scientific writing, I expect the repository to evolve into a more general writing toolkit over time.

## A modular writing architecture

For my LaTeX documents, I have adopted a modular preamble separating packages, macros and configuration:

```text
preamble/
├── packages.tex
├── macros.tex
└── config.tex
```

This makes templates easier to use and maintain. 
I am gradually migrating older templates to this structure.

## Templates

The document types covered are

- journal articles;
- technical notes;
- referee responses;
- conference abstracts;
- abstract collections;
- research proposals; and
- cover letters.

For each document, both

```text
main.tex
main.pdf
```

are provided for a quick preview.

I use the Libertinus typeface together with the corresponding Libertinus math font.
Besides liking their appearance, they are open source, widely available, and produce consistent output across Linux, macOS and Windows.
For proposals and cover letters, however, I switch to sans serif to make them easier to read.

## Command-line utilities

Helper scripts are provided for automating repetitive tasks:

`buildtex`: A wrapper around the standard LaTeX toolchain supporting

- PDF compilation with BibTeX, including bibunits;
- generation of files for arXiv submission;
- project cleanup; and
- standard compilation while retaining intermediate files.

`builddown`: Converts Markdown documents into PDF using Pandoc and XeLaTeX.

`gitush`: A wrapper around

```bash
git add .
git commit -m "<message>"
git push
```

It is intended for quick commits where all current changes are staged together.

`sortbib`: Sorts BibTeX databases alphabetically by entry key and orders the fields likewise within each entry.

I use this less nowadays in favour of JabRef.

## Requirements

Depending on which templates and utilities you use, the following may be required:

- TeX Live;
- XeLaTeX;
- Pandoc;
- Python;
- Git.

## Contributing

Suggestions and contributions of additional templates are welcome.

## License

This project is licensed under the GPL-3.0 License.
