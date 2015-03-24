TARGETS=colorbrewer.tex palette-all.pdf
LATEXMK=latexmk -pdf -latexoption="--shell-escape -halt-on-error -file-line-error" -bibtex- -time

all: $(TARGETS)

default: all

colorbrewer.js:
	curl colorbrewer2.org/export/colorbrewer.js -o colorbrewer.js

colorbrewer.tex: colorbrewer.pl colorbrewer.js
	./colorbrewer.pl

palette-all.pdf: colorbrewer.tex
	$(LATEXMK) palette-all.tex

clean:
	rm -f *.pdf *.aux *.auxlock *.dvi *.log *.nav *.out *.ps *.snm *.toc *.dep *.dpth *.notes *.fdb_latexmk *.fls *.tex *.js
