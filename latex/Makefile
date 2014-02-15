TARGETS=colorbrewer.tex palette-all.pdf

all: $(TARGETS)

default: all

colorbrewer.js:
	wget -N colorbrewer2.org/export/colorbrewer.js

colorbrewer.tex: colorbrewer.pl colorbrewer.js
	./colorbrewer.pl

palette-all.pdf: colorbrewer.tex
	pdflatex palette-all.tex

clean:
	rm -f *.tex *~ *.pdf *.log *.aux
