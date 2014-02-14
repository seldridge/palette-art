TARGETS=colorbrewer.tex palette-all.pdf

all: $(TARGETS)

default: all

colorbrewer.tex: colorbrewer.pl
	./colorbrewer.pl

palette-all.pdf: colorbrewer.tex
	pdflatex palette-all.tex

clean:
	rm -f *.tex *~
