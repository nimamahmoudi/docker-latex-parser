# Docker Latex Parser
a parser for latex files including tools to generate pdf and parse the files.

## Usage for parsing files

```
export BUILD_DIR=$(pwd)

# Pandoc
docker run -t --mount src=$BUILD_DIR/,target=/repo,type=bind nimamahmoudi/latex-parser /bin/bash -c "cd /repo/ && pandoc main.tex -f latex --bibliography=references.bib --csl=ieee.csl -t docx -o output.docx"
docker run -t --mount src=$BUILD_DIR/,target=/repo,type=bind nimamahmoudi/latex-parser /bin/bash -c "cd /repo/ && pandoc main.tex -f latex --bibliography=references.bib --csl=ieee.csl -o output.pdf"

# Latex
docker run -t --mount src=$BUILD_DIR/,target=/repo,type=bind nimamahmoudi/latex-parser /bin/bash -c "cd /repo/ && pdflatex main && bibtex main && pdflatex main && pdflatex main"
# Or use latexmk
docker run -t --mount src=$BUILD_DIR/,target=/repo,type=bind nimamahmoudi/latex-parser /bin/bash -c "cd /repo/ && latexmk -pdf"
```

## Notes
- profile readme in pypi can be auto-generated!
