# CV Build Instructions

## Files
- `resume.tex` — LaTeX source (main file)
- `resume.pdf` — compiled output (committed for convenience)

## Requirements
- **MiKTeX** (Windows) or **TeX Live** (Linux/macOS)
- Required packages (auto-installed by MiKTeX): `lmodern`, `microtype`, `parskip`, `enumitem`, `titlesec`, `xcolor`, `hyperref`, `fontawesome5`, `tabularx`, `helvet`

## Build Command
```bash
# First pass
pdflatex -interaction=nonstopmode resume.tex

# Second pass (for correct hyperref bookmarks)
pdflatex -interaction=nonstopmode resume.tex
```

## Updating the CV
1. Edit `resume.tex`
2. Run `pdflatex` twice
3. Review `resume.pdf`
4. Commit both `.tex` and `.pdf`

## Design Notes
- Engine: pdfLaTeX (compatible with MiKTeX 26.1 and TeX Live 2025)
- Paper: A4, 2 pages
- Typography: Helvetica (sans-serif), clean single-column layout
- ATS-friendly: no graphics, copyable text, clickable hyperlinks
- Sections: Summary, Skills, Experience, Projects, Education, Languages
